#algorithms 
- characterized by *lower bound* on asymptotic behavior 
- means **grows at least as fast** as a certain rate
> [!example] Example
> For the function
> $$
> f(n) = 7n^3 + 100n^2 -20n + 6
> $$
> the highest order term is $7n^3$
> 
>We can say that this function grows *at least as fast* as $n^3$
>
>Therefore, we can write it is $Ω(n^3)$

We can also say that the function is $Ω(n^2)$ and $Ω(n)$ which is also correct that it grows no faster than that. 

More generally it is $Ω(n^c)$ for any constant $c \le 3$.
