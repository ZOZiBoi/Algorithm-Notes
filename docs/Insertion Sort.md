---
tags:
  - algorithms
time complexity: O(n^2)
---
#algorithms 
```pseudo
\begin{algorithm}
\caption{Insertion-Sort}
\begin{algorithmic}
\Procedure{Insertion-Sort}{A, n}
    \For{$i \gets 2$ to $n$}
        \State $key \gets A[i]$
        \Comment{Insert $A[i]$ into the sorted subarray $A[1 \dots i-1]$.}
        \State $j \gets i - 1$
        \While{$j > 0$ and $A[j] > key$}
            \State $A[j + 1] \gets A[j]$
            \State $j \gets j - 1$
        \EndWhile
        \State $A[j + 1] \gets key$
    \EndFor
\EndProcedure
\end{algorithmic}
\end{algorithm}
```

