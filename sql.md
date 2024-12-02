## having与where的区别:

having是在分组后对数据进行过滤

where是在分组前对数据进行过滤

having后面可以使用聚合函数

where后面不可以使用聚合

## 各种join

cross 和 inner join是一样的，都是返回笛卡尔积，如果有on条件则返回筛选后的结果

left join 和right join 必须跟着on一起使用，返回值只是包含了左边或右边为空的数据。

（记录的比较抽象，只有自己看的懂）

## 常见函数

聚合函数：sum,min,max,avg,coun

其他：if null,round
