def fibonacci(n):
    """Calcule les n premiers termes de la suite de Fibonacci"""
    a, b = 0, 1
    for _ in range(n):
        print(a, end=' ')
        a, b = b, a + b
    print()

def est_premier(num):
    """Vérifie si un nombre est premier"""
    if num < 2:
        return False
    for i in range(2, int(num**0.5) + 1):
        if num % i == 0:
            return False
    return True

# Exemple d'utilisation
print("Suite de Fibonacci (10 premiers termes):")
fibonacci(10)

print("\nVérification des nombres premiers entre 1 et 20:")
for num in range(1, 21):
    if est_premier(num):
        print(f"{num} est premier"