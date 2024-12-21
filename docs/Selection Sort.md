---
tags:
  - algorithms
time complexity: O(n^2)
---
# Pseudocode
```pseudo
\begin{algorithm}
\caption{Selection Sort}
\begin{algorithmic}
\Function{SelectionSort}{A, n}
\FOR{i = 1 to n-1}
    \STATE minIndex $\gets$ i
    \FOR{j = i+1 to n}
        \IF{A[j] < A[minIndex]}
            \STATE minIndex $\gets$ j
        \ENDIF
    \ENDFOR
	\STATE \Call{Swap}{A[i], A[minIndex]}
\ENDFOR
\EndFunction
\end{algorithmic}
\end{algorithm}
```
