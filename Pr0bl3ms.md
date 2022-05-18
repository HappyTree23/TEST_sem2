## PROBLEM 1
```html
<!DOCTYPE html>
<html>
<head></head>
<body>
    <center>PHP is a backend programming language</center>
</body>
</html>
```

## PROBLEM 2
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

## PROBLEM 3
```php
<!DOCTYPE html>
<html>
<head></head>
<body></body>
<?php
  $nums = array();
  for ($i = 1; $i <= 5; $i++) {
    $line = array();
    for ($j=1; $j<=5; $j++) {
      array_push($line, rand(1, 100));
    }
    array_push($nums, $line);
  }

  echo "<table id='table1'>";
  for ($i = 1; $i<=5; $i++) {
    echo "<tr>";
    for ($j=1; $j<=5; $j++) {
      echo "<td>" . $nums[$i][$j] . "</td>";
    }
    echo "</tr>";
  }
echo "</table>";
?>
</html>
```
