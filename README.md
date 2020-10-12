# 关注算法，提升Coding
关注算法，题目来源于LeetCode。涵盖：数组、链表、栈、堆、二叉树、BST树等数据结构，算法有搜索、排序、去重、找出现次数最多等问题。
- 使用Java8来实现

--- 
### 2. 两数相加
- 迭代法  
因为从链表往下个节点变换时，依次是个位、十位、百位
从链表头向下依次遍历叠加
时间复杂度：O(n)
空间复杂度：O(1)

--- 
### 5. 最长回文子串.给定一个字符串 s，找到 s 中最长的回文子串。你可以假设 s 的最大长度为 1000。
- 从大到小迭代法  
将字符串转成字符数组，从字符串最大的长度依次递减；并判断是否为回文字串；如果不是则整体向后移动；
如果当前循环没有找到最大回文字串，则将遍历的回文字串长度--，继续循环
时间复杂度：O(n^3)
空间复杂度：O(1)
--- 
### 07. 给出一个 32 位的有符号整数，你需要将这个整数中每位上的数字进行反转。
- 方法：每次获取剩余整数的个位数，可以一次构建反转整数的一位数字。在这样做的时候，我们可以预先检查向原整数附加另一位数字是否会导致溢出。

---
### 8. 请你来实现一个 atoi 函数，使其能将字符串转换成整数。
- 思路：这个问题其实没有考察算法的知识，模拟的是日常开发中对于原始数据的处理（例如「参数校验」等场景）

--- 
### 9. 判断一个整数是否是回文数。回文数是指正序（从左向右）和倒序（从右向左）读都是一样的整数。
- 方法一：字符串法，并检查字符串是否为回文。但是，这需要额外的非常量空间来创建问题描述中所不允许的字符串。
- 方法二：数字本身反转，但直接操作的话可能越界，考虑只反转int 数字的一半？毕竟，如果该数字是回文，其后半部分反转后应该与原始数字的前半部分相同。

--- 
### 11. 盛最多水的容器
- 暴力解法  
使用两次for循环，两两相乘可得
时间复杂度：O(n^2)
空间复杂度：O(1)

- 双指针法  
面积受限于最短边【代表高度】、距离【宽度】;
每次固定最长的那条边，移动最矮的那条边，然后向中间移动，看看能不能找到面积更大的点
时间复杂度：O(n)
空间复杂度：O(1)

--- 
### 14. 编写一个函数来查找字符串数组中的最长公共前缀。
- 思路：横向扫描，依次遍历每个字符串，更新最长公共前缀。另一种方法是纵向扫描。纵向扫描时，从前往后遍历所有字符串的每一列，比较相同列上的字符是否相同，如果相同则继续对下一列进行比较，如果不相同则当前列不再属于公共前缀，当前列之前的部分为最长公共前缀。

--- 
### 15. 三数之和。给你一个包含 n 个整数的数组nums，判断nums中是否存在三个元素 a，b，c ，使得a + b + c = 0 ？请你找出所有满足条件且不重复的三元组。注意：答案中不可以包含重复的三元组。
- 双指针法  
先对数组排序，固定一数num[i]，然后使用双指针指向剩余部分的首尾，计算三数之和是否等于0。满足则添加到集合中
如果num[i] 大于0，则三数之和无法等于0，退出循环
如果num[i] == num[i-1]，则说明该数字重复，会导致重复结果，所以应该跳过
当sum == 0时，num[start] == num[start+1]，则会导致重复结果，start++
当sum == 0时，num[end] == num[end-1]，则会导致重复结果，end--;

--- 
### 21. 将两个升序链表合并为一个新的 升序 链表并返回。新链表是通过拼接给定的两个链表的所有节点组成的。
- 思路：迭代法，我们可以用迭代的方法来实现上述算法。当 l1 和 l2 都不是空链表时，判断 l1 和 l2 哪一个链表的头节点的值更小，将较小值的节点添加到结果里，当一个节点被添加到结果里之后，将对应链表中的节点向后移一位。

--- 
### 26. 给定一个排序数组，你需要在 原地 删除重复出现的元素，使得每个元素只出现一次，返回移除后数组的新长度。
- 思路：双指针法，数组完成排序后，我们可以放置两个指针 i 和 j，其中 i 是慢指针，而 j 是快指针。i指针表示不重复的新的位置，j表示遍历进度下标

--- 
### 27. 给你一个数组 nums和一个值 val，你需要 原地 移除所有数值等于val的元素，并返回移除后数组的新长度。
- 思路：双指针法，我们可以放置两个指针 i 和 j，其中 i 是慢指针，而 j 是快指针。i指针表示可以存放的新的位置，j表示遍历进度下标。如果遇到不需要移除的值则两个指针同时移动

--- 
### 28. 实现strStr()函数。
- 思路：

--- 
### 35. 搜索插入位置。给定一个排序数组和一个目标值，在数组中找到目标值，并返回其索引。
- 思路：二分查找

--- 
### 38. 外观数列  
- 迭代法  
从1开始，逐步向后取得对应的整数序列
时间复杂度：O(n^2)
空间复杂度：O(n)

--- 
### 53. 最大子序和。给定一个整数数组 nums，找到一个具有最大和的连续子数组（子数组最少包含一个元素），返回其最大和。
- 贪心算法：若当前指针所指元素之前的和小于0，则丢弃当前元素之前序列

--- 
### 58. 最后一个单词的长度
- 尾部遍历法  
查找最后一个单词长度，从尾部遍历，如果找到有效单词返回即可
时间复杂度：O(n)
空间复杂度：O(1)

--- 
### 66. 加一。给定一个由整数组成的非空数组所表示的非负整数，在该数的基础上加一。
- 数组后续向前遍历法  
数组后续遍历，如果当前下标值为9，则进位，该位置为0；如果当前下标值小于9，直接原地++，直接返回
最后需要考虑99、999这种特殊情况，则数组长度扩长1位，首位置1即可
时间复杂度：O(n)
空间复杂度：O(1)

--- 
### 67. 二进制求和
- 迭代法  
时间复杂度：O(n)
空间复杂度：O(n)

--- 
### 69. x 的平方根。实现int sqrt(int x)函数；计算并返回x的平方根，其中x 是非负整数。由于返回类型是整数，结果只保留整数的部分，小数部分将被舍去。
- 二分查找法  
时间复杂度：O(logN)
空间复杂度：O(1)
- 从小遍历法  
- 使用库函数法，估记会被怼  

--- 
### 70. 爬楼梯。假设你正在爬楼梯。需要 n 阶你才能到达楼顶。每次你可以爬 1 或 2 个台阶。你有多少种不同的方法可以爬到楼顶呢？
- 动态规划法：从1阶开始计算
- 递归法：使用递归很容易解决此问题，但适用于n较小的情况下，n 较大则方法嵌套过深

--- 
### 88. 合并两个有序数组。给你两个有序整数数组nums1 和 nums2，请你将 nums2 合并到nums1中，使 nums1 成为一个有序数组。
- 归并法，因为两个都是有序数组，使用两个指针pos1 和 pos2分别记录两个有序数组完成的进度，并判断nums1[pos1] , nums2[pos2] 大小，使用新数据进行存储

--- 
### 94. 二叉树的中序遍历
- 递归法  
中序遍历：先左、再中、再右
时间复杂度：O(n)
空间复杂度：O(n)

- 栈  
方法一的递归函数我们也可以用迭代的方式实现，两种方式是等价的，区别在于递归的时候隐式地维护了一个栈，而我们在迭代的时候需要显式地将这个栈模拟出来
时间复杂度：O(n)
空间复杂度：O(n)

--- 
### 98. 验证二叉搜索树
- 非递归中序遍历    
采用中序遍历能将二叉搜索树转换为从小到大的顺序访问；可以前后两两比较
时间复杂度：O(n)
空间复杂度：O(n)
- 中序遍历  
中序遍历输出为一个链表，并对链表顺序访问大小
时间复杂度：O(2n)
空间复杂度：O(n)


--- 
### 100. 相同的树
- 遍历法  
采用前序遍历，逐一比较当前元素是否相同
时间复杂度：O(n)
空间复杂度：O(1)

--- 
### 104. 二叉树的最大深度
- 查询左子节点最大深度，再查询左子节点最大深度，然后取左、右字节点最大深度 + 1

--- 
### 107. 二叉树的层次遍历 II
- 广度优先搜索  
时间复杂度：O(n)
空间复杂度：O(n)

--- 
### 108. 将有序数组转换为二叉搜索树
- 递归法  
时间复杂度：O(N)
空间复杂度：O(logN)

--- 
### 113. 路径总和 II
- 我们可以采用深度优先搜索的方式，枚举每一条从根节点到叶子节点的路径。当我们遍历到叶子节点，且此时路径和恰为目标和时，我们就找到了一条满足条件的路径。

--- 
### 121. 买卖股票的最佳时机
- 核心思想：向前探寻下一次最低价格，如果最低价格后面的收益更大，则更新收益

--- 
### 136. 只出现一次的数字。给定一个非空整数数组，除了某个元素只出现一次以外，其余每个元素均出现两次。找出那个只出现了一次的元素。
- 方法一：哈希表
- 方法二：异或（XOR）
1.如果我们对 0和二进制位做XOR运算，得到的仍然是这个二进制位
2.如果我们对相同的二进制位做XOR运算，返回的结果是0
3.XOR满足交换律和结合律

--- 
### 141. 环形链表。给定一个链表，判断链表中是否有环。
- 方式一：HashSet存储遍历过的链表节点，如果遍历过程中发现有之前的链表节点则存在有环
- 方法二：快慢指针，使用快指针每次向前走2步，慢指针每次向前走1步，如果链表有环则快慢指针一定会相遇

--- 
### 155. 最小栈，设计一个支持 push ，pop ，top 操作，并能在常数时间内检索到最小元素的栈。
- 思路：设计一个MyNode节点类，存储节点信息（值val，当前栈最小值min，下一个节点next），每次插入向头节点插入、弹出也是头节点弹出、返回最小值只需要返回当前头的最小值即可

--- 
### 160. 相交链表。编写一个程序，找到两个单链表相交的起始节点。
- 方式一：双指针分别走两个单链表，如果能相遇则存在相交的起始节点
- 方法二：HashMap法，将第一个单链表存入HashMap中，然后遍历第二个单链表，如果在第二个单链表中发现与hashMap相同的节点则存在相交的起始节点

--- 
### 169. 给定一个大小为 n 的数组，找到其中的多数元素。多数元素是指在数组中出现次数大于 ⌊ n/2 ⌋ 的元素
- 方法一：哈希表     我们知道出现次数最多的元素大于n/2次，所以可以用哈希表来快速统计每个元素出现的次数  
- 方法二：排序       如果将数组 nums 中的所有元素按照单调递增或单调递减的顺序排序，那么下标为 n/2 的元素（下标从 0 开始）一定是众数。

--- 
### 206. 反转链表。反转一个单链表。
- 使用双向链表作为额外空间辅助，遍历单向链表时不断向双向链表添加；然后通过双向链表从尾部遍历获取反向单向链表
  时间复杂度：O(n)
  空间复杂度：O(n)
- 使用栈作为辅助结构，根据栈先进后出的特性满足单向链表反向
  时间复杂度：O(n)
  空间复杂度：O(n)
-  迭代法：使用前驱、后驱节点进行遍历，将单向链表指针反向
  时间复杂度：O(n)
  空间复杂度：O(1) 

--- 
### 217. 存在重复元素。给定一个整数数组，判断是否存在重复元素。如果任意一值在数组中出现至少两次，函数返回 true 。如果数组中每个元素都不相同，则返回 false 。
- 排序法
先排序，再遍历。如果存在相同元素，则前驱元素必定会与当前遍历元素相同
时间复杂度：O(nlogn)
空间复杂度：O(1)
- HashMap法
遍历数组元素，并向hashMap中判断之前是否存在；如果存在则存在重复元素、不存在的话则向hashMap中插入元数
时间复杂度：O(n)
空间复杂度：O(n) 
- 异或法：
排序后，再对数组相邻元素两两异或。如果异或为0，则代表存在一样的元素；
时间复杂度：O(nlogn)
空间复杂度：O(1)

--- 
### 226. 翻转二叉树
- 递归法  
从根节点左、右子节点翻转，然后再翻转左节子点树、再翻转右子节点树
时间复杂度：O(n)
空间复杂度：O(1)

--- 
### 231. 2的幂 给定一个整数，编写一个函数来判断它是否是 2 的幂次方。
- 递归法：
递归法：如果n为奇数（除1外）都不是2的幂次；如果n为偶数则继续判断它的一半是否为2的幂次
时间复杂度：O(logN)
空间复杂度：O(1)
- 位运算法：
若 n = 2^x 且 x为自然数（即 nn 为 22 的幂），则一定满足以下条件：  
    1、恒有 n & (n - 1) == 0，这是因为：  
        n 二进制最高位为 1，其余所有位为 00； 
        n−1 二进制最高位为 0，其余所有位为 1；  
    2、一定满足 n > 0。  
时间复杂度：O(1)
空间复杂度：O(1)

--- 
### 235. 二叉搜索树的最近公共祖先，给定一个二叉搜索树, 找到该树中两个指定节点的最近公共祖先。
先中、再左、再右探寻法(递归、非递归实现)
先判断当前root是否与p、q相等，如果相等则返回root;
否则判断p、q是否都在左侧，是则继续递归左侧；
否则判断p、q是否都在右侧，是则继续递归右侧;
时间复杂度：O(logN)
空间复杂度：O(1)

--- 
### 237. 删除链表中的节点。请编写一个函数，使其可以删除某个链表中给定的（非末尾）节点。传入函数的唯一参数为 要被删除的节点 。
- 原地删除法 
将下一个节点的值赋值到当前节点的val，然后当前节点指针指向【当前节点的下一个、下一个节点】即可
时间复杂度：O(1)
空间复杂度：O(1)

--- 
### 292. Nim 游戏。你和你的朋友，两个人一起玩Nim 游戏：桌子上有一堆石头，每次你们轮流拿掉1 - 3 块石头。 拿掉最后一块石头的人就是获胜者
- 如果堆中石头的数量 nn 不能被 44 整除，那么你总是可以赢得 Nim 游戏的胜利。
时间复杂度：O(1)
空间复杂度：O(1)

--- 
### 344. 反转字符串。编写一个函数，其作用是将输入的字符串反转过来。输入字符串以字符数组 char[] 的形式给出。
- 首尾同时向中间逼近法
使用首、尾指针分别指向数组的首、尾两端，并进行首尾元素的交换；
然后首指针++、尾指针--。当首尾指针相遇时，说明已经完成数据的交换了
时间复杂度：O(n)
空间复杂度：O(1)

--- 
### 350. 两个数组的交集 II。给定两个数组，编写一个函数来计算它们的交集。
- 双链表法，一个链表用来存储其中一个数组无素，另一个则用来存储交集元素

--- 
### 459. 重复的子字符串。给定一个非空的字符串，判断它是否可以由它的一个子串重复多次构成。给定的字符串只含有小写英文字母，并且长度不超过10000。
- 从小开始遍历法，不断地从最小子串判断

--- 
### 530. 二叉搜索树的最小绝对差  
- 中序遍历【非递归实现】  
时间复杂度：O(n)
空间复杂度：O(n)

--- 
### 557. 反转字符串中的单词 III。给定一个字符串，你需要反转字符串中每个单词的字符顺序，同时仍保留空格和单词的初始顺序。
- 原地反转法  
将字符串转换成数组，然后识别出新的单词，使用双指针原地进行反转
时间复杂度：O(n)
空间复杂度：O(1)

--- 
### 701. 二叉搜索树中的插入操作。给定二叉搜索树（BST）的根节点和要插入树中的值，将值插入二叉搜索树。 返回插入后二叉搜索树的根节点。 输入数据保证，新值和原始二叉搜索树中的任意节点值都不同。
- 根据 val 与 root.val 的大小关系，就可以确定要将 val 插入到哪个子树中。如果该子树不为空，则问题转化成了将 val 插入到对应子树上。否则，在此处新建一个以 val 为值的节点，并链接到其父节点root 上

--- 
### 844. 比较含退格的字符串。给定 S 和 T 两个字符串，当它们分别被输入到空白的文本编辑器后，判断二者是否相等，并返回结果。 # 代表退格字符。
- 借助栈Stack 数据结构完成即可

--- 
### 867. 转置矩阵。给定一个矩阵 A， 返回 A 的转置矩阵。矩阵的转置是指将矩阵的主对角线翻转，交换矩阵的行索引与列索引。
- 使用新数组直接复制

--- 
### 1576. 替换所有的问号。给你一个仅包含小写英文字母和 '?' 字符的字符串 s，请你将所有的 '?' 转换为若干小写字母，使最终的字符串不包含任何 连续重复 的字符。
- 使用前驱字符、后驱字符记录当前字符前、后字符信息，遇到 '?'，从可用字符中排除前驱字符、后驱字符即可完成

