---
Title: "Beware with PHP non strict comparison"
Date: 2017-04-03 16:48:48
Categories: [programming]
tags: [php]
Authors: sedlav
---

Beware when you use non strict comparison in PHP, for example the following code print "TRUE"

```php
<?php
if (0 == '') {
  echo 'TRUE';
}
```
