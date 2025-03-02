
# Bitácora - Actividad 4: De algoritmo a código fuente

## 1. ¿Por qué crees que el pseudocódigo es útil antes de escribir un programa en C?

El pseudocódigo es útil porque nos permite organizar las ideas antes de preocuparnos por la sintaxis exacta de C. Así, primero nos enfocamos en la lógica y el orden de las operaciones, asegurando que el proceso sea claro. Después, traducirlo a C es mucho más fácil, porque ya tenemos una ruta definida. Además, el pseudocódigo es más fácil de entender para cualquier persona, incluso si no sabe programar.

---

## 2. Pseudocódigo - Calcular promedio de calificaciones

```
INICIO
    Leer cantidad de calificaciones
    suma = 0
    Para i desde 1 hasta cantidad
        Leer calificación
        suma = suma + calificación
    promedio = suma / cantidad
    Mostrar promedio
FIN
```

---

## 3. Traducción a C

```c
#include <stdio.h>

int main() {
    int cantidad;
    float calificacion, suma = 0, promedio;

    printf("¿Cuántas calificaciones vas a ingresar? ");
    scanf("%d", &cantidad);

    for (int i = 0; i < cantidad; i++) {
        printf("Ingresa la calificación %d: ", i+1);
        scanf("%f", &calificacion);
        suma += calificacion;
    }

    promedio = suma / cantidad;
    printf("El promedio es: %.2f\n", promedio);

    return 0;
}
```

---

## 4. ¿Por qué es importante declarar el tipo de variable antes de usarla en C?

En C, declarar el tipo de variable es obligatorio porque el compilador necesita saber cuánto espacio reservar en memoria y qué tipo de operaciones puede realizar. Si no declaramos correctamente el tipo, el programa puede fallar o arrojar resultados incorrectos.

---

## 5. ¿Por qué es importante comentar el código?

Comentar el código facilita entender el propósito de cada sección, tanto para nosotros mismos como para otros programadores. Además, refleja buena práctica y organización, lo cual es clave en entornos académicos y profesionales.

---

## 6. Reto Final - Traducción de pseudocódigos

### Ejercicio 1: Área de un rectángulo

```c
#include <stdio.h>

int main() {
    float base, altura, area;

    printf("Ingresa la base del rectángulo: ");
    scanf("%f", &base);

    printf("Ingresa la altura del rectángulo: ");
    scanf("%f", &altura);

    area = base * altura;

    printf("El área es: %.2f\n", area);
    return 0;
}
```

### Ejercicio 2: Par o impar

```c
#include <stdio.h>

int main() {
    int numero;

    printf("Ingresa un número: ");
    scanf("%d", &numero);

    if (numero % 2 == 0) {
        printf("Es par\n");
    } else {
        printf("Es impar\n");
    }
    return 0;
}
```

### Ejercicio 3: Mayor de edad

```c
#include <stdio.h>

int main() {
    int edad;

    printf("Ingresa tu edad: ");
    scanf("%d", &edad);

    if (edad >= 18) {
        printf("Eres mayor de edad\n");
    } else {
        printf("Eres menor de edad\n");
    }
    return 0;
}
```

### Ejercicio 4: Convertir grados Celsius a Fahrenheit

```c
#include <stdio.h>

int main() {
    float celsius, fahrenheit;

    printf("Ingresa la temperatura en grados Celsius: ");
    scanf("%f", &celsius);

    fahrenheit = celsius * 9.0 / 5.0 + 32;

    printf("Equivale a %.2f grados Fahrenheit\n", fahrenheit);
    return 0;
}
```

### Ejercicio 5: Promedio de tres números

```c
#include <stdio.h>

int main() {
    float num1, num2, num3, promedio;

    printf("Ingresa el primer número: ");
    scanf("%f", &num1);

    printf("Ingresa el segundo número: ");
    scanf("%f", &num2);

    printf("Ingresa el tercer número: ");
    scanf("%f", &num3);

    promedio = (num1 + num2 + num3) / 3;

    printf("El promedio es: %.2f\n", promedio);
    return 0;
}
```

---

## 7. Después de este tutorial, ¿qué puntos crees que deberías reforzar?

1. La sintaxis exacta de funciones y estructuras de control.
2. El manejo correcto de tipos de datos y operadores.
3. La forma correcta de declarar y usar variables dentro de ciclos y funciones.

Con más práctica, me sentiré más segura al traducir cualquier pseudocódigo a C.

---
