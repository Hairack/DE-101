1. Установил БД Dbeaver
2. Создал таблицы согласно видео урока, скопировав скрипты в приложение.
   

<h2>SQL запросы</h2>
<pre>
       <div class="container">
        <div class="block two first">
            <h2>Выборка покупателей от 1000 до 5000</h2>
                       <div class="wrapper">                                                
select distinct(customer_name),
	   sales,
	   segment
from orders
where sales > 1000 and sales < 5000
group by customer_name, sales, segment  
order by sales desc               
            </div>
        </div>
    </div>
</pre>
