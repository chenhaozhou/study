## 题目
[面试题 10.05. 稀疏数组搜索](https://leetcode-cn.com/problems/sparse-array-search-lcci/)

## 解题思想
    二分搜索思想。
    但是该题目是稀疏数组，则数组中存在空字符串，所以不能用传统的二分搜索。
    先取数组中间值，判断是否为空字符串，如果是，则向右移动寻找非空字符串为止。
    如果右边全部是空字符串，那么就将数组右索引指到中间位置减一。
    
    二分搜索都会涉及循环，所以要特别注意循环的退出边界。
    二分搜索比较中间值后，如果不相等，那么移动对应的左/右索引，需要注意将中间索引加/减 1.
    