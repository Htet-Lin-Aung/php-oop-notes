# PHP OOP – Student Handout

## 1️⃣ What we are learning
We are learning **PHP Object-Oriented Programming (OOP)** using:
- Visiual Studio Code (simple editor)
- XAMPP (local server)
- Browser (Chrome)

👉 Goal: Understand how PHP really works on a server

---

## 2️⃣ What is XAMPP? (Very important)

**XAMPP = Local server on your computer**

It includes:
- Apache (Web Server)
- PHP (Programming language)

❗ Browser cannot run PHP by itself.
PHP must run through a server.

---

## 3️⃣ Download & Install XAMPP

### Step 1: Download
Open browser and go to:

👉 https://www.apachefriends.org

Download XAMPP (PHP 8.x)

---

### Step 2: Install
During installation:
- ✔ Apache
- ✔ PHP
- ❌ MySQL (optional, not needed now)

Click **Next → Finish**

---

## 4️⃣ Start Apache (Every day before class)

1. Open **XAMPP Control Panel**
2. Click **Start** next to Apache
3. Apache must turn **green** ✅

---

## 5️⃣ Test PHP is working

### Step 1: Create file
Go to:
```
C:\xampp\htdocs\
```

Create file:
```
test.php
```

### Step 2: Write code
```php
<?php
echo "PHP is working";
```

### Step 3: Open browser
```
http://localhost/test.php
```

If you see text → SUCCESS 🎉

---

## 6️⃣ Our First OOP Example

Create file:
```
oop.php
```

```php
<?php
error_reporting(E_ALL);
ini_set('display_errors', 1);

class Car {
  public $color;

  public function drive() {
    echo "Car is driving";
  }
}

$car = new Car();
$car->color = "Red";
$car->drive();
```

Open:
```
http://localhost/oop.php
```

---

## 7️⃣ VERY IMPORTANT RULES ❗

❌ Do NOT double-click `.php` files
❌ Do NOT open with `file:///`

✅ Always use:
```
http://localhost/filename.php
```

---

## 8️⃣ Common Errors (Don’t Panic)

### Example error:
```php
class Car {
  public $color
}
```

Error message:
```
Parse error: syntax error
```

👉 Read the error and fix it.
Errors are NORMAL.

---

## 9️⃣ Simple Diagram (Remember this)

Browser → Apache → PHP → Output

---

## 🔟 Daily Checklist for Students

Before coding:
- [ ] Apache is running (green)
- [ ] File saved in `htdocs`
- [ ] File extension is `.php`
- [ ] Open with `http://localhost`

---

## 🎯 Final Advice

Learn OOP slowly.
Understand Class vs Object.
Do NOT memorize code.

Good luck 🚀

