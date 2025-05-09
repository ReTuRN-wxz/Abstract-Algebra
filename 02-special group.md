#### 交换群(Abel群)

接下来我们要考虑一种比较特殊的群,顾名思义就是有 $gg'=g'g$ 的群,那我们直观上肯定会有这样一个感觉,就是交换群是依靠一些互相独立的元生成的,那就有以下定理:

**有限交换群结构定理**:任意有限交换群 $G$ 都可以分解为素数幂阶循环群的直和,即当 $|G|=\prod_{i=1}^{t} p_i^{k_i}$ :

$$
G \cong \bigoplus_{i=1}^{t}(\mathbb{Z}/p_i^{k_i} \mathbb{Z})
$$

首先我们得解释**同态**这个概念:

如果有一个映射 $\varphi:G \to G_1$ 使得 $\varphi(ab)=\varphi(a)\varphi(b)$ ,那么就可以称 $\varphi$ 为**单(满)同态**, 如果既单又满称为**同构**,如果同构,记做 $G \cong G_1$ .

自然的,在考虑同态的时候, $\varphi:G \to G_1$ 中必然会考虑 $im \varphi$ 和 $\ker \varphi$ ,其中 $im \varphi$ 就是像集, $\ker \varphi=\{x \in G \mid \phi(x)=e\}$ 被称为**核**.

那容易发现 $im \phi \leqslant G_1$ , $\ker \phi \unlhd G$ ,第二个我们通过 $\varphi(a^{-1}ha)=e$ 证明,并且有一个很重要的事实:

$$
G/ \ker \varphi \cong im \varphi
$$

考虑映射 $\phi$ ,对于 $G / \ker \varphi$ 中一个陪集 $G'$ 将其映射到 $\varphi(g')$ , $\forall g' \in G'$ ,很显然这是一个正确的映射.

现在我们考虑怎么说明一个映射 $\varphi$ 可以说明 $G,G_1$ 是同构的?

可以说 $\ker \varphi=\{e\}$ 是一个等价条件,因为这个条件下说明了如果 $\varphi(a)=\varphi(b)$ ,那就有 $\varphi(ab^{-1})=e$ 从而 $a=b$ ,从而是单射,另一方面肯定要保证 $|G|=|G_1|$ 那就是这两个条件.

回过头来,为了证明结构定理,我们证明以下命题: $G$ 是有限交换群,并且 $|G|=p^km$ , $(p,m)=1$ ,那么有 $G \cong G_{p^k} \times G_m$ ,其中 $G_{p^k}:=\{x \in G \mid ord(x) \mid p^k\}$ , $G_m:=\{x \in G \mid ord(x) \mid m \}$ .

**证明**: 首先容易说明 $G_{p^k},G_m$ 是 $G$ 的子群,考虑将 $G_{p^k} \times G_m \to G$ , 映射方式就是 $(y,z) \to yz$ ,那么显然有 $f(y,z)f(y',z')=f(yy',zz')$ (由于是交换群),并且容易发现由Bezout可知这是一个满射,另一方面通过 $ord$ 可知 $\ker \varphi =\{(e,e)\}$ ,那这样也就证明这是一个群同构.

回到原题,直接归纳即可.

PS: 我们也好奇是否能直接求出 $|G_{p^k}|$ 和 $|G_m|$ ? 
