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

## Slide 7 – Encapsulation (The "Security" Pillar)
This is about bundling data and methods into a single unit (a class) and restricting access to the inner workings.
- Goal: Protect the internal state of an object from outside interference.
- PHP Tool: Access modifiers (public, private, protected).

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

## Slide 9 – Abstraction (The "Simplicity" Pillar)
Abstraction is about hiding complexity. It means showing only the essential features of an object to the outside world while hiding the "how it works" logic.

- Analogy: You know how to use a steering wheel to turn a car, but you don't need to know how the rack-and-pinion gear system works under the hood.
- PHP Tool: abstract classes and interfaces.

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

## Slide 11 – Inheritance (The "Reuse" Pillar)
Inheritance allows one class to use another class.

- Goal: Create a hierarchy and reuse logic.
- PHP Tool: The extends keyword.

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

## Slide 13 – Polymorphism (The "Flexibility" Pillar)
Polymorphism means:
- Same method name
- Different behavior
- Example: A Circle and a Square are both Shapes. You can call a calculateArea() method on both, but the math inside is different for each.
- PHP Tool: Method overriding and interfaces.

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

## Slide 15 - Four Pillars of Object-Oriented Programming (OOP)

The table below summarizes the **four main pillars of OOP**, their focus, and key benefits.

| Pillar | Focus | Key Benefit |
|------|------|-------------|
| **Encapsulation** | Hiding data | Security & control |
| **Inheritance** | Sharing code | Less duplication |
| **Abstraction** | Hiding complexity | Easier to use |
| **Polymorphism** | Changing behavior | Flexibility |

---

## 🎯 Slide 16 - Key Takeaway

> The four pillars of OOP work together to create software that is **secure, reusable, simple, and flexible**.

---

## Slide 17 – OOP Summary
- Class → Blueprint
- Object → Real thing
- Encapsulation → Protect data
- Abstraction → Hide details
- Inheritance → Reuse
- Polymorphism → Many forms

---

## Slide 18 – Final Advice
- Understand concepts, not memorize code
- Practice small examples
- Draw diagrams
- OOP becomes easy with practice

