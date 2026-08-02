# make classic question into quantum pattern
- Schrodinger equation:   $i \hbar \partial_t \Psi = H \Psi$ 
- classic wave function :  $\partial ^2 _t h-c^2 \partial ^2 _x h =0$

We can transform the wave function into a Schrodinger equation by following steps:

1. to convert the second derivative to the first derivative,we define new variables:
$$
h_1 =c \partial _t h
\\
h_2 =\partial _x h
$$

2. then, we define the "Hamitonian" and "wave function" :
$$
 \Psi(x,t)=\left(\begin{array}{c}h_1(x,t)\\h_2(x,t)\end{array}\right)\quad H=c\left(\begin{array}{cc}0& 1\\1 & 0\end{array}\right)(i\partial_x).
$$

3. we have:
$$
i\hbar \partial _t \Psi =i\hbar \left(\begin{array}{c}\partial _t h_1 \\\partial _t h_2 \end{array}  \right)=i\hbar \left(\begin{array}{c}c \partial _x h_2 \\ c \partial _x h_1 \end{array}  \right) =\hbar c \left( \begin{array}{c} 0 \quad 1 \\ 1 \quad 0 \end{array}\right )(i\partial _x)\left(\begin{array}{c}h_1 \\ h_2 \end{array}\right)
$$

# Bloch's therom for bulk electrons
For periodic structure,we have:
- location:  $a=(l,n)$
- $H_{(l,n)(l',m)}=H_{(l,n-m)(l',0)} $

Bloch's theorem points out that ,for such Hamitonian ,we have ansatz for electron's wave in the orbit $l$ of the lattice $n$ :
$$\psi_{(l,n)}=e^{ikn} u_l$$
And Brillouin Zone refers to the range : $k \in [-\pi,\pi]$

Put the ansatz into the time-independent Shrodinger equation:
$$
\hat H [e^{ikn} u_l] =E [e^{ikn} u_l]
$$
where
$$
\hat H=\sum H_{(l,n)(l',m)}=\sum H_{(l,n-m)(l',0)}
$$
Define $$r\coloneqq n-m $$
leading to:


$$
\hat H [e^{ikn} u_l]=\sum _{r,l'}H_{(l,r)(l',0)}e^{ik(n-r)}u_{l'}=\sum _r \sum _{l'} H_{(l,r)(l',0)}e^{-ikr}u_{l'}\cdot e^{ikn}
$$
the part before the dot is function about $l$ and $l'$。So we can define it as :
$$
H_{l l'}\coloneqq \sum _{l'} H_{(l,r)(l',0)}e^{-ikr}
$$
Then,the function doesn't conclude $r$,which make the Schrodinger as:
$$
\sum H_{ll'} u_{l'}=E u_l
$$

## S-S-H model
S-S-H model can be seen as an easy example of previous situation,which requires:
$$
l\in \{ L,R \} \quad r\in \{-1,0,1\}\\
H_{(L,0)(R,0)}=H_{(R,0)(L,0)}=t_1\\
H_{(L,1)(R,0)}=H_{(R,-1)(L,0)}=t_2\\
$$

From these conditions,we can rewrite equations as:
$$
H_{12 }=\sum H_{(L,r)(R,0)}e^{-ikr}
=H_{(L,-1)(R,0)}(=0)e^{ik}+H_{(L,0)(R,0)}e^0+H_{(L,1)(R,0)}\\
H_{12}=t_1+t_2e^{-ik}
$$


Write it as a matrix form, we have:
$$
H=\left( \begin{array}{c} 0&\quad t_1+t_2e^{-ik}\\t_1+t_2e^{ik} \quad & 0\end{array} \right)
$$

We can see that the time-independent Schrodinger equation has the form of eigenvalues problems,so we can solve $E$ easily:
$$
p_E=E^2-[t_1^2+t^2_2+t_1 t_2(e^{ik}+e^{-ik})]=0\\
E^{(\pm)}(k)=\pm \sqrt{t_1^2+t_2^2+2 t_1 t_2\cos{k}}.
$$
Take a close look, $E^+$ is no smaller than $|t_1-t_2| $,while $E^+$ is no bigger than $-|t_1-t_2| $.So there is a gap between two $E$ s,which is bigger than $2|t_1-t_2| $.In some cases ,this can be seen as an insulator.

## k-p perturbation theory
Taylor express:
$$
H(k)\approx H(k=0)+ k H'(k=0)+\frac{k^2}{2}H''(k=0)
$$
For first order:
$$
Hu=Eu\\
H'u+Hu'=E'u+Eu'
$$
Using Bra-ket :
$$
H' |u \rangle  +H |u'\rangle =E'|u\rangle +E | u' \rangle
$$
times $\langle u |$:
$$
\langle u  | H' |u \rangle+ \langle u  | H |u' \rangle=E' +E \langle u  |u' \rangle
$$
where
$$
\langle u|H =( H | u \rangle )^\dagger=( E | u \rangle )^\dagger=\langle u| E
$$
So,we have:
$$
E'=\langle u|H'|u\rangle 
$$
For second order:
$$
\begin{array}{rl}
E''&=\langle u'|H'|u\rangle +\langle u|H''|u\rangle +\langle u|H'|u' \rangle\\
&=\langle u|H''|u\rangle  + \langle u|H'|u'\rangle +(\langle u|H'|u'\rangle )^\dagger\\
&=\langle u|H''|u\rangle  + 2Re(\langle u|H'|u'\rangle)

\end{array}
$$
So long ,we assume all the $u$ refers to the same orbit,so call $n$.What we really talk about was:
$$
H' |u_n \rangle  +H |u'_n\rangle =E'_n|u_n \rangle +E_n| u'_n  \rangle
$$
This time,we times $\langle u|$:

$$
\langle u_m  | H' |u_n \rangle+ \langle u_m  | H |u'_n \rangle=E'_n\lang u_m|u_n\rang +E_n\langle u_m  |u'_n \rangle
$$
Orthogonality requires: $\lang u_m|u_n\rang=0$.And  Shrodinger equation requires: $\lang u_m|H=\lang u_m| E_m$.Bring these back ,we have:
$$
\langle u_m  | H' |u_n \rangle=(E_n-E_m)\lang u_m | u_n' \rang
$$
Project $u'_n$ onto the orthonormal basis $u_m$:
$$
|u'_n \rang =\sum |u_m \rang \lang u_m|u_n'\rang
$$
Come back to the real part:
$$
\langle u_n|H'|u'_n\rangle=\sum \lang u_n |H'|u_m \rang \lang u_m|u_n'\rang
=\sum \frac{|\lang u_m|H'|u_n\rang|^2}{E_n-E_m}
$$
which means,what insides "Re(..)" is already real.Finally back to $E''$:
$$
E''=\langle u'|H'|u\rangle +\sum \frac{|\lang u_m|H'|u_n\rang|^2}{E_n-E_m}
$$
If we assume $k=\pi + q $,where $q$ is a small quantity,we can partially expand the former equation:
$$
E^{-}(k)=- \sqrt{t_1^2+t_2^2+2 t_1 t_2\cos{k}}\approx -(t_1 - t_2)- \frac{t_1 t_2}{2(t_1-t_2)}k^2
$$

## Discretizing
$$
\psi_k(x)=e^{ikx}\\
\partial_x \psi_x = ike^{ikx}\\
\to\hat k= - i \partial _x
$$
Discretizing the distance into an integer multiple of a certain minimum distance:$x_n= n \wedge$.
Use the mean value as approximation:
$$
\partial_x\psi(x_n)\approx \frac{\psi_{n+1}-\psi_{n-1}}{2\wedge}\\
\hat k\psi (x_n)=-\frac{i}{2\wedge}(\psi_{n+1}-\psi_{n-1})
$$

Camparing with matrix
$(K\psi)_n=\sum_mK_{nm}\psi_m$ ,we have:
$$
K_{nm}
=
-\frac{i}{2\Lambda}
\left(
\delta_{m,n+1}-\delta_{m,n-1}
\right).
$$
which can be rewreitten as:
$$
K=
\frac{1}{2\Lambda}
\begin{pmatrix}
0&-i&0&\cdots&0\\
i&0&-i&\ddots&\vdots\\
0&i&0&\ddots&0\\
\vdots&\ddots&\ddots&\ddots&-i\\
0&\cdots&0&i&0
\end{pmatrix}
=
-\frac{i}{2\Lambda}
\sum_n
\left(
|n\rangle\langle n+1|
-
|n+1\rangle\langle n|
\right).
\\
$$
$$

\hat H(k=0)\to \sum H_{ab}(k=0)|a,n\rang\lang b,n|\\

H'K=\frac{i}{2 \wedge} \sum H_{ab}'(k=0)(|a,n+1\rang\lang b,n|-|a,n\rang\lang b,n+1|)
$$
taking it back to the Taylor function:
$$
H_{disc}=\sum H_{ab}(k=0)|a,n\rang\lang b,n| +\frac{i}{2 \wedge} \sum H_{ab}'(k=0)(|a,n+1\rang\lang b,n|-|a,n\rang\lang b,n+1|)
$$
During this section,we can not directlt calculate the derivation,for the space is discretized.So we use the mean value to replace it,which we do know $\psi$ in certain dots to use this method.