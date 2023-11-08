# Reto_11_ya_se_puso_visag

## Punto 1

Desarrolle un programa que permita realizar la suma/resta de matrices. El programa debe validar las condiciones necesarias para ejecutar la operación.


suma:

```

def ingresar_matriz(filas, columnas):
    matriz = []
    for i in range(filas):
        fila = []
        for j in range(columnas):
            num = int(input(f"Ingrese el valor de la matriz en la posición {i},{j}: "))
            fila.append(num)
        matriz.append(fila)
    return matriz

def sumar_matrices(matriz1, matriz2):
    filas = len(matriz1)
    columnas = len(matriz1[0])

    matriz_suma = []
    for i in range(filas):
        fila_suma = []
        for j in range(columnas):
            suma = matriz1[i][j] + matriz2[i][j]
            fila_suma.append(suma)
        matriz_suma.append(fila_suma)

    return matriz_suma

def mostrar_matriz(matriz):
    filas = len(matriz)
    columnas = len(matriz[0])

    for i in range(filas):
        for j in range(columnas):
            print(matriz[i][j], end=" ")
        print()


filas = int(input("Ingrese el número de filas de la matriz: "))
columnas = int(input("Ingrese el número de columnas de la matriz: "))

matriz1 = ingresar_matriz(filas, columnas)
matriz2 = ingresar_matriz(filas, columnas)

matriz_suma = sumar_matrices(matriz1, matriz2)

print("La matriz resultante de la suma es: ")
mostrar_matriz(matriz_suma)

```

Resta:

```

def ingresar_matriz(filas, columnas):
    matriz = []
    for i in range(filas):
        fila = []
        for j in range(columnas):
            num = int(input(f"Ingrese el valor de la matriz en la posición {i},{j}: "))
            fila.append(num)
        matriz.append(fila)
    return matriz

def resta_matrices(matriz1, matriz2):
    filas = len(matriz1)
    columnas = len(matriz1[0])

    matriz_resta = []
    for i in range(filas):
        fila_resta = []
        for j in range(columnas):
            suma = matriz1[i][j] - matriz2[i][j]
            fila_resta.append(suma)
        matriz_suma.append(fila_resta)

    return matriz_resta

def mostrar_matriz(matriz):
    filas = len(matriz)
    columnas = len(matriz[0])

    for i in range(filas):
        for j in range(columnas):
            print(matriz[i][j], end=" ")
        print()


filas = int(input("Ingrese el número de filas de la matriz: "))
columnas = int(input("Ingrese el número de columnas de la matriz: "))

matriz1 = ingresar_matriz(filas, columnas)
matriz2 = ingresar_matriz(filas, columnas)

matriz_suma = resta_matrices(matriz1, matriz2)

print("La matriz resultante de la suma es: ")
mostrar_matriz(matriz_resta)

```







## Punto 2

Desarrolle un programa que permita realizar el producto de matrices. El programa debe validar las condiciones necesarias para ejecutar la operación.

```

import numpy as np

def ingresar_matriz(filas, columnas):
    matriz = []
    for i in range(filas):
        fila = []
        for j in range(columnas):
            num = int(input(f"Ingrese el valor de la matriz en la posición {i},{j}: "))
            fila.append(num)
        matriz.append(fila)
    return matriz

def producto_matrices(matriz1, matriz2):
    try:
        matriz_producto = np.dot(matriz1, matriz2)
        return matriz_producto
    except ValueError:
        print("Las matrices no pueden ser multiplicadas")
        return None

def mostrar_matriz(matriz):
    filas = len(matriz)
    columnas = len(matriz[0])

    for i in range(filas):
        for j in range(columnas):
            print(matriz[i][j], end=" ")
        print()

# Programa principal
print("Ingrese el tamaño de las matrices: ")
filas = int(input("Ingrese el número de filas de la matriz: "))
columnas = int(input("Ingrese el número de columnas de la matriz: "))

matriz1 = ingresar_matriz(filas, columnas)
matriz2 = ingresar_matriz(filas, columnas)

matriz_producto = producto_matrices(matriz1, matriz2)

if matriz_producto is not None:
    print("La matriz resultante del producto es: ")
    mostrar_matriz(matriz_producto)

```




## Punto 3

Desarrolle un programa que permita obtener la matriz transpuesta de una matriz ingresada. El programa debe validar las condiciones necesarias para ejecutar la operación.

```
import numpy as np

def ingresar_matriz(filas, columnas):
    matriz = []
    for i in range(filas):
        fila = []
        for j in range(columnas):
            num = int(input(f"Ingrese el valor de la matriz en la posición {i},{j}: "))
            fila.append(num)
        matriz.append(fila)
    return matriz

def transpuesta_matriz(matriz):
    return np.transpose(matriz)

def mostrar_matriz(matriz):
    filas = len(matriz)
    columnas = len(matriz[0])

    for i in range(filas):
        for j in range(columnas):
            print(matriz[i][j], end=" ")
        print()


print("Ingrese el tamaño de las matrices: ")
filas = int(input("Ingrese el número de filas de la matriz: "))
columnas = int(input("Ingrese el número de columnas de la matriz: "))

matriz = ingresar_matriz(filas, columnas)

print("La matriz transpuesta es: ")
mostrar_matriz(transpuesta_matriz(matriz))

```






## Punto 4

Desarrollar un programa que sume los elementos de una columna dada de una matriz.

```
import numpy as np

def ingresar_matriz(filas, columnas):
    matriz = []
    for i in range(filas):
        fila = []
        for j in range(columnas):
            num = int(input(f"Ingrese el valor de la matriz en la posición {i},{j}: "))
            fila.append(num)
        matriz.append(fila)
    return matriz

def transpuesta_matriz(matriz):
    return np.transpose(matriz)

def sumar_columna(matriz, columna):
    suma = 0
    for fila in matriz:
        suma += fila[columna]
    return suma


print("Ingrese el tamaño de las matrices: ")
filas = int(input("Ingrese el número de filas de la matriz: "))
columnas = int(input("Ingrese el número de columnas de la matriz: "))

matriz = ingresar_matriz(filas, columnas)

columna = int(input("Ingrese el número de la columna a sumar: "))
suma = sumar_columna(matriz, columna)

print(f"La suma de la columna {columna} es: {suma}")

```





## Punto 5

Desarrollar un programa que sume los elementos de una fila dada de una matriz

