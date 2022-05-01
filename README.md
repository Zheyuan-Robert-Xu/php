# PHP
Global and Local Scope

A variable declared outside a function has a GLOBAL SCOPE and can only be accessed outside a function:

var_dump is used to dump information about a variable. 

Create a PHP Constant

To create a constant, use the define() function. Constants are automatically global and can be used across the entire script.
Syntax
define(name, value, case-insensitive)

The following example will output both the keys and the values of the given array ($age):
Example
<?php
$age = array("Peter"=>"35", "Ben"=>"37", "Joe"=>"43");

foreach($age as $x => $val) {
  echo "$x = $val<br>";
}
?> 

 <?php declare(strict_types=1); // strict requirement

function addNumbers(int $a, int $b) {
  return $a + $b;
}
echo addNumbers(5, "5 days");
// since strict is enabled and "5 days" is not an integer, an error will be thrown
?> 

Passing Arguments by Reference

In PHP, arguments are usually passed by value, which means that a copy of the value is used in the function and the variable that was passed into the function cannot be changed.

When a function argument is passed by reference, changes to the argument also change the variable that was passed in. To turn a function argument into a reference, the & operator is used:
 <?php
function add_five(&$value) {
  $value += 5;
}

$num = 2;
add_five($num);
echo $num;
?> 
