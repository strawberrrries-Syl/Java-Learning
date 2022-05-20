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
```
