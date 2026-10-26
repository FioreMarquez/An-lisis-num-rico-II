Van a estar subidos los pseudocódigos acá. 


 Algoritmo 22: El Método de Jacobi Global ($n \times n$)Qué es: Es el algoritmo iterativo principal que toma la matriz simétrica completa $A \in \mathbb{R}^{n \times n}$ y busca reducir la norma fuera de la diagonal $\text{off}(A) \le \epsilon$36

Mecánica:En cada iteración $k$, busca cuál es el elemento fuera de la diagonal principal de mayor módulo: $|A_{ij}| = \max_{r \neq s} |A_{rs}|$23.Extrae la submatriz de $2 \times 2$ formada por las intersecciones de las filas y columnas $\{i, j\}$ e invoca al Algoritmo 21 para obtener los valores $c$ y $s$ necesarios para anular a $A_{ij}$3.Aplica la rotación de Givens en $\mathbb{R}^{n \times n}$ para actualizar las filas/columnas $i$ y $j$ ($A \leftarrow J^T A J$) y acumula los autovectores en $Q$23.Repite este proceso iterativamente hasta cumplir el criterio de detención

Resumen: El Algoritmo 21 calcula la rotación puntual para anular un elemento específico de $2 \times 2$1. El Algoritmo 22 controla el bucle global de $n \times n$ e invoca repetidamente al Algoritmo 21 para diagonalizar la matriz completa
