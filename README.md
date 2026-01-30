# Introduccion_a_la_programacion_con_Python_UNAL
Este repositorio contiene ejercicios y prácticas desarrolladas durante el curso
**Introducción a la Programación con Python** de la Universidad Nacional de Colombia.


## Objetivo
Fortalecer los fundamentos de programación en Python y desarrollar pensamiento lógico
aplicado a la resolución de problemas.

## herramientas
- Google colab
- Github
- UNcode (programa propio de la UNAL para la ejecución y calificación de codigos)

################# UNIDAD 1 ###################

## temas
1. # conversión de tipos

str:permite convertir valores al tipo de datos de texto (str).
int:permite convertir valores al tipo de dato entero (int).
float:permite convertir valores al tipo de dato decimal (float).
complex:permite convertir valores al tipo de dato complejo (complex).

Ejemplo 

# Valor original de tipo 'str'.
cadena = "52"

# Función 'int'
num = int(cadena)

# Vemos el contenido y el tipo de 'num'.
print(num)
type(num)

NOTA: En el caso de los números complejos la operación de conversión a entero o flotante NO está definida.

2. # Formato de valores númericos

- Dígitos decimales (f) 

La  (P) es la cantidad de dígitos decimales que queremos representar

{VALOR:f} | {VALOR:.Pf}

Ejemplo:
Calculamos la raíz de dos como 2 elevado a 1/2.
raiz = 2 ** 0.5

f"Raíz de 2: {raiz:.6f}"

- Notación científica (e) 

{VALOR:e} | {VALOR:.Pe}

Ejemplo:
num = 6.5734 * 10 ** 20

print(f"Valor en notación científica: {num:.2e}")    # Notación científica con dos dígitos decimales.

- Porcentaje (%)

{VALOR:%} | {VALOR:.P%}

Ejemplo:
porcentaje = 0.5274645641

print(f"Número en formato de porcentaje: {porcentaje:%}")

NOTA: También podemos elegir la cantidad de dígitos indicando el parámetro .P. No olvide que estos parámetros deberán ser indicados con el símbolo de punto .al inicio.

- Separador de millas (,)

valor:,

Ejemplo:
valor = 7785964164146454

print(f"Número con separador de miles: {valor:,}")

3. # tutor de phyton

herramienta para la visualización de la ejecución de código en Python y otros lenguajes. Para utilizarlo, debemos instalarlo y configurarlo con una celda como la siguiente:

!pip3 -q install tutormagic
%load_ext tutormagic

## EJERCICIO ##

##################################################
### 💻  Ejemplo: Ejercicios de física (I)  💻 ###
##################################################


# 1) Obtener de la entrada del programa los parámetros iniciales.


x0 = input()
v0 = input()
a = input()
t = input()


# 2) Convertir cada valor de texto obtenido de la entrada en un valor numérico decimal.

x0 = float(x0)
v0 = float(v0)
a = float(a)
t = float(t)

# 3) Utilizar los valores numéricos en una expresión matemática y obtener el valor de la posición final.


x = x0+v0*t+0.5*a*t**2


# 4) Reportar el resultado de la operación con dos dígitos decimales.

print(f"La posición final es {x:.2f} metros.")

## EJERCICIO 2##

##################################################
#### 💻 Tarea: Ejercicios de física (II)  💻 ####
##################################################

## 👇 Escriba su código DEBAJO de esta línea 👇 ##


# 1) Obtener de la entrada del programa los parámetros iniciales.
x0 = input()
v0 = input()
a = input()
t = input()

# 2) Convertir cada valor de texto obtenido de la entrada en un valor numérico decimal.
x0 = float(x0)        # m
v0 = float(v0)        # km/h
a = float(a)          # m/s^2
t = float(t)          # s

# 3) Realizar las operaciones matemáticas para las conversiones de unidad de medida necesarias.
# Convertir velocidad inicial de km/h a m/s
v0_ms = v0 / 3.6

# 4) Utilizar los valores numéricos en las expresiones matemáticas de cada ecuación y obtener el valor de:
# i. Posición final (m)
x = x0 + v0_ms * t + 0.5 * a * t**2

# ii. Velocidad final (m/s)
v_ms = v0_ms + a * t

# Convertir velocidad final a km/h
v = v_ms * 3.6

# 5) Reportar el resultado de la operación con el formato solicitado.
print(f"La posición final es de {x:.2f} m y la velocidad es de {v:.3f} km/h")


########### UNIDAD 2 ###################

### Estructuras de control condicionales con Python ###

1. Valores booleanos:  dato primitivo que representa el valor de verdad de una condición lógica

Verdadero si la condición SÍ se cumple.
Falso si la condición NO se cumple.

Estos valores pueden ser escritos como valores literales con las palabras reservadas True(para verdadero) y False(para falso)

s.islower(): Determina si la cadena está compuesta solo por caracteres en minúscula

# ¿La cadena 'hola' solo tiene caracteres en minúscula? -> VERDADERO
"hola".islower()

Otro ejemplo claro es identificar si un valor corresponde a un tipo de dato en particular, posible con la función isinstance:

# ¿El valor 500.5 es un valor de tipo entero (int)? -> FALSO
isinstance(500.5, int)

1.1 Operadores relacionales: la familia de operadores relacionales , con la cual podemos comparar dos o más valores, dando como resultado una expresión booleana 

# Los valores tienen que ser estrictamente iguales.
50.00000000 == 49.99999999

En ese sentido 'b'es menor que 'c', pues aparece antes en el alfabeto, pero es mayor que 'C', pues las mayúsculas están codificadas antes que las minúsculas.

# Los dígitos van antes que las mayúsculas, que van antes que las minúsculas.
'1' < 'B'

1.2 Operadores lógicos

¿Y si quisiéramos combinar valores booleanos para obtener expresiones booleanas que consideren varios valores?

Por ejemplo, imagine que está encargado de los pedidos de una empresa. Para despachar un pedido debe verificar que la cantidad de productos sea mayor que 0 (no tiene sentido despachar productos negativos o nulos) ya su vez que la cantidad del pedido sea menor que la cantidad de productos que se tienen en inventario.

con la formaA and B. Esta expresión se conoce como conjunción lógica (representada en matemáticas con el operador ) y solo se cumple si 𝐴 ∧ 𝐵  ambas condiciones se cumplen, es decir, si ambas expresiones tienen como valorTrue

# Ejemplo del pedido y el stock.
n_pedido = 4
n_inventario = 100

(n_pedido > 0) and (n_pedido <= n_inventario)

la condición 𝐴  O la condición , escrita en 𝐵  Python comoA or B. Esta expresión se conoce como disyunción lógica (representada en matemáticas con el operador ) y solo se cumple si yo ∨ yo  alguna de las condiciones se cumple.

# Ejemplo del registro con teléfono o email.

is_valid_email = False
is_valid_phone = True

is_valid_email or is_valid_phone

num == 5 or 6 or 7 # NO ES CORRECTO
El operador ordebe unir los resultados de las tres condiciones de igualdad, pues cada extremo del operador orespera una expresión booleana y recibe un valor numérico. 
num == 5 or num == 6 or num == 7

Finalmente, podemos realizar expresiones compuestas con los tres operadores lógicos con la ayuda de paréntesis y usar expresiones booleanas como las obtenidas al usar operadores relacionales:

a = 10
b = 5

a < b  or not (a == 0 or b == 0)

2. Sentencias de control condicional

2.1 Sentencia (if)

if CONDICIÓN:
  # <---- El bloque de código debe estar correctamente indentado.
  # <---- Por lo general se hace con el tabulador (o con 2 espacios en blanco).
  # Código que se ejecuta si la condición es VERDADERA.
  # ...
# Código que se ejecuta si la condición es FALSA o cuando
# termine de ejecutarse el código dentro de la estructura.



 














