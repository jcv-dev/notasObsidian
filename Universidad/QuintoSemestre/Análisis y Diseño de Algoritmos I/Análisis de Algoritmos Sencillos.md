# Linear Search
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

## Implementación
```python
def busquedaLineal(lista, elemento):
    for i in range(len(lista)):
        if lista[i] == elemento:
            return i  # Se encontró el elemento en la posición i
    return -1  # El elemento no está en la lista
```

Complejidad temporal: $O(n)$

# Binary Search
La búsqueda binaria, o "Binary Search" en inglés, es un algoritmo de búsqueda eficiente utilizado para encontrar la posición de un elemento en una lista ordenada. Este algoritmo aprovecha el hecho de que la lista está ordenada para reducir el espacio de búsqueda a la mitad en cada iteración. Aquí hay un análisis del algoritmo de búsqueda binaria:

1. **Entrada:**
    - Una lista ordenada de elementos.
    - El elemento que se está buscando en la lista.

2. **Proceso:**
    - Inicializa dos punteros, `inicio` y `fin`, al principio y al final de la lista respectivamente.
    - Calcula el índice medio, `mitad`, de la lista actual (`(inicio + fin) // 2`).
    - Compara el elemento en la posición `mitad` con el valor buscado.
        - Si son iguales, se ha encontrado el elemento y el algoritmo termina.
        - Si el elemento buscado es menor que el elemento en `mitad`, la búsqueda se centra en la mitad inferior de la lista (izquierda de `mitad`).
        - Si el elemento buscado es mayor, la búsqueda se centra en la mitad superior de la lista (derecha de `mitad`).
    - Repite este proceso ajustando los punteros `inicio` y `fin` hasta que se encuentre el elemento o hasta que `inicio` sea mayor que `fin`, indicando que el elemento no está presente en la lista.

3. **Salida:**
    - Si se encuentra el elemento, se devuelve la posición (o índice) en la lista donde se encuentra.
    - Si no se encuentra, se devuelve -1 para indicar que el elemento no está presente en la lista.

Este algoritmo es bastante eficiente para listas grandes, pues va reduciendo el tamaño de las mismas hasta hallar el elemento esperado; no obstante, cabe recalcar que la estructura de datos en la que se realiza la búsqueda debe estar ordenada, por lo tanto, no podría aplicarse a Set's o estructuras similares. 

La estrategia principal utilizada en este algoritmo es "Divide y Vencerás", dado que se divide el problema en subproblemas más pequeños. 

## Implementación iterativa
```python
def busquedaBinaria(lista, elemento):
    inicio, fin = 0, len(lista) - 1
    
    while inicio <= fin:
        mitad = (inicio + fin) // 2
        if lista[mitad] == elemento:
            return mitad
        elif lista[mitad] < elemento:
            inicio = mitad + 1
        else:
            fin = mitad - 1
            
    return -1  # El elemento no está en la lista
```

## Implementación recursiva
```python
def busquedaBinariaRec(arr, elemento, inicio, fin):
    if inicio <= fin:
        mitad = (inicio + fin) // 2

        if arr[mitad] == elemento:
            return mitad  # Elemento encontrado, devolver la posición
        elif arr[mitad] < elemento:
            return busquedaBinariaRec(arr, elemento, mitad + 1, fin)  # Buscar en la mitad derecha
        else:
            return busquedaBinariaRec(arr, elemento, inicio, mitad - 1)  # Buscar en la mitad izquierda
    else:
        return -1  # Elemento no encontrado
```

Complejidad temporal: $O(\log n)$

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

## Implementación
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
