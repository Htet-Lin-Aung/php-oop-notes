# Inheritance in Object-Oriented Programming (OOP)

## What is Inheritance?

**Inheritance** allows one class to **reuse the properties and methods** of another class.

- The existing class is called the **Parent (Base / Super) class**
- The new class is called the **Child (Derived / Sub) class**

Inheritance represents an **IS-A relationship**.

### 🧠 Real-Life Example
- A **Dog** is an **Animal**
- A **Student** is a **Person**

---

## 1️⃣ Why Use Inheritance?

Inheritance helps us to:
- Reuse code
- Avoid duplication
- Create a logical class hierarchy
- Make code easier to maintain

---

## 2️⃣ PHP Inheritance Example

```php
<?php

class Animal {
    public function eat() {
        echo "Eating food";
    }
}

class Dog extends Animal {
    public function bark() {
        echo "Woof!";
    }
}

// Usage
$dog = new Dog();
$dog->eat();   // Inherited from Animal
$dog->bark();  // Dog's own method

?>
