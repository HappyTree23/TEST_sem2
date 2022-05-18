## PROBLEM 1 -- Flexbox alignment
```html
<!DOCTYPE html>
<html>
<head></head>
<body>
  <div class="container">
    <div id="center">PHP is a backend programming language</div>
  </div>
</body>
  <style>
    .container {
      display: flex;
    }
    #center {
      margin-left: auto;
      margin-right: auto;
    }
  </style>
</html>
```

## PROBLEM 2 -- layout change
```php
<!DOCTYPE html>
<html>
<head></head>
<body>
  <form id="form1" action="" method="POST">
    <div id="frow">
      <input type="number" name="num1" class="num-fld">
      <div id="plus">+</div>
    </div>
    <div id="frow">
      <input type="number" name="num2" class="num-fld">
      <input type="submit" value="=" id="sub-btn">
    </div>
    <div id="line"> </div>
  </form>
</body>
  
<?php
if ($_POST) {
  $num1 = $_POST["num1"];
  $num2 = $_POST["num2"];
  echo "<div id='number'>" . ($num1 + $num2) . "</div>";
}
?>
  
<style>
  body {
    font-family: sans-serif;
  }
  #form1 {
    display: flex;
    flex-direction: column;
    align-content: flex-start;
  }
  .num-fld {
    width: 60px;
    height: auto;
    margin-left: 5px;
    margin-right: 5px;
    margin-bottom: 2px;
  }
  
  #frow {
    display: flex;
    flex-direction: row;
  }
  
  #plus {
    font-weight: bold;
  }
  #line {
    margin: 2px;
    border: thin solid black;
    width: 76px;
  }
  #sub-btn {
    width: 20px;
    height: auto;
    
  }
  #number {
    margin-left: 8px;
  }
</style>
</html>
```

## PROBLEM 3 -- Better table
```php
<!DOCTYPE html>
<html>
<head></head>
<body></body>
<?php
  $nums = array();
  for ($i = 1; $i <= 5; $i++) {
    $line = array();
    for ($j=1; $j <= 5; $j++) {
      array_push($line, rand(1, 100));
    }
    array_push($nums, $line);
  }

  echo "<table id='table1'>";
  for ($i = 0; $i<5; $i++) {
    echo "<tr>";
    for ($j=0; $j<5; $j++) {
      echo "<td>" . $nums[$i][$j] . "</td>";
    }
    echo "</tr>";
  }
echo "</table>";
?>
<style>
  table {
    border: 1px solid black;
    border-collapse: collapse;
  }
  td {
    text-align: center;
    width: 30px;
    height: 30px;
    border: 2px solid black;
  }
</style>
</html>
```

## PROBLEM 4
```php
<!DOCTYPE html>
<html>
<head></head>
<body></body>
<?php
  $nums = array();
  for ($i=1; $i<=25; $i++)
    array_push($nums, rand(1, 100));
  echo "min: " . min($nums);
  echo "<br>";
  echo "max: " . max($nums);
?>
</html>
```

## PROBLEM 5
```php
$age = array("Peter"=>"35", "Michelle"=>"37", "Joe"=>"43", "Andrew"=>"25", "Bob"=>"33", "John"=>"53", "Paul"=>"22", "Bill"=>"17", "Anna"=>"43");
asort($age);
foreach($age as $person => $pers_age)
    echo $person . ": " . $pers_age . "<br>";
```

## PROBLEM 6
```php
$age = array("Peter"=>"35", "Michelle"=>"37", "Joe"=>"43", "Andrew"=>"25", "Bob"=>"33", "John"=>"53", "Paul"=>"22", "Bill"=>"17", "Anna"=>"43");
krsort($age);
foreach($age as $person => $pers_age)
    echo $person . ": " . $pers_age . "<br>";
```

## PROBLEM 7
```php
<!DOCTYPE html>
<html>
<head></head>
<body>
    <form method="POST">
        Name: <input type="text" name="pname">
        Age: <input type="number" name="age">
        <input type="submit">
    </form>
</body>
<?php
    if ($_POST)
    {
        echo "Hello, " . $_POST["pname"] . "! You are " . $_POST["age"] . " years old.";
    }
?>
</html>
```
