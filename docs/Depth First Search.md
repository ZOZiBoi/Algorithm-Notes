---
aliases:
  - DFS
tags:
  - algorithms
time complexity: O(V + E)
---
- basically just go further and then go back
# Iterative Pseudocode

> [!NOTE] Note
> It is exactly like [[Breadth First Search|BFS]] except it uses a [[Stack]] instead of a [[Queue]]

```pseudo
\begin{algorithm}
\caption{Depth-First Search}
\begin{algorithmic}
\Procedure{DFS}{G, v}
    \State $stack \gets [v]$
    \While{$len(queue) > 0$}
        \State $v \gets stack.pop()$
        \If{not $marked[v]$}
            \State $visit(v)$
            \State $marked[v] \gets True$
            \For{$w \text{ in } G.neighbors(v)$}
                \If{not $marked[w]$}
                    \State $stack.append(w)$
                \EndIf
            \EndFor
        \EndIf
    \EndWhile
\EndProcedure
\end{algorithmic}
\end{algorithm}
```
# Recursive Pseudocode
```pseudo
\begin{algorithm}
\caption{Depth-First Search}
\begin{algorithmic}
\State $marked \gets \text{array of size } G.size() \text{ initialized to False}$
\Procedure{DFS}{G, v}
	\State $visit(v)$
	\State $marked[v] \gets True$
	\For{$w \text{ in } G.neighbors(v)$}
		\If{not $marked[w]$}
			\State $DFS(G,w)$
	    \EndIf
    \EndFor
\EndProcedure
\end{algorithmic}
\end{algorithm}
```

# Time Complexity
## $O(V + E)$
