# 1. Deffinition
```java
PriorityQueue<Integer> q = new PriorityQueue<>();
```
默认是小顶堆

# 2. Operation
```java
q.add(int x); // 插入
q.offer();

q.peek();
q.poll();
q.remove();

q.clear();      // 移除所有元素
q.contains(int x);   // boolean

q.toArray();
q.toArray(Object o);    //可以指定类型
```