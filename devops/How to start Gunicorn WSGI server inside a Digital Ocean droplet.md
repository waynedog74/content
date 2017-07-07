---
Title: "How to start Gunicorn WSGI server inside a Digital Ocean droplet"
Date: 2017-06-05 21:56:40
Categories: [devops]
tags: [gunicorn, wsgi]
Authors: sedlav
---

When you create a Digital Ocean droplet using "One-click apps" configuration:

![One-click apps](/images/digital-ocean-droplet.png)

You will have these app availables: PostgreSQL, Gunicorn, NGINX, Django and this project structure by default under /home/django:

```
../django_project/
├── django_project
│   ├── __init__.py
│   ├── __init__.pyc
│   ├── settings.py
│   ├── settings.pyc
│   ├── settings.py.orig
│   ├── urls.py
│   ├── urls.pyc
│   ├── wsgi.py
│   └── wsgi.pyc
└── manage.py
```

If you look for the gunicorn.service service under /etc/systemd/system/, you will find a text like this

```
[Unit]
Description=Gunicorn daemon for Django Project
Before=nginx.service
After=network.target

[Service]
WorkingDirectory=/home/django/django_project
/usr/bin/gunicorn --name=django_project --pythonpath=/home/django/django_project --bind unix:/home/django/gunicorn.socket --config /etc/gunicorn.d/gunicorn.py django_project.wsgi:application
Restart=always
SyslogIdentifier=gunicorn
User=django
Group=django


[Install]
WantedBy=multi-user.target
```

But if you want to serve a different project developed using Django REST framework for example, probably you will have a dir structure like this:

```
my-project/
├── apps
│   └── web
│       ├── management
│       │   └── commands
│       └── migrations
├── my-project
├── certs
├── conf
│   └── settings
├── requirements
└── templates
```

So in order to Gunicorn starts successfuly, you must change these lines:

```
WorkingDirectory=/home/django/django_project
/usr/bin/gunicorn --name=django_project --pythonpath=/home/django/django_project --bind unix:/home/django/gunicorn.socket --config /etc/gunicorn.d/gunicorn.py django_project.wsgi:application
```

By these ones:

```
WorkingDirectory=/home/django/my-project
ExecStart=/usr/bin/gunicorn --name=my-project --pythonpath=/home/django/my-project --bind unix:/home/django/gunicorn.socket --config /etc/gunicorn.d/gunicorn.py conf.wsgi:application
```

NGINX config

```
upstream app_server {
    server unix:/home/django/gunicorn.socket fail_timeout=0;
}

server {
    listen 80 default_server;
    listen [::]:80 default_server ipv6only=on;
    #error_log /var/log/nginx/error.log debug;

    root /usr/share/nginx/html;
    index index.html index.htm;

    client_max_body_size 8m;
    server_name _;

    keepalive_timeout 5;

    # Your Django project's media files - amend as required
    #location /media  {
        #alias /home/django/django_project/django_project/media;
        #alias /usr/local/lib/python2.7/dist-packages/django/contrib/admin/static/admin/css; 
    #}

    # your Django project's static files - amend as required
    #location /static {
    #    alias /home/django/django_project/django_project/static;
    #}

    # Proxy the static assests for the Django Admin panel
    location /static/admin {
       alias /usr/local/lib/python2.7/dist-packages/django/contrib/admin/static/admin; 
       #alias /usr/lib/python2.7/dist-packages/django/contrib/admin/static/admin/;
    }

    location / {
            proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
            proxy_set_header Host $host;
            proxy_redirect off;
            proxy_buffering off;

            proxy_pass http://app_server;
    }
}
```