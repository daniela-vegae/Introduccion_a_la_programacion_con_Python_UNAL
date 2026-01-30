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









