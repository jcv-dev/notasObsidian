## Linear Search
El algoritmo de búsqueda lineal, búsqueda secuencial, o "Linear Search" en inglés, es uno de los métodos más simples para encontrar un elemento en una lista o arreglo. La idea principal es recorrer la lista elemento por elemento hasta encontrar el elemento deseado o hasta que se haya revisado toda la lista. Una explicación más detallada del algoritmo sería la siguiente:

1. **Entrada:**
    - Una lista o arreglo de elementos.
    - El elemento que se está buscando.

2. **Proceso:**
    - Comienza desde el primer elemento de la lista y compara cada elemento con el valor buscado.
    - Si el elemento actual coincide con el valor buscado, se ha encontrado el elemento y el algoritmo termina.
    - Si no coincide, se pasa al siguiente elemento en la lista y se repite el proceso.
    - Este proceso continúa hasta que se encuentra el elemento buscado o se ha explorado toda la lista sin éxito.

3. **Salida:**
    - Si se encuentra el elemento, la posición (o índice) en la lista donde se encuentra.
    - Si no se encuentra, se puede indicar que el elemento no está presente en la lista.

Este algoritmo es fácil de entender e implementar, pero puede ser ineficiente para grandes conjuntos de datos. En el peor de los casos, este algoritmo deberá recorrer todos y cada uno de los elementos de la lista.

```python
def busquedaLineal(lista, elemento):
    for i in range(len(lista)):
        if lista[i] == elemento:
            return i  # Se encontró el elemento en la posición i
    return -1  # El elemento no está en la lista
```

Complejidad temporal: $O(n)$

#
# Insertion Sort
El algoritmo de ordenamiento por inserción, o "Insertion Sort" en inglés, es un algoritmo simple y eficiente que ordena una lista construyendo una secuencia ordenada de elementos uno a la vez. Los pasos lógicos que sigue este algoritmo son los siguientes:

1. **Entrada:**
	- Una lista o arreglo de elementos.

2. **Proceso:**
	- Comienza con el primer elemento de la lista y lo considera como una lista ordenada de un solo elemento. 
	- Toma el siguiente elemento y lo inserta en la posición correcta dentro de la lista ordenada anterior, de modo que la nueva lista también se encuentre ordenada.
	- Repite el proceso hasta que todos los elementos de la lista original estén insertados en la lista ordenada

3. **Salida:**
	- Lista ordenada

El algoritmo de ordenamiento por inserción puede compararse con la forma en que una persona ordenaría cartas en una mano: se toma una carta, se compara con las existentes en la mano y se coloca en la posición correcta.

```python
def insertionSort(arr):
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1
        
        # Mueve los elementos de arr[0..i-1] que son mayores que key
        # a una posición adelante de su posición actual
        while j >= 0 and arr[j] > key:
            arr[j + 1] = arr[j]
            j = j - 1
        arr[j + 1] = key

```

Complejidad temporal: $O(n^2)$
