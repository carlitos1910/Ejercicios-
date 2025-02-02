Rama 1
def desglose_basico(cantidad):
billetes_monedas = [500, 200, 100, 50, 20, 10, 5, 2, 1]
desglose = {}

for valor in billetes_monedas:
    if cantidad >= valor:
        desglose[valor] = cantidad // valor
        cantidad = cantidad % valor

return desglose
def main():
try:
cantidad = int(input("Introduce una cantidad entera de euros: "))
if cantidad < 0:
print("La cantidad debe ser un número entero positivo.")
return

    resultado = desglose_basico(cantidad)
    print("Desglose en billetes y monedas:")
    for valor, cantidad in resultado.items():
        print(f"{cantidad} x {valor} euros")

except ValueError:
    print("Por favor, introduce un número entero válido.")
si nombre == " principal ":
principal()

def desglose_mejorado(cantidad):
billetes_monedas = [500, 200, 100, 50, 20, 10, 5, 2, 1]
desglose = {}

for valor in billetes_monedas:
    if cantidad >= valor:
        desglose[valor] = cantidad // valor
        cantidad = cantidad % valor

return desglose
def obtener_cantidad():
while True:
try:
cantidad = int(input("Introduce una cantidad entera de euros: "))
if cantidad < 0:
print("La cantidad debe ser un número entero positivo.")
else:
return cantidad
excepto ValueError:
print("Por favor, introduzca un número entero válido.")
Rama 2
def main():
cantidad = obtener_cantidad()
resultado = desglose_mejorado(cantidad)
print("Desglose en billetes y monedas:")
for valor, cantidad in resultado.items():
print(f"{cantidad} x {valor} euros ")

si nombre == " principal ":
principal()

def desglose_formateado(cantidad):
billetes_monedas = [500, 200, 100, 50, 20, 10, 5, 2, 1]
desglose = {}

for valor in billetes_monedas:
    if cantidad >= valor:
        desglose[valor] = cantidad // valor
        cantidad = cantidad % valor

return desglose
def obtener_cantidad():
while True:
try:
cantidad = int(input("Introduce una cantidad entera de euros: "))
if cantidad < 0:
print("La cantidad debe ser un número entero positivo.")
else:
return cantidad
excepto ValueError:
print("Por favor, introduzca un número entero válido.")
Rama 3
def main():
cantidad = obtener_cantidad()
resultado = desglose_formateado(cantidad)
print("Desglose en billetes y monedas:")
for valor, cantidad in resultado.items():
if valor >= 5:
print(f"{cantidad } billete(s) de {valor} euros")
else:
print(f"{cantidad} moneda(s) de {valor} euro(s)")

si nombre == " principal ":
principal()
