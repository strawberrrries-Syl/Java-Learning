# The `finally` keyword

```java
try {
    statementX;
    return 1;
} catch (SomeException e) {
    e.printStackTrace();        // help you debug the code  -> Java took
    return 2;                   // a snapshot of stack.
} finally {
    f.close();
    return 3;
}
```

* If `try` statement begins, the `finally` clove will be executed at the end, no matter what.

* StatementX causes SomeException -> `catch` clause executes, then `finally` clause.

* StatementX causes other Exception -> `finally` clause executes, then exception continues done stack.

* Exception thrown in `catch` clause. As usual, `finally` still executed first. 

* Exception thrown in `finally` clause: new exception replaces old method ends immediately.

# Exception Constructors

Most throwables have 2 constructors
```java
class MyException extends Exception {
    public MyException() { super(); }
    public MyException(String s) { super(s); }
    // string s -> error message: 
}
```
* printed if exception propagates out of `main()`.
* Read by `Throwable.getMessage()`.

# Filed shadowing
Fileds can be "shadowed" in subclasses. 

Different from overriding. 

Choice of methods dictated by dynamic type.

Choice of fileds dictated by static type.
```java
class Sub extends Super{
    int x = 4;              // shadows Super.x
    int f() {return 4;}     // overrides Super.f()
}
```

# simplified for

```java 
int[] array = {7, 12, 3, 8, 4, 95};

for (int i : array) {                   // working on Objects too
    SYstem.out.print(i + " ");
}
```

# Iterator class

```java
for(ListIterator l : myList) {...}
```