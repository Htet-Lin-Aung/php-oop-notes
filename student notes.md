# PHP OOP – Exam-Ready Student Notes

## 1️⃣ What is OOP?
Object-Oriented Programming (OOP) is a way of programming using **objects**.

An **object** contains:
- **Data** → properties
- **Actions** → methods

OOP helps to:
- Organize code
- Reuse code
- Maintain programs easily

---

## 2️⃣ Class and Object

### Class
A **class** is a blueprint or template.
It defines what data and actions an object will have.

```php
class Car {
  public $color;
  public function drive() {
    echo "Driving";
  }
}
```

### Object
An **object** is a real instance of a class.

```php
$car = new Car();
$car->color = "Red";
$car->drive();
```

**Remember:** Class ≠ Object

---

## 3️⃣ Encapsulation
Encapsulation means:
- Keeping data and methods together
- Protecting data from direct access

We use access modifiers:
- `public`
- `private`

```php
class BankAccount {
  private $balance = 0;

  public function deposit($amount) {
    $this->balance += $amount;
  }

  public function getBalance() {
    return $this->balance;
  }
}
```

---

## 4️⃣ Abstraction
Abstraction means:
- Showing only important features
- Hiding complex details

```php
class Car {
  public function drive() {
    $this->startEngine();
    echo "Driving";
  }

  private function startEngine() {}
}
```

---

## 5️⃣ Inheritance
Inheritance allows one class to use another class.

It creates an **IS-A** relationship.

```php
class Animal {
  public function eat() {
    echo "Eating";
  }
}

class Dog extends Animal {
  public function bark() {
    echo "Woof";
  }
}
```

---

## 6️⃣ Polymorphism
Polymorphism means:
- Same method name
- Different behavior

```php
class Animal {
  public function sound() {}
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
```

---

## 7️⃣ Composition
Composition is a **HAS-A** relationship.

Example: Car has an Engine.

```php
class Engine {}

class Car {
  private $engine;
  public function __construct() {
    $this->engine = new Engine();
  }
}
```

---

## 8️⃣ Aggregation
Aggregation is a weak HAS-A relationship.
Objects can exist independently.

```php
class Player {}

class Team {
  public $players = [];
}
```

---

## 9️⃣ Association
Association is a relationship where classes work together.

```php
class Teacher {}
class Student {
  public $teacher;
}
```

---

## 🔟 Dynamic Binding
Dynamic binding means method call is decided at runtime.

```php
$animal = new Dog();
$animal->sound();
```

---

## 📝 Exam Tips
- Write definitions clearly
- Use small code examples
- Explain with real-life examples
- Do not memorize, understand concepts

---

## 📌 One-Line Summary Table

| Concept | Meaning |
|------|------|
| Class | Blueprint |
| Object | Real instance |
| Encapsulation | Protect data |
| Abstraction | Hide details |
| Inheritance | Reuse code |
| Polymorphism | Many forms |
| Composition | Strong HAS-A |
| Aggregation | Weak HAS-A |
| Association | Uses relationship |

