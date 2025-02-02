Rama 1: Versión básica

def generar_lista():
lista = []
for i in range(1, 101):
if i % 2 == 0:
lista.append(i ** 2) # Cuadrado de números pares
else:
lista.append(i ** 3) # Cubo de números impares
return lista

def sumar_hasta_limite(lista, limite):
suma = 0
contador = 0
for numero in lista:
if suma + numero >= limite:
break
suma += numero
contador += 1
return contador, suma

Generar la lista

lista = generar_lista()

Calcular cuántos números sumar para acercarse a un millón

limite = 1_000_000
contador, suma_total = sumar_hasta_limite(lista, limite)

print(f"Rama 1: Se deben sumar {contador} números para obtener una suma de {suma_total} (inferior a {limite}).")

Rama 2: Versión con listas por comprensión

def generar_lista():
return [i ** 2 si i % 2 == 0 de lo contrario i ** 3 para i en rango(1, 101)]

def sumar_hasta_limite(lista, limite):
suma = 0
for contador, numero in enumerate(lista):
if suma + numero >= limite:
return contador, suma
suma += numero
return contador, suma

Generar la lista

lista = generar_lista()

Calcular cuántos números sumar para acercarse a un millón

limite = 1_000_000
contador, suma_total = sumar_hasta_limite(lista, limite)

print(f"Rama 2: Se deben sumar {contador} números para obtener una suma de {suma_total} (inferior a {limite}).")

Rama 3: Versión con acumulación usando itertools

importar itertools

def generar_lista():
return [i ** 2 si i % 2 == 0 de lo contrario i ** 3 para i en rango(1, 101)]

def sumar_hasta_limite(lista, limite):
suma_acumulada = itertools.accumulate(lista)
for contador, suma in enumerate(suma_acumulada):
if suma >= limite:
return contador, suma - lista[contador]
return contador, suma

Generar la lista

lista = generar_lista()

Calcular cuántos números sumar para acercarse a un millón

limite = 1_000_000
contador, suma_total = sumar_hasta_limite(lista, limite)

print(f"Rama 3: Se deben sumar {contador} números para obtener una suma de {suma_total} (inferior a {limite}).")
