## 学习笔记
 

+ 递归
	+ 思维要点：
		+ 不要人肉进行递归
		+ 找最近重复子问题
		+ 数学归纳法思维 （例子放鞭炮）

````
def recursion(level, param1, param2, ...):
	# 终止循环条件
	if level > max_level:
		process_result
		return
	
	# 处理当前层
	process(level, data...)
	
	# 下探
	self.recursion(level+1, p1, ..)
	
	# 清扫当前层的状态
	
````
		
+ 分治

````
def divide_conquer(problem, param1, param2, ...):
	# 终止循环条件
	if problem is None:
		print_result
		return
		
	# 处理当前逻辑 大问题分成小问题
	data = prepare_data(problem)
	subproblems = split_problem(problem, data)
	
	# 下探到下一层
	subresult1 = self.divide_conquer(subproblems[0], p1, ...)
	subresult2 = self.divide_conquer(subproblems[1], p1, ...)
	subresult3 = self.divide_conquer(subproblems[2], p1, ...)
	...
	
	# 最终结果
	result = process_result(subresult1,	subresult2, subresult3, ...)

```` 


+ 回溯 （例子：八皇后）
	+ 不断的在每一层去试



|#|标题|解决思路|
|---|---|------|
|17|[电话号码的字母组合](https://leetcode-cn.com/problems/letter-combinations-of-a-phone-number/)	||
|22|[括号生成](https://leetcode-cn.com/problems/generate-parentheses/)|递归（设置left,right,n)|
|46|[全排列](https://leetcode-cn.com/problems/permutations/)|回溯|
|47|[全排列 II](https://leetcode-cn.com/problems/permutations-ii/)|比起46，需要多判断一步是否和之前添加过的元素重复|
|50|[Pow(x,n)](https://leetcode-cn.com/problems/powx-n/)|分治法|
|51|[N皇后](https://leetcode-cn.com/problems/n-queens/)|2|
|70|[爬楼梯](https://leetcode-cn.com/problems/two-sum/description/)| 递归（超时）；优化使用动态规划|
|77|[组合](https://leetcode-cn.com/problems/combinations/)|回溯+剪枝|
|78|[子集](https://leetcode-cn.com/problems/subsets/)|类似括号题的思路，给n个格子，可选可不选|
|98|[验证二叉搜索树](https://leetcode-cn.com/problems/validate-binary-search-tree/)|递归|
|104|[二叉树的最大深度](https://leetcode-cn.com/problems/maximum-depth-of-binary-tree/)|递归(返回左边的最大深度和右边的最大深度的最大值 +1)|
|105|[从前序和中序遍历构造二叉树](https://leetcode-cn.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/)|前序遍历得到根结点位置，再划分左右结点不断遍历|
|111|[二叉树的最小深度](https://leetcode-cn.com/problems/minimum-depth-of-binary-tree/)|递归考虑三种情况；深度优先搜索:遍历整棵树，记录最小深度|
|169|[多数元素](https://leetcode-cn.com/problems/majority-element/description/)|哈希；排序取n/2|
|226| [翻转二叉树]()| 左右子树不断交换位置|
|236|[二叉树的最近公共祖先](https://leetcode-cn.com/problems/lowest-common-ancestor-of-a-binary-tree/)||
