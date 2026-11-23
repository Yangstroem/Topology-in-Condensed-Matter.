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

## Bloch Theorem
### Periodicity
for periodic structure like crystal , we divided it into single unit.To describe one position,we need two parameters:   which unit by lattice vectors $n$ and which orbitals in this cell by $l$.

### translational symmetry
to transport from one orbital of one cell ,to another orbital of another cell,the energy we need only depends on the relative locaton for two orbitals ,that's why we hope the H satisfies:
$H_{(l,n),(l‘，m)}=H_{(l,n-m),(l',0)}$
## Bloch Equation
$$Hψ = Eψ$$
in cristal ,each position could come from every positions in this finite crystal,that's why we need the Hamitonian to be like:
$$

Σ_{l',m} H_{(l,n),(l',m)}
$$
simplify the Schrodinger equation,we got:
$$
H(k)u(k)=E(k)u(k)
$$
k is called crystal momentum.Each translation of one unit cell, the phase of the wave function increases by k.The range $[−π,π]$ where $k$ is confined in ,  is referred to as the Brillouin Zone. 
## SSH Model
For some $1-D$ periodic materials like polyacetylene,there are two different part in each repeated unit,let's call the $L$ part and the $R$ part.For the $L$ part in unit labeled $n$,the $R$ part in the unit $n$ is on its right side while the $R$ part in unit $n-1$ is on its left side.And,the energy gap between $L_n $and $R_n$ is very likely different from that between $R_{n-1}$ and $L_n$.
$$
H_{(L,0),(R,0)}=H _{(R,0),(L,0)}=t_ 1
\\
H_{(L,1),(R,0)}=H _{(R,−1),(L,0)}=t_ 2
$$
According to Bloch therom,we can write the Hamitonian as below:
$$
H(k) =
\begin{pmatrix}
0               &  t_1 + t_2 e^{-ik} \\
 t_1 + t_2 e^{ik}  & 0                
\end{pmatrix}
$$
The $E$ ,which appears to be the eigenvalue,will be:
$$
E(k) = ± |t_1 + t_2 e^{ik}|
E(k)^{\pm}=\pm \sqrt{ t_1^2+t_2^2+2t_1t_2\cos(k)}
$$
As $k$ varies,
$$
E^{+}(k) ≥ |t_1 - t_2|\\
E^{-}(k) ≤ -|t_1 - t_2|
$$
And there is a gap for energy:from 
$−∣t_1−t _2∣ $ to $ ∣t _1−t_ 2∣$.So,it's an insulator.
