# 1. lib
`import java.util.HashMap;`

# 2. constructor
```java
// 1. 
HashMap<Integer, String> Sites = new HashMap<Integer, String>();
// 2. 
Map<String, String> map = Map.of("google", "google.com");   // google->google.com
```

# 3. adding
```java
Sites.put(key, value);
```

# 4. get value
```java
Sites.get(key);

Sites.containsKey();  // whether contains the key
```

# 5. remove
```java
Sites.remove(key);  // remove the pair
```

# 6. clear
```java
Sites.clear();
```

# 7. size()
```java
Sites.size();

```
# 8. iteration
```java
for(Integer i : Sites.keySet()) {
  Syste.out.println(Sites.get(i));
  
}


// 一般用这个
for(Map.Entry<String, String> entry : mapName.entrySet()) {
  entry.getKey();
  entry.getValue();
}
```

# 9. HashSet
## 9.1 constructor
```java
HashSet();

HashSet(int initialCapacity); // init number of hashset

HashSet<Character> vowels = new HashSet<Character>(Arrays.asList('a', 'e', 'i', 'o', 'u', 'A', 'E', 'I', 'O', 'U')); // inti a set with multiple values in one time.
```

## 9.2 Mainly used APIs
```java
HashSet set = new HashSet();

boolean set.add(Object);  // add objects
boolean set.contains(Object object);  // whether contains
boolean set.isEmpty();  // whether is empty
boolean set.remove(Object object);
int set.size(); // size of set
```

## 9.3 iteration
```java
// 1. iterator
for(Iterator iterator = set.iterator(); iterator.hasNext();) {
  iterator.next();
}

// or
for(int k : hashset)
{
  ...
}
```


