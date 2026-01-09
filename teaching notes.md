# PHP OOP – Slide-by-Slide Teaching Notes (Beginner)

---

## Slide 1 – Title
**Object-Oriented Programming (OOP) in PHP**  
Beginner Level

---

## Slide 2 – What is OOP?
- Programming using **objects**
- Object = data + actions
- Models real-world things

**Example:** Car
- Data: color, brand
- Actions: drive(), stop()

---

## Slide 3 – Why OOP?
- Code is organized
- Easy to reuse
- Easy to maintain
- Used in real projects (Laravel)

---

## Slide 4 – Core Building Blocks
- Class
- Object

Remember:
> Class = blueprint  
> Object = real thing

---

## Slide 5 – Class (Definition)
A **Class** is a template that defines:
- Properties (data)
- Methods (actions)

```php
class Car {
  public $color;
  public function drive() {
    echo "Car is driving";
  }
}
```

---

## Slide 6 – Object (Definition)
An **Object** is a real instance of a class

```php
$myCar = new Car();
$myCar->color = "Red";
$myCar->drive();
```

---

## Slide 7 – Encapsulation
- Keep data and methods together
- Protect data from direct access
- Use `private`, `public`

---

## Slide 8 – Encapsulation Example
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

## Slide 9 – Abstraction
- Show only important features
- Hide complex logic

**Real life:** Driving a car without knowing engine details

---

## Slide 10 – Abstraction Example
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

## Slide 11 – Inheritance
- One class uses another class
- "IS-A" relationship

Example:
- Dog is an Animal

---

## Slide 12 – Inheritance Example
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

## Slide 13 – Polymorphism
- Same method name
- Different behavior

---

## Slide 14 – Polymorphism Example
```php
class Animal {
  public function sound() {}
}

class Dog extends Animal {
  public function sound() { echo "Woof"; }
}

class Cat extends Animal {
  public function sound() { echo "Meow"; }
}
```

---

## Slide 15 – Composition (HAS-A)
- Strong relationship
- One object is part of another

Example: Car has Engine

---

## Slide 16 – Composition Example
```php
class Engine {
  public function start() {}
}

class Car {
  private $engine;
  public function __construct() {
    $this->engine = new Engine();
  }
}
```

---

## Slide 17 – Association & Aggregation
- Association: objects work together
- Aggregation: weak HAS-A relationship

Example:
- Student uses Teacher
- Team has Players

---

## Slide 18 – Dynamic Binding
- Method call decided at runtime

```php
$animal = new Dog();
$animal->sound();
```

---

## Slide 19 – OOP Summary
- Class → Blueprint
- Object → Real thing
- Encapsulation → Protect data
- Abstraction → Hide details
- Inheritance → Reuse
- Polymorphism → Many forms

---

## Slide 20 – Final Advice
- Understand concepts, not memorize code
- Practice small examples
- Draw diagrams
- OOP becomes easy with practice

