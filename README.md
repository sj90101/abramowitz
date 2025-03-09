# abramowitz

The Abramowitz functions $J_n$ of order $n$, defined by

$$J_n(z)=\int_0^\infty t^n e^{-t^2-z/t} dt , \quad n\in \mathbb{Z},$$

are frequently encountered in kinetic theory, where the integral equations
resulting from linearization of the Boltzmann equation have these
functions as the kernels.  The $n$-th order Abramowitz function $J_n$ satisfies 
the third order ODE

$$zJ_n^{'''}-(n-1)J_n^{''}+2J_n=0$$

and the recurrence relations

$$J_n'(z)=-J_{n-1}(z),$$

$$2J_n(z)=(n-1)J_{n-2}(z)+zJ_{n-3}(z).$$

This software package implements an efficient and accurate numerical scheme
for the evaluation of Abramowitz functions when its argument $z$ is in
the right half of the complex plane for $n\ge -1$.



# Copyright (C) 

2019: Jiang, Shidong

Contact: Jiang, Shidong <sjiang@flatironinstitute.org> 

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


# Callable Fortran subroutines

abramm1.f - Abramowitz function $J_{-1}(z), Re(z) >= 0$

abram0.f - Abramowitz function $J_0(z), Re(z) >= 0$ 

abram1.f - Abramowitz function $J_1(z), Re(z) >= 0$ 

abram2.f - Abramowitz function $J_2(z), Re(z) >= 0$ 

abramn.f - Abramowitz function $J_n(z), Re(z) >= 0$ 



# Callable Fortran quad precision subroutines

Note: all quad precision files need to be compiled using -freal-8-real-16 option in gfortran.

abramm1quad.f - Abramowitz function $J_{-1}(z)$, $Re(z) >= 0$, real *16 version

abram0quad.f - Abramowitz function $J_0(z), Re(z) >= 0$, real *16 version

abram1quad.f - Abramowitz function $J_1(z), Re(z) >= 0$, real *16 version

abram2quad.f - Abramowitz function $J_2(z), Re(z) >= 0$, real *16 version



# Callable Matlab functions

abramm1.m - Abramowitz function $J_{-1}(z), Re(z) >= 0$

abram0.m - Abramowitz function $J_0(z), Re(z) >= 0$ 

abram1.m - Abramowitz function $J_1(z), Re(z) >= 0$ 

abram2.m - Abramowitz function $J_2(z), Re(z) >= 0$ 

# Citing

If you find abromowitz useful in your work, please star this repository and cite it and the following. 


```
@article{GJL2020jcp,
    title={Evaluation of {A}bramowitz functions in the right half of the complex plane},
    author={Zydrunas Gimbutas and Shidong Jiang and Li-Shi Luo},
  JOURNAL = {Journal of Computational Physics},
    volume={405},
  pages={109169},
    year={2020},
}
```
# Main developers

* Shidong Jiang, Flatiron Institute, Simons Foundation
* Zydrunas Gimbutas, National Institute of Standards and Technology
* Li-Shi Luo, Old Dominion University
