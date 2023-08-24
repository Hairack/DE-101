1. Установил БД Dbeaver
2. Создал таблицы согласно видео урока, скопировав скрипты в приложение.
   

<h2>SQL запросы</h2>
	<h5>Выборка продаж по клиентам от 1000 до 5000</h5>

```sql
select distinct(customer_name),
	   sales
from orders
where sales > 1000 and sales < 5000
group by customer_name, sales  
order by sales desc
```
       
<h5>Выборка продаж по регионам</h5>

```sql
select sum(sales) as sales,
	   count (order_id),
	   region
from orders
group by 3
order by sales desc

```
<h5>Выборка возвратов по регионам</h5>

```sql
select distinct (o.region),
 		count(r.order_id) as return
 from orders o 
 join returns r on r.order_id = o.order_id 
 group by 1
 order by 1 desc
```




