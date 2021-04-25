#<center>Towards a Unified Analysis of Random Fourier Features（ICML2019）</center>#
#<center>面向傅里叶变换的统一分析</center>#
###<center>作者：Zhu Li，Jean-François Ton，Dino Oglic，Dino Sejdinovic</center>###

##简介##

<font size=4>
随机傅里叶变换是一个被广泛应用于加速核算法的手段，首先我们介绍它的原理。假设$k$是一个平移不变核，即$k(x,y) = k(x-y)$。设该核函数的谱测度$d\tau$的概率密度函数为$p(\cdot)$，那么相应的平移不变核可以写为

\begin{equation}
k(x,y) = \int_\mathcal{V}e^{-2\pi i v^\top (x - y)}d\tau(v)
\end{equation}

\begin{equation}
= \int_\mathcal{V} (e^{-2\pi i v^\top x})(e^{-2\pi i v^\top y})^* p(v)dv
\end{equation}

进而，将其表示为

$$
k(x,y) = \int_\mathcal{V} z(v,x)z(v,y)p(v)dv
$$
其中$z:\mathcal{V}\times\mathcal{X}\rightarrow\mathbb{R}$是一个关于$v$和$x$的连续有界函数。随机傅里叶变换主要的想法就是通过Monte-Carlo采样

$$\hat{k}(x,y) = \frac{1}{s} \sum_{i=1}^s z({v_i},x) z({v_i},y)$$
 
去近似真正的核函数，其中$s$为采样数。




</font>