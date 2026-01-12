
---

# 📄 `Polymorphism.md`

```md
# Polymorphism in Object-Oriented Programming (OOP)

## What is Polymorphism?

**Polymorphism** means:
> One method name, many behaviors

Different objects can respond **differently** to the same method call.

---

### 🧠 Real-Life Example
- A **Dog** makes a sound → Woof
- A **Cat** makes a sound → Meow

Same action, different result.

---

## 1️⃣ Why Use Polymorphism?

Polymorphism allows:
- Flexible code
- Easy extension
- Cleaner conditional-free logic

---

## 2️⃣ Method Overriding (Runtime Polymorphism)

```php
<?php

class Animal {
    public function sound() {
        echo "Animal sound";
    }
}

class Dog extends Animal {
    public function sound() {
        echo "Woof";
    }
}

class Cat extends Animal {
    public function sound() {
        echo "Meow";
    }
}

// Usage
$animals = [new Dog(), new Cat()];

foreach ($animals as $animal) {
    $animal->sound();
}

?>
