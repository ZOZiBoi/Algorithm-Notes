---
tags:
  - algorithms
time complexity: O(n + k), where "n" is the number of elements in the input array and "k" is the range of values within the array
---
# Pseudocode
```pseudo
\begin{algorithm}
\caption{Counting Sort}
\begin{algorithmic}
\Function{CountingSort}{A, B, k}
\STATE Create an array $C[0 \ldots k]$, initialized to $0$
\FOR{$i \gets 1 \textbf{ to } length(A)$}
    \STATE $C[A[i]] \gets C[A[i]] + 1$
\ENDFOR
\FOR{$i \gets 1 \textbf{ to } k$}
    \STATE $C[i] \gets C[i] + C[i-1]$
\ENDFOR
\FOR{$j \gets length(A) \textbf{ downto } 1$}
    \STATE $B[C[A[j]]] \gets A[j]$
    \STATE $C[A[j]] \gets C[A[j]] - 1$
\ENDFOR
\EndFunction
\end{algorithmic}
\end{algorithm}
```
