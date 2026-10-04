## 56. Merge Intervales

## Idea: 
Para este punto del taller, la clave fue plantear la solución utilizando el algoritmo de ordenamiento. La idea central es ordenar primero la lista de intervalos de menor a mayor tomando como referencia su punto de inicio; al tenerlos ordenados, el criterio local consiste en recorrerlos secuencialmente y comparar el inicio del intervalo actual con el final del último intervalo guardado: si se solapan, elijo fusionarlos actualizando el límite final, y si no, añado el intervalo actual como un nuevo elemento independiente.Para este punto del taller, la clave fue plantear la solución utilizando el algoritmo de ordenamiento. La idea central es ordenar primero la lista de intervalos de menor a mayor tomando como referencia su punto de inicio; al tenerlos ordenados, el criterio local consiste en recorrerlos secuencialmente y comparar el inicio del intervalo actual con el final del último intervalo guardado: si se solapan, elijo fusionarlos actualizando el límite final, y si no, añado el intervalo actual como un nuevo elemento independiente.

## Complejidad:
Complejidad de Tiempo: O(n log n), donde n es la cantidad total de intervalos en la entrada. El algoritmo de ordenamiento inicial es el proceso más costoso y el que domina el tiempo de ejecución, ya que el ciclo posterior donde recorro y fusiono los arreglos se hace en un tiempo lineal de O(n).
Complejidad de Espacio: O(n), donde n es el número de intervalos. Este espacio es el que necesito para la lista resultante donde voy almacenando los elementos definitivos (que en el peor de los casos, si no hay solapamientos, serán los mismos n elementos) y por el espacio de memoria auxiliar que utiliza el método de ordenamiento del lenguaje.

## Link:
![Accepted - Merge Intervals](Evidencias/merge-interval-accepted.png)

## 200. Number of Islands

## Idea: 
La idea es contar el número de componentes conexas del grafo. Para esto, recorro toda la matriz celda por celda; cada vez que encuentro un '1' que no he visitado, sé que encontré una nueva isla, así que sumo 1 a mi contador. Inmediatamente lanzo una Búsqueda en Profundidad (DFS) desde esa celda para recorrer toda la isla y "hundirla" (marco cada celda contigua reemplazando el '1' por '0'). De esta manera, me aseguro de que el DFS marque toda la componente conexa y no la vuelva a contar en el recorrido principal.

## Complejidad:
Complejidad de Tiempo: $\Theta\$(m x n), donde $m$ son las filas y n las columnas de la grilla. Aunque hay llamados recursivos del DFS, cada celda de la matriz se procesa (se visita y se marca) un número constante de veces a lo sumo, por lo que el tiempo de ejecución crece de forma estrictamente proporcional al tamaño total de la grilla.
Complejidad de Espacio: O(m x n). Este es el espacio que necesito en el peor de los casos para la pila de llamadas (call stack) de la recursividad del DFS. Esto ocurriría en un escenario extremo donde toda la matriz fuera pura tierra formando un solo camino en zigzag, haciendo que el DFS se anide m x n veces.

## Link:
![Accepted - Number of Islands](Evidencias/number-of-islands-accepted.png)
