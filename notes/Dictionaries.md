# Dictionaries

Two-letter words & definitions. Word is a key that addresses the definition. 26 * 26 = 676 different words.

Insert a definition into dictionary: 
```java
// maps each word (key) to integer 0 ... 675 Index into array.
function hashCode() 
// 提前保留了所有可能出现的结果的位置（其实就是哈希值），每次操作时只对相应位置的数据操作。
```

# Hash Tables:
n: number of keys(words) stored.
Table of N buckets. N a bit larget than n.

A hash table maps huge set of possible keys into N buckets by applying a compression function to each hash code.

最简单的方法是取模，让所有可能key值落入到（0～N-1）中，但会有重复。

# Chaining: 
each bucket references a linked list of entries, called a chain. 桶里有链表，存多个值。

Store each key in table with definition. Entry = (key, value)

# implication
```java
public Entry insert(key, value)
// compute the key's hash code
// compress it to determine bucket
// insert the entry into bucket's chain.

public Entry find(key)
// Hash the key
// Search chain for entry with given key
// If found, return it; Otherwise null.

public Entry remove(key)
// Hash key
// Search chain
// Remove from chahin if found.
// return entry or null.
```
2 entries with same key, 2 approaches:
* insert both; find() arbitrarikly returns one.
* Replace old value with new one. -> what Java is doing.

**Load factor** : $\frac{n}{N}$

load factor small. fast.
load factor big. slow.

Need compression

Bad compression function:

Suppose keys are ints, hashCode(i) = i. Compression fn h(hashCOde) = hashCode mode N. N = 10000 buckets.

Suppose ekys are divisible by 4. h() os divisible by 4 too. Quarters of buckets are never used. Waisted. 

If N is prime, it will be better.

h(hashCode) = ((d*hashCode + b)mod p) mod N.

a, b, p: positive integers.
p is large prime
p>>N. Now, N(buckets doesn't be prime).




