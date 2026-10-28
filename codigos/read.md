Van a estar subidos los pseudocódigos acá. 


 Algoritmo 22: El Método de Jacobi Global n x n. Qué es: Es el algoritmo iterativo principal que toma la matriz simétrica completa A en {R}^(n x n) y busca reducir la norma fuera de la diagonal off(A) < epsilon

Mecánica:En cada iteración k, busca cuál es el elemento fuera de la diagonal principal de mayor módulo: |A_{ij}| = max_{r<s} |A_{rs}|.Extrae la submatriz de 2 x 2 formada por las intersecciones de las filas y columnas {i, j} e invoca al Algoritmo 21 para obtener los valores $c$ y $s$ necesarios para anular a A_{ij}.Aplica la rotación de Givens en {R}^{nxn} para actualizar las filas/columnas i y j (A <- J^T A J) y acumula los autovectores en Q.Repite este proceso iterativamente hasta cumplir el criterio de detención

Resumen: El Algoritmo 21 calcula la rotación puntual para anular un elemento específico de 2 x 2. El Algoritmo 22 controla el bucle global de n x n e invoca repetidamente al Algoritmo 21 para diagonalizar la matriz completa
