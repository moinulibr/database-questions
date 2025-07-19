
# 📚 Database Interview Questions (Full List - 160+)

## ✅ 1. Basic Database Questions (General)

1. What is a Database?
2. What is a DBMS? What are its functions?
3. What is the difference between SQL and NoSQL databases?
4. Difference between RDBMS and DBMS?
5. What is a primary key and foreign key?
6. What is a unique key? How is it different from a primary key?
7. What is a composite key?
8. What is a candidate key?
9. What is a surrogate key?
10. What is a super key?
11. What is schema in a database?
12. What is a database instance?
13. What is data redundancy?
14. What is data integrity?
15. What is the difference between a database and a table?

---

## 🔄 2. Database Normalization Related Questions

16. What is normalization? Why is it important?
17. What are the different normal forms (1NF, 2NF, 3NF, BCNF)?
18. Difference between normalization and denormalization?
19. What are the advantages and disadvantages of normalization?
20. What is a functional dependency?
21. What is partial dependency?
22. What is transitive dependency?
23. What is multivalued dependency?
24. What is lossless join?
25. What is dependency preservation?
26. What are anomalies in database (insertion, update, deletion)?
27. What is decomposition?

---

## 🚀 3. Database Optimization / Performance Questions

28. What are indexes? How do they improve performance?
29. What is the difference between clustered and non-clustered index?
30. When should you avoid using indexes?
31. What is query optimization? How does it work?
32. How do you analyze slow queries?
33. How to use EXPLAIN or EXPLAIN ANALYZE to debug queries?
34. What is the Query Execution Plan?
35. How to avoid full table scan?
36. What is a covering index?
37. What is indexing overhead?
38. What are the best practices for indexing?
39. How do you optimize SELECT queries?
40. How do you optimize JOIN queries?
41. What are materialized views?
42. What is caching in the context of databases?
43. How does database connection pooling work?
44. What is table partitioning?
45. What are views and how do they affect performance?

---

## 🔐 4. Data Integrity & Constraints

46. What is referential integrity?
47. What are different types of constraints in SQL? (NOT NULL, UNIQUE, CHECK, DEFAULT, etc.)
48. How do foreign key constraints help maintain integrity?
49. What is cascading delete and update?
50. What is a check constraint?
51. What is default constraint?
52. What is the difference between TRUNCATE and DELETE?
53. What is a NULL value and how is it handled in SQL?
54. What are domain constraints?

---

## 🔁 5. Transactions, ACID, Concurrency

55. What are database transactions?
56. What is ACID property in DBMS?
57. What is the difference between COMMIT and ROLLBACK?
58. What is concurrency control?
59. What is isolation level?
60. What is a dirty read?
61. What is a phantom read?
62. What is a non-repeatable read?
63. What are the different isolation levels (READ UNCOMMITTED, READ COMMITTED, REPEATABLE READ, SERIALIZABLE)?
64. How do you prevent deadlocks?
65. What is a lock in a database?
66. What is optimistic vs pessimistic locking?
67. What is write-ahead logging?
68. What is two-phase commit protocol?

---

## 💼 6. Real-Life & System Design Questions

69. How do you design a database schema for a multi-tenant system?
70. How do you handle large datasets in a web application?
71. What is data sharding?
72. What is replication and why is it used?
73. Difference between vertical and horizontal scaling?
74. What are stored procedures and when should you use them?
75. What are triggers?
76. What is a deadlock and how to prevent it?
77. What is database migration?
78. How do you handle versioning of a database schema?
79. What is data warehousing?
80. What is ETL process?
81. How do you perform database backup and restore?
82. What is connection pooling and how do you use it in Laravel/NestJS/etc.?
83. How do you log or audit database activities?
84. How to secure sensitive data in a database?
85. What is anonymization and pseudonymization?

---

## 📦 7. NoSQL (MongoDB, Redis, etc.) Specific Questions

86. What is document-based storage in MongoDB?
87. What are collections and documents?
88. When to use NoSQL over SQL?
89. What is indexing in MongoDB?
90. How does MongoDB handle relationships? (embedded vs referenced documents)
91. What is the difference between Redis and MongoDB?
92. What is eventual consistency?
93. How is scaling handled in MongoDB?
94. What is aggregation pipeline?
95. What is TTL index in MongoDB?
96. What is Redis used for?
97. What is a key-value store?
98. What is pub/sub in Redis?
99. How does Redis store data in memory?

---

## 🧪 8. Scenario-Based / Practical Questions

100. Suppose you have a slow-loading report. How will you find the cause and optimize it?
101. You have a products table with millions of rows. How would you ensure fast search?
102. How do you design a database for an e-commerce system?
103. What precautions will you take while writing delete queries?
104. How do you track changes to a record (audit trail)?
105. How do you handle soft deletes?
106. How would you model user roles and permissions?
107. How would you ensure email uniqueness with concurrent signups?
108. How would you design a tagging system (many-to-many relationship)?
109. How do you manage product variants and attributes in e-commerce?
110. How to store hierarchical data (e.g., categories, menus)?
111. How would you structure a notification system schema?
112. What is the best way to store images/files in database?
113. What are the pros and cons of storing files as BLOBs?
114. How to prevent SQL injection attacks?

---

## 🧠 9. Advanced SQL / MySQL Specific

115. What is the difference between CHAR and VARCHAR?
116. What is the difference between IN and EXISTS?
117. What is the difference between UNION and UNION ALL?
118. What is the difference between HAVING and WHERE?
119. How do you perform pagination in SQL?
120. What are window functions?
121. What is ROW\_NUMBER(), RANK(), DENSE\_RANK()?
122. What is CTE (Common Table Expression)?
123. What is recursive CTE?
124. What are aggregate functions?
125. What is a correlated subquery?
126. What is a lateral join?
127. How does GROUP BY work internally?
128. How to filter grouped records using HAVING?
129. What is a NULL-safe comparison?
130. What are case statements in SQL?
131. What is the difference between stored function and stored procedure?
132. What is ENUM in MySQL?
133. What are prepared statements?
134. How does AUTO\_INCREMENT work?
135. What are temporary tables?
136. What is the purpose of INFORMATION\_SCHEMA?
137. How to get all table names in a database using SQL?
138. How to get column details using SQL?
139. How to monitor slow queries in MySQL?
140. How to create full-text search index in MySQL?
141. How to sort mixed numeric and string data?
142. How to calculate running total or cumulative sum?
143. How to compare two tables and find unmatched rows?
144. How to avoid N+1 problem in SQL?
145. What is JSON column in MySQL and how to query it?
146. What is UUID and how to use it as primary key?
147. How to store time zones in SQL?
148. What is a pivot table query?
149. How to create audit log triggers in MySQL?
150. What are invisible indexes?
151. What is MySQL Performance Schema?
152. How to tune innodb\_buffer\_pool\_size?
153. What is query cache in MySQL?
154. How to optimize ORDER BY with LIMIT?
155. What is the difference between DELETE and DROP?
156. What is the difference between BETWEEN vs >= AND <= ?
157. How to log all queries executed in MySQL?
158. What is binary log in MySQL?
159. What is the difference between MyISAM and InnoDB?
160. What is the maximum number of rows in MySQL?
161. What is SQL\_MODE in MySQL?
162. What is safe update mode in MySQL?
163. What is "ONLY\_FULL\_GROUP\_BY" mode?
164. What is the difference between logical and physical backup?
165. How to generate ERD (Entity Relationship Diagram) from MySQL?
166. How to perform bulk insert efficiently in MySQL?

---

**Total: 166+ Questions** ✅

