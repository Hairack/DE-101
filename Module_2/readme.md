1. Установил БД Dbeaver
2. Создал таблицы согласно видео урока, скопировав скрипты в приложение.
   

<h2>SQL запросы</h2>
	<h5>Выборка продаж по клиентам от 1000 до 5000</h5>

<div class="highlight highlight-source-sql notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">select distinct</span>
	state ,
	<span class="pl-c1">count</span>(order_id) <span class="pl-k">as</span> orders,
	<span class="pl-c1">sum</span>(sales) <span class="pl-k">as</span> rev
<span class="pl-k">from</span> orders
<span class="pl-k">group by</span> <span class="pl-c1">1</span>
<span class="pl-k">having</span> <span class="pl-c1">count</span>(order_id) <span class="pl-k">&gt;</span> <span class="pl-c1">10</span>
<span class="pl-k">order by</span> rev <span class="pl-k">desc</span>;</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="select distinct(customer_name),
	   sales,
	   segment
from orders
where sales > 1000 and sales < 5000
group by customer_name, sales, segment  
order by sales desc;" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
