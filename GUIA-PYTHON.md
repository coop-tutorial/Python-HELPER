 cómo usar `input` en Python y cómo agregar color al texto y al banner utilizando la biblioteca `colorama` en un script:

**Paso 1: Instala colorama**
Si aún no has instalado `colorama`, asegúrate de hacerlo utilizando `pip`:

```bash
pip install colorama
```

**Paso 2: Crea un script de Python**

Crea un nuevo archivo de script en Python, por ejemplo, "edad.py".

**Paso 3: Importa las bibliotecas necesarias**

Al comienzo de tu script, importa las bibliotecas `colorama` y `init`:

```python
from colorama import Fore, Back, Style, init
```

Luego, inicializa `colorama`:

```python
init(autoreset=True)
```

**Paso 4: Crea el banner con color**

Agrega el banner con el color deseado antes de solicitar la entrada del usuario:

```python
print(Fore.GREEN + Back.BLACK + "Calculando edades")
```

Puedes cambiar `Fore.GREEN` y `Back.BLACK` a los colores de tu elección.

**Paso 5: Solicita la entrada del usuario**

Solicita la entrada del usuario utilizando `input` y almacena el valor en una variable:

```python
tu_edad = int(input("Ingresa tu edad: "))
```

Este código solicita la edad y la convierte en un número entero.

**Paso 6: Realiza la verificación y muestra el resultado**

Usa una estructura condicional para verificar si el usuario es mayor de edad:

```python
if tu_edad >= 18:
    print("Eres mayor de edad.")
else:
    print("No eres mayor de edad.")
```

**Paso 7: Ejecuta el script**

Guarda el archivo y ejecuta el script desde tu terminal:

```bash
python edad.py
```

El usuario verá el banner con color y podrá ingresar su edad. El programa mostrará si es mayor o menor de edad según la entrada.

¡Así es como puedes usar `input` en Python y agregar color al texto y al banner en tu script utilizando `colorama`!
