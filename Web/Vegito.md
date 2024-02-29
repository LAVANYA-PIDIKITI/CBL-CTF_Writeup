# Vegito
There's web link provided and as you click that , you can see there's a php file
```php
<?php
    highlight_file(__FILE__);
    ini_set('display_errors', 0);

    $cmd = $_GET['cmd'];
    parse_str($_GET['parse'], $a);

    echo (strlen($cmd) < 3) ? @shell_exec($cmd) : $action($args, '');
?>
```

# Solution:
Now as I read the code , I understood that cmd is taken parsed and executed in shell , which means it should be a command which is of length < 3 and executed in shell. I tried cd , cd.. and that's when ls worked
```
http://174.129.132.216:5010/w7?cmd=ls
```
![image](https://github.com/LAVANYA-PIDIKITI/CBL-CTF_Writeup/assets/98797256/29f37280-b381-42a5-af57-225fa3fa82e5)
