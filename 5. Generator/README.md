# 生成器

简介：https://www.runoob.com/python3/python3-iterator-generator.html

进阶：

* https://eastlakeside.gitbook.io/interpy-zh/generators
* https://pythonhowto.readthedocs.io/zh_CN/latest/iterator.html

### yield from

* `*`[展开嵌套的序列](https://python3-cookbook.readthedocs.io/zh_CN/latest/c04/p14_flattening_nested_sequence.html)
* `*`[使用生成器代替线程](https://python3-cookbook.readthedocs.io/zh_CN/latest/c12/p12_using_generators_as_alternative_to_threads.html)

## 作业

[牛顿近似法](https://en.wikipedia.org/wiki/Newton%27s_method)常被用于数值求解方程。假设有一方程为$f(x)
=0$，$x_n$是$n$次迭代后得到的近似解，则$x_{n+1}=x_n-\frac{f(x_n)}{f'(x_n)}$是比$x_n$更接近根的近似值，如图。

<p align="center">
<img src=https://upload.wikimedia.org/wikipedia/commons/8/8c/Newton_iteration.svg alt="Newton_iteration">
</p>

使用牛顿法，经过有限次迭代，我们总能得到与正确解误差小于指定精度的近似解。下面以牛顿法求2的平方根，要求保留19位有效数字，即精度达到1e-18。
同时为了直观显示牛顿法的收敛速度，要求从1.5开始迭代，并利用生成器把每一次迭代的近似解乘1e18取整后以二进制输出。

提示：Python内置浮点数类型float无法达到19位有效数字，请用Decimal类。
