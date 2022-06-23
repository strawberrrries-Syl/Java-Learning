# 1. For int[][]
```java
int[][] intervals;
Arrays.sort(intervals, (a, b) -> a[0] > b[0] ? 1:-1);
// if  using a[0] - b[0], overflow

// Or
Arrays.sort(intervals, Comparator.comparingInt(o -> o[1]));

//将二维数组interval中的一维数组按首字母排序， 小->大
```

# 2. For others
```java
Collections.sort();
```

# 3. Normal comparator
```java
Arrays.sort(intervals, new Comparator<int[]>() {
     @Override
     public int compare(int[] o1, int[] o2) {
         return (o1[1] < o2[1]) ? -1 : ((o1[1] == o2[1]) ? 0 : 1);
     }
});
```