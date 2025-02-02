def obtener_resto(dni):
    """
    Calcula el resto de la división entera del número de DNI entre 23.
    """
    return dni % 23

def obtener_letra(resto):
    """
    Devuelve la letra correspondiente al resto calculado.
    """
    letras = "TRWAGMYFPDXBNJZSQVHLCKE"
    return letras[resto]

def main():
    """
    Función principal que solicita el número de DNI al usuario y muestra la letra correspondiente.
    """
    try:
        dni = int(input("Introduce tu número de DNI (sin letra): "))
        if dni < 0:
            print("El número de DNI no puede ser negativo.")
            return
        
        resto = obtener_resto(dni)
        letra = obtener_letra(resto)
        
        print(f"La letra correspondiente a tu DNI es: {letra}")
        print(f"Tu DNI completo sería: {dni}{letra}")
    
    except ValueError:
        print("Por favor, introduce un número válido.")

if __name__ == "__main__":
    main()
