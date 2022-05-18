## <!-- PROBLEM 1 -->
```php
<!DOCTYPE html>
<html>
<head></head>
<body>
    <center>PHP is a backend programming language</center>
</body>
</html>
```

## <!-- PROBLEM 2 -->
```php
<!DOCTYPE html>
<html>
<head></head>
<body>
  <form id="form1" action="" method="POST">
    <input type="number" name="num1">
    <input type="number" name="num2">
    <input type="submit" value="Add">
  </form>
</body>
<?php
if ($_POST) {
  $num1 = $_POST["num1"];
  $num2 = $_POST["num2"];
  echo $num1 + $num2;
}
</html>
```
