---
time complexity: O(nlogn)
tags:
  - algorithms
---
# Pseudocode 
```pseudo
\begin{algorithm}
\caption{QuickSort}
\begin{algorithmic}
\Function{QuickSort}{A, p, r}
\IF{$p < r$}
    \STATE $q \gets$ \Call{Partition}{A, p, r}
    \STATE \Call{QuickSort}{A, p, q-1}
    \STATE \Call{QuickSort}{A, q+1, r}
\ENDIF
\EndFunction
\State
\Function{Partition}{A, p, r}
\STATE $x \gets A[r]$ \COMMENT{Choose pivot as the last element}
\STATE $i \gets p - 1$
\FOR{$j \gets p$ \textbf{to} $r-1$}
    \IF{$A[j] \leq x$}
        \STATE $i \gets i + 1$
        \STATE \Call{Swap}{$A[i], A[j]$}
    \ENDIF
\ENDFOR
\STATE \Call{Swap}{A[i+1], A[r]}
\RETURN $i+1$
\EndFunction
\end{algorithmic}
\end{algorithm}
```
