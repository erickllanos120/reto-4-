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

punto 3

Dado un carácter, construya un programa en Python para determinar si el carácter es un dígito o no.

punto 4

Realice un programa que lea dos números reales y determine si el primero es múltiplo del segundo.

punto 5

Dado un número real x, construya un programa que permita determinar si el número es positivo, negativo o cero. Para cada caso de debe imprimir el texto que se especifica a continuación:

Positivo: "El número x es positivo"
Negativo: "El número x es negativo"
Cero (0): "El número x es el neutro para la suma"

punto 6 

Dado el centro y el radio de un círculo, determinar si un punto de R2 pertenece o no al interior del círculo.

punto 7

Dadas tres longitudes positivas, determinar si con esas longitudes se puede construir un triángulo.

punto 8

Escriba un programa que reciba el nombre en minúsculas de un país de America y retorne la ciudad capital, si el país no pertenece al continente debe arrojar país no identificado (Utilice match-case).
