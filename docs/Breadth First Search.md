---
aliases:
  - BFS
---
# Iterative Code

> [!NOTE] Note
> It is exactly like [[Depth First Search|DFS]] except it uses a [[Queue]] instead of a [[Stack]]

```pseudo
\begin{algorithm}
\caption{Breadth-First Search (BFS)}
\begin{algorithmic}
\State $marked \gets \text{array of size } G.size() \text{ initialized to False}$
\Procedure{BFS}{G, v}
    \State $queue \gets [v]$
    \While{$len(queue) > 0$}
        \State $v \gets queue.pop(0)$
        \If{not $marked[v]$}
            \State $visit(v)$
            \State $marked[v] \gets True$
            \For{$w \text{ in } G.neighbors(v)$}
                \If{not $marked[w]$}
                    \State $queue.append(w)$
                \EndIf
            \EndFor
        \EndIf
    \EndWhile
\EndProcedure
\end{algorithmic}
\end{algorithm}
```
We go breadth first in the sense that we go through the depths of the graph via the levels 