# 1. Constructor
4 ways
```java
Vector();   // default, size = 10

Vector(int size); // size = size

Vector(int size, int incr);   // 创建指定大小的向量，并且增量用 incr 指定。增量表示向量每次增加的元素数目。

Vector(Collection c);   // Vector that include c
```
 # 2. methods
 ```java
  add(index, Object element); // as .push_back() in c++
 
 	boolean addAll(Collection c) 
  // 将指定 Collection 中的所有元素添加到此向量的末尾，按照指定 collection 的迭代器所返回的顺序添加这些元素。
  
  boolean addAll(int index, Collection c) 
  // 在指定位置将指定 Collection 中的所有元素插入到此向量中。
  
  boolean contains(Object elem) 
  // 如果此向量包含指定的元素，则返回 true。
  
  Object get(int index) 
  // 返回向量中指定位置的元素。
 
  int indexOf(Object elem, int index);  // 不包含返回 -1
  
  Object remove(Object o);
  
  Object set(int index, Object element)
  // 用指定的元素替换此向量中指定位置处的元素。
  
  int size() 
  // 返回此向量中的组件数。
  
 ```
 
 
 
