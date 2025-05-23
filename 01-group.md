### 群

**Lagrange定理**: $|G|=|H|\left[ G:H \right]$ .

得先考虑陪集的性质,如果 $H$ 是一个子群,那么 $gH$ 构成一个划分,那得证明几件事情:

1. $|gH|=|H|$ , $\forall g \in G$ .
2. 假如对于 $g_1,g_2 \in G$ ,有 $g_1H \cap g_2H \ne \emptyset$ ,那么 $g_1H=g_2H$ .

对于第一件事情,我们只用证明 $gh_1 \ne gh_2$ 即可,左乘一个 $g^{-1}$ 即可.

对于第二个,假如有 $g_1h_1=g_2h_2$ ,那么对于任意一个 $g_1h=g_1h_1h'=g_2h_2h' \in g_2H$ ,从而得到 $g_1H \subseteq g_2H$ ,同理也有 $g_2H \subseteq g_1H$ ,也就得到了 $g_1H=g_2H$ .

有这两件事情就知道陪集构成了一个划分,同时也就证明了 $|H|$ 是 $|G|$ 的约数.

所以这样回头看**Lagrange定理**,就得知 $H$ 的不同左(右)陪集个数是 $\left[ G:H \right]$ .

然后我们研究这样一个问题 $|HK|=|KH|$ ? 

有一个解释是这样的,因为 $hk=e \iff kh=e$ ,这是因为 $kh=h^{-1}h=e$ ,所以这件事情是等价的后我们就有:

$$
|HK|=\frac{|H| \cdot |K|}{hk=e \text{的组数} }
$$

这个还有一种看法就是说我们考虑 $|HK|$ 中肯定是某些 $hK$ 的并,那么 $h_1K=h_2K$ 等价于 $h_1=h_2k$ ,也就是当且仅当 $k \in H$ 的时候,所以换句话说上面那个式子就成立了,然后还能写得好看一点就是:

$$
|HK| = \frac{|H| \cdot |K|}{|H \cap K|}
$$

这样我们就可以说 $|HK|=|KH|$ ,进一步的我们就会问什么时候 $HK=KH$ ?

然后我们引入了**正规子群**: 如果对任意 $g \in G$ ,有 $gH=Hg$ 那么称 $H$ 是一个正规子群,记做 $H \unlhd G$ , 有以下性质:

我们会好奇如果 $H,K$ 都是子群,那 $HK$ 会是子群吗?

假如 $HK$ 是子群,那就有 $(hk)^{-1}=k^{-1}h^{-1} \in HK$ ,那就有 $KH \subseteq HK$ ,同理交换 $HK \subseteq KH$ ,那就有 $HK=KH$ .

这貌似是等价的,就是说当 $HK=KH$ 时, $h_1k_1h_2k_2=h_1h'k'k_2 \in HK$ ,从而必然是一个子群.

所以对于上述问题,答案是等价于 $HK=KH$ .

然后对于正规子群的验证,我们可以验证对于任意 $g \in G$ 都有 $gHg^{-1} \in H$ 从而验证 $H$ 是一个正规子群,这是因为如果 $ghg^{-1}=h'$ ,那么$gh=h'g$ 从而得到 $gH=Hg$ ,同时如果 $gH=Hg$ ,也能推出 $gh=h'g$ ,也就有 $ghg^{-1} \in H$ ,所以这是等价的.

正规子群还有一个非常重要的性质,就是他良定义了**商群**:即 $G/H$ ,设想如果 $H$ 只是一个子群,那么我们还是使用 $G/H$ 去定义一个“商群”,此时对于 $\bar{a},\bar{b}$ ,运算的性质消失了: $ah_1bh_2$ 无法计算,所以正规子群可以良定义商群.  
