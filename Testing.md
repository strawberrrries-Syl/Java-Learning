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


# Testing
## 1. Modular testing
Test drivers & stubs

`e.g.a` Test drivers call the code, check the results.

Usually in main()

If class is entry point for program:
```java
public class MyProgram {
  public static void testDriver() {
    ...
  }
}

public class TestMyProgram{
  ...
  main(...) {
    MyProgram.TestDriver();
  }
}

```

`e.g.b.` Stubs: bits of code called by the code being tested.
i. Fill in for missing method.

ii. Determine whether bug lies in calling method or callee by replacing callee with stub.

iii. `Produce test data that real subroutines rarel produce.` or `Produces repeatable test data.`

## 2. Integration Testing
Define interfaces well! No ambiguity in descriptions of behaviors.

## 3. Result Verification

`e.g.a.` Datastructure integrity checkers.

Inspects data structure & verifies that all invariants are satisfied.

`e.g.b.` Algorithm result checker.

Sorting --> check that each # <= its successor.

Assertion: Code that tests an invariant or result
```java
assert (x == 3) ;
assert (list.size == list.countLength());
```

**Turn assertion on: "java -ea"//Turn them off: "java -da" (code is fast).**

## Regression Testing
Regression test: test suite that can be re-run when changes are made.


