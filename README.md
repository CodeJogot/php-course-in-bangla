# PHP Introduction

## Table of Contents

1. [What is PHP?](#what-is-php)
2. [Why Use PHP?](#why-use-php)
3. [How PHP Works](#how-php-works)
4. [Installing PHP](#installing-php)
5. [Writing Your First PHP Script](#writing-your-first-php-script)
6. [PHP Syntax](#php-syntax)
7. [Embedding PHP in HTML](#embedding-php-in-html)
8. [PHP Variables](#php-variables)
9. [PHP Data Types](#php-data-types)
10. [PHP Comments](#php-comments)
11. [Key Points to Remember](#key-points-to-remember)

---

## 1. What is PHP?

PHP (Hypertext Preprocessor) হলো একটি **server-side scripting language** যা ওয়েব ডেভেলপমেন্টের জন্য ব্যবহৃত হয়। এটি মূলত **dynamic website এবং web applications** তৈরি করতে ব্যবহৃত হয়। PHP সাধারণত **HTML-এর সাথে মিশে কাজ করে** এবং এটি ডাটাবেসের সাথে সংযোগ স্থাপনে সক্ষম।

**PHP-এর কিছু গুরুত্বপূর্ণ বৈশিষ্ট্য:**

- Open-source এবং বিনামূল্যে পাওয়া যায়।
- Server-side language (কোড ব্রাউজারে নয়, সার্ভারে এক্সিকিউট হয়)।
- Database (MySQL, PostgreSQL, Oracle) এর সাথে সহজেই কাজ করতে পারে।
- PHP ফাইলের এক্সটেনশন `.php` হয়।

---

## 2. Why Use PHP?

PHP ব্যবহার করার প্রধান কিছু কারণ:

1. **Easy to Learn**: PHP শেখা সহজ এবং এটি HTML-এর সাথে সহজেই একত্রে ব্যবহার করা যায়।
2. **Server-Side Execution**: PHP কোড ব্রাউজারে সরাসরি দেখা যায় না, এটি সার্ভারে execute হয় এবং HTML output পাঠায়।
3. **Database Integration**: PHP-এর মাধ্যমে বিভিন্ন ডাটাবেসের সাথে সংযোগ করা যায়, যেমন **MySQL, PostgreSQL, SQLite**।
4. **Framework Support**: Laravel, CodeIgniter, Symfony-এর মতো জনপ্রিয় frameworks PHP ব্যবহার করে।
5. **Cross-Platform Compatibility**: PHP Windows, Linux, Mac-এ সমানভাবে কাজ করে।

---

## 3. How PHP Works

PHP সাধারণত **server-side** এ execute হয় এবং ব্রাউজারে HTML output পাঠায়। নিচের ধাপে এটি কিভাবে কাজ করে তা দেখানো হলো:

1. **User** ব্রাউজারে একটি PHP ফাইল অনুরোধ করে (e.g., `index.php`).
2. **Web Server (Apache/Nginx)** PHP interpreter-কে ফাইলটি execute করতে বলে।
3. **PHP Interpreter** কোডটি process করে এবং output হিসাবে **HTML generate** করে।
4. **Web Server** HTML ব্রাউজারে পাঠায়।

![PHP Workflow](https://upload.wikimedia.org/wikipedia/commons/2/27/PHP-logo.svg)

---

## 4. Installing PHP

PHP ব্যবহার করতে হলে প্রথমে আমাদের কম্পিউটারে এটি ইন্সটল করতে হবে। PHP ইন্সটল করার জন্য বিভিন্ন সফটওয়্যার package রয়েছে, যেমন:

1. **XAMPP (Windows, Linux, Mac)**
2. **WAMP (Windows)**
3. **MAMP (Mac)**
4. **LAMP (Linux)**

**XAMPP ইন্সটল করার ধাপ:**

1. [XAMPP Official Website](https://www.apachefriends.org/) থেকে XAMPP ডাউনলোড করুন।
2. সফটওয়্যারটি ইন্সটল করুন।
3. **Apache এবং MySQL** সার্ভার চালু করুন।
4. ব্রাউজারে গিয়ে `http://localhost` লিখে চেক করুন।

---

## 5. Writing Your First PHP Script

একটি **Hello World** PHP স্ক্রিপ্ট তৈরি করা যাক:

```php
<?php
  echo "Hello, World!";
?>
```

**ব্যাখ্যা:**

- `<?php` দিয়ে PHP কোড শুরু হয়।
- `echo` ব্যবহার করে output দেখানো হয়।
- `?>` দিয়ে PHP কোড শেষ করা হয়।

এটি চালাতে `index.php` নামে একটি ফাইল তৈরি করুন এবং **XAMPP** চালু রেখে ব্রাউজারে `http://localhost/index.php` ভিজিট করুন।

---

## 6. PHP Syntax

PHP syntax সাধারণত **C, Java, Python** এর মতোই। PHP কোড **semicolon (`;`)** দিয়ে শেষ করতে হয়।

```php
<?php
  $name = "John";  // Variable
  echo "Welcome, " . $name;
?>
```

---

## 7. Embedding PHP in HTML

PHP কোড HTML-এর মধ্যে **embed** করা যায়:

```php
<!DOCTYPE html>
<html>
<head>
    <title>PHP with HTML</title>
</head>
<body>
    <h1>Welcome to My Website</h1>
    <p>The current year is: <?php echo date("Y"); ?></p>
</body>
</html>
```

---

## 8. PHP Variables

PHP-তে **variables** ঘোষণা করার জন্য `$` চিহ্ন ব্যবহার করা হয়:

```php
<?php
  $name = "Alice";
  $age = 25;
  echo "Name: " . $name . "<br>";
  echo "Age: " . $age;
?>
```

**নিয়ম:**

- Variable নাম `$` চিহ্ন দিয়ে শুরু করতে হয়।
- Variable case-sensitive হয় (e.g., `$name` এবং `$Name` আলাদা)।
- Variable নাম **letter** বা **underscore (\_) দিয়ে শুরু** হতে পারে, তবে সংখ্যা দিয়ে শুরু করা যাবে না।

---

## 9. PHP Data Types

PHP-তে বিভিন্ন ধরণের **data types** আছে:

| Data Type | Example                        |
| --------- | ------------------------------ |
| String    | `"Hello"`                      |
| Integer   | `123`                          |
| Float     | `3.14`                         |
| Boolean   | `true / false`                 |
| Array     | `["Apple", "Banana", "Mango"]` |
| Object    | `class Person {}`              |
| NULL      | `NULL`                         |

```php
<?php
  $string = "Hello, PHP!";
  $integer = 42;
  $float = 3.14;
  $boolean = true;
  $array = ["Apple", "Mango", "Banana"];
  var_dump($string);
?>
```

---

## 10. PHP Comments

PHP-তে **comments** ব্যবহার করা হয় কোড ব্যাখ্যা করার জন্য। এগুলো execute হয় না।

```php
<?php
  // This is a single-line comment

  /*
     This is a
     multi-line comment
  */
?>
```

---

## 11. Key Points to Remember

- PHP একটি **server-side scripting language**।
- এটি সাধারণত **dynamic websites** এবং **web applications** তৈরিতে ব্যবহৃত হয়।
- PHP ফাইলের এক্সটেনশন **`.php`** হয়।
- PHP কোড **server**-এ execute হয় এবং **HTML output** ব্রাউজারে পাঠায়।
- PHP **variables `$` চিহ্ন দিয়ে শুরু** হয়।
- PHP **MySQL, PostgreSQL** সহ বিভিন্ন ডাটাবেসের সাথে কাজ করতে পারে।

[Back to Top](#php-introduction)
