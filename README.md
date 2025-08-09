
# Database Related Interview Questions
## 1. Basic Database Concepts
1. What is a **Database**?
2. What is a **DBMS**?
3. What are the **functions of DBMS**?
4. Difference between **DBMS and RDBMS**?
5. What is **SQL**?
6. Difference between **SQL and NoSQL**?
7. What is a **primary key**?
8. What is a **foreign key**?
9. What is a **unique key**?
10. Difference between **unique key and primary key**?
11. What is a **composite key**?
12. What is a **super key**?
13. What is a **candidate key**?
14. What is a **surrogate key**?
15. What is a **schema**?
16. What is a **view**?
17. What is **metadata**?
18. What is a **domain constraint**?
19. What are **constraints in SQL**?
20. What is a **table**?
21. What is a **tuple**?
22. What is an **attribute**?
23. Difference between **DELETE, TRUNCATE, and DROP**?
24. Difference between **WHERE and HAVING**?
25. Difference between **IN and EXISTS**?
26. Difference between **UNION and UNION ALL**?
27. What is a **subquery**?
28. What is a **correlated subquery**?
29. Difference between **JOIN and UNION**?
30. What are the types of **JOINs** in SQL?
31. What is a **self join**?
32. What is a **cross join**?
33. What is a **natural join**?
34. What is a **Cartesian product**?

---

## 2. SQL Command Categories
35. What are **DDL, DML, DCL, and TCL**?
36. Difference between **DML and DDL**?
37. Examples of **DDL commands**?
38. Examples of **DML commands**?
39. What is **COMMIT and ROLLBACK**?
40. What is **SAVEPOINT**?
41. What is **GRANT and REVOKE**?

---

## 3. Normalization
42. What is **normalization**?
43. Why is **normalization important**?
44. Types of **normal forms** (1NF, 2NF, 3NF, BCNF)?
45. **1NF with example**?
46. **2NF with example**?
47. **3NF with example**?
48. What is **BCNF**?
49. What is **functional dependency**?
50. What is **transitive dependency**?
51. What is **partial dependency**?
52. What is **denormalization**?
53. Difference between **normalization and denormalization**?
54. Advantages of **normalization**?
55. Disadvantages of **normalization**?
56. What is **redundancy**?
56.1. What is **Denormalization**?
56.2. Difference between **Normalization and Denormalization**?
---

## 4. Indexing & Query Performance
57. What is an **index**?
58. How do **indexes improve performance**?
59. What is a **clustered index**?
60. What is a **non-clustered index**?
61. Difference between **clustered and non-clustered index**?
62. What is a **covering index**?
63. What are **composite indexes**?
64. What is **index cardinality**?
65. When to **avoid indexes**?
66. What is **query optimization**?
67. What is a **query plan / execution plan**?
68. What is **EXPLAIN / EXPLAIN ANALYZE**?
69. How to **identify slow queries**?
70. How to **optimize JOIN queries**?
71. How does **caching help performance**?
72. How to avoid **full table scans**?
73. Difference between **sequential scan and index scan**?
74. What is **index selectivity**?

---

## 5. Data Integrity & Constraints
75. What is **data integrity**?
76. What is **referential integrity**?
77. What are **NOT NULL, UNIQUE, CHECK, DEFAULT constraints**?
78. What is a **default constraint**?
79. What is a **check constraint**?
80. What is **ON DELETE CASCADE**?
81. What is **ON UPDATE CASCADE**?
82. What is **constraint violation**?
83. How do **constraints help maintain quality**?

---

## 6. Transactions & ACID
84. What is a **database transaction**?
85. What are **ACID properties**?
86. What is **atomicity**?
87. What is **consistency**?
88. What is **isolation**?
89. What is **durability**?
90. What is **isolation level**?
91. Types of **isolation levels**?
92. What is **locking**?
93. Difference: **optimistic vs pessimistic locking**?
94. What is a **deadlock**?
95. How to **prevent deadlocks**?
96. Difference: **shared lock vs exclusive lock**?

---

## 7. Stored Procedures, Triggers & Functions
97. What is a **stored procedure**?
98. What is a **function in SQL**?
99. Difference between **procedure and function**?
100. What are **triggers**?
101. Types of **triggers** (BEFORE, AFTER)?
102. Use cases of **triggers**?
103. What is a **cursor**?
104. Difference: **implicit vs explicit cursor**?

---

## 8. Advanced / Real-World Database Design
105. How to design a **multi-tenant system**?
106. How to design an **e-commerce DB**?
107. How to build an **order management system**?
108. How to store **audit trails / logs**?
109. What is **schema migration**?
110. What is **data migration**?
111. How to handle **large datasets**?
112. What is **horizontal scaling**?
113. What is **vertical scaling**?
114. What is **replication**?
115. What is **master-slave replication**?
116. What is **sharding**?
117. What is **partitioning**?
118. What is a **materialized view**?
119. What is a **trigger log table**?
120. How to model **many-to-many relationships**?
121. How to handle **optional relationships** in database schema?

---

## 9. NoSQL / MongoDB / Redis
122. What is **NoSQL**?
123. Types of **NoSQL** (document, key-value, column, graph)?
124. When to use **NoSQL over SQL**?
125. What is **MongoDB**?
126. What is a **document in MongoDB**?
127. What is a **collection**?
128. What is **ObjectId**?
129. What is the **Aggregation Pipeline**?
130. What is **MapReduce**?
131. What is **indexing in MongoDB**?
132. What is a **TTL index**?
133. What is a **capped collection**?
134. **Embedded vs Referenced documents**?
135. How to perform **joins in MongoDB ($lookup)**?
136. What is **Redis**?
137. Use cases of **Redis**?
138. Difference: **Redis vs MongoDB**?
139. What is **cache invalidation**?

---

## 10. Security, Compliance & Backup
140. How to **secure sensitive data** in DB?
141. What is **SQL Injection**?
142. How to **prevent SQL injection**?
143. What is **role-based access control (RBAC)**?
144. What is **encryption in DBMS**?
145. What is **hashing**?
146. What is **GDPR**?
147. What is **data anonymization**?
148. What is **data masking**?
149. What is **backup and restore**?
150. What is **point-in-time recovery**?
151. **Hot vs Warm vs Cold backups**?

---

## 11. OLTP, OLAP, and Data Warehousing
152. What is **OLTP**?
153. What is **OLAP**?
154. Difference between **OLTP and OLAP**?
155. What is a **data warehouse**?
156. What is **ETL**?
157. Difference: **ETL vs ELT**?
158. What is a **fact table**?
159. What is a **dimension table**?
160. What is a **star schema**?
161. What is a **snowflake schema**?

---

## 12. Scenario-Based / Problem Solving
162. A report is **slow  how to fix it**?
163. **10M rows in product table  how to search faster**?
164. How to implement **soft delete**?
165. How to **permanently delete data safely**?
166. How to **rollback accidental DELETE**?
167. How to **track changes in DB**?
168. How to **audit updates/deletes in sensitive data**?
169. How to **reduce DB storage size**?
170. How to store **product variants (size/color)**?
171. How to build **order system for multi-vendor marketplace**?
172. You've been told to **speed up the app**  where do you start?
173. What tools or metrics do you use to **measure database performance**?
174. How to design a scalable DB for **dynamic product attributes**?
