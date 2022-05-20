## Primitive variables:

### For Java, there's a method similar as `eval` in python.

```java
int X = Integer.parseInt("1984"); // get int from string;
double d = Double.parseDouble("3.14");
```
### You can give a long a int variable. But you cannot vise versa.

### Force turning
```java
int i = 23;
long l = 23l;
i = (int)l; // force turning
```

## Boolean values:
can not represent by intergers. Only `true` or `false`.

## Switch:

```java
// Just the same as cpp
  switch (month) {      // month -> variable can use int/char/boolean
    case 2:
      days = 28;
      break;
    case 4:
    case 6:
    case 9:
    case 11;
      days = 30;  // or can be exchanged by return
      break;      //
    default:
      days = 31;
      break;
  }
```

## function in Java
A method declared to return a non-void type.

## Getters and Setters

## For int and String convert
```java
Integer.parseInt("1986");                   // String to int
double d = 42.5;
String doubleString = Double.toString(d);   // Double to String
```

## wrapping
When you need to treat aprimitive like an object. Especially using mashmap or arraylist
```java
int i = 288;
Integer iWrap = new Integer(i);   // wrapping
int unWarpped = iWrap.intValue(); // unWrapping
```

% Screen Shot 2022-05-20 at 13.39.36.png
## Formating
```java

%[argument number][flags][width][.precision] type

```
