volatile关键字

自定义注解

反射

异常处理

新特性

@service是加在接口还是加在实现类：接口



## 为什么选择java有什么好处

首先在web的应用场景下，java的生态非常成熟了，比如Spring，xxx等，此外

java还有如下特性

跨平台：jvm

面向对象

内存回收



## Spring设计原理,常见设计模式

ioc 控制反转，把对象注入ioc容器里面，然后需要就去取。@autowire 按类型 @Resource 按名称

aop： 面向切面编程，纵向切割（事务处理、日志管理、权限控制），利用动态代理



工厂模式

单例模式

代理模式：aop

模版模式：JDBC

观察者模式：领域驱动

## 值传递和引⽤传递的区别 

 参数传递⽅式主要有值传递和引⽤传递两种，但需要注意的是 Java 中的参数传递是始终按值传递的。 

值传递：在值传递中，传递给函数的是实际参数的值的副本。当在函数内修改这个副本时，不会影响到原始值 

引⽤传递：⽅法接收的直接是实参所引⽤的对象在堆中的地址，不会创建副本，对形参的修改将影响到实参。

 但在 Java 中，虽然传递的是引⽤的值（对象的地址），但仍然是按值传递。实际上，传递的是引⽤的副本，因此 在函数内对引⽤的修改会影响到原始的引⽤，但⽆法修改引⽤指向的对象。

对于基本类型，不会被改变

对于类类型存在堆空间的会被改变

```java
public class test03 {
    public static void main(String[] args) {
        int i = 1;
        add(i);
        // 1
        System.out.println(i);
        add1(i);
        // 1
        System.out.println(i);
        nums1 nums1 =new nums1(i);
        add2(nums1);
        // 2
        System.out.println(nums1.num);

    }
    public static void add(int i)
    {
        i++;
    }
    public static void add1 (Integer i)
    {
        i++;
    }
    public static void add2(nums1 i)
    {
        i.num++;
    }
    private static class nums1{
        public int num;
        nums1(int i){
            this.num = i;
        }
    }
    
}
```

## 抽象类和接口有什么区别，如何区分使用

区别

