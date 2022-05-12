# `equals()`
Every class has an `equals()` method.

Default: r1.equals(r2) same as `r1 == r2`

Many classes define equals() to compare content.

*e.g. String*
```java
String S1 = "Yes";
String S2 = "Yes";
String S3 = S2;

S1==S2; // false
S1.equals(S2); // true
S2==S3; // true
S2.equals(S3);  //true
```
*Summary:* equals compares the variable inside objects. == compares the "address" of the objects.

## 4 degrees of equality
### 1. Reference equality; ==
### 2. Shallow structural equality
fileds are ==.
### 3. Deep structural equality
fileds are equals().
### 4. Logical equality
*e.g.a.* Fractions 1/3 and 2/6 are "equals"
*e.g.b.* "Set" objects are equals if they contain same elements (even stored in different orders)

### example
