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
