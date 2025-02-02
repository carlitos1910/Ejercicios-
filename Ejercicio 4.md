def fibonacci(n):
    """Calcula el n-ésimo número de Fibonacci."""
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        a, b = 0, 1
        for _ in range(2, n + 1):
            a, b = b, a + b
        return b

def fibonacci_sequence(n):
    """Genera una lista de números de Fibonacci hasta n."""
    sequence = []
    for i in range(n):
        sequence.append(fibonacci(i))
    return sequence

def main():
    """Función principal para ejecutar el cálculo de la sucesión de Fibonacci."""
    n = int(input("Introduce el valor de n para calcular la sucesión de Fibonacci: "))
    fib_sequence = fibonacci_sequence(n)
    print(f"La sucesión de Fibonacci para n={n} es: {fib_sequence}")

if __name__ == "__main__":
    main()
