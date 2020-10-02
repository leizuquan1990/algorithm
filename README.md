# 关注算法，提升Coding
关注算法，题目来源于LeetCode。涵盖：数组、链表、栈、堆、二叉树、BST树等数据结构，算法有搜索、排序、去重、找出现次数最多等问题。
### 使用Java8来实现

--- 
### 169题：给定一个大小为 n 的数组，找到其中的多数元素。多数元素是指在数组中出现次数大于 ⌊ n/2 ⌋ 的元素
- 方法一：哈希表     我们知道出现次数最多的元素大于n/2次，所以可以用哈希表来快速统计每个元素出现的次数  
- 方法二：排序       如果将数组 nums 中的所有元素按照单调递增或单调递减的顺序排序，那么下标为 n/2 的元素（下标从 0 开始）一定是众数。
