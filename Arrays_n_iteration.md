# Automatic

## 1. Construction

```java
int[][] table = new int[x][y];
// create an array of x references to array.

```
# 2. Initializers:
```java
Human[] b = {kayla, rishi, new Human("Paolo")};
int[][] c = {{7,3,2}, {x}, {8,5,6,0}, {y+z,3}}; // feasible in initializers, not in assignment.
int[] a,b,c;        // all reference arrays.
int a[], b, c[][];  //a is 1d, b is not array, c is 2d
Arrays.fill(a, 0);  //批量化赋值

// 如果想直接return int[]
return new int[2]{0,0};
```
# 3. copy
```java
int[] ans = Arrays.copyOf(nums, nums.length);
int[] ans = Arrays.copyOfRange(nums, start, end);
// nums->原数组，nums.length->复制长度
```

# 4. List<String>[]
一种数组，数组中装的是List，链表可以链接任何结构。
```java
List<Integer>[] map = new List[n];
```


# Do-loop
"do" loop always executes loop body at least once
*Important*
``` java
if() {
  break;
}// will not go here
```

# label:
```java
test:
  if(x == 0) {
  loop:
  while(i < 9) {
    blablabla;  
  }
}
```

# Constants:
`final` keyword: value that can never be changed. -->like define
BAD: 
```java
if(month == 2) {
}
```
GOOD: 
```java
public final stati int FEBRUARY = 2;  // just like define
```

For any array x, `x.length` is a "final" field. Cannot be changed.

`final varialble`: means you can't chage its **value**.

`final method`: means you can't override the **method**.

`final class`: means you can't extend the class(can't make a subclass)


# for loop
You can write the code like:
```java
for(statement : expression)
{
  //...
}

// like below:
for(int x : numbers) {
  System.out.print( x );  
}
```

# if-else 
Same as rules in C++.

# switch
Same as rules in C++.
```java
switch(expression) {
  case value :
  break;
  case value :
  break;
  ...
  default:
  break;
}
```


# 9. Arrays的比较
``` java
Arrays.equals(pCount, sCount);
// 比较两个数组是否相等
```
