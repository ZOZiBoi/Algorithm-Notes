---
time complexity: O(V + E)
---
- only works in **Directed Acyclic Graph (DAG)**
- begin with a selected node 
- do a [[Depth First Search|DFS]] exploring only unvisited node
- on the recursive callback of the [[Depth First Search|DFS]], add current node to the topological ordering in reverse order.
![[Pasted image 20241221034353.png]]
Start from node H, arbitrarily 
![[Pasted image 20241221034508.png]]
Keep going until you reach deadend
![[Pasted image 20241221034601.png]]
Backtrack from deadend
![[Pasted image 20241221034628.png]]
Add M (the deadend) to the last element to the topological ordering 
Keep going until all nodes are visited
# Pseudocode
```pseudo
\begin{algorithm}
\caption{Topological Sort}
\begin{algorithmic}
\Procedure{TopSort}{G(V,e)}
	\State $N \gets G.size()$
	\State $visited \gets \text{array of size } N \text{ initialized to False}$
	\State $ordering \gets \text{array of size } N \text{ initialized to 0}$
	\State $i \gets N - 1$
	\Comment{Index for ordering array}
	\For{$at \gets 0 \text{ to } N$}
		\If{V[at] = False}
			\State $i \gets$ \Call{DFS}{i, visited, ordering, graph}
        \EndIf
	\EndFor
	\Return $ordering$
\EndProcedure

\end{algorithmic}
\end{algorithm}
```
