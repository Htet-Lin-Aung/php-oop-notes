# PHP OOP: Constructors & Encapsulation

This guide demonstrates how to use constructors to initialize objects while keeping data secure using encapsulation.

---

## 1. Combining Concepts
In professional PHP, we rarely leave properties `public`. We use the **Constructor** to set **Private** data, ensuring the object is "valid" from the moment it is created.

### The Secure Student Example


```php
<?php
class Student {
    // Encapsulation: Properties are private
    private $id;
    private $name;
    private $grade;

    // Constructor: Initializes the data automatically
    public function __construct($id, $name, $grade) {
        $this->id = $id;
        $this->name = $name;
        $this->setGrade($grade); // Using a method to validate data
    }

    // A setter with validation logic
    public function setGrade($grade) {
        if ($grade >= 0 && $grade <= 100) {
            $this->grade = $grade;
        }
    }

    public function getSummary() {
        // $this refers to the current object's data
        return "Student: {$this->name} (ID: {$this->id}) - Grade: {$this->grade}%";
    }
}

// Instantiate the object
$student1 = new Student(101, "Aung Aung", 95);

echo $student1->getSummary();
?>
```

# Pro-Tip: PHP 8.0+ Shortcut
If you are using modern PHP, you can use Constructor Property Promotion. This combines the property declaration and the assignment into one line:

```php
<?php
public function __construct(
    private int $id, 
    private string $name, 
    private int $grade
) {}
?>