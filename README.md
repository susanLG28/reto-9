# reto-9
### 1. Desarrollar un algoritmo que calcule el promedio de un arreglo de reales.

 ``` python
# Función que calcula el promedio de los elementos de una lista
def calcular_promedio(lista):
    # Si la lista está vacía, se retorna 0 para evitar división por cero
    if len(lista) == 0:
        return 0
    
    # Calcula la suma total de los elementos
    suma = sum(lista)
    
    # Calcula el promedio dividiendo la suma entre la cantidad de elementos
    promedio = suma / len(lista)
    
    # Retorna el resultado del promedio
    return promedio

# Inicialización de una lista vacía para almacenar los números reales
lista = []

# Solicita al usuario cuántos números reales quiere ingresar
n = int(input("¿Cuántos números reales deseas ingresar? "))

# Bucle para ingresar cada número y agregarlos a la lista
for i in range(n):
    numero = float(input(f"Ingrese el número {i + 1}: "))  # Pide un número real
    lista.append(numero)  # Lo añade a la lista

# Llama a la función para calcular el promedio de la lista
promedio = calcular_promedio(lista)

# Imprime el resultado del promedio calculado
print("El promedio es:", promedio)

```

### 2. Desarrollar un algoritmo que calcule el producto punto de dos arreglos de números enteros (reales) de igual tamaño.

```python
def producto_punto(lista1, lista2):
    if len(lista1) != len(lista2):
        print("Error: las listas no tienen el mismo tamaño.")
        return None
    
    producto = 0
    for i in range(len(lista1)):
        producto += lista1[i] * lista2[i]
    
    return producto

# Crear las dos listas vacías
lista1 = []
lista2 = []

# Solicitar el tamaño de las listas
n = int(input("¿Cuántos elementos tendrán los arreglos? "))

# Llenar la primera lista
print("Ingrese los elementos del primer arreglo:")
for i in range(n):
    num = float(input(f"Elemento {i + 1}: "))
    lista1.append(num)

# Llenar la segunda lista
print("Ingrese los elementos del segundo arreglo:")
for i in range(n):
    num = float(input(f"Elemento {i + 1}: "))
    lista2.append(num)

# Calcular el producto punto
resultado = producto_punto(lista1, lista2)

# Mostrar el resultado
if resultado is not None:
    print("El producto punto es:", resultado)
```

### 3. Hacer un algoritmo que deje al final de un arreglo de números todos los ceros que aparezcan en dicho arreglo.

```python
def mover_ceros_al_final(lista):
    nueva_lista = []
    ceros = []

    for num in lista:
        if num == 0:
            ceros.append(num)        # Guarda los ceros aparte
        else:
            nueva_lista.append(num)  # Guarda los demás números

    return nueva_lista + ceros       # Junta los no ceros + ceros al final

# Entrada del usuario
lista = []
n = int(input("¿Cuántos elementos tendrá el arreglo? "))

for i in range(n):
    num = int(input(f"Ingrese el elemento {i + 1}: "))
    lista.append(num)

# Aplicar el algoritmo
resultado = mover_ceros_al_final(lista)

# Mostrar el resultado
print("Arreglo con ceros al final:", resultado)
```
