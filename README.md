# MySQL-courses-easy-medium-hard-

### 1. Recyclable and Low Fat Products

Table: Products

+-------------+---------+  
| Column Name | Type    |  
+-------------+---------+  
| product_id  | int     |  
| low_fats    | enum    |  
| recyclable  | enum    |  
+-------------+---------+  

product_id is the primary key (column with unique values) for this table.  
low_fats is an ENUM (category) of type ('Y', 'N') where 'Y' means this product is low fat and 'N' means it is not.  
recyclable is an ENUM (category) of types ('Y', 'N') where 'Y' means this product is recyclable and 'N' means it is not.  
 

Write a solution to find the ids of products that are both low fat and recyclable.  

Return the result table in any order.  
#####################################################  
select product_id from Products  
where low_fats = 'Y' and recyclable = 'Y';  
#####################################################  

### 2. Find Customer Referee  

Table: Customer
  
+-------------+---------+  
| Column Name | Type    |  
+-------------+---------+  
| id          | int     |  
| name        | varchar |  
| referee_id  | int     |  
+-------------+---------+  
In SQL, id is the primary key column for this table.  
Each row of this table indicates the id of a customer, their name, and the id of the customer who referred them.  
 

Find the names of the customer that are not referred by the customer with id = 2.  

Return the result table in any order.  
