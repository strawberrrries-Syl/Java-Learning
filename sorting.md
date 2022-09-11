# 1. 排序算法总览
|算法名称 | 英文名称| 时间复杂度 |
|---|---| --- |
|选择排序|Selection Sort|$O(n^2)$|
|冒泡排序|Bubble Sort|$O(n^2)$|
|插入排序|Insertion Sort|$O(n^2)$|
|希尔排序|Shell's Sort|$O(n \cdot log \cdot n)$|
|归并排序|Merge Sort|$O(n \cdot log \cdot n)$|
|快速排序|Quick Sort|$O(n \cdot log \cdot n)$|
|堆排序  |Heap Sort|$O(n \cdot log \cdot n)$|
|计数排序|Count Sort|$O(n+k)$|
|桶排序  |Bucket Sort|$O(n+k)$|
|基数排序|Radix Sort|$O(n\times k)$|

后文全部实现小->大顺序排序

# 1. 冒泡排序 Bubble Sort
两两比较，当出现大小顺序不对的pair时，交换两个值。不断循环，直至没有需要交换的为止。


