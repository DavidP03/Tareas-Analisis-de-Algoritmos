## 56. Merge Intervales

## Idea: 
Para este punto del taller, la clave fue plantear la solución utilizando el algoritmo de ordenamiento. La idea central es ordenar primero la lista de intervalos de menor a mayor tomando como referencia su punto de inicio; al tenerlos ordenados, el criterio local consiste en recorrerlos secuencialmente y comparar el inicio del intervalo actual con el final del último intervalo guardado: si se solapan, elijo fusionarlos actualizando el límite final, y si no, añado el intervalo actual como un nuevo elemento independiente.Para este punto del taller, la clave fue plantear la solución utilizando el algoritmo de ordenamiento. La idea central es ordenar primero la lista de intervalos de menor a mayor tomando como referencia su punto de inicio; al tenerlos ordenados, el criterio local consiste en recorrerlos secuencialmente y comparar el inicio del intervalo actual con el final del último intervalo guardado: si se solapan, elijo fusionarlos actualizando el límite final, y si no, añado el intervalo actual como un nuevo elemento independiente.

## Complejidad:
Complejidad de Tiempo: O(n log n), donde n es la cantidad total de intervalos en la entrada. El algoritmo de ordenamiento inicial es el proceso más costoso y el que domina el tiempo de ejecución, ya que el ciclo posterior donde recorro y fusiono los arreglos se hace en un tiempo lineal de O(n).
Complejidad de Espacio: O(n), donde n es el número de intervalos. Este espacio es el que necesito para la lista resultante donde voy almacenando los elementos definitivos (que en el peor de los casos, si no hay solapamientos, serán los mismos n elementos) y por el espacio de memoria auxiliar que utiliza el método de ordenamiento del lenguaje.

## Link:
![Accepted - Merge Intervals](Evidencias/merge-intervals-accepted.png)
