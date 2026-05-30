# Conjugação Topológica e Sistemas Planares

# Equações diferenciais e fluxo

Nesta seção, começaremos com um sistema dinâmico dado pelo tipo mais
simples de equação diferencial, da forma $$\dot{x}(t) = ax(t),
    \label{eq:edo}$$ em que $x=x(t)$ é uma função e $a$ é um parâmetro.
Podemos obter a seguinte solução por meio de uma integração simples:
$$x(t)=ke^{at}.
    \label{eq:solucao_edo}$$ Ao tomarmos a derivada, podemos verificar
que a função acima de fato é uma solução:
$$\dot{x}(t) = \frac{d}{dt}\left[ke^{at}\right]
    = ake^{at}
    = ax(t)
    \label{eq:verifica_solucao}$$

A solução acima é, de fato, a solução geral, conforme mostraremos. Seja
$u(t)$ uma outra solução. Calcularemos a derivada de $u(t)e^{-at}$,
$$\frac{d}{dt}\left( u(t)e^{-at} \right) = u'(t)e^{-at}+u(t)(-ae^{-at}) = au(t)e^{-at}-au(t)e^{-at} = 0
    \label{eq:unicidade_solucao}$$ Isso implica que $u(t)e^{-at}$ é uma
constante, neste caso, a constante $k$. Logo $u(t)=ke^{at}$, uma solução
da forma já encontrada. Sendo assim, todas as soluções da equação em
questão são da forma $ke^{at}$.

Podemos determinar a constante $k$ se, para algum instante $t_0$, o
valor $x(t_0)=x_0$ for dado. Sendo $x(t)$ uma solução com $x(t_0)=x_0$,
temos $ke^{at_0}=x_0$, que implica $k=x_0e^{-at_0}$. Por conveniência
podemos tomar $t_0=0$, obtendo $k=x_0$, sem perda de generalidade. Se
$u(t)$ é uma solução com $u(0)=x_0$, então $v(t) = u(t-t_0)$ é uma
solução com $v(t_0)=x_0$.

A função que representa a solução de uma equação diferencial depende de
$t$ e da condição inicial $x_0$. Podemos definir uma função que também
constitui as soluções, mas com uma ênfase na dependência da condição
inicial:
$$\phi(t,x_0) \qquad (\phi:\mathbb{R}\times\mathbb{R}\rightarrow\mathbb{R}).
    \label{eq:forma_fluxo}$$ Essa função é denominada *fluxo* do sistema
dinâmico.

Com isso, para a equação $\dot{x}(t) = ax(t)$, temos
$$\phi(t, x_0) = x_0 e^{at}.
    \label{eq:fluxo_edo}$$ como o seu fluxo.

É pertinente questionar qual será o comportamento do fluxo (Eq.
[\[eq:fluxo_edo\]](#eq:fluxo_edo){reference-type="ref"
reference="eq:fluxo_edo"}) ao longo do tempo. Para isso, tomaremos os
limites do fluxo $\phi(t, x_0)$ para $t \rightarrow +\infty$. Note que o
comportamento do fluxo pode variar para diferentes valores de $a$ e
$x_0$. Investigaremos os casos distintos.

**Caso 1.** Suponha $a > 0$ e $x_0 > 0$. Temos que
$$\lim_{t \rightarrow +\infty}{\phi(t, x_0)} = \lim_{t \rightarrow +\infty}{x_0 e^{at}} = x_0\lim_{t \rightarrow +\infty}{e^{at}} = +\infty.$$
$$\lim_{t \rightarrow -\infty}{\phi(t, x_0)} = \lim_{t \rightarrow -\infty}{x_0 e^{at}} = x_0\lim_{t \rightarrow -\infty}{e^{at}} = 0.$$

**Caso 2.** Suponha $a > 0$ e $x_0 < 0$. Temos que
$$\lim_{t \rightarrow +\infty}{\phi(t, x_0)} = \lim_{t \rightarrow +\infty}{x_0 e^{at}} = -\infty.$$
$$\lim_{t \rightarrow -\infty}{\phi(t, x_0)} = \lim_{t \rightarrow -\infty}{x_0 e^{at}} = 0.$$

**Caso 3.** Suponha $a < 0$ e $x_0 > 0$. Temos que
$$\lim_{t \rightarrow +\infty}{\phi(t, x_0)} = \lim_{t \rightarrow +\infty}{x_0 e^{at}} = 0.$$
$$\lim_{t \rightarrow -\infty}{\phi(t, x_0)} = \lim_{t \rightarrow -\infty}{x_0 e^{-at}} = +\infty.$$

**Caso 4.** Suponha $a < 0$ e $x_0 < 0$. Temos que
$$\lim_{t \rightarrow +\infty}{\phi(t, x_0)} = \lim_{t \rightarrow +\infty}{x_0 e^{at}} = 0.$$
$$\lim_{t \rightarrow -\infty}{\phi(t, x_0)} = \lim_{t \rightarrow -\infty}{x_0 e^{at}} = -\infty.$$

# Homeomorfismos da reta real

Antes de introduzir o conceito de conjugação topológica entre sistemas,
vamos enfatizar alguns fatos úteis sobre homeomorfismos da reta real.

::: definition
**Definição 1**. Uma função $h:\mathbb{R} \rightarrow \mathbb{R}$ é um
*homeomorfismo em $\mathbb{R}$* se e somente se é bijetiva, contínua e
possui inversa contínua.
:::

::: {#theorem:monotonicidade_funcao .theorem}
**Teorema 1** (Curso de Análise Vol. 1, Elon Lages Lima, Cap. VII, Sec.
3, Teorema 13). *Seja $f: I \rightarrow R$ uma função contínua injetora,
definida num intervalo $I$. Então $f$ é monótona, sua imagem $J = f(I)$
é um intervalo e sua inversa $f^{-1} : J \rightarrow R$ é contínua. *
:::

O teorema acima é válido para funções que são contínuas e injetoras.
Portanto, o fato também se aplica aos homeomorfismos da reta real, que
são, por definição, funções contínuas e bijetivas.

::: {#corollary:monotonicidade_homeom .corollary}
**Corolário 1**. *Se $h$ é homeomorfismo de $\mathbb{R}$ em
$\mathbb{R}$, então $h$ é monótona. *
:::

::: proof
*Proof.* Suponha que $h$ é um homeomorfismo de $\mathbb{R}$ em
$\mathbb{R}$; isso implica, por definição, que $h$ é injetora e contínua
definida em $\mathbb{R}$. Portanto, pelo Teorema
[1](#theorem:monotonicidade_funcao){reference-type="ref"
reference="theorem:monotonicidade_funcao"}, $h$ é uma função monótona. ◻
:::

Logo, temos que os homeomorfismos de $\mathbb{R}$ em $\mathbb{R}$ são
funções bijetoras e monótonas. Com isso, podemos investigar os seus
comportamentos assintóticos para os casos monotonicamente crescentes ou
monotonicamente decrescentes.

::: {#lemma:homeo_cresc_mais_infinito .lemma}
**Lema 1**. *Se $h$ é um homeomorfismo de $\mathbb{R}$ em $\mathbb{R}$ e
é crescente, então $$\lim_{x \rightarrow +\infty}{h(x)} = + \infty,$$ *
:::

::: proof
*Proof.* Suponha que $(x_n)$ uma sequência de números reais que diverge
para $+\infty$.

Seja $M \in \mathbb{R}$ dado tal que $M > 0$. Existe um
$x_0 \in \mathbb{R}$ tal que $h(x_0) > M$, uma vez que $h$ é sobrejetora
em $\mathbb{R}$. Uma vez que a sequência diverge para $+\infty$, existe
um $n_0$ tal que para todo $n \geq n_0$, temos $x_n > \max{(M, x_0)}$.

*(a)* Caso $M < x_0$, isso implica diretamente que $x_n > x_0$. Uma vez
que $h$ é crescente, temos que $h(x_n) > h(x_0) > M$.

*(b)* Porém, caso $M$ seja suficientemente grande, temos que
$x_n > M > x_0$. Novamente, sendo $h$ crescente, temos que
$h(x_n) > h(x_0) > M$.

Uma vez que isso é válido para $M>0$ arbitrário, isso implica que
$$\lim_{x \rightarrow +\infty}h(x) = +\infty.$$ ◻
:::

::: {#lemma:homeo_decresc_menos_infinito .lemma}
**Lema 2**. *Se $h$ é um homeomorfismo de $\mathbb{R}$ em $\mathbb{R}$ e
é decrescente, então $$\lim_{x \rightarrow +\infty}{h(x)} = - \infty,$$
*
:::

::: proof
*Proof.* Suponha que $(x_n)$ uma sequência de números reais que diverge
para $+\infty$.

Seja $M \in \mathbb{R}$ dado tal que $M < 0$. Existe um
$x_0 \in \mathbb{R}$ tal que $h(x_0) < M$, uma vez que $h$ é sobrejetora
em $\mathbb{R}$. Uma vez que a sequência diverge para $+\infty$, existe
um $n_0$ tal que para todo $n \geq n_0$, temos $x_n > \max{(M, x_0)}$.

*(a)* Caso $M < x_0$, isso implica diretamente que $x_n > x_0$. Uma vez
que $h$ é decrescente, temos que $h(x_n) < h(x_0) < M$.

*(b)* Porém, caso $M > x_0$, temos que $x_n > M > x_0$. Novamente, sendo
$h$ decrescente, temos que $h(x_n) < h(x_0) < M$.

Uma vez que isso é válido para $M<0$ arbitrário, isso implica que
$$\lim_{x \rightarrow +\infty}h(x) = -\infty.$$ ◻
:::

# Conjugações topológicas em dimensão um

A seção anterior sobre homeomorfismos da reta real estabelece fatos
úteis para o estudo do conceito de conjugação topológica.

Dois sistemas são topologicamente conjugados quando os seus
comportamentos assintóticos são iguais. Portanto, no caso de sistemas da
forma $\dot{x}(t) = a x(t)$, observaremos que dois sistemas podem ou não
ser topologicamente conjugados, mesmo com valores diferentes $a$.

Partiremos da definição precisa de sistemas topologicamente conjugados:

::: {#def:conjugacao_topologica .definition}
**Definição 2**. Sejam $\dot{x}(t) = ax(t)$ e $\dot{y}(t) = by(t)$ dois
sistemas com fluxos $\phi^{a}$ e $\phi^{b}$, respectivamente. Definimos
esses sistemas como *topologicamente conjugados* quando existe um
homeomorfismo $h: \mathbb{R} \rightarrow \mathbb{R}$ tal que
$$h\left(\phi^a(t, x_0)\right) = \phi^{b}\left(t, h(x_0)\right).$$
Chamamos esse homeomorfismo $h$ de *conjugação*.
:::

Com isso, para provarmos que dois sistemas descritos por $\phi^{a}$ e
$\phi^{b}$ são topologicamente conjugados, precisamos construir um
homeomorfismo que satisfaz a Definição
[2](#def:conjugacao_topologica){reference-type="ref"
reference="def:conjugacao_topologica"}. Agora, caso dois sistemas não
sejam topologicamente conjugados, não existe um homeomorfismo $h$ que
satisfaz a Definição
[2](#def:conjugacao_topologica){reference-type="ref"
reference="def:conjugacao_topologica"}.

A seguir, mostraremos um fato particular que não é válido para
homeomorfismos em geral, mas que é válido quando esse homeomorfismo é
uma conjugação entre dois sistemas da forma $\dot{x}(t) = ax(t)$.

::: {#lemma:conj_em_zero .lemma}
**Lema 3**. *Se $h$ é uma conjugação topológica entre dois sistemas das
formas $\dot{x}(t) = ax(t)$ e $\dot{y}(t) = by(t)$ na reta com
$a,b \neq 0$, então $h(0)=0$. *
:::

::: proof
*Proof.* Sejam os fluxos associados aos dois sistemas dados por
$\phi^{a}(t, x_0) = x_0 e^{at}$ e $\phi^{b}(t, y_0) = y_0 e^{bt}$.
Suponha que $h:\mathbb{R} \rightarrow \mathbb{R}$ é uma conjugação entre
esses dois sistemas. Portanto, pela Definição
[2](#def:conjugacao_topologica){reference-type="ref"
reference="def:conjugacao_topologica"}, temos que $h$ é um homeomorfismo
e sabemos que
$$h\left(\phi^a(t, x_0)\right) = \phi^{b}\left(t, h(x_0)\right).$$

Note que $$h\left(\phi^a(t, 0)\right) = \phi^b(t, h\left(0\right)).$$
Porém, sendo $\phi^a(t, 0) = 0 e^{at} = 0$, temos que
$$h\left(0\right) = \phi^b(t, h\left(0\right)),$$ que é equivalente a
$$h(0) = h(0) e^{bt}.$$ Se caso $h(0) \neq 0$, temos que $e^{bt} = 1$
para todo $t$, o que é uma contradição. Portanto $h(0) = 0$. ◻
:::

::: {#lemma:conj_mesmo_sinal .lemma}
**Lema 4**. *Dois sistemas $\dot{x}(t) = ax(t)$ e $\dot{y}(t) = by(t)$,
com $a$ e $b$ de mesmo sinal e não nulos, são topologicamente
conjugados. *
:::

::: proof
*Proof.* Sejam $\dot{x}(t) = ax(t)$ e $\dot{y}(t) = by(t)$ dois sistemas
com $a, b > 0$ ou $a, b < 0$. Logo, seus fluxos são dados por
$$\phi^{a}(t, x_0) = x_0 e^{at}, \qquad \phi^{b}(t, y_0) = y_0 e^{bt}.$$
Seja a função $h:\mathbb{R}\rightarrow \mathbb{R}$ dada por
$$h(x) = \begin{cases}
            0, \textit{ se } x=0       \\
            x^{b/a}, \textit{ se } x>0 \\
            -|x|^{b/a}, \textit{ se } x<0
        \end{cases}$$ Note que, uma vez que $a$ e $b$ possuem mesmo o
sinal, o termo $b/a$ é sempre positivo. Também é direto perceber que
$h(x) > 0$ se e somente se $x > 0$, e $h(x) < 0$ se e somente se
$x < 0$, e $h(x) = 0$ se e somente se $x = 0$.

Se $x_0>0$, então $\phi^{a}(t, x_0) = x_0e^{at} > 0$, portanto
$$\begin{aligned}
        h\left(\phi^{a}(t, x_0)\right)
         & = \left(x_0 e^{at}\right)^{b/a} \\
         & = x_0^{b/a} (e^{at})^{b/a}      \\
         & = x_0^{b/a} e^{bt}              \\
         & = \phi^{b}(t, h(x_0)).
    
\end{aligned}$$

Se $x_0<0$, então $\phi^{a}(t, x_0) = x_0e^{at} < 0$, portanto
$$\begin{aligned}
        h\left(\phi^{a}(t, x_0)\right)
         & = -\left|x_0 e^{at}\right|^{b/a} \\
         & = -|x_0|^{b/a} |e^{at}|^{b/a}    \\
         & = -|x_0|^{b/a} e^{bt}            \\
         & = \phi^{b}(t, h(x_0)).
    
\end{aligned}$$

Se $x_0 = 0$, então $$\begin{aligned}
        \phi^{a}(t, 0) = 0e^{at} = 0, \qquad \phi^{b}(t, h(0)) = h(0)e^{bt} = 0.
    
\end{aligned}$$ Portanto, $$\begin{aligned}
        h\left(\phi^{a}(t, x_0)\right) = \phi^{b}(t, h(x_0)).
    
\end{aligned}$$

Logo, a função $h$ tem o comportamento esperado de uma conjugação.
Porém, ainda precisamos provar que $h$ é um homeomorfismo.

Uma vez que $h(x)$ é uma composição de funções contínuas para $x > 0$ e
$x < 0$, precisamos verificar se $h$ é contínua em $x = 0$. Faremos isso
por meio dos limites laterais:
$$\lim_{x \rightarrow 0^{+}} {h(x)} = \lim_{x \rightarrow 0^{+}} {x^{b / a}} = 0;$$
$$\lim_{x \rightarrow 0^{-}} {h(x)} = \lim_{x \rightarrow 0^{-}} {- |x|^{b / a}} = 0;$$
$$h(0) = 0.$$ Portanto, a função $h(x)$ é contínua para todo $x$ real.

Seja a função $g(x)$ dada por $$g(x) = \begin{cases}
            0, \textit{ se } x=0       \\
            x^{a/b}, \textit{ se } x>0 \\
            -|x|^{a/b}, \textit{ se } x<0
        \end{cases}$$ Mostraremos que essa função é a inversa de $h(x)$.
Portanto, precisamos mostrar que $(h \circ g) = (g \circ h) = I_d$, em
que $I_d$ é a função identidade.

No caso em que $x = 0$, temos $$(h \circ g)(0) = (g \circ h)(0) = 0.$$
Caso $x>0$, temos $$(h \circ g)(x) = h(x^{a/b}) = (x^{a/b})^{b/a} = x;$$
$$(g \circ h)(x) = g(x^{b/a}) = (x^{b/a})^{a/b} = x.$$ Agora, caso
$x < 0$, temos
$$(h \circ g)(x) = h(-|x|^{a/b}) = -|-|x|^{a/b}|^{b/a} = x = -(|x|^{b/a})^{a/b} = -|x| = x;$$
$$(g \circ h)(x) = g(-|x|^{b/a}) = -|-|x|^{b/a}|^{a/b} = x = -(|x|^{a/b})^{b/a} = -|x| = x.$$
Portanto, uma vez que a função $h$ admite uma inversa $h^{-1} = g$,
sabemos que $h$ é bijetora. Pelo Teorema
[1](#theorem:monotonicidade_funcao){reference-type="ref"
reference="theorem:monotonicidade_funcao"}, sabemos que essa função
inversa é contínua.

Portanto, os sistemas $\dot{x}(t) = ax(t)$ e $\dot{y}(t) = by(t)$ são
topologicamente conjugados quando $a$ e $b$ têm o mesmo sinal. ◻
:::

::: {#lemma:nao_conj_sinal_oposto .lemma}
**Lema 5**. *Dois sistemas $\dot{x}(t) = ax(t)$ e $\dot{y}(t) = by(t)$,
com $a$ e $b$ de sinais opostos e não nulos, não são topologicamente
conjugados, e em particular $a,b \neq 0$. *
:::

::: proof
*Proof.* Suponha, por contradição, que existe um homeomorfismo $h$ que
satisfaz as condições apontadas acima. Os fluxos dos sistemas acima são,
respectivamente
$$\phi^{a}(t, x_0) = x_0 e^{a t} \qquad \phi^{b}(t, y_0) = y_0e^{b t}$$

Uma vez que $a > 0$, temos que
$$\lim_{t \rightarrow \infty}{|\phi^{a}(t, x_0)|}
        = \lim_{t \rightarrow \infty}{|x_0e^{a t}|} = \infty.$$ Sendo
$b$ negativo, temos que
$$\lim_{t \rightarrow \infty}{|\phi^{b}(t, h(x_0))|}
        = \lim_{t \rightarrow \infty}{|h(x_0) e^{b t}|} = 0.$$

Uma vez que $h$ é um homeomorfismo da reta real, $h$ é bijetivo e
monótono. Portanto, temos que
$$\lim_{t \rightarrow \infty}{|h(\phi^{a}(t, x_0))|}
        = \lim_{t \rightarrow \infty}{|h(x_0e^{a t})|} = \infty$$

Porém, note que $$\lim_{t \rightarrow \infty}{|h(\phi^{a}(t, x_0))|}
        = \lim_{t \rightarrow \infty}{|\phi^{b}(t, h(x_0))|}
        = \lim_{t \rightarrow \infty}{|h(x_0)e^{b t}|}
        = 0$$

Alcançamos uma contradição, logo os sistemas não são topologicamente
conjugados. ◻
:::

Portanto, utilizando os dois lemas anteriores, chegamos ao seguinte
teorema:

::: theorem
**Teorema 1**. *Dois sistemas $\dot{x}(t) = ax(t)$ e
$\dot{y}(t) = by(t)$ são topologicamente conjugados se e somente se $a$
e $b$ possuem o mesmo sinal.*
:::

# Sistemas lineares no plano

Introduziremos agora sistemas em dimensão dois. Restringiremos o estudo
para um caso especial. Estudaremos sistemas lineares planares autônomos,
que são da forma $$\begin{aligned}
    x' = ax + by \\
    y' = cx + dy \nonumber.
\end{aligned}$$ Podemos reescrevê-lo como $X' = AX$, em que $A$ é a
matriz dos coeficientes.

De fato, os sistemas que estudamos anteriormente podem ser reduzidos em
três tipos de matrizes: $$\text{(I):} \begin{pmatrix}
        \lambda & 0   \\
        0       & \mu
    \end{pmatrix}, \qquad
    \text{(II):}\begin{pmatrix}
        \alpha & \beta  \\
        -\beta & \alpha
    \end{pmatrix}, \qquad
    \text{(III):}\begin{pmatrix}
        \lambda & 1       \\
        0       & \lambda
    \end{pmatrix}.$$ Chamamos essas formas de *formas canônicas*.
Podemos transformar qualquer sistema linear $X' = AX$ em uma forma
canônica por meio de uma mudança de coordenadas.

Seja $X = (x, y)$. Os sistemas com matrizes do tipo (I) têm seus fluxos
na forma $$\phi^{\text{I}}(t, X) = x e^{\lambda_1 t}\begin{pmatrix}
        1 \\ 0
    \end{pmatrix} + y e^{\lambda_2 t}\begin{pmatrix}
        0 \\ 1
    \end{pmatrix}.$$

No caso das matrizes do tipo (II), temos
$$\phi^{\text{II}}(t, X) = x e^{\alpha t}\begin{pmatrix}
        \cos{\beta t} \\ -\sin{\beta t}
    \end{pmatrix}
    + y e^{\alpha t}\begin{pmatrix}
        \sin{\beta t} \\ \cos{\beta t}
    \end{pmatrix}.$$

E no tipo (III), temos
$$\phi^{\text{III}}(t) = x e^{\lambda t}\begin{pmatrix}
        1 \\ 0
    \end{pmatrix}
    + y e^{\lambda t} \begin{pmatrix}
        t \\ 1
    \end{pmatrix}$$

# Conjugação topológica de sistemas planares

Podemos introduzir uma definição similar à anterior no caso de sistemas
planares.

::: definition
**Definição 3**. Sejam $X' = AX$ e $X' = BX$ dois sistemas com fluxos
$\phi^{A}$ e $\phi^{B}$, respectivamente. Definimos esses sistemas como
*conjugados* quando existe um homeomorfismo
$H: \mathbb{R}^2 \rightarrow \mathbb{R}^2$ tal que
$$H\left(\phi^A(t, X_0)\right) = \phi^{B}\left(t, H(X_0)\right).$$
Chamamos esse homeomorfismo $H$ de *conjugação*.
:::

::: definition
**Definição 4**. Uma matriz $A$ é *hiperbólica* se nenhum de seus
autovalores tem parte real nula. Dizemos também que um sistema $X' = AX$
é *hiperbólico*.
:::

::: lemma
**Lema 6**. *Sejam $X' = AX$ e $X' = BX$ dois sistemas planares
hiperbólicos em uma das formas canônicas, e conjugados com autovalores
$\lambda_1, \lambda_2$ de $A$ e $\mu_1, \mu_2$ de $B$. Se
$H:\mathbb{R}^2 \rightarrow \mathbb{R}^2$ é uma conjugação entre esses
dois sistemas, então $H(0, 0) = (0, 0)$.*
:::

::: proof
*Proof.* Seja $0 = (0, 0)$. Independentemente da forma canônica da
matriz $A$, temos que $$\phi^{A}\left(t, 0 \right) = 0.$$ Definiremos
$$H\left(X\right) = (x_{h}, y_{h})
        \qquad
        H\left(0\right) = (x_{h,0}, y_{h, 0}).$$ Separaremos a prova em
três casos, para cada uma das possíveis formas de $B$.

**Caso 1.** $B$ é da forma canônica (I).

Sendo assim, o fluxo de $B$ em $H(X)$ é dado por
$$\phi^{B}(t, H(X)) = \begin{pmatrix}
            x_{h} e^{\mu_1 t} \\ y_{h} e^{\mu_2 t}
        \end{pmatrix}$$ Uma vez que $H$ é uma conjugação, temos que
$$H\left(\phi^{A}\left(t, X\right)\right)
        = \phi^{B}(t, H(X)).$$ Em particular, temos que
$$H\left(\phi^{A}\left(t, 0\right)\right)
        = \phi^{B}(t, H(0)).$$ Utilizando as equações anteriores, isso
implica que $$\begin{pmatrix}
            x_{h,0} \\ y_{h,0}
        \end{pmatrix} = \begin{pmatrix}
            x_{h,0} e^{\mu_1 t} \\ y_{h,0} e^{\mu_2 t}
        \end{pmatrix}$$ Se $x_{h,0} \neq 0$, temos que $e^{\mu_1 t} = 1$
para todo $t$, o que é uma contradição, portanto $x_{h,0} = 0$.
Similarmente, se $y_{h,0}$, então $e^{\mu_2 t} = 1$ para todo $t$, que
também é uma contradição, e nos leva a $y_{h, 0} = 0$.

**Caso 2.** $B$ é da forma canônica (II) com $\alpha, \beta \neq 0$.

Sendo assim, o fluxo de $B$ em $H(X)$ é dado por
$$\phi^{B}(t, H(X)) = \begin{pmatrix}
            e^{\alpha t} \left( x_h \cos{\beta t} + y_h \sin{\beta t}\right) \\ e^{\alpha t}\left(-x_h \sin{\beta t} + y_h \cos{\beta t}\right)
        \end{pmatrix}$$ Uma vez que $H$ é uma conjugação, temos que
$$H\left(\phi^{A}\left(t, X\right)\right)
        = \phi^{B}(t, H(X)).$$ Em particular, temos que
$$H\left(\phi^{A}\left(t, 0\right)\right)
        = \phi^{B}(t, H(0)).$$ Utilizando as equações anteriores, isso
implica que $$\begin{pmatrix}
            x_{h,0} \\ y_{h,0}
        \end{pmatrix} = \begin{pmatrix}
            e^{\alpha t} \left( x_{h,0} \cos{\beta t} + y_{h,0} \sin{\beta t}\right) \\ e^{\alpha t}\left(-x_{h,0} \sin{\beta t} + y_{h,0} \cos{\beta t}\right)
        \end{pmatrix}.$$ Suponha, por contradição, que
$x_{h, 0} \neq 0$. Isso nos leva a
$$e^{\alpha t}\left(\cos{\beta t} + \frac{y_{h,0}}{x_{h,0}} \sin{\beta t}\right)  = 1$$
para todo $t$. Tomando $t_1 = 2\pi / \beta$, temos
$$e^{\alpha t_1}\left(\cos{2\pi} + \frac{y_{h,0}}{x_{h,0}} \sin{2\pi}\right) = 1 \implies e^{\alpha t_1} = 1$$
Tomando $t_2 = 4\pi / \beta$, temos
$$e^{\alpha t_2}\left(\cos{4\pi} + \frac{y_{h,0}}{x_{h,0}} \sin{4\pi}\right) = 1 \implies e^{\alpha t_2} = 1$$
Portanto, temos que
$$e^{\alpha t_1} = e^{\alpha t_2} \implies \alpha t_1 = \alpha t_2.$$
Isso implica que $t_1 = t_2$ ou $\alpha = 0$, e ambos não são
admissíveis. Portanto, ao assumir $x_0 \neq 0$ temos uma contradição.

Similarmente, suponha, por contradição, que $y_{h, 0} \neq 0$. Isso nos
leva a
$$e^{\alpha t} \left(\cos{\beta t} -\frac{x_{h,0}}{y_{h,0}} \sin{\beta t}\right) = 1$$
para todo $t$. Tomando $t_1 = 2\pi / \beta$, temos
$$e^{\alpha t_1} \left(\cos{2\pi} -\frac{x_{h,0}}{y_{h,0}} \sin{2\pi}\right) = 1 \implies e^{\alpha t_1} = 1$$
Tomando $t_2 = 4\pi / \beta$, temos
$$e^{\alpha t_2} \left(\cos{4\pi} -\frac{x_{h,0}}{y_{h,0}} \sin{4\pi}\right) = 1 \implies e^{\alpha t_2} = 1$$
Portanto, temos que
$$e^{\alpha t_1} = e^{\alpha t_2} \implies \alpha t_1 = \alpha t_2.$$ A
mesma contradição do caso anterior. Concluindo, provamos que
$x_0 = y_0 = 0$, ou seja, $H(0) = 0$, como queríamos demonstrar.

**Caso 3.** $B$ é da forma canônica (III).

Sendo assim, o fluxo de $B$ em $H(X)$ é dado por
$$\phi^{B}(t, H(X)) =\begin{pmatrix}
            x_h e^{\lambda t} + y_h te^{\lambda t} \\ y_h e^{\lambda t}
        \end{pmatrix}$$ Uma vez que $H$ é uma conjugação, temos que
$$H\left(\phi^{A}\left(t, X\right)\right)
        = \phi^{B}(t, H(X)).$$ Em particular, temos que
$$H\left(\phi^{A}\left(t, 0\right)\right)
        = \phi^{B}(t, H(0)).$$ Utilizando as equações anteriores, isso
implica que $$\begin{pmatrix}
            x_{h, 0} \\ y_{h, 0}
        \end{pmatrix}
        = \begin{pmatrix}
            x_{h,0} e^{\lambda t} + y_{h, 0} te^{\lambda t} \\ y_{h, 0} e^{\lambda t}
        \end{pmatrix}$$ Suponha que $y_{h,0} \neq 0$. Temos que
$e^{\lambda t} = 1$ para todo $t$, que é uma contradição. Utilizando que
$y_{h,0} = 0$ e assumindo que $x_{h,0} \neq 0$, temos novamente que
$e^{\lambda t} = 1$, uma contradição. Portanto, $H(0) = 0$, conforme
queríamos demonstrar. ◻
:::

::: lemma
**Lema 7**. *Sejam $X' = AX$ e $X' = BX$ dois sistemas planares em que
as matrizes são da forma $$A = \begin{pmatrix}
            \lambda_1 & 0 \\ 0 & \lambda_2
        \end{pmatrix}
        \qquad
        B = \begin{pmatrix}
            \mu_1 & 0 \\ 0 & \mu_2
        \end{pmatrix}.$$ Suponha também que
$\lambda_1, \lambda_2, \mu_1 > 0$ e que $\mu_2 < 0$. Sendo assim, não
existe uma conjugação $H:\mathbb{R}^2 \rightarrow \mathbb{R}^2$.
Portanto, os sistemas não são conjugados.*
:::

::: proof
*Proof.* Suponha, por contradição, que os dois sistemas são conjugados.
Portanto, existe um homeomorfismo
$H:\mathbb{R}^2 \rightarrow \mathbb{R}^2$ tal que
$$H(\phi^A(t, X)) = \phi^{B}(t, H(X))$$ para todo $X \in \mathbb{R}^2$.
Definiremos $X = (x, y)$. Os fluxos dos sistemas são dados por
$$\phi^{A}(t, X) = \begin{pmatrix}
            x e^{\lambda_1 t} \\  y e^{\lambda_2 t}
        \end{pmatrix}
        \qquad
        \phi^{B}(t, X) = \begin{pmatrix}
            x e^{\mu_1 t} \\ y e^{\mu_2 t}
        \end{pmatrix}.$$ Uma vez que $H$ é homeomorfismo, existe um
$X_v = (x_v, y_v) \in \mathbb{R}^2$ tal que $H(X_v) = v_2 = (0, 1)$. Uma
vez que $H$ é uma conjugação, é fato que
$$H(\phi^A(t, X_v)) = \phi^{B}(t, H(x_v)) = \phi^{B}(t, v_2).$$
Aplicando a inversa, temos que
$$\phi^{A}(t, X_v) = H^{-1}(\phi^{B}(t, v_2))$$ Podemos observar o
comportamento do lado esquerdo da equação tendendo a zero:
$$\begin{aligned}
        \lim_{t \rightarrow \infty}{\left\Vert
            H^{-1}(\phi^B(t, v_2))
            \right\Vert}
        = \lim_{t \rightarrow \infty}{\left\Vert H^{-1}\begin{pmatrix}
                                                               0 \\  e^{\mu_2 t}
                                                           \end{pmatrix}\right\Vert}
        = \left\Vert H^{-1}\begin{pmatrix}
                               0 \\ 0
                           \end{pmatrix} \right\Vert
        = 0
    
\end{aligned}$$ Note que $H(x_v) = v_2 \neq (0,0)$, portanto, sendo $H$
uma bijeção e $H(0, 0) = (0,0)$, então $X_v \neq (0,0)$. Logo, do lado
direito temos $$\lim_{t \rightarrow \infty}{\left\Vert
            \phi^{A}(t, X_v)
            \right\Vert}
        = \lim_{t \rightarrow \infty}{\left\Vert
            \begin{pmatrix}
                x_v e^{\lambda_1 t} \\  y_v e^{\lambda_2 t}
            \end{pmatrix}
            \right\Vert}
        = \infty$$ ◻
:::

::: lemma
**Lema 8**. *Sejam $X' = AX$ e $X' = BX$ dois sistemas planares. Suponha
também que os dois autovalores $\lambda_1$ e $\lambda_2$ de $A$ tem
parte real positiva; e que os dois autovalores $\mu_1$ e $\mu_2$ de $B$
são tais que $\mu_1$ tem parte real positiva e $\mu_2$ tem parte real
negativa. Sendo assim, não existe uma conjugação
$H:\mathbb{R}^2 \rightarrow \mathbb{R}^2$. Portanto, os sistemas não são
conjugados.*
:::

::: proof
*Proof.* Suponha, por contradição, que os dois sistemas são conjugados.
Portanto, existe um homeomorfismo
$H:\mathbb{R}^2 \rightarrow \mathbb{R}^2$ tal que
$$H(\phi^A(t, X)) = \phi^{B}(t, H(X))$$ em que
$X = (x, y) \in \mathbb{R}^2$. Uma vez que $H$ é homeomorfismo, existe
um $X_v = (x_v, y_v) \in \mathbb{R}^2$ tal que $H(X_v) = v_2 = (0, 1)$.
Uma vez que $H$ é uma conjugação, é fato que
$$H(\phi^A(t, X_v)) = \phi^{B}(t, v_2).$$ Aplicando a inversa, temos que
$$\phi^{A}(t, X_v) = H^{-1}(\phi^{B}(t, v_2))$$ Note que
$H(X_v) = v_2 \neq (0,0)$, portanto, sendo $H$ uma bijeção e
$H(0, 0) = (0,0)$, então $X_v \neq (0,0)$. Logo, do lado direito temos
$$\lim_{t \rightarrow \infty}{\left\Vert
            \phi^{A}(t, X_v)
            \right\Vert}
        = \infty$$

Podemos observar o comportamento do lado esquerdo da equação tendendo ao
infinito: $$\lim_{t \rightarrow \infty}{\left\Vert
            H^{-1}(\phi^B(t, v_2))
            \right\Vert}
        = \left\Vert H^{-1}(0, 0) \right\Vert
        = 0$$ ◻
:::

::: lemma
**Lema 9**. *Sejam $X' = AX$ e $X' = BX$ dois sistemas planares. Suponha
também que os dois autovalores $\lambda_1$ e $\lambda_2$ de $A$ tem
parte real negativa; e que os dois autovalores $\mu_1$ e $\mu_2$ de $B$
são tais que $\mu_1$ tem parte real negativa e $\mu_2$ tem parte real
positiva. Sendo assim, não existe uma conjugação
$H:\mathbb{R}^2 \rightarrow \mathbb{R}^2$. Portanto, os sistemas não são
conjugados.*
:::

::: proof
*Proof.* Suponha, por contradição, que os dois sistemas são conjugados.
Portanto, existe um homeomorfismo
$H:\mathbb{R}^2 \rightarrow \mathbb{R}^2$ tal que
$$H(\phi^A(t, X)) = \phi^{B}(t, H(X))$$ em que
$X = (x, y) \in \mathbb{R}^2$. Uma vez que $H$ é homeomorfismo, existe
um $X_v = (x_v, y_v) \in \mathbb{R}^2$ tal que $H(X_v) = v_2 = (0, 1)$.
Uma vez que $H$ é uma conjugação, é fato que
$$H(\phi^A(t, X_v)) = \phi^{B}(t, v_2).$$ Note que
$H(X_v) = v_2 \neq (0,0)$, portanto, sendo $H$ uma bijeção e
$H(0, 0) = (0,0)$, então $X_v \neq (0,0)$. Logo, do lado direito temos
$$\lim_{t \rightarrow \infty}{\left\Vert
            H(\phi^A(t, X_v))
            \right\Vert}
        = H(0)
        = 0.$$

Do lado esquerdo, temos $$\lim_{t \rightarrow \infty}{\left\Vert
            \phi^B(t, v_2)
            \right\Vert}
        = \infty$$ uma vez que $\mu_2$ é positivo.

Portanto, alcançamos a contradição $0 = \infty$, e com isso concluímos
que os sistemas não são conjugados. ◻
:::

::: proposition
**Proposição 1**. *Suponha que $A_1$ e $A_2$ são duas matrizes
hiperbólicas. Sendo assim, se ambas possuem o mesmo número de
autovalores com parte real negativa, então os sistemas $X' = A_1 X$ e
$X' = A_2 X$ são conjugados.*
:::

::: proof
*Proof.* *Caso (a)* Suponha que temos dois sistemas lineares,
$X' = A_i X$ para $i=1,2$, ambos com autovalores $\lambda_i < 0 < \mu_i$
ou $0 <\lambda_i \leq \mu_i$ ou $\lambda_i \leq \mu_i < 0$. Logo, sendo
os sistemas na forma canônica, temos sistemas da forma $$\begin{cases}
            x' & = \lambda_{1} x \\
            y' & = \mu_{1}y
        \end{cases}
        \qquad
        \begin{cases}
            x' & = \lambda_{2} x \\
            y' & = \mu_{2}y
        \end{cases}$$ Com isso, temos fluxos da forma
$$\phi^{1}(t, X_0) = (x_0e^{\lambda_1}, y_0e^{\mu_1})\qquad\phi^{2}(t, X_0) = (x_0e^{\lambda_2}, y_0e^{\mu_2})$$

Conforme vimos anteriormente, para o caso unidimensional podemos definir
uma função $h(x)$ que é um homeomorfismo da reta real e funciona como
uma conjugação. Podemos definir as seguintes funções:
$$h_{\lambda}(x) = \begin{cases}
            0,                            & \text{  se  } x = 0 \\
            x^{\lambda_2 / \lambda_1},    & \text{  se  } x > 0 \\
            -|x|^{\lambda_2 / \lambda_1}, & \text{  se  } x < 0
        \end{cases}, \qquad
        h_{\mu}(y) = \begin{cases}
            0,                    & \text{  se  } y = 0 \\
            y^{\mu_2 / \mu_1},    & \text{  se  } y > 0 \\
            -|y|^{\mu_2 / \mu_1}, & \text{  se  } y < 0
        \end{cases}.$$

Afirmamos que a função
$$H(x, y) = \left(h_{\lambda}(x), h_{\mu}(y)\right)$$ é uma conjugação
entre $\phi^{1}$ e $\phi^{2}$. Uma vez que $H(x)$ é um produto de
homeomorfismos, podemos afirmar que $H(x)$ é um homeomorfismo.
Verifiquemos que $H(x)$ é uma conjugação.

Suponha $x_0, y_0 > 0$, logo $$\begin{aligned}
        H( & \phi^1(t, X_0))                                                                                \\
           & = H\left(x_0e^{\lambda_1t}, \, y_0e^{\mu_1t}\right)                                            \\
           & = \left(h_{\lambda}(x_0e^{\lambda_1t}), \, h_{\mu}(y_0e^{\mu_1t})\right)                       \\
           & = \left((x_0^{\lambda_2/\lambda_1}) e^{\lambda_2 t}, \, (y_0^{\mu_2/\mu_1}) e^{\mu_2 t}\right) \\
           & = \phi^{2}(t, H(X_0)).
    
\end{aligned}$$ O resultado é análogo para $x_0$ e $y_0$ negativos ou de
sinais opostos.

Note que o resultado não é válido para $\lambda_1$ e $\lambda_2$ de
sinais diferentes, e igualmente para $\mu_1$ e $\mu_2$.

*Caso (b)* Considere o sistema $X' = AX$ em que $A$ está em uma forma
canônica mas não está na forma: $$\begin{pmatrix}
            \lambda & 0 \\ 0 & \lambda
        \end{pmatrix}$$

Logo, a matriz é da forma $$A = \begin{pmatrix}
            \alpha & \beta \\ -\beta & \alpha
        \end{pmatrix} \qquad
        \alpha < 0.$$

Vamos mostrar que o sistema é conjugado a $X' = BX$ em que
$$B = \begin{pmatrix}
            -1 & 0 \\ 0 & -1
        \end{pmatrix}.$$

Considere a circunferência unitária no plano, parametrizada pela curva
$$S^1: \, X(\theta) = (\cos{\theta}, \sin{\theta}).$$ Podemos mostrar
que os pontos em $S^1$ de um campo vetorial dado pelo sistema associado
a $A$ sempre aponta para dentro de $S^1$. Temos o campo vetorial em
$S^{1}$ dado por $$V(\theta) = AX(\theta) = \begin{pmatrix}
            \alpha \cos{\theta} + \beta \sin{\theta}
            \\ -\beta \cos{\theta} + \alpha \sin{\theta}
        \end{pmatrix}.$$ O vetor normal (unitário, perpendicular à
circunferência e apontando para fora) da circunferência é dado por
$$N(\theta) = \begin{pmatrix}
            \cos{\theta} \\ \sin{\theta}
        \end{pmatrix}.$$

Podemos encontrar o produto escalar entre esses dois campos vetoriais
$$AX(\theta) \cdot N(\theta) = \alpha (\cos^2{\theta}+\sin^2{\theta}).$$
Uma vez que $\alpha<0$, isso implica que
$AX(\theta) \cdot N(\theta) < 0$. Isso implica também que cada solução
de $X' = AX$ cruza $S^{1}$ apenas uma vez.

Seja $\phi^{A}_t$ o mapa de tempo $t$ para o sistema $X' = AX$. Seja
$\tau = \tau(x, y)$ o tempo em que $\phi^{A}_t$ cruza $S^1$. Logo, temos
$$\left|\phi^{A}_{\tau(x, y)}\right| = 1.$$

Seja $\phi^{B}_t$ o mapa de tempo $t$ para o sistema $X' = BX$. Logo,
$$\phi^{B}_t(x, y) = \left(e^{-t}x, e^{-t}y\right).$$

Podemos definir uma função $H$ e mostrar que ela é uma conjugação. Seja
$H(0, 0) = (0, 0)$, e seja
$$H(x, y) = \phi^{B}_{-\tau(x, y)}\left(\phi^{A}_{\tau(x, y)} (x, y)\right). \qquad (x, y) \neq (0, 0)$$
Representando com uma figura, temos

<figure id="fig:tau_x_y">
<p><img src="assets/tau_x_y.png" style="width:50.0%" alt="image" />
<span id="fig:tau_x_y" data-label="fig:tau_x_y"></span></p>
</figure>

Se pegarmos um ponto $(x,y)$ qualquer no plano e aplicarmos o mapa de
tempo $s$ nesse ponto, obtemos $\phi_s^A(x,y)$. Utilizando
$\phi_s^A(x,y)$ como entrada em um mapa de tempo $\tau-s$, obtemos
$\phi_{\tau-s}\phi_s(x,y)$. Supondo $0 < s < \tau$, temos que
$\phi_s^A(x,y)$ associa $(x,y)$ a um ponto mais próximo de
$\phi_{\tau(x, y)}$; então $\phi_{\tau-s}\phi_s(x,y)$ associa o ponto
$\phi_s^A(x,y)$ ao ponto $\phi_{\tau}(x,y)$, isto é, faz com que a
solução ande o caminho que falta em direção a $S^1$. Em termos
matemáticos:
$$\phi^{A}_{\tau-s}  \phi^{A}_{s}(x,y) = \phi^{A}_{\tau}(x, y) \in S^1.$$

Com isso, temos que o tempo necessário para associar a o ponto
$\phi^{A}_s(x,y)$ ao ponto $\phi_{\tau}(x,y)$, isto é, o tempo
$\tau(\phi^{A}_s(x,y))$, é igual ao tempo necessário para associar
$(x,y)$ subtraído do tempo já percorrido pela solução, que é o tempo
$s$. Em termos matemáticos: $$\tau(\phi^{A}_s(x,y)) = \tau(x, y) - s.$$

Com isso, temos que $$\begin{aligned}
        H(\phi^{A}_s(x,y))
         & = \phi^{B}_{-\tau{(\phi^{A}_s(x,y))}}\phi^{A}_{\tau{(\phi^{A}_s(x,y))}}(\phi^{A}_s(x,y)) \\
         & = \phi^{B}_{-\tau(x,y) + s}\phi^{A}_{\tau(x,y) - s}(\phi^{A}_s(x,y))                     \\
         & = \phi^{B}_{-\tau(x,y) + s}\phi^{A}_{\tau(x,y)}(x,y)                                     \\
         & = \phi^{B}_{s}\left(\phi^{B}_{-\tau(x,y)}\phi^{A}_{\tau(x,y)}(x,y)\right)                \\
         & = \phi^{B}_{s}\left(H(x,y)\right)
    
\end{aligned}$$

Logo, $H$ dispõe do comportamento esperado de uma conjugação. Porém,
ainda precisamos mostrar que $H$ é um homeomorfismo.

Podemos construir uma inversa usando um processo análogo à construção de
$H$, e chamaremos essa inversa de $G$. Temos $G(0, 0) = (0, 0)$ e
$$G(x,y) = \phi^{A}_{-\tau_{1}(x,y)}\phi^{B}_{\tau_1(x,y)}(x,y), \qquad (x,y) \neq (0, 0)$$
em que $\tau_1(x,y)$ é o tempo em que $X' = BX$ cruza $S^1$.

Note que, diferente do caso anterior, podemos construir uma expressão
para $\tau_1(x,y)$, pois o sistema $X' = BX$ é totalmente conhecido.
Definiremos $r ^2= x^2 + y^2$ para simplificar. Com isso, podemos
encontrar a distância entre um mapa de tempo $t$ qualquer e a origem:
$$|\phi^{B}_t(x,y)| = \sqrt{(xe^{-t})^2+(ye^{-t})^2} = \sqrt{(e^{-2t})(x^2+y^2)} = e^{-t}r$$
Basta utilizarmos $$\left|\phi^{B}_{\tau_1(x, y)}(x,y)\right| = 1,$$ com
isso, temos $$e^{-\tau_1(x,y)}r = 1 \implies \tau_1(x,y) = \ln{r}$$

Essa função $G$ é contínua para $(x,y) \neq (0, 0)$, pois podemos
escrevê-la como
$$G(x,y) = \phi^{A}_{-\ln{r}}\left(\frac{x}{r}, \frac{y}{r}\right),$$
que é uma composição de funções contínuas.

Podemos mostrar que $G$ é contínua também na origem. Suponha que
$(x, y)$ é próximo da origem, o que implica que $r$ é próximo de $0$.
Note que $r \rightarrow 0$ implica $-\ln{r} \rightarrow \infty$. Logo,
para $r$ suficientemente pequeno, $\phi^{A}_{-\ln r}$ mapeia o círculo
unitário muito próximo de $(0, 0)$. Portanto, $G$ é contínua na origem.

Agora, precisamos mostrar a continuidade de $H(x,y)$. Podemos fazer isso
mostrando que $\tau(x,y)$ é contínua. Sabemos que $\tau(x,y)$ é
determinado por $$\left|\phi^{A}_{\tau(x, y)}\right| = 1.$$

Escreveremos $\phi^{A}_t = \left(x(t), y(t)\right)$. Podemos calcular a
derivada parcial da equação acima: $$\begin{aligned}
        \frac{\partial }{\partial t}\left|\phi^{A}_{\tau(x, y)}\right| & = \frac{\partial }{\partial t} \sqrt{(x(t))^2 + (y(t))^2}               \\
                                                                       & = \frac{1}{\sqrt{(x(t))^2 + (y(t))^2}}\left(x(t)x'(t)+y(t)y'(t)\right)  \\
                                                                       & = \frac{1}{\left|\phi^{A}_{\tau(x, y)}\right|}\left(\begin{pmatrix}
                                                                                                                                     x(t) \\ y(t)
                                                                                                                                 \end{pmatrix} \cdot
        \begin{pmatrix}
                x'(t) \\ y'(t)
            \end{pmatrix}
        \right).
    
\end{aligned}$$

Note que o produto escalar acima não pode ser nulo para
$t = \tau{(x, y)}$, uma vez que $(x'(t), y'(t))$ aponta para dentro de
$S^1$.

Partindo do fato que
$\frac{\partial }{\partial t}\left|\phi^{A}_{t(x, y)}\right|\neq 0$ em
$(\tau(x,y), x, y)$, o Teorema da Função Implícita afirma que
$\tau(x,y)$ é diferenciável, e portanto contínua. A continuidade na
origem é válida pelo mesmo raciocínio que $G(x,y)$.

Portanto, conclui-se que $H$ é um homeomorfismo e temos uma conjugação
entre $X' = AX$ e $X' = BX$.

No caso de autovalores com parte real positiva, a prova é análoga.

*Caso (c)* Suponha que $$A = \begin{pmatrix}
            \lambda & 1 \\ 0 & \lambda
        \end{pmatrix}, \qquad \lambda < 0.$$ O campo vetorial associado
não aponta sempre para a origem. Porém, se tivermos
$$T = \begin{pmatrix}
            1 & 0 \\ 0 & \epsilon
        \end{pmatrix},$$ em que $e>0$, podemos calcular a matriz
$$(T^{-1} A T) = \begin{pmatrix}
            \lambda & \epsilon \\ 0 & \lambda
        \end{pmatrix}.$$

Vamos aplicar o sistema $Y' = (T^{-1} A T) Y$ na circunferência unitária
$S_1$ com o intuito de encontrar soluções que sempre para o interior de
$S_1: X({\theta})$; com isso, teremos um valor adequado de $\epsilon$.
Em outras palavras, faremos o produto escalar
$(T^{-1} A T)X(\theta) \cdot N(\theta)$ e escolheremos $\epsilon>0$ tal
que esse produto seja sempre negativo.

$$\begin{aligned}
         & \left(T^{-1} A T\begin{pmatrix}
                               \cos{\theta} \\ \sin{\theta}
                           \end{pmatrix}\right) \cdot
        \begin{pmatrix}
            \cos{\theta} \\ \sin{\theta}
        \end{pmatrix}                                                           \\
         & \quad= \begin{pmatrix}
                      \lambda \cos\theta + \epsilon \sin\theta \\ \lambda\sin\theta
                  \end{pmatrix}
        \cdot
        \begin{pmatrix}
            \cos\theta \\ \sin\theta
        \end{pmatrix}                                                               \\
         & \quad = (\lambda \cos\theta + \epsilon \sin\theta)\cos\theta + \lambda\sin^2\theta \\
         & \quad = \lambda \cos^2\theta + \epsilon \sin\theta\cos\theta + \lambda\sin^2\theta \\
         & \quad = \lambda(\sin^2\theta + \cos^2\theta) + \epsilon \sin\theta\cos\theta       \\
         & \quad = \lambda + \epsilon \sin\theta\cos\theta                                    \\
    
\end{aligned}$$ que é negativo se $\epsilon < -\lambda$.

Logo, a mudança de coordenadas nos coloca novamente no Caso 2, uma vez
que todas as soluções atravessam $S_1$ apenas uma vez.

A prova está completa. ◻
:::
