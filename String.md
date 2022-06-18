# 1. Constructor    
(String is immutable)
## 1.1 basic
```java
String str = "hello";
```
## 1.2 new
```java
String str2 = new String("hello");
```
## 1.3 from char[]
```java
char[] helloArray = {'h','e','l','l','o'};
String helloString = new String(helloArray);
```
# 2. difference
  直接用“”创建的字符串存在stack中，如果创建多个相同的，则互相为引用关系。
  用new创建的字符串对象stack上。
  
# 3. length
```java
str.length();
```

# 4. concate 
```java
// 1.
String string1 = "Hello, ";
String string2 = "you";
string1.concate(string2);
//2. 
"Hello, ".concat("you");
//3. 
"Hello, " + "you";
// all generate "Hello, you"
```

# 5. Methods:

```java
// 1. 返回指定索引处的 char 值。
char charAt(int index);
// 2. 当且仅当字符串与指定的StringBuffer有相同顺序的字符时候返回真。
boolean contentEquals(StringBuffer sb);
// 3. 返回指定字符在此字符串中 第一次/最后一次 出现处的索引。
  int indexOf(int ch);    	int lastIndexOf(int ch);
  // 返回在此字符串中第一次出现指定字符处的索引，从指定的索引开始搜索。
  int indexOf(int ch, int fromIndex);
  // 返回指定子字符串在此字符串中第一次出现处的索引。
  int indexOf(String str);
  // 返回指定子字符串在此字符串中第一次出现处的索引，从指定的索引开始。
  int indexOf(String str, int fromIndex);
// 4. 根据给定正则表达式的匹配拆分此字符串。
String[] split(String regex);
// 5. 子字符串
String substring(int beginIndex, int endIndex)；
// 6. 全大写
String toUpperCase();
// 7. 返回copy，忽略前导空白和后导空白
String trim();
// 8. 判断是否包含制定的字符系列
contains(CharSequence chars);
// 9. 判断是否为空
isEmpty();

// 10. 如果想判断是否包含子字符串， 可以用indexOf()
// 是子字符串时，返回值>0
// 处理String相关问题时，永远先判断是否是子字符串

```
# 6. StringBuffer & StringBuilder
Mutable. Always using StringBuilder (faster). But StringBuilder is not safe in multithread.
*无需提前确定容量* 
`sbf.append("...")`, `sbf.insert(pos, str)`, `sbf.delete(5,8)`->delete the calue at 5 and 8.
```java
int capacity();

int indexOf(String str, int fromIndex);
int lastIndexOf(String str, int fromIndex);

int length();

void setCharAt(int index, char ch);
// 返回新的String， 包含此序列当前所包含的字符子序列。
String substring(int start, int end);

```

# 7. String and StringBuilder convert
```java
String s = new String("assdfdgagds");

StringBuilder newstring = new StringBuilder(s);

String sconvert = newstring.to_String();

```
# 8. String 的自身排序（单个String的元素排序）
```java
String s = ",lkdsfjsa";

Char[] cStr = s.toCharArray();    //string to char[]

Arrays.sort(cStr);

String newS = new String(sCtr);   // char[] to string
```






