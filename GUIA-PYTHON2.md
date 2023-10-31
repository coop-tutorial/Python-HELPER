Para crear un menú con opciones dentro de submenús en Python, puedes seguir estos pasos:

**Paso 1: Importar biblioteces (si es necesario)**
Si tu aplicación necesita bibliotecas adicionales, asegúrate de importarlas al principio de tu script.

**Paso 2: Definir funciones para las opciones**
Crea funciones separadas para cada opción en tu menú y submenús. Cada función debe realizar la acción asociada a esa opción. Por ejemplo:

```python
def opcion1():
    print("Opción 1 seleccionada")
    # Aquí colocarías el código para realizar la opción 1

def opcion2():
    print("Opción 2 seleccionada")
    # Código para la opción 2

def subopcion1():
    print("Subopción 1 seleccionada")
    # Código para la subopción 1

def subopcion2():
    print("Subopción 2 seleccionada")
    # Código para la subopción 2
```

**Paso 3: Crear el menú principal**
Dentro de una función o un bucle, muestra el menú principal y permite al usuario seleccionar opciones. Puedes usar un bucle `while` para mantener el menú en funcionamiento hasta que el usuario decida salir:

```python
def menu_principal():
    while True:
        print("Menú Principal:")
        print("1. Opción 1")
        print("2. Opción 2")
        print("3. Submenú")
        print("4. Salir")
        
        opcion = input("Selecciona una opción: ")

        if opcion == "1":
            opcion1()
        elif opcion == "2":
            opcion2()
        elif opcion == "3":
            menu_sub()
        elif opcion == "4":
            print("Saliendo del programa.")
            break
        else:
            print("Opción no válida. Inténtalo de nuevo.")
```

**Paso 4: Crear submenús**
Si tienes submenús, crea funciones para ellos y repite el proceso del menú principal en cada submenú. Aquí hay un ejemplo de un submenú:

```python
def menu_sub():
    while True:
        print("Submenú:")
        print("1. Subopción 1")
        print("2. Subopción 2")
        print("3. Volver al menú principal")

        opcion = input("Selecciona una opción: ")

        if opcion == "1":
            subopcion1()
        elif opcion == "2":
            subopcion2()
        elif opcion == "3":
            print("Volviendo al menú principal.")
            break
        else:
            print("Opción no válida. Inténtalo de nuevo.")
```

**Paso 5: Ejecutar el menú principal**
Llama a la función del menú principal al final de tu script para iniciar la aplicación:

```python
if __name__ == "__main__":
    menu_principal()
```

Con estos pasos, has creado un menú con opciones y submenús en Python. El usuario puede navegar por las opciones y realizar acciones según su elección. Asegúrate de personalizar las opciones y las funciones según tus necesidades.

### Aquí tienes un ejemplo completo que incluye un menú principal con opciones y un submenú:

```python
def opcion1():
    print("Opción 1 seleccionada")
    # Código para la opción 1

def opcion2():
    print("Opción 2 seleccionada")
    # Código para la opción 2

def subopcion1():
    print("Subopción 1 seleccionada")
    # Código para la subopción 1

def subopcion2():
    print("Subopción 2 seleccionada")
    # Código para la subopción 2

def menu_principal():
    while True:
        print("Menú Principal:")
        print("1. Opción 1")
        print("2. Opción 2")
        print("3. Submenú")
        print("4. Salir")
        
        opcion = input("Selecciona una opción: ")

        if opcion == "1":
            opcion1()
        elif opcion == "2":
            opcion2()
        elif opcion == "3":
            menu_sub()
        elif opcion == "4":
            print("Saliendo del programa.")
            break
        else:
            print("Opción no válida. Inténtalo de nuevo.")

def menu_sub():
    while True:
        print("Submenú:")
        print("1. Subopción 1")
        print("2. Subopción 2")
        print("3. Volver al menú principal")

        opcion = input("Selecciona una opción: ")

        if opcion == "1":
            subopcion1()
        elif opcion == "2":
            subopcion2()
        elif opcion == "3":
            print("Volviendo al menú principal.")
            break
        else:
            print("Opción no válida. Inténtalo de nuevo.")

if __name__ == "__main__":
    menu_principal()
```

Este es un ejemplo completo de un programa en Python que tiene un menú principal con opciones y un submenú. El usuario puede seleccionar diferentes opciones y ejecutar acciones correspondientes en función de su elección. Asegúrate de personalizar el código y las funciones según tus necesidades.
