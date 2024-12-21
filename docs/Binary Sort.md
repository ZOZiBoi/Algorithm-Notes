---
tags:
  - algorithms
time complexity: O(logn)
---
# Pseudocode
```pseudo
\begin{algorithm}
\caption{Binary Search}
\begin{algorithmic}
\Function{BinarySearch}{A, key, low, high}
\WHILE{$\text{low} \leq \text{high}$}
    \STATE $\text{mid} \gets \lfloor (\text{low} + \text{high})/2 \rfloor$
    \IF{$A[\text{mid}] = \text{key}$}
        \RETURN $\text{mid}$
    \ELSIF{$A[\text{mid}] > \text{key}$}
        \STATE $\text{high} \gets \text{mid} - 1$
    \ELSE
        \STATE $\text{low} \gets \text{mid} + 1$
    \ENDIF
\ENDWHILE
\RETURN \textbf{Not Found}
\EndFunction
\end{algorithmic}
\end{algorithm}
```
ez pz. rmr the book splitting example from CS50.