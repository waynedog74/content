---
Title: "How to use PHP empty function"
Date: 2017-02-07 18:43:15
Categories: [programming]
tags: [php, empty]
Authors: sedlav
---

PHP empty function determines if a variable does not exist or if its value equals FALSE then never use it in this way:

```php
<?php
if (!empty($myvar) && ($myvar === false)) {
  // do something
}
```

because in the above logic, "do something" will never executed it's better to use:

```php
<?php
if (isset($myvar) && ($myvar === false)) {
  // do something
}
```

also you can use it in this way for true testing

```php
<?php
if (!empty($myvar) && ($myvar === true)) {
  // do something
}
```
