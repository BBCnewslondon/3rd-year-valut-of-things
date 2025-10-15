The time independent Schrodinger equation for the hydrogen atom is
$$\left[ -\frac{h^2}{2\mu}\nabla^2 -\frac{e^2}{4 \pi \epsilon_{0}|\vec{r}|} \right]\psi(\vec{r})=E\psi(\vec{r})$$
The new constant being $\mu$ is the reduced mass which is written as $$\mu=\frac{m_{e}m_{p}}{m_{e}+m_{p}}$$
Where $m_{e}$ and $m_{p}$ are the masses of electrons and protons respectively.

The potential in this case is spherically symmetric. As a result of this using spherical co-ordinates simplifies the problem as it effectively reduces the number of variables we need to look at.

The laplacian in spherical co-ordinates is 

$$\nabla^2=\frac{1}{r^2} \frac{\partial}{\partial r}\left( r^2 \frac{\partial}{\partial r} \right)+\frac{1}{r^2\sin(\theta)} \frac{\partial}{\partial \theta}\left( \sin (\theta) \frac{\partial}{\partial \theta} \right) +\frac{1}{r^2\sin^2(\theta)} \frac{\partial^2}{\partial \phi^2}$$

and so this would recreate the schrodinger equation as 
$$-\frac{h^2}{2\mu}\left[ \frac{1}{r^2} \frac{\partial}{\partial r}\left( r^2 \frac{\partial}{\partial r} \right)+\frac{1}{r^2\sin(\theta)} \frac{\partial}{\partial \theta}\left( \sin (\theta) \frac{\partial}{\partial \theta} \right) +\frac{1}{r^2\sin^2(\theta)} \frac{\partial^2}{\partial \phi^2} \right] \psi-\frac{e^2}{4\pi\epsilon_{0}\vec{r}}\psi=E\psi$$
---
Now the equation has been found we can see that its a partial differential equation with 3 distinct functions  being $\theta,\phi,r$ . As there are no mixed derivatives we can solve this problem via separation of variables
$$\psi(r,\theta,\phi)=R(r)\Theta(\theta)\Phi(\phi)$$


