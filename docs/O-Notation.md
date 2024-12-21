---
tags:
  - algorithms
---
# Overview
- characterizes an _upper bound_ on the asymptotic behavior 
- it says that **a function grows no faster than a certain rate**
- based on highest order term

> [!example] Example
> For the function
> $$
> f(n) = 7n^3 + 100n^2 -20n + 6
> $$
> the highest order term is $7n^3$
> 
>We can say that this function has a growth rate of $n^3$
>
>Therefore, we can write it is $O(n^3)$

We can also say that the function is $O(n^4)$ which is also correct that it grows no faster than that. Therefore, $O(n^5)$ and $O(n^6)$ are also correct. 

More generally it is $O(n^c)$ for any constant $c \ge 3$.

