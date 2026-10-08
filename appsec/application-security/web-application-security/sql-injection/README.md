# SQL Injection

**SQL Injection (SQLi)** is a type of security vulnerability that occurs when an attacker is able to manipulate a web application's SQL query by injecting malicious SQL code. SQL injection attacks can lead to unauthorized access to a database, data manipulation, data theft, and even potentially complete control over a web application's database.

There are several types of SQL Injection attacks:

1. **Classic SQL Injection:**
   * **Example:** Consider a web application that uses a query like this to authenticate users:

     ```sql
     SELECT * FROM users WHERE username = '$username' AND password = '$password'
     ```

     An attacker might input a username like `' OR '1'='1` and leave the password field empty. The SQL query becomes:

     ```sql
     SELECT * FROM users WHERE username = '' OR '1'='1' AND password = ''
     ```

     Since `'1'='1'` is always true, the attacker can log in without knowing a valid password.
2. **Blind SQL Injection:**
   * In Blind SQL Injection, the attacker doesn't directly see the application's responses but can infer information through boolean-based or time-based techniques.
   * **Example:** An attacker might input a username like `admin' AND 1=1--` in a login form. If the application responds positively (e.g., "Welcome, admin"), the attacker knows the input is valid.
3. **Time-Based Blind SQL Injection:**
   * Similar to Blind SQL Injection but relies on timing delays in database responses to infer information.
   * **Example:** An attacker might input a username like `admin' AND IF(1=1, SLEEP(5), 0)--` in a login form. If the application takes significantly longer to respond, it indicates a true condition.
4. **Out-of-Band SQL Injection:**
   * In Out-of-Band SQL Injection, data is exfiltrated through a different channel, such as DNS requests.
   * **Example:** An attacker might craft an input that triggers DNS requests to a controlled server, revealing sensitive information.
5. **Second-Order SQL Injection:**
   * In Second-Order SQL Injection, the malicious payload is stored in the application's database and executed later, often by another user.
   * **Example:** An attacker submits a comment containing SQL injection, which is stored in the application's database. Another user views the comment, and the payload is executed in their context.
6. **Boolean-Based SQL Injection:**
   * In Boolean-Based SQL Injection, the attacker's payload results in a true or false condition.
   * **Example:** An attacker might input a username like `admin' AND '1'='1` to test if a condition is true or `'1'='2` to test if it's false.

SQL Injection vulnerabilities are critical security issues that can lead to data breaches and unauthorized access to databases. To prevent SQL Injection, developers should use prepared statements or parameterized queries and avoid directly inserting user input into SQL queries. Security testing and code reviews are essential to identify and mitigate SQL Injection vulnerabilities in web applications.

## In this section

* 🚧 [Union Based SQL Injection](union-based-sql-injection.md)
* 🚧 [Blind SQL Injection](blind-sql-injection.md)
