$$\left[-\frac{\hbar^2}{2\mu}\nabla^2 - \frac{e^2}{4\pi \varepsilon_0 r}\right]\psi(\mathbf{r}) = E\psi(\mathbf{r}).$$
Is the Schrodinger equation in 3d

For 2d this would be simplified to $$-\frac{\hbar^2}{2\mu} \nabla ^2 \psi+V(x,y)\psi(x,y)=E\psi(x,y)$$
Since there's only two variables for this problem. The problem would use polar symmetry ie using the co-ordinate transformation
$$x=r\cos \theta\brace y=r\sin \theta$$
This makes the 2d laplacian 
$$\nabla ^2=\frac{\partial^2}{\partial r^2}+\frac{1}{r} \frac{\partial}{\partial r}+\frac{1}{r^2} \frac{\partial^2}{\partial \theta^2}$$
so the equation would be $$-\frac{\hbar^2}{2\mu}\left[ \frac{\partial}{\partial r^2}+\frac{1}{r} \frac{\partial}{\partial r}+\frac{1}{r^2} \frac{\partial^2}{\partial \theta^2} \right]\psi -\frac{e^2}{4\pi\epsilon_{0}r}\psi=E\psi$$
writing $\psi(x,y)=R(r)\Theta(\theta)$ 
$$-\frac{\hbar^2}{2\mu}\left[ \frac{\partial^2 R}{\partial r^2}\Theta+\frac{1}{r} \frac{\partial R}{\partial r}\Theta+\frac{1}{r^2} \frac{\partial^2\Theta}{\partial \theta^2}R \right]-VR\Theta=ER\Theta$$
multiplying by $\frac{r^2}{R\Theta}$
$$-\frac{\hbar^2}{2\mu}\left[ \frac{r^2}{R} \frac{\partial^2R}{\partial r^2}+\frac{r}{R} \frac{\partial R}{\partial r}+\frac{\partial^2\Theta}{\partial \theta^2} \frac{1}{\Theta} \right]-Vr^2=Er^2$$

Also multiplying out the constants ie $\frac{2\mu}{\hbar^2}$
$$\left[ \frac{r^2}{R} \frac{\partial^2R}{\partial r^2}+\frac{r}{R} \frac{\partial R}{\partial r} \right]+\frac{\partial^2\Theta}{\partial\theta} \frac{1}{\Theta}-\frac{2Vr^2\mu}{\hbar^2}=\frac{2E\mu}{\hbar^2}$$

which can be rearranged to give you
$$[ \frac{r^2}{R} \frac{\partial^2R}{\partial r^2}+\frac{r}{R} \frac{\partial R}{\partial r}]-\frac{2Vr^2\mu}{\hbar^2}-\frac{2E\mu}{\hbar^2}=-\frac{\partial^2\Theta}{\partial\theta} \frac{1}{\Theta} $$
Now we have separated the variables we can now say that each side of the equation is equal to some constant vale. For the *Angular part* we get

$$-\frac{1}{\Theta} \frac{\partial^2\Theta}{\partial \theta^2}=m^2 \implies \frac{\partial^2\Theta}{\partial\theta^2}=-m^2\Theta$$
This equation would have solutions as a complex exponential $\Theta(\theta)=Ae^{ im\theta}$  

For the wave function to be cyclical then we constrain m to integers ie $m\in \mathbb{Z}$  
We call $m$ the **Magnetic quantum number**

This makes the equation $$\left[ \frac{r^2}{R} \frac{d^2R}{dr^2}+\frac{r}{R} \frac{dR}{dr} \right]+\frac{2\mu r^2}{\hbar^2}(E+V(r))=m^2$$
Which can be further simplified to
$$\frac{1}{r} \frac{d}{dr}\left( r \frac{dR}{dr} \right)+\left[ \frac{2\mu}{\hbar^2}(E-V(r))-\frac{m^2}{r^2} \right]R=0$$

---
## Solving the radial part of the equation
Firstly starting from the equation. (expanding things out)

$$\frac{d^2R}{dr^2}+\frac{1}{r} \frac{dR}{dr}+\left( \frac{2\mu E}{\hbar^2}+\frac{2\mu e^2}{4\pi\epsilon_{0}\hbar^2} \frac{1}{r}-\frac{m^2}{r^2} \right)R(r)=0$$
To save time in writing this whole thing out I'm adding some constants.

1. $\kappa^2=\frac{2\mu E}{\hbar^2}$
2. $\lambda=\frac{2\mu e^2}{4\pi\epsilon_{0}\hbar^2}$ 
This makes the equation $$\frac{d^2R}{dr^2}+\frac{1}{r} \frac{dR}{dr}+\left( -\kappa^2+\frac{\lambda}{r}-\frac{m^2}{r^2} \right)R(r)=0$$
Now this is a **2nd order linear differential equation**  However we need to find out some things on how the equation acts based on the values of r first. These being 
$$\lim_{ r \to \infty } R(r)$$
As $r  \rightarrow \infty$ all the terms which are being divided by $r$ will go to 0. This means our equation would simplify to 
$$\frac{d^2R}{dr^2}\approx \kappa^2R(r)$$
This equation has solutions $R(r) \approx e^{\kappa r}$ and $R(r)\approx e^{-\kappa r}$ 
In order to get a real physical value we need our radial function to be able to be normalized. $\int \mid\psi\mid d^2r<\infty  \implies$ the function will go to 0 at $\infty$   . Due to this constraint we already know that the first solution $e^{\kappa r}$ would diverge at large values of $r$ and so we reject this solution. Leaving us with the other solution.

For the other limit $$\lim_{ r \to 0 } R(r) $$

In this case the opposite is true. As $r$ gets small the $\frac{1}{r^2}$ is the main term. This causes the radial equation to be.
$$\frac{d^2R}{dr^2}+\frac{1}{r} \frac{dR}{dr}-\frac{m^2}{r^2} R(r)\approx 0$$
This equation can be solved using the guess of $R(r)\approx r^s$ 
Using this guess we get
$s(s-1)r^{s-2}+{sr}^{s-2}-m^2r^{s-2}=0$ 
This is simplified to $s^2-s+s-m^2=0\implies s^2=m^2\implies s=\pm m$ 
giving us 2 solutions again. These being
$R=r^{|m|}$ and $R=r^{-|m|}$ . At small $r$ the 2nd solution would diverge and so for the same reason as the other limit we reject it. 

---

### solving the ode by making another one
Now we know how our function of $R(r)$ should behave , we can try and finally solve our equation via power series. Essentially we multiply the functions we found as our limiting functions and some unknown function **This method is pain and suffering** 
$$R(r)=r^{|m|}e^{-\kappa r}F(r)$$
Firstly I'm going to make some more substitutions because I don't wanna deal with moduli and the  less square terms the better. Saves a lot of time when differentiating trust me.

1. $\rho=2\kappa r$ 
2. $\nu=\frac{\lambda}{2\kappa}$ 
3. $s=|m|$
This makes the equation now $$\frac{d^2R}{d\rho^2}+\frac{1}{\rho} \frac{dR}{d\rho}+\left( -\frac{1}{4}+\frac{\nu}{\rho}-\frac{s^2}{\rho^2} \right)R=0$$

Using the new transformed equation from earlier
$$R(\rho)=\rho^se^{-\rho/2}F(\rho)$$
Now we have the guess for our solution now we just have to sub it in. **PAIN**
I'm also using the other notation now because writing out full derivatives takes wayyyyy too long.
$$R'=\left( s^{2}\rho^{s-1}e^{-\rho/2}-\frac{1}{2}\rho^s e^{-\rho/2} \right)F(\rho)+\rho^s e^{-\rho/2}F'(\rho)$$
Which we can simplify a bit to $$R'=e^{-\rho/2}\left[ \left( sp^{s-1}-\frac{1}{2}\rho^s \right)F+\rho^s F'\right]$$

Now for the 2nd derivatives :(
This would give$$R''=-\frac{1}{2}e^{-\rho/2}\left[ s\rho^{s-1}-\frac{1}{2}\rho^s)F+\rho^s F'\right]+e^{-\rho/2} \frac{d}{d\rho}\left[ \left( s \rho^{s-1}-\frac{1}{2} \rho^s \right)F+\rho^s F'\right]$$
Which should end up being $$R''=e^{-\rho/2}[\rho^sF''+(2s \rho^{s-1}-\rho^s)F'+\left( s(s-1)\rho^{s-2}-s \rho^{s-1}+\frac{1}{4} \rho^s \right)F]$$

After subbing our values into our radial equation from earlier, collecting terms and dividing by $\rho^{s-1}$ (since $\rho\neq 0$)

$$\rho F''+(2s +1-\rho)F'+\left( \nu-s-\frac{1}{2} \right)F=0$$
---
## Using the power series 

Now that we have the equation in such a way we make the guess that we can write $F(\rho)$
 as a power series
 $$F(\rho)=\sum_{j=0}^\infty a_{j}p^j$$
 with it's derivatives being $$F'(\rho)=\sum_{j=0}^\infty ja_{j}\rho^{j-1}$$
 and $$F''(\rho)=\sum_{j=0}^\infty j(j-1)a_{j}\rho^{j-2}$$
 subbing these new results into the new differential equation for $F$
 we get
$$\rho \sum_{j=0}^\infty j(j-1)a_{j}\rho^{j-2}+(2s+1)\sum_{j=0}^\infty ja_{j}\rho^{j-1}-\rho \sum_{j=0}^\infty ja_{j}\rho^{j-1}+\left( \nu-s-\frac{1}{2} \right)\sum_{j=0}^\infty a_{j}\rho^j=0$$

which when the extra $\rho$ is multiplied into some sums that have it we get
$$\rho \sum_{j=0}^\infty j(j-1)a_{j}\rho^{j-1}+(2s+1)\sum_{j=0}^\infty ja_{j}\rho^{j-1}-\rho \sum_{j=0}^\infty ja_{j}\rho^{j}+\left( \nu-s-\frac{1}{2} \right)\sum_{j=0}^\infty a_{j}\rho^j=0$$
---

## Index shifting
Now that absolute mess of a solution makes no sense to anybody. We want to try and get all the indices over some common index. I'm gonna use $k$
- for the $\rho^j$ terms we just make $k=j$
  $\sum_{k=0}^\infty\left[ -k+\left( \nu-s-\frac{1}{2} \right) \right]a_{k}\rho^k$
- for the $\rho^{j-1}$ we have to make $k=j-1 \implies j=k+1$
  when $j=0$ , the term is also 0 . The sum then starts at $j=1$
  and when $j=1$ then $k=0$ so the overall sum starts at $k=0$
  $\sum_{k=0}^\infty (k+1)(k)a_{k+1}\rho^k+\sum_{k=0}^\infty (2s+1)(k+1)a_{k+1}\rho^k$
Now we have everything we can combine everything over one sum
$$\sum_{k=0}^\infty \left( (k+1)(k+2s+1)a_{k+1}+\left[ -k+\nu-s-\frac{1}{2} \right]a_{j} \right)\rho^j=0  $$
---
## The recurrence relationship
In order for this polynomial to be 0 for all values of $\rho$ the terms for each power must also be 0. This is where the recurrence relationship comes from
$$(k+1)(k+2s+1)a_{k+1}+\left[ \nu-s-\frac{1}{2}-k \right]a_{k}=0$$
solving for the next term in the form of the previous terms
$$a_{k+1}=\frac{\left( k+s+\frac{1}{2}-\nu \right)}{(k+1)(k+2s+1)}a_{k}$$
Now the fun thing about this relationship is essentially for very large values of k. This recurrence is actually the same as $e^{2\kappa r}$ . So if we go way up and remember the original guess for the radial function
$$R(r)=r^{|m|}e^{-\kappa r}F(r)$$ $$\lim_{ r \to \infty } R(r)\approx e^{-\kappa r} \times e^{2\kappa r}=e^{\kappa r}$$
Now this just means our solution won't give a physical answer. The equation will diverge, not be able to be normalized etc. However we haven't come up with a better solution to this problem so we slap a bandage on the whole solution and just assume the recurrence relationship just stops at some value.

For this to be true for the recurrence relationship to have some finite conclusion 
$$a_{k+1}=\frac{\left( k+s+\frac{1}{2}-\nu \right)}{(k+1)(k+2s+1)}a_{k}$$ would have to have its numerator become 0 for some value of $k$ calling this final point $n_{r}$
we get 

$$n_{r}+s+\frac{1}{2}-\nu=0\implies \nu\equiv \frac{\lambda}{2\kappa}=n_{r}+|m|+\frac{1}{2} $$
and so we can now call $n_{r}$ our radial quantum number

---

## The energy eigenvalues and solutions
Now we have our quantum numbers we just have to find our energies.

To get this we just square our previous result.
$$\left( n_{r}+|m|+\frac{1}{2} \right)^2=\left( \frac{\lambda}{2\kappa} \right)^2=\frac{\lambda^2}{4\kappa^2}$$
now going just undoing the original substitution. 
$$=\frac{\left( \frac{2\mu e^2}{4\pi\epsilon_{0}\hbar^2} \right)^2}{4\left( \frac{2\mu E}{\hbar^2} \right)}=\left( \frac{4\mu^2e^4}{(4\pi\epsilon_{0})^2\hbar^4} \right)\left( \frac{\hbar^2}{8\mu E} \right)$$
which simplifies to $$\left( \frac{\mu e^4}{2(4\pi\epsilon_{0})^2\hbar^2} \right) \frac{1}{E}$$
where the term in brackets is actually the Rydberg energy.

Rearranging for energy gives us the known result $$E=\frac{E_{r}}{\left( n_{r}+|m|+\frac{1}{2} \right)^2}$$
Which is the equation for the energy spectrum for a 2d hydrogen atom.

The solutions to $F(r)$ that you find out from this whole process are the generalized Laguerre polynomials, These show up in both the 3d and 2d version of this problem. The spherical harmonics do not show up in this because we're only dealing with 1 variable for the angles.

$$%why did I spend so long writing this thing omg. This was such a waste of time if anyone finds this comment. Then props to you man, You read this whole thing, hopefully you enjoyed my pain and suffering cuz I sure didn't$$

