```java
public interface Nukeable { // in Nukeabke.java
  public void nuke();
}

public interface Comparable { // in java.lang
  public int compareTo(Object o);
}

public class SList extends List inplements Nukeable, Comparable {
  public void nuke () {
    head = null;
    size = 0;
  }
  
  public int compareTo(Object o) {
  
  }
}
```

You can declare a static type as a interface type.
```java
Nukeable n = new SList();
Comparable c = (Comparable) n;

n.nuke();
if(c.compareTo(c2) > 0) {...}
```
Array class in java.util sorts arrays of comparable objects.
```java
public static void sort(Object[] a)
```
Run-time error occurs if any item in a is not comparable.

A subinterface can have multiple subinterfaces.
```java
public interface NukeAndCompare extends Nukeable, Comparable {}
```



# Java Packages
## 1. deffination
package: collection of classes, java interfaces, and subpackages.

## 2. Benefits of packages.
1. Packages cna contain hidden classes not visible outside package.
2. Classes can have field & methods visible inside package only.
3. Different packages can have classes with same name.
```java
java.awt.Frame & photo.Frame; // namespace is different
```
* example:
java.io strandard library.

## 3. Using Packages

`Fully qualified name`: java.lang.System.out.println("blah");

```java
import java.io.File;  // Can now refer to File
import java.io.*;     // Can now refer to everything in java.io
```
Every program inplicitly imports `java.lang.*`.

## 4. Finding the path of a class
```java
% printenv CLASSPATH
.:/home/ff/
```
## 5. Building Packages
```java
//list/SList.java
package list;

public class SList {
  SListNode head;
  int size;
}

// list/SListNode.java
package list;

class SListNode {
  Object item;
  SListNode next;
}
```
*Package protection is default.* It's between private & protected.

A class/variable with package protection is visible to any class in the same package; Not outside package (Files outside directory).

Files outside only see public classes/methods/fields.


*Public class must be declared in file named after class.*

## 6. Compiling & running must be done from outside package

**?**

```java
java -g list/SList.java
java list.SList
```
## 7. declaration
```
`Visible:`  |in the same package | in a subclass | everywhere
"public"    |         X          |       X       |      X
"protected" |         X          |       X       |
package     |         X          |               |
"private"   |                    |               |
```
