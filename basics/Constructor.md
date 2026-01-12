# PHP OOP Basics: Constructors and $this

This guide covers the fundamental building blocks of PHP objects: the constructor method and the `$this` keyword.

---

## 1. Constructor (`__construct()`)
A **constructor** is a special method that runs automatically the moment an object is created (instantiated).

### Why use a constructor?
* **Initialize object data:** Set values as soon as the object is born.
* **Avoid manual assignment:** You don't have to manually set every property after creating the object.
* **Mandatory Data:** Ensure an object cannot exist without certain pieces of information.



### PHP Constructor Example

```php
<?php
class Student {
    public $name;
    public $id;

    // The constructor method
    public function __construct($id, $name) {
        $this->id = $id;
        $this->name = $name;
    }

    public function getInfo() {
        return "ID: $this->id, Name: $this->name";
    }
}

// Creating an object (The constructor runs here)
$student1 = new Student(101, "Aung Aung");

echo $student1->getInfo(); 
// Output: ID: 101, Name: Aung Aung
?>