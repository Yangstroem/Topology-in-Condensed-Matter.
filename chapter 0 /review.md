# 1.Schrödinger equation
Quantum mechanics requires a perspective that we should treat particles as wave.There comes the Schrödinger equation:
$$i\hbar\frac{\partial}{\partial t}\Psi(\mathbf{r},t)=\mathrm{H}\Psi(\mathbf{r},t)$$
We can relate Schrödinger’s equation to wave equation in classical context.For equation:
$$\partial ^2 _t h-c^2 \partial ^2 _x h=0$$

By define ￼
$$ h_1 = \frac{1}{c} \partial _t h\\ h_2 = \partial _x h
\\
\Psi = \begin{pmatrix}
h_1\\
h_2
\end{pmatrix}
\\
 H=\hbar c \begin{pmatrix}
0 & 1\\
1 & 0
\end{pmatrix}
(i\partial _x)

$$
 we turn the classical equation for string wave to Schrödinger equation.
# 2.Electron
For electrons, we have 

## the Hamiltonian:  ￼
$$H = -\frac{\hbar^2}{2m}\partial ^2 _x +V(x)$$
## Pauli exclusion principle:  

when there are $N$ electrons, each occupies $N$ orthogonal wave-functions.

And, there are some method to simplify the equation:
## Time-independent:
$$ \Psi(x,t)=\psi(x)e^{-\frac{iEt}{\hbar}} \\
\begin{aligned}
\mathrm{H}\Psi(\mathbf{r},t) 
&=i\hbar\frac{\partial}{\partial t}\Psi(\mathbf{r},t) \\
& =E \psi(x)e^{-\frac{iEt}{\hbar}}\\
&=E\Psi
\end {aligned}



$$

## Tight binding approximation: 
we treat $\psi$ as a combination of $\psi_{a}$ from each orbital, and the $H$,therefore, need to be a matrix. 

Such $H$ have following properties:
- For $H \in F^{N\times N}$,there are N eigenvalue;
- $H$ is Hermitian: $H_{ab}=H^{*}_{ba}$
- Orthogonal: ￼$\psi^{(n)\dagger}\psi^{(m)} = 0 \quad \text{for } m \ne n.$

## Bra & Ket
- bra:  $H=\Sigma_{ab}H_{ab}|a \rangle \langle b|$
- Ket:  $\psi \to |\psi\rangle = \Sigma_{a}\psi _a 
|a \rangle$
- bra times ket:  $\langle b | a \rangle = \delta_{ab}.$