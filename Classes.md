## Defining Classes:
Fields:
* Variables stored in objects.
* Used to store data.
* Aka instance variables.

```java
kayla.introduce();  // method call
kayla.age;          // field
```
*A class human we diffined: *
```java
class Human {
  // fields
  public int age;
  publi String name;
  // methods:
  public void introduce() {
    System.out.println("I'm " + name + " and I'm " + age + "years old.")
  }
}
```

Using it
```Java
Human kayla = new Human();
kayla.age = 12;
kayla.name = "Kayla";
```

**int and String are different with each others**
int can change its value whenever you want, but String cannot. 

### Constructors in class
name always as same as class's name.

Java always product a default constructor for you.
But if you write a constructor, it will go away.

## The `This` keywords

```java
this.age; //explicite
age;      // implicite

// to avoid some confusion, please always using this.filed as explicite way.
```
## The "static" keyword

* a single variable shared by a whole class of objects.
* Also called class variables.

```java
class Human {
  public int age;
  public String name;
  public static int numberOfHumans = 0;
  public Human() {
    numberOfHumans++;
  }
  
}

// Try to use it
int Kids = Human.numberOfHumans / 4;

```
**System.out** is a static field.

* main() is always static
* In a static method, THERE IS NO "THIS".


## Initialize for some type

In Java, variables have init value before assigned.
int -> 0;
float -> 0.0;
booleans -> false;
reference -> null;

