# MySQL-courses-(LeetCode)

### 1. Recyclable and Low Fat Products

![image](https://github.com/KoshCocna/MySQL-courses-easy-medium-hard-/assets/76080450/c3f0e58a-9a6a-4a1d-88b6-b62eca95fc2d)

select product_id from Products  
where low_fats = 'Y' and recyclable = 'Y';  

### 2. Find Customer Referee  

![image](https://github.com/KoshCocna/MySQL-courses-easy-medium-hard-/assets/76080450/072cd77a-72d7-425d-9516-ecb525bb3097)

select name from Customer  
where referee_id != 2 or referee_id is null;  

--where coalesce(referee_id, 0) != 2;

### 3. Big Countries  

![image](https://github.com/KoshCocna/MySQL-courses-easy-medium-hard-/assets/76080450/c408049e-a993-4e59-ab7e-1bff9768ad9c)
 
select name, population, area from World  
where area >= 3000000 or population >= 25000000;    

### 4. Article Views I  

![image](https://github.com/KoshCocna/MySQL-courses-easy-medium-hard-/assets/76080450/55b4e426-cc90-4246-8800-4bf648b7b161)

select distinct author_id as id from Views  
where author_id = viewer_id  
order by id;  


