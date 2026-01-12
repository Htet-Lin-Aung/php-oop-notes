
---

# 📄 `Abstraction.md`

```md
# Abstraction in Object-Oriented Programming (OOP)

## What is Abstraction?

**Abstraction** means:
- Showing **only essential features**
- Hiding **internal implementation details**

The user knows **what** an object does, not **how** it does it.

---

### 🧠 Real-Life Example
When driving a car:
- You press the accelerator
- You don’t need to know how the engine works

---

## 1️⃣ Why Use Abstraction?

Abstraction helps to:
- Reduce complexity
- Improve focus on important behavior
- Make code easier to use and modify

---

## 2️⃣ Abstraction in PHP (Using Methods)

```php
<?php

class Car {
    public function drive() {
        $this->startEngine();
        echo "Car is driving";
    }

    private function startEngine() {
        // Hidden complex logic
    }
}

// Usage
$car = new Car();
$car->drive();

?>
