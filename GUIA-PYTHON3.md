
1. `if`: La declaración `if` se usa para tomar decisiones en tu programa. Evalúa una expresión como verdadera o falsa y ejecuta un bloque de código si la expresión es verdadera. Por ejemplo:
   
   ```python
   edad = 18
   if edad >= 18:
       print("Eres mayor de edad")
   ```

2. `elif` (abreviatura de "else if"): Se utiliza cuando deseas evaluar múltiples condiciones en orden. Si la expresión de un `if` es falsa, se pasa a la siguiente expresión en un bloque `elif`. Si alguna de las expresiones es verdadera, se ejecutará el bloque de código asociado a esa expresión. Ejemplo:

   ```python
   nota = 75
   if nota >= 90:
       print("Aprobaste con A")
   elif nota >= 80:
       print("Aprobaste con B")
   elif nota >= 70:
       print("Aprobaste con C")
   else:
       print("Reprobaste")
   ```

3. `else`: La declaración `else` se utiliza para proporcionar un bloque de código que se ejecuta si ninguna de las expresiones `if` o `elif` anteriores es verdadera. Es una especie de caso predeterminado. Ejemplo:

   ```python
   numero = 5
   if numero > 0:
       print("El número es positivo")
   else:
       print("El número no es positivo")
   ```

Estas estructuras de control son fundamentales para tomar decisiones en tus programas Python y permiten que el flujo del programa se ajuste según las condiciones que establezcas.
