#  排序算法总览
|算法名称 | 英文名称| 时间复杂度 |
|---|---| --- |
|选择排序|Selection Sort|$O(n^2)$|
|冒泡排序|Bubble Sort|$O(n^2)$|
|插入排序|Insertion Sort|$O(n^2)$|
|希尔排序|Shell's Sort|$O(n \cdot log ^2 n)$|
|归并排序|Merge Sort|$O(n \cdot log \cdot n)$|
|快速排序|Quick Sort|$O(n \cdot log \cdot n)$|
|堆排序  |Heap Sort|$O(n \cdot log \cdot n)$|
|计数排序|Count Sort|$O(n+k)$|
|桶排序  |Bucket Sort|$O(n+k)$|
|基数排序|Radix Sort|$O(n\times k)$|

后文全部实现小->大顺序排序

# 1. 冒泡排序 `Bubble Sort`
两两比较，当出现大小顺序不对的pair时，交换两个值。不断循环，直至没有需要交换的为止。

`平均时间复杂度`$O(n^2)$

`最好时是`$O(n)$

# 2. 选择排序 `Selection Sort`
`step1` 在每次循环中找到最小值，放在起始位置。

`step2` 在剩下未排序的元素中再次进行操作。

`平均时间复杂度一直是`$O(n^2)$

# 3. 插入排序 `Insertion Sort`
维护一个有序部分，遍历无序部分，插入到有序部分中的适当位置。

`时间复杂度`$O(n^2)$

# 4. 希尔排序 `Shell's Sort`
通常从总数的一半开始分组，进行组内排序。组内用插入排序。
Shell Sort其实是一种选择排序，不过步长是变化的。
`时间复杂度为` $O(logn)\cdot O(n) \cdot O(logn) = O(n\cdot log^2 n)$

# 5. 归并排序 `Merge Sort`
分治法为中心思想。
`时间复杂度都是`$O(nlogn)$
`空间复杂度比上面的`$O(1)$大，一般为$O(n)$

# 6. 快速排序 `Quick Sort`
`时间复杂度`$O(nlogn)$ 也是用分治法为中心思想。将一个list分为两个list。
分区操作，基准左边都是比它大的数，右边都是比他小的数。可以用迭代实现。

# 7.堆排序 `Heap Sort`
利用堆的特性进行排序。

`小-大`：小顶堆
`大-小`：大顶堆

`堆` 1. 完全二叉树；2. leaf和parent大小符合规则。一般用数组实现（因为是完全二叉树）

`step1` 实现堆的数据结构以及方法
`step2` 每次将最小的堆顶拿出来，再调整堆的结构

如果为了理解算法，用`list<Integer>` 比较方便。可以尝试用`int[]`. 

`时间复杂度都是`$O(nlogn)$











