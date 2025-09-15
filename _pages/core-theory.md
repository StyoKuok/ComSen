---
layout: page
title: 核心理论
description: 深入探讨压缩感知的数学理论基础和关键概念
permalink: /core-theory/
---
压缩感知（CS）中的重建算法旨在从少量的测量数据中恢复原始信号。根据现有研究，算法可以分为几大类。

贪婪算法 (Greedy Algorithms)
贪婪算法是压缩感知中一类重要的重建算法，其核心思想是迭代地寻找信号中最稀疏的成分，每次选择与当前残差最相关的原子。文献研究表明，这类算法在重建质量和速度上表现出色。

典型代表

匹配追踪 (Matching Pursuit, MP)

正交匹配追踪 (Orthogonal Matching Pursuit, OMP)

分段正交匹配追踪 (Stagewise Orthogonal Matching Pursuit, StOMP)

压缩采样匹配追踪 (Compressive Sampling Matching Pursuit, CoSaMP)

梯度追踪 (Gradient Pursuit, GP)

压缩梯度追踪 (Compressive Gradient Pursuit, CGP)

快速贝叶斯匹配追踪 (Fast Bayesian Matching Pursuit, FBMP)

算法性能与对比

重建质量：研究表明，StOMP 和 CoSaMP 通常能提供比 MP 和 OMP 更低的重建误差。在某些应用中，如超声层析成像，CoSaMP 在图像质量方面表现尤为出色。

运行速度：GP 和 CGP 的运行速度通常比 MP 和 OMP 更快。

影响因素：所有贪婪算法的性能都高度依赖于信号的稀疏度和测量数量。

凸优化算法 (Convex Optimization)
在所调研的文献摘要中，并未发现关于凸优化算法的直接研究。但这类方法是压缩感知理论中的另一个重要分支，其核心思想是通过求解凸优化问题来实现信号重建。

贝叶斯方法 (Bayesian Methods)
文献中除了将 FBMP 归类为贪婪算法外，未发现关于经典贝叶斯方法的详细讨论。

参考文献

L. Du, et al. "Analysis on Greedy Reconstruction Algorithms Based on Compressed Sensing." 2012.

Shamael A. Al-Shuhail. "Image Reconstruction in a Tomographic Multiphase Flow Meter: A Greedy Compressed Sensing Approach." 2018.

Yang Hai. "Greedy Algorithms and Compressed Sensing." 2011.