# Encapsulation in Object-Oriented Programming (OOP)

## What is Encapsulation?

In **Object-Oriented Programming (OOP)**, **Encapsulation** is the practice of **bundling data (properties)** and the **methods (functions)** that operate on that data into a **single unit called a class**.

More importantly, encapsulation **hides the internal state of an object** from the outside world and allows interaction **only through a controlled public interface**.

### 🧠 Real-Life Analogy
Think of encapsulation like a **pill capsule** 💊:
- The medicine is hidden and protected inside
- You only interact with the outer shell
- You don’t need to know the internal details to use it safely

---

## 1️⃣ Core Concept: Access Modifiers

Encapsulation is implemented using **access modifiers**, which control visibility and access.

| Modifier | Description |
|--------|------------|
| `public` | Accessible from anywhere |
| `protected` | Accessible within the class and its child classes |
| `private` | Accessible only within the class |

---

## 2️⃣ PHP Code Example: Bank Account

Without encapsulation, anyone could directly change their bank balance to **$1,000,000**.  
Encapsulation prevents this by making sensitive data **private** and exposing safe methods to access or modify it.

### 📌 PHP Example

```php
<?php

class BankAccount {

    // Private property: cannot be accessed directly
    private $balance;

    public function __construct($initialBalance) {
        $this->balance = $initialBalance;
    }

    // Getter: safely read the balance
    public function getBalance() {
        return "$" . number_format($this->balance, 2);
    }

    // Setter: safely modify the balance
    public function deposit($amount) {
        if ($amount > 0) {
            $this->balance += $amount;
            echo "Deposited: $amount\n";
        } else {
            echo "Invalid deposit amount.\n";
        }
    }
}

// Usage
$myAccount = new BankAccount(500);

// $myAccount->balance = 1000000; // ❌ ERROR: private property
$myAccount->deposit(150);        // ✅ Valid interaction
echo $myAccount->getBalance();   // Output: $650.00

?>
```

---
### 📌 Without Encapsulation (Bad Practice)

```php
<?php
class BankAccount {
    public $balance;
}

$account = new BankAccount();
$account->balance = -5000; // ❌ No protection

⚠️ Anyone can set invalid values.

?>