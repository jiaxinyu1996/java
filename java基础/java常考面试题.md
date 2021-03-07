- String str = "abcd" , String str1 = new String("abcd"),str与str1是否相等

```
不一样；JVM先去常量池中查找该对象，常量池(方法区)中如果存在，直接将str指向常量池中的对象；如果常量池中不存在,则会在常量池中创建一个对象，将str指向它；str1会指向JVM在堆中新创建的对象；两个对象肯定不相等。
```

- String、StringBuffer、StringBuilder的区别

```
String是字符串常量，因为String中存储字符的数组被定义为final类型的，如果经常对字符串
StringBuffer是字符串变量，并且是线程安全的，因为它里面的方法每一个都加了sychronized，多线程下能保证数据的一致性。
StringBuilder是字符串变量，不是线程安全的，单线程的情况下使用它效率会高一些。
```

