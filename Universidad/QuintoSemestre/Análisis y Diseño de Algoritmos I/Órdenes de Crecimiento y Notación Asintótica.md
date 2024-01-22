# Órdenes de Crecimiento
Los órdenes de crecimiento en computación se refieren a la manera en que se evalúa y describe la eficiencia de un [[Introducción#¿Qué es un algoritmo?|algoritmo]] en términos de su comportamiento en relación con el tamaño de la entrada.

![](https://i.imgur.com/5ThWMYS.png)

# Notación Asintótica
En el contexto del análisis de algoritmos y complejidad computacional, la notación asintótica, especialmente la notación Big O, se usa para describir el límite superior del crecimiento de una función en términos de otra función, principalmente cuando se trata del tamaño de la entrada.

Por ejemplo, si se tiene un algoritmo cuyo tiempo de ejecución está representado por una función $f(n)$, donde $n$ es el tamaño de la entrada, se puede expresar su complejidad usando la notación Big O para indicar cómo crece el tiempo de ejecución conforme $n$ se hace grande. Si este tiempo de ejecución se describe como $O(n^2)$, significa que el tiempo de ejecución del algoritmo no crecerá más rápido que cuadráticamente en función del tamaño de la entrada.

Algunas de las notaciones más utilizadas son:

1. **Notación Big O (O)**: Es la notación más común y representa el límite superior asintótico de una función. Se usa para describir la cota superior del crecimiento de una función en términos de otra función a medida que la variable tiende hacia un valor específico, generalmente hacia el infinito. Por ejemplo, si un algoritmo tiene una complejidad O(n^2), indica que el tiempo de ejecución crece a lo sumo cuadráticamente en relación con el tamaño de la entrada. 

   > [!tip]
   > La notación Big O tiene como objetivo encontrar el peor escenario posible, es decir, representa la complejidad máxima del algoritmo.

2. **Notación Theta (Θ)**: Representa el comportamiento ajustado o exacto de una función. Se usa para describir la relación asintótica entre dos funciones cuando estas están limitadas tanto superior como inferiormente por la misma función, dentro de un cierto factor constante. En resumen, Θ describe el crecimiento de una función de manera precisa. Por ejemplo, si un algoritmo tiene una complejidad Θ(n), indica que el tiempo de ejecución crece linealmente en relación con el tamaño de la entrada.
   
>[!tip]
>La notación Big Θ tiene como objetivo encontrar el escenario promedio, es decir, la complejidad esperable del algoritmo.

3. **Notación Omega (Ω)**: Es la contraparte de la notación Big O. Representa el límite inferior asintótico de una función. Se utiliza para describir el límite inferior del crecimiento de una función en términos de otra función a medida que la variable tiende hacia un valor específico, generalmente hacia el infinito. Por ejemplo, si un algoritmo tiene una complejidad Ω(n), indica que el tiempo de ejecución crece al menos linealmente en relación con el tamaño de la entrada.
   
   >[!tip]
   >La notación Big Ω tiene como objetivo encontrar el mejor escenario posible, es decir, representa la complejidad mínima del algoritmo.

Estas notaciones proporcionan diferentes perspectivas para analizar y describir el comportamiento de las funciones, lo que es fundamental en el análisis de algoritmos para entender su eficiencia en términos de tiempo y espacio.

Algunas complejidades comunes son:
- $O(1)$: Constante
- $O(log(n))$: Logarítmica
- $O(n)$: Lineal
- $O(n*log(n))$: Linealítmica
- $O(n^2)$: Cuadrática
- $O(2^n)$: Exponencial
- $O(n!)$: Factorial

# ¿Cómo se calcula Big O?
Para el cálculo de la complejidad de un algoritmo, podemos utilizar ciertas normas iniciales, las cuales especifican que las asignaciones, operaciones aritméticas y returns tienen un costo computacional de 1. Podemos, por ejemplo, calcular la complejidad de la siguiente función, la cual recibe como argumentos una lista *a* de enteros, un entero *n*, correspondiente al tamaño de la lista y un entero *z*, y finalmente devuelve si existe un par de elementos en *a* cuya suma sea igual a *z*:

```cpp
bool findPair(int a[], int n, int z)
{
    for (int i = 0; i < n; i++)
        for (int j = 0; j < n; j++)
            if (i != j && a[i] + a[j] == z)
                return true;

    return false;
}
```

En el cuerpo de la función podemos hallar, inicialmente, un bucle for, el cual realiza dos operaciones (comparar y asignar), dándole un costo 2, y se ejecuta n+1 veces, pues debe verificar n+1 veces la condición. Nuestra complejidad empezaría a verse así:

	$T_{sum} = 2*(n+1)$

No obstante, observamos la existencia de un bucle for anidado, lo que significa que se repetirá tanto dentro de sí mismo como dentro del bucle anterior, por lo que debemos modificar nuestra ecuación de la siguiente forma:

	$T_{sum} = (2*(n+1))^2$

Dentro del segundo bucle, podemos hallar una expresión if, la cual realiza una operación aritmética y dos comprobaciones, por lo que tiene un coste de 3. Adicionalmente, esta expresión if puede llegar a ejecutarse tantas veces como los bucles for, por lo cual:

	$T_{sum} = (2*(n+1))^2 + 3*n^2$

Finalmente, se retorna un valor. Es importante tener en cuenta que las expresiones return sólo se ejecutan una vez, por lo que su cálculo es sencillo:

	$T_{sum} = (2*(n+1))^2 + 3n^2 + 1$

Simplificamos la expresión:

	$T_{sum} = 7n^2 + 8n + 5$

En la notación Big O, prescindimos de los términos de orden inferior y las constantes, dejando únicamente el término dominante, por lo tanto, nuestra complejidad final sería expresada como:

	$O(n^2)$

>[!abstract] Resumen General
>Los órdenes de crecimiento y las notaciones asintóticas ayudan a describir cómo cambia la eficiencia de un algoritmo a medida que varía el tamaño de la entrada. La notación Big O, Theta y Omega se utilizan para establecer límites superiores, comportamientos ajustados/exactos y límites inferiores, respectivamente, del crecimiento de una función en relación con otra función a medida que la variable de entrada tiende hacia valores específicos, generalmente hacia el infinito.