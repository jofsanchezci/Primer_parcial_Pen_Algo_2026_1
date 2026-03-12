# Primer Parcial
- Resolver los siguiente ejericios. Siga las instrucciones de cada uno de los puntos. 
- El diseño de las soluciones deben ser como se indican en las secciones entradas y salidas.
- Envie por cada punto un archivo .py solo con el nuemero del punto. Ejemplo: punt_1.py, punto_2.py, etc.
- Solo para el punto 5 realice un diagrama de flujo.


# Problema 1: Resultado de un Partido de Baloncesto

En el baloncesto existen tres tipos de jugadas que otorgan puntos:

- Un **tiro de tres puntos**, que vale **3 puntos**.
- Un **tiro de dos puntos**, que vale **2 puntos**.
- Un **tiro libre**, que vale **1 punto**.

Usted acaba de observar un partido de baloncesto entre los equipos **Apples** y **Bananas**, y registró el número de jugadas exitosas de cada tipo para ambos equipos.

Su tarea consiste en **determinar el resultado del partido**: si el equipo **Apples ganó**, si **Bananas ganó**, o si el partido terminó **empatado**.

---

## Entrada

El programa recibe **seis líneas de entrada**.

Las **primeras tres líneas** corresponden al equipo **Apples**, y las **últimas tres líneas** corresponden al equipo **Bananas**.

1. La **primera línea** contiene el número de **tiros de tres puntos** exitosos del equipo **Apples**.
2. La **segunda línea** contiene el número de **tiros de dos puntos** exitosos del equipo **Apples**.
3. La **tercera línea** contiene el número de **tiros libres** exitosos (de un punto) del equipo **Apples**.

4. La **cuarta línea** contiene el número de **tiros de tres puntos** exitosos del equipo **Bananas**.
5. La **quinta línea** contiene el número de **tiros de dos puntos** exitosos del equipo **Bananas**.
6. La **sexta línea** contiene el número de **tiros libres** exitosos (de un punto) del equipo **Bananas**.

Cada valor de entrada es un **número entero entre 0 y 100**.

---

## Salida

El programa debe imprimir **un único carácter**:

- **A** si el equipo **Apples** obtuvo más puntos que **Bananas**.
- **B** si el equipo **Bananas** obtuvo más puntos que **Apples**.
- **T** si ambos equipos obtuvieron **la misma cantidad de puntos**.

---

## Cálculo de Puntos

Para calcular los puntos de cada equipo se utiliza la siguiente regla:

- Cada **tiro de tres puntos** suma **3 puntos**.
- Cada **tiro de dos puntos** suma **2 puntos**.
- Cada **tiro libre** suma **1 punto**.

# Problema 2: Llamada de Telemercadeo

## Descripción

En este problema asumiremos que los **números telefónicos tienen cuatro dígitos**.

Un número telefónico **pertenece a un telemercader (telemarketer)** si sus cuatro dígitos cumplen **todas** las siguientes condiciones:

* El **primer dígito** es **8 o 9**.
* El **cuarto dígito** es **8 o 9**.
* El **segundo y tercer dígito** son **iguales**.

Por ejemplo, el número **8119** pertenece a un telemercader porque:

* El primer dígito es **8**.
* El cuarto dígito es **9**.
* El segundo y tercer dígito son **iguales (1 y 1)**.

Su tarea es **determinar si un número telefónico pertenece a un telemercader** y decidir si **debemos contestar la llamada o ignorarla**.

---

## Entrada

El programa recibe **cuatro líneas de entrada**.

Cada línea contiene **un dígito del número telefónico**, en el siguiente orden:

1. La **primera línea** contiene el **primer dígito** del número.
2. La **segunda línea** contiene el **segundo dígito** del número.
3. La **tercera línea** contiene el **tercer dígito** del número.
4. La **cuarta línea** contiene el **cuarto dígito** del número.

Cada dígito es un **número entero entre 0 y 9**.

---

## Salida

* Si el número telefónico **pertenece a un telemercader**, el programa debe imprimir:

```
ignore
```

* En caso contrario, el programa debe imprimir:

```
answer
```

# Problema 3: Conteo de Palabras

Debes **contar el número de palabras** que aparecen en una línea de texto.

Para este problema, una **palabra** se define como **cualquier secuencia de letras minúsculas**.

Por ejemplo:

- `hello` es una palabra.
- También se consideran válidas secuencias como `bbaabbb`, aunque no sean palabras del inglés.

---

## Entrada

La entrada consiste en **una sola línea de texto**, que contiene:

- **letras minúsculas**
- **espacios**

Se garantiza que:

- Existe **exactamente un espacio entre cada par de palabras**.
- **No hay espacios antes de la primera palabra ni después de la última**.

La longitud máxima de la línea es **80 caracteres**.

---

## Salida

El programa debe imprimir **un único número entero**, que corresponde a:

**El número de palabras presentes en la línea de entrada.**

# Problema 4: Volumen de un Cono
Calcular el **volumen de un cono circular recto**.

---

## Entrada

La entrada consiste en **dos líneas de texto**:

1. La **primera línea** contiene un número entero **r**, que representa el **radio del cono**.
2. La **segunda línea** contiene un número entero **h**, que representa la **altura del cono**.

Se garantiza que:

* **1 ≤ r ≤ 100**
* **1 ≤ h ≤ 100**

Es decir, el valor mínimo de **r** y **h** es **1** y el valor máximo es **100**.

---

## Salida

El programa debe imprimir **el volumen del cono circular recto** cuyo radio es **r** y cuya altura es **h**.

La fórmula para calcular el volumen es:

$V=\frac{\pi r^2 h}{3}$

# Problema 5: Clasificación de Acceso a un Sistema

## Descripción

Una universidad está implementando un **sistema automático de acceso a sus laboratorios de computación**.

Cada estudiante puede ingresar al laboratorio dependiendo de tres condiciones:

1. **Si es estudiante activo.**
2. **Si tiene reserva de laboratorio.**
3. **Si llegó dentro del horario permitido.**

Las reglas de acceso son las siguientes:

* Si **no es estudiante activo**, el sistema debe **denegar el acceso** inmediatamente.
* Si **es estudiante activo**, entonces:

  * Si **tiene reserva**, se debe verificar el horario.

    * Si **llegó dentro del horario**, se **permite el acceso**.
    * Si **llegó fuera del horario**, el acceso es **denegado por horario**.
  * Si **no tiene reserva**, el acceso es **denegado por falta de reserva**.

El objetivo del programa es **determinar el resultado del intento de acceso al laboratorio**.

---

## Entrada

El programa recibe **tres líneas de entrada**:

1. La primera línea contiene un entero **E**

   * `1` si la persona **es estudiante activo**
   * `0` si **no lo es**

2. La segunda línea contiene un entero **R**

   * `1` si **tiene reserva de laboratorio**
   * `0` si **no tiene reserva**

3. La tercera línea contiene un entero **H**

   * `1` si **llegó dentro del horario permitido**
   * `0` si **llegó fuera del horario**

---

## Salida

El programa debe imprimir **uno de los siguientes mensajes**:

| Condición                                            | Salida              |
| ---------------------------------------------------- | ------------------- |
| No es estudiante activo                              | `acceso_denegado`   |
| Estudiante activo pero sin reserva                   | `reserva_requerida` |
| Estudiante activo con reserva pero fuera del horario | `fuera_de_horario`  |
| Estudiante activo con reserva y dentro del horario   | `acceso_permitido`  |

---

## Restricciones

* Todos los valores de entrada serán **0 o 1**.

