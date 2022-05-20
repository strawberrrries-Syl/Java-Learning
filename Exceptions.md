# Exceptions
Run-time error: Java "throws an exception".

*Exception is a kind of object*

You can prevent the error by "catching" the Exception

## 1. Purpose of Exception
### 1.1 Surviving errors

*e.g.* Try to oepn a file that doesn't exist. --> You can catch exception, print error message, continue.
```java
try {
  f = new FileInputStream("~cs61b/pj2.solution");
  i = f.read();
}   // file might not exists
catch(FileNoteFoundException e1) {    //e1 is a variable
  whine("Failed!!!");                 // You can call exception on e1(since it's an object)
}
catch (IOException e2) {
  f.close();                  // Exception handlers
}
```

a. Executes the code inside "try".

b. If "try"code executes normally, skip "catch" clauses.

c. If "try" code throws exception, do not finish "try" code. Junmp to first "catch" clause that  matches exception; execute. 
"Matches" - exception object thrown is some class/subclass of type in "catch" clause.

d. Jumps to code after all catch clauses.

**Only the first matching "catch" is executed.**

### 1.2 Escaping a sinking ship
Throw your own exception. 
```java
public class ParseException extends Exception {     // Why want to declare a new class? Distinguishable from other type of Exceptions
  
}

public parseTree parseExpression() throws ParserException {   // throws key word!
  [loops]
  if(somethingWrong) {
    throw new ParserException();    // throw v.s. throws
    
    ..
    ..
    
    return parseTree;
  }
}
```
`throw` Different from `return`?

* Don't have to return anything.
* An exception can fl many mehods down the stack.

```java
public ParseTree parse() throws ParserException, DumbCodeException {
  [loops]
  
    p = parseExpression();
    
    [..]
    
}
public void compile() throws DumbCodeException {
  ParseTree p;
  try {
    p = parse();
    p.toByteCode();
  }
}
catch(ParserException e1) {
  
}
```

## 2. `Checked` & `Unchecked` Exceptions
```
Throwable 
/           \
Exceptions    Error

Error -> Rnning out of memory or stack space.               --|
Exception |->  RunTimeException    -> NullPointer...          |-> Unchecked; no "throws" declaration needed.
          |->  ParserException                              --|
```
When method calls method that "throws" a checked exception, 2 choices.
1. It can catch the exception
2. "Throws" the same exception itself.





