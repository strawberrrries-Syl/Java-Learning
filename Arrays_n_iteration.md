# Automatic

## 1. Construction

```java
int[][] table = new int[x][y];
// create an array of x references to array.

```
# Initializers:
```java
Human[] b = {kayla, rishi, new Human("Paolo")};
int[][] c = {{7,3,2}, {x}, {8,5,6,0}, {y+z,3}}; // feasible in initializers, not in assignment.
int[] a,b,c;        // all reference arrays.
int a[], b, c[][];  //a is 1d, b is not array, c is 2d
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
