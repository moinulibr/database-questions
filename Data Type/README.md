
### ✅ MySQL Data Types Cheatsheet (with Size, Range, Use Case)

| Data Type         | Size (Bytes) | Signed Range                             | Unsigned Range                  | Max Digits                       | Example Use Case                        |
| ----------------- | ------------ | ---------------------------------------- | ------------------------------- | -------------------------------- | --------------------------------------- |
| `TINYINT`         | 1            | -128 to 127                              | 0 to 255                        | 3 digits                         | Age (0–150), Ratings (0–5)              |
| `SMALLINT`        | 2            | -32,768 to 32,767                        | 0 to 65,535                     | 5 digits                         | Number of likes, small counters         |
| `MEDIUMINT`       | 3            | -8,388,608 to 8,388,607                  | 0 to 16,777,215                 | 7 digits                         | Moderate record counts                  |
| `INT` / `INTEGER` | 4            | -2,147,483,648 to 2,147,483,647          | 0 to 4,294,967,295              | 10 digits                        | ID, salary, total views                 |
| `BIGINT`          | 8            | -9,223,372,036,854,775,808 to +9,223...  | 0 to 18,446,744,073,709,551,615 | 19 digits                        | Phone numbers, National ID              |
| `DECIMAL(p,s)`    | Varies       | Custom fixed-point precision             | Custom precision                | e.g. `DECIMAL(10,2)` → 10 digits | Money values (৳12345678.90)             |
| `FLOAT`           | 4            | Approx. ±3.4E38                          | Approx. ±3.4E38                 | \~6-7 digits                     | Sensor data, temperature                |
| `DOUBLE`          | 8            | Approx. ±1.7E308                         | Approx. ±1.7E308                | \~15-17 digits                   | Scientific data, accurate measurements  |
| `BIT`             | 1 bit        | 0 or 1                                   | 0 or 1                          | 1 digit                          | Boolean flags                           |
| `BOOLEAN`         | 1            | False (0), True (1)                      | —                               | 1 digit                          | Status, active/inactive                 |
| `CHAR(n)`         | n (fixed)    | —                                        | —                               | Up to 255 characters             | Gender ('M', 'F'), Country Code ('BD')  |
| `VARCHAR(n)`      | Varies       | —                                        | —                               | Up to 65,535 bytes\*             | Names, Emails, Flexible strings         |
| `TEXT`            | Up to 64KB   | —                                        | —                               | Up to 65,535 characters          | Article content, comments               |
| `TINYTEXT`        | Up to 255B   | —                                        | —                               | Up to 255 characters             | Short description, summary              |
| `MEDIUMTEXT`      | Up to 16MB   | —                                        | —                               | Up to 16,777,215 characters      | Medium-size documents                   |
| `LONGTEXT`        | Up to 4GB    | —                                        | —                               | Up to 4,294,967,295 characters   | Long articles, books                    |
| `DATE`            | 3            | '1000-01-01' to '9999-12-31'             | —                               | —                                | Birthdate, Published date               |
| `DATETIME`        | 8            | '1000-01-01 00:00:00' to '9999-12-31...' | —                               | —                                | Created\_at, Updated\_at                |
| `TIMESTAMP`       | 4            | '1970-01-01 00:00:01' UTC to 2038...     | —                               | —                                | Auto time record, created\_at           |
| `TIME`            | 3            | '-838:59:59' to '838:59:59'              | —                               | —                                | Duration, working hours                 |
| `YEAR`            | 1            | 1901 to 2155                             | —                               | 4 digits                         | Academic year, Product year             |
| `ENUM`            | Varies       | Fixed set of values                      | —                               | —                                | Status (`active`, `inactive`), Roles    |
| `SET`             | Varies       | Multiple predefined values               | —                               | —                                | Permissions (`read`, `write`, `delete`) |

> 📝 `VARCHAR(n)` actual storage depends on character set and row size — max is 65,535 bytes including row overhead.

---