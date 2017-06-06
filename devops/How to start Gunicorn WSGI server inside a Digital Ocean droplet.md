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
