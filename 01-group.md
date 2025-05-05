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

#### 交换群(Abel群)

接下来我们要考虑一种比较特殊的群,顾名思义就是有 $gg'=g'g$ 的群,那我们直观上肯定会有这样一个感觉,就是交换群是依靠一些互相独立的元生成的,那就有以下定理:

**有限交换群结构定理**:任意有限交换群 $G$ 都可以分解为素数幂阶循环群的直和,即当 $|G|=\prod_{i=1}^{t} p_i^{k_i}$ :

$$
G \cong \bigoplus_{i=1}^{t}(\mathbb{Z}/p_i^{k_i} \mathbb{Z})
$$

首先我们得解释**同态**这个概念:

如果有一个映射 $\varphi:G \to G_1$ 使得 $\varphi(ab)=\varphi(a)\varphi(b)$ ,那么就可以称 $\varphi$ 为**单(满)同态**, 如果既单又满称为**同构**,如果同构,记做 $G \cong G_1$ .

自然的,在考虑同态的时候, $\varphi:G \to G_1$ 中必然会考虑 $\image \varphi$ 和 $\ker \varphi$ ,其中 $\image \varphi$ 就是像集, $\ker \varphi=\{x \in G \mid \phi(x)=e\}$ 被称为**核**.

那容易发现 $\image \phi \leqslant G_1$ , $\ker \phi \unlhd G$ ,第二个我们通过 $\varphi(a^{-1}ha)=e$ 证明,并且有一个很重要的事实:

$$
G/ \ker \varphi \cong \image \varphi
$$

考虑映射 $\phi$ ,对于 $G / \ker \varphi$ 中一个陪集 $G'$ 将其映射到 $\varphi(g')$ , $\forall g' \in G'$ ,很显然这是一个正确的映射.

现在我们考虑怎么说明一个映射 $\varphi$ 可以说明 $G,G_1$ 是同构的?

可以说 $\ker \varphi=\{e\}$ 是一个等价条件,因为这个条件下说明了如果 $\varphi(a)=\varphi(b)$ ,那就有 $\varphi(ab^{-1})=e$ 从而 $a=b$ ,从而是单射,另一方面肯定要保证 $|G|=|G_1|$ 那就是这两个条件.

回过头来,为了证明结构定理,我们证明以下命题: $G$ 是有限交换群,并且 $|G|=p^km$ , $(p,m)=1$ ,那么有 $G \cong G_{p^k} \times G_m$ ,其中 $G_{p^k}:=\{x \in G \mid ord(x) \mid p^k\}$ , $G_m:=\{x \in G \mid ord(x) \mid m \}$ .

**证明**: 首先容易说明 $G_{p^k},G_m$ 是 $G$ 的子群,考虑将 $G_{p^k} \times G_m \to G$ , 映射方式就是 $(y,z) \to yz$ ,那么显然有 $f(y,z)f(y',z')=f(yy',zz')$ (由于是交换群),并且容易发现由Bezout可知这是一个满射,另一方面通过 $ord$ 可知 $\ker \varphi =\{(e,e)\}$ ,那这样也就证明这是一个群同构.

回到原题,直接归纳即可.

PS: 我们也好奇是否能直接求出 $|G_{p^k}|$ 和 $|G_m|$ ? 
