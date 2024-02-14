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

### 5. Invalid Tweets 

![image](https://github.com/KoshCocna/MySQL-courses-easy-medium-hard-/assets/76080450/f1c624a8-4415-4a8c-b839-f823525fa09f)

select tweet_id from Tweets  
where length(content) > 15;  

### 6. Replace Employee ID With The Unique Identifier

![image](https://github.com/KoshCocna/MySQL-courses-easy-medium-hard-/assets/76080450/0d4e6e85-327e-4e6d-b851-50b496b5af5b)

select unique_id, name from Employees left join EmployeeUNI on EmployeeUNI.id = Employees.id;  

--select unique_id, name from EmployeeUNI right join Employees on EmployeeUNI.id = Employees.id;  
 
### 7. Product Sales Analysis I

![image](https://github.com/KoshCocna/MySQL-courses-easy-medium-hard-/assets/76080450/19b4f27d-8e33-4fe4-8483-f473fae14fd6)

select product_name, year, price from Sales left join Product on Sales.product_id = Product.product_id;  

--select product_name, year, price from Product right join Sales on Sales.product_id = Product.product_id;  

### 8. Customer Who Visited but Did Not Make Any Transactions

![image](https://github.com/KoshCocna/MySQL-courses-easy-medium-hard-/assets/76080450/a42f4217-4405-4624-af1a-de53186af98b)

select v.customer_id, count(v.visit_id) as count_no_trans   
from Visits v   
left join Transactions t   
on v.visit_id = t.visit_id    
where t.transaction_id is null   
group by v.customer_id;   

### 9. Rising Temperature

![image](https://github.com/KoshCocna/MySQL-courses-easy-medium-hard-/assets/76080450/ddabd775-b60c-4362-8e26-23171b4f53e9)

select w2.id from Weather w1   
join Weather w2  
on w2.temperature > w1.temperature and   
datediff(w2.recordDate, w1.recordDate) = 1;  

### 10. 
