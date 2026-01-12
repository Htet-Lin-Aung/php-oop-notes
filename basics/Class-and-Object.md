# Class and Object in Object-Oriented Programming (OOP)

## What is Object-Oriented Programming (OOP)?

Object-Oriented Programming (OOP) is a way of writing programs by organizing code into **objects**.  
Each object represents a **real-world entity** and contains **data** and **behavior**.

---

## 1️⃣ What is a Class?

A **class** is a **blueprint** or **template** for creating objects.

It defines:
- **Properties** → data / variables
- **Methods** → functions / behaviors

### 🧠 Real-Life Example
Think of a **class** as a **house plan** 🏠  
The plan itself is not a house, but it describes how houses should be built.

---

### PHP Example: Class

```php
<?php

class Car {
    public $color;
    public $brand;

    public function drive() {
        echo "The car is driving";
    }
}

?>

$car1 = new Car();
$car1->color = "Red";
$car1->brand = "Toyota";

$car2 = new Car();
$car2->color = "Blue";
$car2->brand = "Honda";

echo $car1->brand; // Toyota
echo $car2->brand; // Honda