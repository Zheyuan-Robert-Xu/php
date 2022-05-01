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
