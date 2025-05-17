# reto-4-
punto 1

Dado un número entero, determinar si ese número corresponde al código ASCII de una vocal minúscula.
segun  el ascii los valores de las vocales son las siguientes

a=97
e=101
i=105
o=111
u=117

entonces el numero debe ser alguno de esos

    def es_vocal_ascii(n):
      return n in [91, 101, 105, 111, 117]

    numero= int(input("ingrese un numero entero:"))
    if es_vocal_ascii(numero):
        print("corresponde al codigo ascii de una vocal en minuscula.")
    else:
        print("no corresponde al codigo ascii de una vocal en minuscula.")
        

punto 2

Dada una cadena de longitud 1, determine si el código ASCII de primera letra de la cadena es par o no.
 
        def es_digito(caracter):
    if len(caracter) != 1:
        return "Debes ingresar solo un carácter."
    
    if caracter.isdigit():
        return f"'{caracter}' es un dígito."
    else:
        return f"'{caracter}' NO es un dígito."
        
    entrada = input("Ingresa un solo carácter: ")
    resultado = es_digito(entrada)
    print(resultado)

punto 3

Dado un carácter, construya un programa en Python para determinar si el carácter es un dígito o no.

    def ascii_par_o_impar(caracter):
    if len(caracter) != 1:
        return "La cadena debe tener solo un carácter."
    
    codigo_ascii = ord(caracter)  # Obtener código ASCII
    if codigo_ascii % 2 == 0:
        return f"El código ASCII de '{caracter}' es {codigo_ascii} y es PAR."
    else:
        return f"El código ASCII de '{caracter}' es {codigo_ascii} y es IMPAR."
    entrada = input("Ingresa un solo carácter: ")
    resultado = ascii_par_o_impar(entrada)
    print(resultado)

punto 4

Realice un programa que lea dos números reales y determine si el primero es múltiplo del segundo.

        def es_multiplo(a, b):
    if b == 0:
        return "No se puede dividir por cero."
    
    if abs(a % b) < 1e-9:
        return f"{a} es múltiplo de {b}."
    else:
        return f"{a} NO es múltiplo de {b}."

    try:
    num1 = float(input("Ingrese el primer número real: "))
    num2 = float(input("Ingrese el segundo número real: "))
    resultado = es_multiplo(num1, num2)
    print(resultado)
    except ValueError:
    print("Debes ingresar números válidos.")
  

punto 5

Dado un número real x, construya un programa que permita determinar si el número es positivo, negativo o cero. Para cada caso de debe imprimir el texto que se especifica a continuación:

Positivo: "El número x es positivo"
Negativo: "El número x es negativo"
Cero (0): "El número x es el neutro para la suma"

    try:
    x = float(input("Ingrese un número real: "))

    if x > 0:
        print(f"El número {x} es positivo")
    elif x < 0:
        print(f"El número {x} es negativo")
    else:
        print(f"El número {x} es el neutro para la suma")
    except ValueError:
    print("Entrada inválida. Debes ingresar un número real.")

punto 6 

Dado el centro y el radio de un círculo, determinar si un punto de R2 pertenece o no al interior del círculo.

    import math

    try:
    # Entrada de datos
    h = float(input("Ingrese la coordenada x del centro del círculo: "))
    k = float(input("Ingrese la coordenada y del centro del círculo: "))
    r = float(input("Ingrese el radio del círculo: "))
    x = float(input("Ingrese la coordenada x del punto: "))
    y = float(input("Ingrese la coordenada y del punto: "))

  
    distancia = math.sqrt((x - h)**2 + (y - k)**2)

    
    if distancia < r:
        print("El punto está en el interior del círculo.")
    elif distancia == r:
        print("El punto está en la frontera del círculo.")
    else:
        print("El punto está fuera del círculo.")
    except ValueError:
    print("Entrada inválida. Por favor, ingresa solo números reales.")

punto 7

Dadas tres longitudes positivas, determinar si con esas longitudes se puede construir un triángulo.

    def es_triangulo(a, b, c):
    if a <= 0 or b <= 0 or c <= 0:
        return "Las longitudes deben ser positivas."
    
    if (a + b > c) and (a + c > b) and (b + c > a):
        return "Se puede construir un triángulo con esas longitudes."
    else:
        return "NO se puede construir un triángulo con esas longitudes."

    try:
    a = float(input("Ingrese la primera longitud: "))
    b = float(input("Ingrese la segunda longitud: "))
    c = float(input("Ingrese la tercera longitud: "))

    resultado = es_triangulo(a, b, c)
    print(resultado)

    except ValueError:
    print("Entrada inválida. Debes ingresar solo números reales positivos.")

punto 8

Escriba un programa que reciba el nombre en minúsculas de un país de America y retorne la ciudad capital, si el país no pertenece al continente debe arrojar país no identificado (Utilice match-case).

        pais = input("Ingrese el nombre de un país de América (en minúsculas): ").strip()

    match pais:
    case "colombia":
        print("Bogotá")
    case "argentina":
        print("Buenos Aires")
    case "brasil":
        print("Brasilia")
    case "chile":
        print("Santiago")
    case "canadá":
        print("Ottawa")
    case "méxico":
        print("Ciudad de México")
    case "perú":
        print("Lima")
    case "estados unidos":
        print("Washington D.C.")
    case "ecuador":
        print("Quito")
    case "venezuela":
        print("Caracas")
    case "uruguay":
        print("Montevideo")
    case "paraguay":
        print("Asunción")
    case "bolivia":
        print("La Paz y Sucre")
    case "panamá":
        print("Ciudad de Panamá")
    case "costa rica":
        print("San José")
    case "cuba":
        print("La Habana")
    case _:
        print("país no identificado")
