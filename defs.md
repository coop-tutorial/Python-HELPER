En Python, `def` se utiliza para definir una función. Una función es un bloque de código reutilizable que realiza una tarea específica. A continuación, te proporciono tres ejemplos de definiciones de funciones en Python, junto con una explicación detallada de cada parte del código:

**Ejemplo 1: Función simple sin argumentos ni valor de retorno**

```python
def saludar():
    print("Hola, mundo!")

# Llamamos a la función para ejecutarla
saludar()
```

- `def saludar():`: Aquí estamos definiendo una función llamada `saludar` sin argumentos. La declaración comienza con la palabra clave `def`, seguida del nombre de la función y paréntesis vacíos (sin argumentos). El colon `:` indica el inicio del bloque de código de la función.
- `print("Hola, mundo!")`: Este es el cuerpo de la función. La función imprime "Hola, mundo!" en la consola.

**Ejemplo 2: Función con argumentos y valor de retorno**

```python
def suma(a, b):
    resultado = a + b
    return resultado

# Llamamos a la función y almacenamos el resultado en una variable
resultado_suma = suma(5, 3)
print("La suma es:", resultado_suma)
```

- `def suma(a, b):`: Estamos definiendo una función llamada `suma` que toma dos argumentos, `a` y `b`.
- `resultado = a + b`: Dentro de la función, calculamos la suma de `a` y `b` y la almacenamos en una variable llamada `resultado`.
- `return resultado`: Devolvemos el valor calculado como resultado de la función.
- Al llamar a la función `suma(5, 3)`, el resultado de la suma se almacena en `resultado_suma` y se imprime.

**Ejemplo 3: Función con argumentos predeterminados**

```python
def saludar(nombre="usuario"):
    print(f"Hola, {nombre}!")

# Llamamos a la función con y sin argumentos
saludar()          # Imprime "Hola, usuario!"
saludar("Juan")    # Imprime "Hola, Juan!"
```

- `def saludar(nombre="usuario"):`: Estamos definiendo una función llamada `saludar` con un argumento `nombre` que tiene un valor predeterminado de "usuario". Esto significa que si no se proporciona un valor al llamar a la función, se utilizará "usuario" como valor predeterminado.
- `print(f"Hola, {nombre}!")`: La función imprime un saludo que incluye el nombre proporcionado o el valor predeterminado si no se proporciona un nombre.

Espero que estos ejemplos te ayuden a comprender cómo se definen y utilizan las funciones en Python.

```python
def saludar(nombre):
    print(f"Hola, {nombre}!")

# Solicitamos el nombre al usuario y luego llamamos a la función
nombre = input("Como te llamas? ")
saludar(nombre)
```

En este código:

1. Definimos la función `saludar` que toma un argumento `nombre`.
2. Luego, fuera de la función, solicitamos al usuario que ingrese su nombre utilizando `input` y almacenamos la entrada en la variable `nombre`.
3. Finalmente, llamamos a la función `saludar` pasando `nombre` como argumento para que la función imprima el saludo con el nombre proporcionado por el usuario.
## mas
Claro, aquí tienes más ejemplos de cómo usar `def` para definir funciones en Python:

**Ejemplo 4: Función con argumentos y sin valor de retorno**

```python
def suma(a, b):
    resultado = a + b

# Llamamos a la función
suma(5, 3)
```

- En este caso, definimos una función `suma` que toma dos argumentos, `a` y `b`. La función calcula la suma de estos números, pero no devuelve ningún valor (no hay `return`).
- Llamamos a la función con `suma(5, 3)`, y la suma se calcula dentro de la función, pero no se almacena ni se muestra en la consola.

**Ejemplo 5: Función con valor de retorno múltiple**

```python
def divide(a, b):
    cociente = a // b  # División entera
    residuo = a % b
    return cociente, residuo

# Llamamos a la función y almacenamos los valores de retorno en variables
resultado_cociente, resultado_residuo = divide(10, 3)
print("Cociente:", resultado_cociente)
print("Residuo:", resultado_residuo)
```

- En este ejemplo, definimos una función `divide` que toma dos argumentos, `a` y `b`. La función calcula tanto el cociente como el residuo de la división de `a` por `b` y los devuelve como una tupla.
- Llamamos a la función con `divide(10, 3)` y almacenamos los valores de retorno en las variables `resultado_cociente` y `resultado_residuo`, que luego imprimimos.

**Ejemplo 6: Función con recursión**

```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)

# Llamamos a la función para calcular el factorial de 5
resultado = factorial(5)
print("Factorial de 5:", resultado)
```

- En este ejemplo, definimos una función `factorial` que calcula el factorial de un número `n` utilizando recursión.
- La función verifica si `n` es igual a 0 y, si es así, devuelve 1 (caso base). Si no, calcula el factorial multiplicando `n` por el factorial de `n - 1`.
- Llamamos a la función con `factorial(5)` para calcular el factorial de 5 y lo almacenamos en `resultado`.

Estos ejemplos muestran diferentes formas de utilizar `def` para definir funciones en Python, desde funciones simples sin valor de retorno hasta funciones con argumentos y valor de retorno, e incluso funciones recursivas.
### Nivel Medio
aquí tienes ejemplos de funciones interactivas de nivel medio que interactúan con el usuario:

**Ejemplo 7: Calculadora simple**

```python
def calculadora():
    print("Selecciona una operación:")
    print("1. Suma")
    print("2. Resta")
    print("3. Multiplicación")
    print("4. División")
    
    opcion = input("Ingresa el número de la operación deseada: ")

    num1 = float(input("Ingresa el primer número: "))
    num2 = float(input("Ingresa el segundo número: "))

    if opcion == "1":
        resultado = num1 + num2
    elif opcion == "2":
        resultado = num1 - num2
    elif opcion == "3":
        resultado = num1 * num2
    elif opcion == "4":
        if num2 != 0:
            resultado = num1 / num2
        else:
            resultado = "Error: División por cero"
    else:
        resultado = "Opción no válida"

    print("Resultado:", resultado)

# Llamamos a la función para realizar cálculos
calculadora()
```

- En este ejemplo, la función `calculadora` interactúa con el usuario para realizar operaciones matemáticas básicas. La función solicita al usuario que seleccione una operación (suma, resta, multiplicación o división), ingrese dos números y luego realiza la operación deseada.

**Ejemplo 8: Conversor de temperatura**

```python
def conversor_temperatura():
    print("Selecciona una opción:")
    print("1. Convertir de Celsius a Fahrenheit")
    print("2. Convertir de Fahrenheit a Celsius")
    
    opcion = input("Ingresa el número de la opción: ")
    temperatura = float(input("Ingresa la temperatura: "))

    if opcion == "1":
        resultado = (temperatura * 9/5) + 32
    elif opcion == "2":
        resultado = (temperatura - 32) * 5/9
    else:
        resultado = "Opción no válida"

    print("Resultado:", resultado)

# Llamamos a la función para realizar conversiones de temperatura
conversor_temperatura()
```

- En este caso, la función `conversor_temperatura` permite al usuario convertir temperaturas entre Celsius y Fahrenheit.

**Ejemplo 9: Juego adivina el número**

```python
import random

def juego_adivina_numero():
    numero_secreto = random.randint(1, 100)
    intentos = 0

    print("Bienvenido al juego Adivina el número.")
    print("Estoy pensando en un número entre 1 y 100. ¡Adivina!")

    while True:
        intento = int(input("Ingresa tu suposición: "))
        intentos += 1

        if intento < numero_secreto:
            print("Demasiado bajo. Intenta de nuevo.")
        elif intento > numero_secreto:
            print("Demasiado alto. Intenta de nuevo.")
        else:
            print(f"Felicitaciones. ¡Adivinaste el número en {intentos} intentos!")
            break

# Llamamos a la función para jugar al juego Adivina el número
juego_adivina_numero()
```

- Este ejemplo implementa un juego interactivo en el que el usuario intenta adivinar un número secreto generado al azar por la computadora.

Estas funciones interactivas permiten a los usuarios realizar cálculos, conversiones o participar en juegos mientras interactúan con el programa.

### Avanzado
Aquí tienes ejemplos de funciones interactivas de nivel avanzado que permiten al usuario realizar tareas más complejas:

**Ejemplo 10: Administrador de tareas**

```python
def administrador_tareas():
    tareas = []
    
    while True:
        print("Opciones:")
        print("1. Agregar tarea")
        print("2. Ver tareas")
        print("3. Salir")
        
        opcion = input("Selecciona una opción: ")

        if opcion == "1":
            tarea = input("Ingresa la tarea: ")
            tareas.append(tarea)
        elif opcion == "2":
            print("Tareas:")
            for i, tarea in enumerate(tareas, start=1):
                print(f"{i}. {tarea}")
        elif opcion == "3":
            break
        else:
            print("Opción no válida. Inténtalo de nuevo.")

# Llamamos a la función para administrar tareas
administrador_tareas()
```

- En este ejemplo, la función `administrador_tareas` permite al usuario agregar, ver y gestionar tareas en una lista interactivamente.

**Ejemplo 11: Calculadora de hipotecas**

```python
def calculadora_hipoteca():
    principal = float(input("Monto del préstamo: $"))
    tasa_interes = float(input("Tasa de interés anual (%): "))
    plazo_anios = int(input("Plazo del préstamo (años): "))

    tasa_interes_mensual = (tasa_interes / 100) / 12
    plazo_meses = plazo_anios * 12

    cuota_mensual = (principal * tasa_interes_mensual) / (1 - (1 + tasa_interes_mensual) ** -plazo_meses)

    print(f"Cuota mensual: ${cuota_mensual:.2f}")

# Llamamos a la función para calcular una hipoteca
calculadora_hipoteca()
```

- En este caso, la función `calculadora_hipoteca` permite al usuario calcular la cuota mensual de una hipoteca en función del monto del préstamo, la tasa de interés y el plazo del préstamo.

**Ejemplo 12: Generador de contraseñas seguras**

```python
import random
import string

def generar_contrasena(longitud):
    caracteres = string.ascii_letters + string.digits + string.punctuation
    contrasena = ''.join(random.choice(caracteres) for _ in range(longitud))
    return contrasena

longitud_contrasena = int(input("Longitud de la contraseña: "))
contrasena_generada = generar_contrasena(longitud_contrasena)

print("Contraseña generada:", contrasena_generada)
```

- Esta función `generar_contrasena` crea contraseñas seguras de la longitud especificada por el usuario, combinando letras mayúsculas y minúsculas, dígitos y caracteres especiales.

Estas funciones avanzadas permiten al usuario realizar tareas más complejas, como administrar tareas, calcular hipotecas y generar contraseñas seguras, mientras interactúan con el programa.

### Extras

Las funciones de nivel profesional interactivo pueden involucrar tareas más complejas o procesamiento de datos. Aquí tienes tres ejemplos de funciones avanzadas que interactúan con el usuario:

**Ejemplo 13: Buscador de archivos en un directorio**

```python
import os

def buscar_archivos():
    ruta = input("Ingresa la ruta del directorio para buscar archivos: ")
    extension = input("Ingresa la extensión de archivo a buscar (por ejemplo, '.txt'): ")

    archivos_encontrados = []

    for directorio_raiz, directorios, archivos in os.walk(ruta):
        for archivo in archivos:
            if archivo.endswith(extension):
                archivos_encontrados.append(os.path.join(directorio_raiz, archivo))

    print("Archivos encontrados:")
    for archivo_encontrado in archivos_encontrados:
        print(archivo_encontrado)

# Llamamos a la función para buscar archivos en un directorio
buscar_archivos()
```

- Esta función permite al usuario especificar un directorio y una extensión de archivo, luego busca y muestra una lista de archivos en ese directorio que coinciden con la extensión especificada.

**Ejemplo 14: Análisis de datos con pandas**

```python
import pandas as pd

def analizar_datos_csv():
    archivo_csv = input("Ingresa la ruta del archivo CSV a analizar: ")

    try:
        df = pd.read_csv(archivo_csv)
        estadisticas = df.describe()
        print(estadisticas)
    except FileNotFoundError:
        print("Archivo no encontrado.")
    except Exception as e:
        print(f"Ocurrió un error: {e}")

# Llamamos a la función para analizar un archivo CSV con pandas
analizar_datos_csv()
```

- En este ejemplo, la función permite al usuario cargar un archivo CSV utilizando la biblioteca Pandas y muestra estadísticas descriptivas del conjunto de datos.

**Ejemplo 15: Envío de correos electrónicos**

```python
import smtplib
from email.mime.text import MIMEText
from email.mime.multipart import MIMEMultipart

def enviar_correo():
    remitente = input("Correo del remitente: ")
    contraseña = input("Contraseña del remitente: ")
    destinatario = input("Correo del destinatario: ")
    asunto = input("Asunto del correo: ")
    mensaje = input("Mensaje: ")

    try:
        servidor_smtp = smtplib.SMTP("smtp.servidor.com", 587)  # Reemplaza con el servidor SMTP correcto
        servidor_smtp.starttls()
        servidor_smtp.login(remitente, contraseña)

        mensaje_correo = MIMEMultipart()
        mensaje_correo["From"] = remitente
        mensaje_correo["To"] = destinatario
        mensaje_correo["Subject"] = asunto
        mensaje_correo.attach(MIMEText(mensaje, "plain"))

        servidor_smtp.sendmail(remitente, destinatario, mensaje_correo.as_string())
        servidor_smtp.quit()
        print("Correo enviado con éxito.")
    except Exception as e:
        print(f"Error al enviar el correo: {e}")

# Llamamos a la función para enviar un correo electrónico
enviar_correo()
```

- Este ejemplo permite al usuario enviar correos electrónicos utilizando la biblioteca `smtplib` de Python.

Estas funciones avanzadas interactúan con el usuario y realizan tareas más complejas, como buscar archivos, analizar datos y enviar correos electrónicos, lo que puede ser útil en aplicaciones profesionales y empresariales.
