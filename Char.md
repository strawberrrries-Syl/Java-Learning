# 1. constructor
## 1.1 directly
```java
char ch = `a`;
```
## 1.2 Unicode
```java
char uniChar = `\u039A`;
```
## 1.3 char array
```java
char[] charArray = {'a', 'b', 'c', 'd', 'e'};
```
## 1.4 wrapped char
`Character`
You can construct a Character object:
```java
Character ch = new Character(`a`);
```
# 2. methods:

```java
isLetter();

isDigit();

isWhitespace();

isUpperCase();

isLowerCase();

toUpperCase();    // 转大写

toLowerCase();    // 转小写

toString();       // 转string
```
