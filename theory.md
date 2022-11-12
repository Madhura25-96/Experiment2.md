# Theory 

In Experiment-1, Part-1 we provided a brief introduction to block codes
and also defined a class of block codes, linear block codes. For rest of
the experiments in this virtual lab we shall now focus on linear block
codes. In the last experiment, we introduced two simple classes of
linear block codes, repetition and single parity check codes. In this
experiment, we shall focus on the theory general linear block codes. We
shall study two important matrices associated with the given linear
block code, a generator matrix, denoted by $G$ and a parity check
matrix, denoted by $H$.

## Generator matrix

For any linear block code, there exists a matrix
$G \in \mathbb{F}_2^{k \times n}$ such that the codeword $\mathbf{v} \in \mathbb{F}_2^n$ corresponding to the message
$\mathbf{m} \in \mathbb{F}_2^k$ is given by
$\mathbf{m} G = \mathbf{v}$, i.e., 
$$
\begin{aligned}
\underbrace{\begin{bmatrix} v_0 & v_1 & \ldots & v_{n-1} \end{bmatrix}}_{\mathbf{v}} = 

\underbrace{\begin{bmatrix} m_0 & m_1 & \ldots & m_{k-1} \end{bmatrix}}_{\mathbf{m}} 
\times 
\underbrace{\begin{bmatrix} 

g_{0,0} & g_{0,1} & \ldots & g_{0,n-1}\\ 
g_{1,0} & g_{1,1} & \ldots & g_{1,n-1}\\ 
\vdots \\
g_{k-1,0} & g_{k-1,1} & \ldots & g_{k-1,n-1}
\end{bmatrix}}_{G}  .
\end{aligned} 
$$
This matrix $G$ is called as a generator matrix of
the given linear block code. Note that the given code is completely
described the generator matrix since by considering all possible message
vectors in $\mathbb{F}_2^k$, one can obtain the entire codebook.
Let us consider some examples.
- Example-1: For example for REP-$3$ code, the codewords corresponding to messages
$0$ and $1$ can be obtained as 
$$\begin{aligned}  
\begin{bmatrix} 0 & 0 & 0 \end{bmatrix} &= [0] \times \begin{bmatrix} 1 & 1 & 1\end{bmatrix}   \\ 
\begin{bmatrix} 1 & 1 & 1 \end{bmatrix} &= [1] \times \begin{bmatrix} 1 & 1 & 1\end{bmatrix},
 \end{aligned}
$$
where it can be seen that the matrix
$G  = \begin{bmatrix} 1 & 1 & 1\end{bmatrix}$ is a generator matrix.


- Example-2: For $(3,2)$ SPC code, the messages and the
    corresponding codewords are given below:
    
    

    These codeword can be written as $$\begin{aligned}
    \begin{bmatrix} 0 & 0 \end{bmatrix} \times \begin{bmatrix} 1 & 0 & 1 \\ 0 & 1 & 1\end{bmatrix}  
    &= \begin{bmatrix} 0 & 0 & 0 \end{bmatrix} \\
    \begin{bmatrix} 0 & 1 \end{bmatrix} \times \begin{bmatrix} 1 & 0 & 1 \\ 0 & 1 & 1\end{bmatrix}  
    &= \begin{bmatrix} 0 & 1 & 1 \end{bmatrix} \\
    \begin{bmatrix} 1 & 0 \end{bmatrix} \times \begin{bmatrix} 1 & 0 & 1 \\ 0 & 1 & 1\end{bmatrix}  
    &= \begin{bmatrix} 1 & 0 & 1 \end{bmatrix} \\ 
    \begin{bmatrix} 1 & 1 \end{bmatrix} \times \begin{bmatrix} 1 & 0 & 1 \\ 0 & 1 & 1\end{bmatrix}  
    &= \begin{bmatrix} 1 & 1 & 0 \end{bmatrix} ,
    \end{aligned}$$
     where the matrix
  $G$ = $$\begin{bmatrix} 1 & 0 & 1 \\ 0 & 1 & 1\end{bmatrix} \hspace{1in} (1)$$ is a
    generator matrix of $(3,2)$ SPC code.

Recall that a linear block code $\mathcal{C} (n,k)$ is a
$k$-dimensional subspace of the vector space $\mathbb{F}_2^n$ 
(see Experiment-1, Part-2 Theory). Let 
$\mathbf{g}_1, \mathbf{g}_2, \ldots, \mathbf{g}_k$ 
be a basis of this
subspace (see Experiment-1, Part-1 Theory). Obtain a matrix
$G \in \mathbb{F}_2^{k \times n}$ corresponding to this basis as
follows $$\begin{aligned}  
G = \begin{bmatrix}
\leftarrow & \mathbf{g}_1 & \rightarrow \\
\leftarrow & \mathbf{g}_2 & \rightarrow \\
 & \vdots &  \\
\leftarrow & \mathbf{g}_k & \rightarrow
\end{bmatrix}
\end{aligned}$$
 Note that the given code $\mathcal{C}(n,k)$ is equal
to the span of $\mathbf{g}_1, \mathbf{g}_2, \ldots, \mathbf{g}_k$,
i.e., the rows of the matrix \(G$ defined in Eq. (1) *generate* (span)
the linear block code. Hence this matrix $G$ is termed as a *generator
matrix*. Note that different bases of the vector space
$\mathcal{C}(n,k)$ will correspond to a different generator matrix and
hence a generator matrix for the given code is not unique.

