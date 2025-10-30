$$\hat{L}=\hat{r}\times \hat{p}$$
That's the equation for the angular momentum operator as the cross product of the position and momentum operators.

To find any specific component for the operator $i,j,k$ . From the definition of the cross product just being the determinant of a matrix we can write any individual component using the cevita symbol $\epsilon_{ijk}$

For $\hat{L}_{j}$ 
$$\hat{L}_{j}=\sum_{k,l}\epsilon_{jkl}\hat{r}_{k}\hat{p}_{l}$$
--- 
## Finding the commutator
Using the definition found earlier
$$[\hat{r}_{i},\hat{L}_{j}]=[\hat{r}_{i}\epsilon_{jkl}\hat{r}_{k}\hat{p}_{l}]$$
The cevita can be pulled out as its just a tensor of constants
$$\epsilon_{jkl}[\hat{r}_{i},\hat{r}_{k}\hat{p}_{l}]$$
Now using the commutator identity being  $[A,BC]=[A,B]C+B[A,C]$
$$[\hat{r}_{i},\hat{L}_{j}]=\epsilon_{jkl}([\hat{r}_{i},\hat{r}_{k}]\hat{p}_{l}+\hat{r}_{k}[\hat{r}_{i},\hat{p}_{l}])$$
The first term is 0 as an operator will always commute with itself.
The other term is known to be $[\hat{r}_{i},\hat{p}_{l}=i\hbar\delta_{il}]$ (I am not deriving that, too much writing)

$$[\hat{r}_{i},\hat{L}_{j}]=i\hbar\epsilon_{jkl} \hat{r_{k}\delta _{il}}$$
leaving $$[\hat{r}_{i},\hat{L}_{j}]=i\hbar\epsilon_{jki}\hat{r}_{k}$$
We have to let $l=i$ as otherwise the delta will always be 0.

Which is the answer to the problem 
$$\boxed{[\hat{r}_{i},\hat{L}_{j}]=i\hbar\epsilon_{ijk}\hat{r}_{k}}$$
