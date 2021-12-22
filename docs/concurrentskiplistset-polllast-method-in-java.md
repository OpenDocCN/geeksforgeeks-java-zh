# Java 中的 ConcurrentSkipListSet pollLast()方法

> 原文:[https://www . geeksforgeeks . org/concurrentskiplistset-poll last-method-in-Java/](https://www.geeksforgeeks.org/concurrentskiplistset-polllast-method-in-java/)

**java . util . concurrentskiplistset**的 **pollLast()** 方法是 Java 中的一个内置函数，它返回检索并删除最后一个(最高的)元素，如果这个集合为空，则返回 null。

**语法:**

```
public E pollLast()
```

**返回值:**函数返回检索并删除最后一个(最高的)元素，如果该集合为空，则返回 null。

下面的程序说明了 ConcurrentSkipListSet.pollLast()方法:

**程序 1:**

```
// Java program to demonstrate pollLast()
// method of ConcurrentSkipListSet

import java.util.concurrent.*;

class ConcurrentSkipListSetpollLastExample1 {
    public static void main(String[] args)
    {
        // Creating a set object
        ConcurrentSkipListSet<Integer> Lset = new ConcurrentSkipListSet<Integer>();

        // Adding elements to this set
        for (int i = 10; i <= 50; i += 10)
            Lset.add(i);

        // Printing the content of the set
        System.out.println("Contents of the set: " + Lset);

        // Retrieving and removing Last element of the set
        System.out.println("The Last element of the set: " + Lset.pollLast());

        // Printing the content of the set after pollLast()
        System.out.println("Contents of the set after pollLast: " + Lset);
    }
}
```

**Output:**

```
Contents of the set: [10, 20, 30, 40, 50]
The Last element of the set: 50
Contents of the set after pollLast: [10, 20, 30, 40]

```

**程序 2:**

```
// Java program to demonstrate pollLast()
// method of ConcurrentSkipListSet

import java.util.concurrent.*;

class ConcurrentSkipListSetpollLastExample2 {
    public static void main(String[] args)
    {
        // Creating a set object
        ConcurrentSkipListSet<Integer> Lset = new ConcurrentSkipListSet<Integer>();

        // Printing the content of the set
        System.out.println("Contents of the set: " + Lset);

        // Retrieving and removing Last element of the set
        System.out.println("The Last element of the set: " + Lset.pollLast());
    }
}
```

**Output:**

```
Contents of the set: []
The Last element of the set: null

```

**参考:**
[https://docs . Oracle . com/javase/8/docs/API/Java/util/concurrentskiplistset . html # pollast–](https://docs.oracle.com/javase/8/docs/api/java/util/concurrent/ConcurrentSkipListSet.html#pollLast--)