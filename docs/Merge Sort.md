---
tags:
  - algorithms
time complexity: O(nlogn)
---
# Pseudocode
```pseudo
\begin{algorithm}
\caption{Merge Sort}
\begin{algorithmic}
\Function{MergeSort}{A, p, r}
\IF{$p < r$}
    \STATE $q \gets \lfloor (p + r)/2 \rfloor$
    \STATE \textsc{MergeSort}(A, $p$, $q$)
    \STATE \textsc{MergeSort}(A, $q+1$, $r$)
    \STATE \textsc{Merge}(A, $p$, $q$, $r$)
\ENDIF
\EndFunction
\STATE
\Function{Merge}{A, p, q, r}
\STATE Create arrays $L \gets A[p \dots q]$ and $R \gets A[q+1 \dots r]$
\STATE Append $\infty$ to the end of both $L$ and $R$
\STATE $i \gets 1, j \gets 1$
\FOR{$k \gets p$ to $r$}
    \IF{$L[i] \leq R[j]$}
        \STATE $A[k] \gets L[i]$
        \STATE $i \gets i + 1$
    \ELSE
        \STATE $A[k] \gets R[j]$
        \STATE $j \gets j + 1$
    \ENDIF
\ENDFOR
\EndFunction

\end{algorithmic}
\end{algorithm}
```
