
নিচের টেবিলে MySQL-এর সর্বাধিক ব্যবহৃত ডেটা টাইপগুলোর তালিকা, তাদের আকার, সীমা, এবং ব্যবহারের উদাহরণ দেওয়া হলো।

| Data Type | Size (Bytes) | Signed Range | Unsigned Range | Max Digits / Length | Fixed/Dynamic | Example Use Case |
|---|---|---|---|---|---|---|
| **`TINYINT`** | 1 | -128 to 127 | 0 to 255 | 3 digits | Fixed | Age, ratings (0-5 stars) |
| **`SMALLINT`** | 2 | -32,768 to 32,767 | 0 to 65,535 | 5 digits | Fixed | Small counters, view counts |
| **`MEDIUMINT`** | 3 | -8,388,608 to 8,388,607 | 0 to 16,777,215 | 7 digits | Fixed | Moderate record counts |
| **`INT`** | 4 | -2,147,483,648 to 2,147,483,647 | 0 to 4,294,967,295 | 10 digits | Fixed | Product quantity, employee ID |
| **`BIGINT`** | 8 | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 | 0 to 18,446,744,073,709,551,615 | 19 digits | Fixed | Phone number, large timestamps |
| **`FLOAT`** | 4 | ±1.175494351 E-38 to ±3.402823466 E+38 | N/A | ~7 digits | Fixed | Temperature, sensor data |
| **`DOUBLE`** | 8 | ±2.2250738585072014 E-308 to ±1.7976931348623157 E+308 | N/A | ~15 digits | Fixed | Scientific calculations |
| **`DECIMAL(p,s)`** | Varies (e.g., 5 digits = 3 bytes) | Depends on precision (p) | Depends on precision (p) | Up to 65 digits | Fixed | Accurate money (৳1234567.89), prices |
| **`CHAR(n)`** | `n` bytes | N/A | N/A | `n` characters (max 255) | Fixed | Country codes ('BD'), zip codes |
| **`VARCHAR(n)`** | `L+1` bytes | N/A | N/A | `L` characters (max 65,535 bytes) | Dynamic | Names, addresses, emails |
| **`TINYTEXT`** | `L+1` bytes | N/A | N/A | Up to 255 characters | Dynamic | Short notes, tags |
| **`TEXT`** | `L+2` bytes | N/A | N/A | Up to 65,535 characters | Dynamic | Articles, long descriptions |
| **`MEDIUMTEXT`** | `L+3` bytes | N/A | N/A | Up to 16,777,215 characters | Dynamic | Blog posts, large descriptions |
| **`LONGTEXT`** | `L+4` bytes | N/A | N/A | Up to 4,294,967,295 characters | Dynamic | Very large documents, reports |
| **`DATE`** | 3 | '1000-01-01' to '9999-12-31' | N/A | 'YYYY-MM-DD' | Fixed | Birth date, event date |
| **`DATETIME`** | 8 | '1000-01-01 00:00:00' to '9999-12-31 23:59:59' | N/A | 'YYYY-MM-DD HH:MM:SS' | Fixed | Created at, updated at |
| **`TIMESTAMP`** | 4 | '1970-01-01 00:00:01' to '2038-01-19 03:14:07' (UTC) | N/A | 'YYYY-MM-DD HH:MM:SS' | Fixed | Logging, record modification time |
| **`TIME`** | 3 | '-838:59:59' to '838:59:59' | N/A | 'HH:MM:SS' | Fixed | Duration, time fields |
| **`YEAR`** | 1 | 1901 to 2155 | N/A | 4 digits (e.g., 2025) | Fixed | Birth year, academic year |
| **`BLOB`** | Varies | N/A | N/A | Up to 65,535 bytes | Dynamic | Small images, files |
| **`MEDIUMBLOB`** | Varies | N/A | N/A | Up to 16,777,215 bytes | Dynamic | Medium-sized images, PDF files |
| **`LONGBLOB`** | Varies | N/A | N/A | Up to 4,294,967,295 bytes | Dynamic | Very large images, videos |
| **`ENUM`** | 1 or 2 | N/A | N/A | Up to 65,535 distinct values | Fixed | Gender ('Male', 'Female', 'Other'), status ('Pending', 'Approved') |
| **`SET`** | Varies | N/A | N/A | Up to 64 unique members | Dynamic | User permissions (e.g., 'Read', 'Write', 'Delete') |

---
**টেবিলের কিছু গুরুত্বপূর্ণ বিষয়:**

* **`L`**: এটি ডেটার actual length বোঝায়। যেমন, `VARCHAR` এর ক্ষেত্রে যদি আপনি ৫ ক্যারেক্টার ইনসার্ট করেন, তাহলে `L=5` হবে।
* **`Size (Bytes)`**: `VARCHAR` ও `TEXT` এর মতো ডেটা টাইপের ক্ষেত্রে এটি variable, কারণ এর আকার ডেটার উপর নির্ভর করে। তবে এর সাথে একটি বা একাধিক বাইট যুক্ত হয় ডেটার দৈর্ঘ্য স্টোর করার জন্য।
* **Fixed/Dynamic**:
    * **Fixed** ডেটা টাইপগুলো সব সময় তাদের নির্ধারিত মেমরি ব্যবহার করে, এমনকি যদি ডেটা ছোট হয়।
    * **Dynamic** ডেটা টাইপগুলো কেবল ডেটার দৈর্ঘ্যের উপর ভিত্তি করে মেমরি ব্যবহার করে, যা মেমরি বাঁচায়।
* **Range**: Signed এবং Unsigned-এর মধ্যে পার্থক্য হলো, `UNSIGNED` ডেটা টাইপ কেবল ধনাত্মক সংখ্যা (positive number) স্টোর করে, ফলে এর রেঞ্জ দ্বিগুণ হয়ে যায়।

--- 
**MySQL-এর প্রায় সব সাধারন Data Type** গুলোর জন্য মেমোরি ব্যবহার কেমন হয়

--

## 🧠 MySQL Data Types: Memory Usage (NULL vs NOT NULL)

MySQL এ একটি ফিল্ড `NULL` হলে মূলত তার জন্য ডাটা রাখা হয় না, কিন্তু প্রতিটি NULL ফিল্ডের জন্য 1-bit ব্যবহৃত হয় **NULL bitmap** এ।

নিচে সাধারন `Data Types` গুলোর মেমোরি ব্যবহার দেয়া হল:

| Data Type                                       | Size When NOT NULL                                | Size When NULL                      |
| ----------------------------------------------- | ------------------------------------------------- | ----------------------------------- |
| **TINYINT**                                     | 1 byte                                            | 0 bytes (but 1 bit in NULL bitmap)  |
| **SMALLINT**                                    | 2 bytes                                           | 0 bytes (1 bit in NULL bitmap)      |
| **MEDIUMINT**                                   | 3 bytes                                           | 0 bytes (1 bit in NULL bitmap)      |
| **INT / INTEGER**                               | 4 bytes                                           | 0 bytes (1 bit in NULL bitmap)      |
| **BIGINT**                                      | 8 bytes                                           | 0 bytes (1 bit in NULL bitmap)      |
| **DECIMAL(p,s)**                                | Depends on p (precision), 4 bytes \~ 17 bytes     | 0 bytes (1 bit in NULL bitmap)      |
| **FLOAT**                                       | 4 bytes (single precision)                        | 0 bytes (1 bit in NULL bitmap)      |
| **DOUBLE**                                      | 8 bytes (double precision)                        | 0 bytes (1 bit in NULL bitmap)      |
| **CHAR(n)**                                     | Fixed n bytes                                     | 0 bytes (1 bit in NULL bitmap)      |
| **VARCHAR(n)**                                  | Actual length + 1 or 2 bytes                      | 0 bytes (1 bit in NULL bitmap)      |
| **TEXT (TINYTEXT, TEXT, MEDIUMTEXT, LONGTEXT)** | Varies (stored separately, + 1-4 bytes pointer)   | Pointer NULL (1 bit used in bitmap) |
| **BLOB (TINYBLOB, BLOB, MEDIUMBLOB, LONGBLOB)** | Same as TEXT                                      | Same (1 bit used in bitmap)         |
| **DATE**                                        | 3 bytes                                           | 0 bytes (1 bit in NULL bitmap)      |
| **DATETIME**                                    | 8 bytes (without fractional), 9-13 bytes with fsp | 0 bytes (1 bit)                     |
| **TIMESTAMP**                                   | 4 bytes (without fsp), 5-9 bytes with fsp         | 0 bytes (1 bit)                     |
| **TIME**                                        | 3 bytes (without fsp), 4-6 bytes with fsp         | 0 bytes (1 bit)                     |
| **YEAR**                                        | 1 byte                                            | 0 bytes (1 bit)                     |
| **ENUM**                                        | 1 or 2 bytes (depends on number of options)       | 0 bytes (1 bit)                     |
| **SET**                                         | 1-8 bytes (bit mask, depends on elements)         | 0 bytes (1 bit)                     |
| **JSON**                                        | Varies                                            | 0 bytes (1 bit in bitmap)           |
| **GEOMETRY types**                              | Varies                                            | 0 bytes (1 bit in bitmap)           |

---

## 🔍 কীভাবে NULL ফিল্ড Memory Consume করে?

* NULL value নিজে কোনো data রাখে না।
* তবে প্রতি row তে একটি "NULL bitmap" থাকে, যেখানে প্রতিটি nullable column এর জন্য **1-bit** রাখা হয়।
* তাই NULL হলে storage কম লাগে, কিন্তু আপনি যদি অনেকগুলো field `NULL` রাখেন, তাহলে শুধুমাত্র 1-bit করে যোগ হয়।

---

## 🧪 Example:

```sql
CREATE TABLE users (
  id INT NOT NULL,
  name VARCHAR(100),
  email VARCHAR(100) NULL,
  age TINYINT NULL
);
```

* `name` যদি NOT NULL হয় এবং `email`, `age` NULL হয়, তাহলে প্রতি row তে:

  * `id` = 4 bytes
  * `name` = actual length + 1 byte
  * `email`, `age` = NULL → শুধু 1-bit করে যোগ হবে (bitmap এ)
  * bitmap: 2 nullable fields → 2 bits = 1 byte (minimum allocation unit)

---

## 📝 Useful Notes:

* InnoDB minimum row size = **1 primary key + 1 row header + 1 NULL bitmap**
* For performance: Avoid unnecessary NULLs in indexed columns.
* `TEXT`, `BLOB` → stored off-page; only pointer stored in row.

---

## ✅ Summary:

* ✅ NOT NULL fields = Fixed size or actual value size.
* ✅ NULL fields = Only 1-bit used in bitmap.
* ✅ Some large types (TEXT/BLOB) → pointer used if NULL.

---

