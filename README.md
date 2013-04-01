php-collection
============

PHP Array Object - A simple struct that implements ArrayAccess, Countable and Iterator. This is just a placeholder for a common struct I use frequently.


Example Usage

```php
<?php

class myObj extends Collection {

  public $object_level_variable = 'haay';

}


$obj = new myObj(array('key1' => 'val1', 'key2' => 'val2'));

echo $obj->key1; // val1
echo $obj->key2; // val2

// set another property
$obj->key3 = 'val3';

echo count($obj); // 3
echo $obj->toArray(); // array('key1' => 'val1', 'key2' => 'val2', 'key3' => 'val3')

// chaning object level properties does not affect our array container
$obj->object_level_variable = 'changed';
echo count($obj); // 3 
echo $obj->object_level_variable; // changed


?>
```
