Definición de constantes

k = 0.45
T0 = 5 # Temperatura inicial de la lata (en ºC)
Ts = 40 # Temperatura ambiente (en ºC)

Función para calcular la temperatura en un tiempo t

def temperatura(t):
devuelve Ts + (T0 - Ts) * math.exp(-k * t)

Función para encontrar el tiempo necesario para estar a una diferencia de temperatura respecto al ambiente

def tiempo_para_diferencia(diferencia):
return -(1 / k) * math.log(diferencia / (T0 - Ts))

Rama 1: Calcular la temperatura en tiempos específicos

def rama_1():
tiempos = [1, 5, 12, 14] # Tiempos en horas
for t in tiempos:
T = temperatura(t)
print(f"La temperatura después de {t} horas es: {T:.2f }°C")

Rama 2: Calcular el tiempo necesario para estar a 0,5 ºC menos que la temperatura ambiente

def rama_2():
diferencia = 0.5 # Diferencia de temperatura respecto al ambiente (en ºC)
t = tiempo_para_diferencia(diferencia)
print(f"El tiempo necesario para estar a {diferencia} ºC menos que la temperatura ambiente es: {t:. 2f} horas")

Rama 3: Combinar ambas funcionalidades en una sola rama

def rama_3():
rama_1() # Calcular temperaturas en tiempos específicos
rama_2() # Calcular tiempo para diferencia de temperatura
