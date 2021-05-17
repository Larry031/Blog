# Larry031的博客
> 开启2021全力冲刺的新阶段，gogogo!
## :fork_and_knife: Linux
- [git入门](https://github.com/Larry031/Note/blob/master/Tools/Git%E6%93%8D%E4%BD%9C%E6%8C%87%E5%8D%97.md)
- [linux]()
- [gcc入门](https://github.com/Larry031/Note/blob/master/Tools/gcc%E5%85%A5%E9%97%A8.md)
- [git bash配置](https://github.com/Larry031/Blog/blob/master/Tools/Git%20Bash%20%E9%85%8D%E7%BD%AE.md)
## 办公工具
- [excel](https://github.com/Larry031/Blog/blob/master/Tools/office/excel.md)
- [windows](https://github.com/Larry031/Blog/blob/master/Tools/office/windows.md)
- [Capture](https://github.com/Larry031/Blog/blob/master/Tools/office/%E5%BD%95%E5%B1%8F%E5%BC%80%E6%BA%90%E8%BD%AF%E4%BB%B6Capture.md)
## 编程语言
- [C菜鸟](https://github.com/Larry031/Blog/blob/master/Tools/C%E8%8F%9C%E9%B8%9F.md)
- [C++菜鸟](https://github.com/Larry031/Blog/blob/master/Tools/C%2B%2B%E8%8F%9C%E9%B8%9F.md)
## 仿真测试
- [Carsim2017.1安装]()
车道线拟合是根据特定数量的采样点拟合出一条多阶的车道线曲线方程。车道线一般使用三阶或五阶的螺旋线，三阶车道线的表示：
$$
y=a_0+a_1*x+a_2*x^2+a_3*x^3
$$
车道线拟合实际上是根据m个采样点$(x_1,y_1),(x_2,y_2)...(x_m,y_m)$,拟合出一条n阶多项式曲线方程：
$$
y(x,A)=a_0+a_1*x+a_2*x^2+a_3*x^3+...a_n*x^n=\sum_{i=0}^{n}a_i*x^i
$$
令
$$A=\begin{bmatrix}
	a_0\\
	a_1\\
	\vdots\\
	a_m
\end{bmatrix},
X=\begin{bmatrix}
	1 & x_1 & x_1^2 & \cdots & x_1^n\\
	1 & x_2 & x_2^2 & \cdots & x_2^n\\
	\vdots & \vdots & \vdots & \ddots & \vdots\\
	1 & x_m & x_m^2 & \cdots & x_m^n
\end{bmatrix}
$$
多项式可表示为：
$$y(x,A)=xA$$
通过设计cost funciton来评价拟合函数的质量，让每个样本点的预测值与目标值(观测值）$t_m$之间的误差最小，使用均方根误差来评价：

$$E_{RMS}=\sqrt{\frac{E(A^*)}{M}}$$

---
- 最小二乘法

误差函数为一元二次，其导数为0时可直接求得方程的唯一解，即解析解（不带正则项的解析解）。
误差函数为：
$$E(A)=\frac 1 2 \sum_{m=1}^{M}{(y(x_m,A)-t_m)^2} \\
      =\frac 1 2 (XA-T)^{\top}(XA-T)$$
对其求导：
$$\frac{\partial E(A)}{\partial A}=X^{\top}XA-X^{\top}T$$
令导数等于0，整理可得：
$$A=(X^{\top}X)^{-1}X^{\top}T$$

