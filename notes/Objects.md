## About reference or copy
Normally, stirng1 = string2 is a reference thing.
If you want to copy the value:
```java
s1 = "Yow!"
String s2 = new String(s1);   // now it i copying

s2 = s1;  // it is reference
```

Can not change the string in the box directly.

*"=" sign means assignment.*

## String constructors:
1. new String() constructs empty string
2. "whatever"
3. new String(s1) takes a parameter s1. **Makes copy of object that s1 references.**

* Constructors always have same name as their class, except "stuff in quotes"
* " " for string, '' for char


## Methods not constructors:
```java
s2 = s1.toUppercase();    // use constructors generate a new copy of original string.
String s3 = s2.concat("!!"); // In java, methods generate some thing, then make the pointer as a varialble. It never gives you the right to contol the pointer inside.
// concate is same as using +
// A method should exist after its object.

```
*In Java, strings are immutable: their contents never change.*

## I/O Classes

`System.out` is a PrintStream object that outputs to the screen.
`System.in` is a InputStream object that reads from the keyboard
`readLine methods is defined on BuferedReader objects.`

### How do we construct a BufferedReader? <- InputStreamReader <- InputStream <- System.in
Looking into java.io.libreary


InputStream -> read row data.
InputStreamReader -> compose into characters.
BufferedReader -> chars into entire lines of text.

// because of modulality --> replace each step easily.

## About first program in Java.
generate a new file with `file->new class`

 ## The `final` keyword:
 Kind of like `static` in C++.
 If an object was declared as final, it can never change the pointer ot remote any other objects even they are in the same class.
 
 ## The `static` keyword:
 Like a global varialble in a class which every member from this class keep the same variable together.
 
 *Static method cannot use non-static values.*
 *Static method cannot use non-static methods either.*

## String can add with int and fenerate new Strings.
e.g.
```java
 String s1 = "0"
 for(int i = 0; i < 10; i ++)
 {
   s1 += i;
   System.out.println(s1);
 }
```

This will print out 00-00123456789. 10 numbers in a sum.

