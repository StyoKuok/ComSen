layout: page title: 核心算法 permalink: /algorithms/
压缩感知重建算法
从少量测量值中恢复出原始信号x是压缩感知中的核心挑战。这是一个欠定问题，需要利用信号的稀疏性来找到唯一的解。这些重建算法通常分为两大类：贪婪算法和凸优化算法。

1. 贪婪算法（Greedy Algorithms）
这类算法通过迭代地选择与残差最相关的原子来逐步逼近最优解。它们通常计算速度快，但在某些情况下可能无法找到全局最优解。

正交匹配追踪（Orthogonal Matching Pursuit, OMP）
OMP是MP算法的改进版本，它在每一步选择最匹配的原子后，会使用正交投影来确保每次迭代的原子都是正交的，从而避免了重复选择相同的原子。

算法步骤:

初始化： 残差r 
0
​
 =y，索引集$\Lambda_0 = \emptyset$。

迭代： 在每次迭代k=1,2,…,K中：

选择原子： 找到与当前残差r_{k-1}$内积最大的测量矩阵$\Phi的列（原子），其索引为：
$$ i_k = \arg\max_{j} |\langle r_{k-1}, \Phi_j \rangle| $$

更新索引集： 将选定的原子索引加入索引集：Λ 
k
​
 =Λ 
k−1
​
 ∪{i 
k
​
 }。

重建： 使用最小二乘法，在已选择的原子上求解信号：
$$ \hat{x}k = \arg\min_x |y - \Phi{\Lambda_k}x|_2^2 $$

更新残差： 计算新的残差：
$$ r_k = y - \Phi_{\Lambda_k}\hat{x}_k $$

终止： 当残差满足一定阈值或迭代次数达到预设的稀疏度K时终止。

2. 凸优化算法（Convex Optimization）
这类算法将L 
0
​
 范数最小化问题松弛为凸的L 
1
​
 范数最小化问题，并通过各种优化方法求解。由于L 
1
​
 范数最小化是凸的，这类算法通常能够保证找到全局最优解。

基追踪（Basis Pursuit, BP）
BP算法直接求解L 
1
​
 范数最小化问题：

$$ \min |x|_1 \quad \text{s.t.} \quad \Phi x = y $$

该问题可以利用线性规划等凸优化技术进行求解。

迭代软阈值算法（Iterative Soft-Thresholding Algorithm, ISTA）
ISTA是一种求解L 
1
​
 范数最小化的有效方法。它通过迭代软阈值操作，逐步逼近最优解。

算法步骤:

初始化：  
x
^
  
0
​
 =0。

迭代： 在每次迭代k=1,2,…中：

计算梯度：  
x
^
  
k+1
​
 = 
x
^
  
k
​
 +Φ 
T
 (y−Φ 
x
^
  
k
​
 )

软阈值： 对结果应用软阈值操作：
$$ \mathcal{T}{\lambda}(z) = \text{sgn}(z)\max(|z| - \lambda, 0) $$
$$ \hat{x}{k+1} = \mathcal{T}{\lambda}(\hat{x}{k+1}) $$

终止： 当$|\hat{x}_{k+1} - \hat{x}_k|_2^2$小于某个阈值时终止。