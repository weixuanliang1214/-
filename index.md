# Hilbert空间中的聚类表现
## 问题建立
聚类的训练集就是要找到由$n$个数据组成的数据集$\mathbf{X} = \lbrace X_1, X_2,..., X_n \rbrace$的$k$个聚类中心$\mathbf{C} = \lbrace \mathbf{c}_1, \mathbf{c}_2,..., \mathbf{c}_k \rbrace$。其实现方法如下，即通过最小化经验聚类风险(empirical clustering risk)寻找聚类中心：

$$W(\mathbf{C},\mu_n) = \frac{1}{n}\sum_{i=1}^n \min_{j=1,...,k} \lVert X_i - \mathbf{c}_j\rVert^2$$

可以用期望聚类风险(expected clustering risk)评价某个聚类中心$\mathbf{C}$在整个数据分布$\mu$上的表现，具体如下式：

$$W(\mathbf{C},\mu) = \int \min_{j=1,...,k} \lVert X - \mathbf{c}_j\rVert^2 d\mu(x)$$

令$\mathbf{C}_n = \min_{\mathbf{C} \in \mathcal{H}^k} W(\mathbf{C},\mu_n)$，$\mathbf{C}_n$是使得经验聚类风险最小的聚类中心。$W^*(\mu) = \inf_{\mathbf{C} \in \mathcal{H}^k} W(\mathbf{C},\mu)$为最优的期望聚类风险。

可以通过
