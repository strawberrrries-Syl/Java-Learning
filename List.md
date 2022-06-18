# List
有序， 遍历后得到的内容与存入顺序相同（set中不同），且可以有重复元素（set不可以）

# Constructor
```java
List<String> s = new ArrayList<>();
List<List<Integer>> si = new ArrayList<>(); // 2D
```

# methods
```java
void s.add(int index, Object, object);

Boolean addAll(int index, Collection c);

Object get(int index);

Object set(int index, Object, obj);

// 翻转
 void Collections.reverse(List l);

```

# Iteration
```java
for(Iterator it = list.iterator(); while(it.hasNext()))
{

}
```

# sort()
small -> big

Time complexity: O(nlogn). Space complexity: O(logn)
```java
List<Integer> curr = new ArrayList<>();
Collections.sort(curr);
```
if you want to sort as your own rule:
```java
class MyComparator implements Comparator<Integer> {
    @Override
    public int compare(Integer o1, Integer o2) {
        // your rules
        return o2 > o1;
    }
}
```
```java
// in main()
Integer[] a = { 9, 8, 7, 2, 3, 4, 1, 0, 6, 5 };
Comparator cmp = new myComparator();
Array.sort(a, cmp);
```

# String List
```java
String[] strArray = new Srtring[];  //这是数组形式
// 可以用C++索引形式遍历

List<String> list = new ArrayList<String>();

// 下面两种都需要是List才可以
// 1.
for(String str : list)
{

}
// 2. 
for(Iterator i = list.iterator(); i.hasNext();)
{

}

```


# About length

* For array, use length;
* For String, use length();
* For other objects, use size();