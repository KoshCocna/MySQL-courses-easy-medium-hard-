# MySQL-courses-(LeetCode)

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

#####################################################  

select name from Customer  
where referee_id != 2 or referee_id is null;  

--where coalesce(referee_id, 0) != 2;

#####################################################  

### 3. Big Countries  

Table: World
  
+-------------+---------+  
| Column Name | Type    |  
+-------------+---------+  
| name        | varchar |  
| continent   | varchar |  
| area        | int     |  
| population  | int     |  
| gdp         | bigint  |  
+-------------+---------+  

name is the primary key (column with unique values) for this table.  
Each row of this table gives information about the name of a country, the continent to which it belongs, its area, the population, and its GDP value.   
   
  
A country is big if:  

it has an area of at least three million (i.e., 3000000 km2), or  
it has a population of at least twenty-five million (i.e., 25000000).  
Write a solution to find the name, population, and area of the big countries.  
  
Return the result table in any order.  

#####################################################  

select name, population, area from World  
where area >= 3000000 or population >= 25000000;  

#####################################################  

### 2. Find Customer Referee  

![image](https://github.com/KoshCocna/MySQL-courses-easy-medium-hard-/assets/76080450/55b4e426-cc90-4246-8800-4bf648b7b161)

select distinct author_id as id from Views  
where author_id = viewer_id  
order by id;  


