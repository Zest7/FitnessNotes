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







EnterpriseContactDetailVO(typecode=[1049:01, 1049:02, 1049:03], source=[1100:1217, 1100:1801, 1100:1313, 1100:1314, 1100:1315, 1100:1318, 1100:1316, 1100:1121, 1100:1317, 1100:1319, 1100:1320, 1100:1321, 1100:1322, 1100:1323, 1100:2001, 1100:1901, 1100:1159, 1100:1215], value=[13287974652, 18660507925, hr@csf.com.cn, zhaopin@csf.com.cn, jiwei@csf.com.cn, luoxd@csf.com.cn, csf@csf.com.cn, liuhao@csf.com.cn, gaoyz@csf.com.cn, csf1@csf.com.cn, csf1@csf.com, 01063211635, 01063211773, 01063211703, 01063211674, 01063211601, 01063211711, 01063211608, 01063211754, 01063211677, 01063211778, 01063211721, 01063211769, 01063211685, 01063211666, 01063211663, 63211661, 65063388], status=[1099:01, 1099:00], phoneValue=[13287974652, 18660507925], qqValue=[], landlineValue=[01063211635, 01063211773, 01063211703, 01063211674, 01063211601, 01063211711, 01063211608, 01063211754, 01063211677, 01063211778, 01063211721, 01063211769, 01063211663, 63211661, 65063388], emailValue=[hr@csf.com.cn, zhaopin@csf.com.cn, jiwei@csf.com.cn], phoneBusinessValue=[], qqBusinessValue=[], landlineBusinessValue=[01063211685, 01063211666], emailBusinessValue=[luoxd@csf.com.cn, csf@csf.com.cn, liuhao@csf.com.cn, gaoyz@csf.com.cn, csf1@csf.com.cn, csf1@csf.com])
