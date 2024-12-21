# Pseudocode
```pseudo
\begin{algorithm}
\caption{Bubble Sort}
\begin{algorithmic}
\Function{BubbleSort}{A, n}
\FOR{i = 1 to n-1}
    \FOR{j = 1 to n-i}
        \IF{A[j] > A[j+1]}
            \STATE \Call{Swap}{A[j], A[j+1]}
        \ENDIF
    \ENDFOR
\ENDFOR
\EndFunction
\end{algorithmic}
\end{algorithm}
```
