# 📍SOLUCIÓN DE RETOS CON SEUDOCODIGO

## Tabla de Contenido
- [1. La Distancia de Dos Puntos en el Plano Cartesiano](#1-la-distancia-de-dos-puntos-en-el-plano-cartesiano)
- [2. Una Modista y las Telas del Extranjeros](#2-una-modista-y-las-telas-del-extranjeros)
- [3. La Hipotenusa del Triángulo Rectángulo](#3-la-hipotenusa-del-triangulo-rectangulo)
- [4. La Edad Actual de una Persona con Su Nacimiento y Cumpleaños](#4-la-edad-actual-de-una-persona-con-su-nacimiento-y-cumpleaños)
- [5. Cuánto es el Sueldo del Trabajador](#5-cuanto-es-el-sueldo-del-trabajador)
- [6. Determinar N Cantidades de Cero](#6-determinar-n-cantidades-de-cero)
- [7. Los Ahorros Diarios y Anuales](#7-los-ahorros-diarios-y-anuales)
- [8. Los Artículos en Descuento](#8-los-articulos-en-descuento)
- [9. La Función Exponencial](#9-la-funcion-exponencial)
- [10. El Seno de un Ángulo](#10-el-seno-de-un-angulo)
- [📊 Tabla de Análisis de los Ejercicios](#-tabla-de-analisis-de-los-ejercicios-con-seudocodigo)

## 1. La Distancia de Dos Puntos en el Plano Cartesiano

    Inicio 
        insertar ("inserta los puntos de las coordenadas");

        leer x1, y1;

        leer x2, y2;

        hacer D = sqrt((x2-x1)^2 + (y2 - y1)^2);

        imprimir ("la distancia de coordenadas es %d", D);
    Fin

## 2. Una Modista y las Telas del Extranjeros

    Inicio 
        Insertar ("inserte las medidas en metro de la tela por favor");

        leer mm; `// mm = medidas en metros`

        hacer mp= mm/0,0254m ; `// mp = medidas en pulgadas`

        imprimir("Las medidas en pulgadas son %d", mp);

    Fin

## 3. La Hipotenusa del Triangulo Rectangulo 
    Inicio
        insertar ("inserte el cateto opuesto (co) y el cateto adyacente (ca), por favor");
        
        leer ca, co;

        hacer h = sqrt(ca^2 + co^2);

        imprimir ("La hipotenusa es %d", h);
    
    fin

## 4. La Edad Actual de una Persona con Su Nacimiento y Cumpleaños
    Inicio
        insertar ("escriba su fecha de nacimiento (f_nac) y la fecha actual de hoy (f_act)");

        leer d_n, m_n, a_n; //f_nac

        leer d_a, m_a, a_a; //f_act

        hacer ed_act = a_a - a_n;

        si m_n < m_a
            imprimir ("ya cumpliste y tienes %d", ed_act);
        
        si no 
            si m_n = m_a
                si d_n < d_a
                    imprimir ("ya cumpliste años y tienes %d", ed_act);
                si no
                    si d_n = d_a
                        imprimir ("hoy es tu cumpleaños felices %d", ed_act);
                    si no 
                        hacer e_r = ed_act - 1;

                        imprimir ("aún falta para tu cumple, actualmente tienes %d", e_r);
    Fin 

## 5. Cuanto es el Sueldo del Trabajador

    Inicio 
        Insertar("Cuantas fueron las horas trabajadas y cuanto es el pago por hora");

        leer h_t; `//h_t = horas trabajadas`

        leer p_h; `// p_h = pago por horas`

            si h_t  <= 40
            
             hacer p_t = h_t * p_h;
             imprimir ("tu salario de este mes es %d", p_t);

            si no
                si h_t <= 45

                    p_t = (40 * p_h) + (h_t - 40) * 2 * p_h;

                    imprimir ("tu pago total este mes es de %d", p_t);
                
                si no 
                    si h_t <= 50
                        hacer p_t = (40 * p_h) + (5 * 2 * p_h) + ((h_t - 45) * 3 * p_h);
                        imprimir ("tu pago total este mes es de %d", p_t);
                    si no 
                        imprimir("trabajaste más de las horas permitidas, habla con administración");
    Fin

## 6. Determinar N Cantidades de Cero
    Inicio
        insertar("¿Cuántas cantidades deseas analizar?")
        leer cantidades

        hacer ceros = 0
        hacer menores = 0
        hacer mayores = 0

        para i = 1 hasta cantidades hacer
            insertar("Escribe el valor de la cantidad %d:", i)
            leer valor

            si valor = 0 entonces
                hacer ceros = ceros + 1
            si no
                si valor < 0 entonces
                    hacer menores = menores + 1
                si no
                    hacer mayores = mayores + 1
                fin si
            fin si
        fin para

        imprimir("De las %d cantidades:", cantidades)
        imprimir("Ceros: %d", ceros)
        imprimir("Menores a cero: %d", menores)
        imprimir("Mayores a cero: %d", mayores)
    Fin
## 7. Los Ahorros Diarios y Anuales
    Inicio
        insertar("¿Cuántos centavos deseas ahorrar el primer día? Escribe la cantidad:");

        leer ahorro_dia; 
        hacer ahorro_anual = 0; 
    
        para dia = 1 hasta 365 hacer
            hacer ahorro_anual = ahorro_anual + ahorro_dia;
            hacer ahorro_dia = ahorro_dia * 3; // Cada día se triplica el ahorro
        fin para

        imprimir("El total ahorrado en el año es %d centavos", ahorro_anual);
    Fin

## 8. Los Articulos en Descuento
    Inicio
        insertar("¿Cuántos productos vas a llevar hoy? Escríbelo aquí:");

        leer articulos; // Total de artículos

        hacer total_pagar = 0; // Acumulador para el pago final

        para item = 1 hasta articulos
            insertar("Escribe el precio del producto %d:", item);
            leer precio;

            si precio >= 200
            hacer descuento = precio * 0.15;
            si no
                si precio > 100 y precio < 200
                    hacer descuento = precio * 0.12;
                si no
                    hacer descuento = precio * 0.10;

            hacer precio_final = precio - descuento;
            imprimir("El producto %d costaba $%0.2f y tuvo un descuento de $%0.2f. Ahora cuesta $%0.2f", item, precio, descuento, precio_final);

            hacer total_pagar = total_pagar + precio_final;

        imprimir("El total a pagar por los %d productos es de $%0.2f", articulos, total_pagar);
    Fin
## 9. La Función Exponencial
   Inicio
        insertar("Ingrese el valor de x");
        leer x;

            insertar("Escriba la cantidad de términos que desea calcular");
        leer términos;

        hacer e^x = 1.0;
        hacer termino = 1.0;

        para i = 1 hasta términos hacer
            hacer termino = termino * x / i;
            hacer e^x = e^x + termino;
        fin para

        imprimir("El valor aproximado de e^x es %.5f", e^x);
    Fin

## 10. El Seno de un Angulo 
    Inicio
        insertar("Escribe el valor del ángulo en radianes:");

        leer x;

        hacer termino = x;
        hacer seno = x;
        hacer signo = -1;

        para i = 3 hasta 15 con incremento de 2 hacer
            hacer termino = (termino * x * x) / (i * (i-1));
            hacer seno = seno + (signo * termino);
            hacer signo = signo * -1;
        fin para

        imprimir("El seno del ángulo es aproximadamente %f", seno);
    Fin

## TABLA DE ANALISIS DE LOS EJERCICIOS CON SEUDOCODIGO
| Ejercicio | Variables de Entrada | Variables de Salida | Variables Internas | Operaciones Realizadas |
|---|---|---|---|---|
| 1. Distancia entre 2 puntos | x1, y1, x2, y2 | D | - | D = sqrt((x2-x1)^2 + (y2-y1)^2) |
| 2. Modista y tela extranjera | mm (metros) | mp (pulgadas) | - | mp = mm / 0.0254 |
| 3. Hipotenusa del triángulo | ca (cateto adyacente), co (cateto opuesto) | h (hipotenusa) | - | h = sqrt(ca^2 + co^2) |
| 4. Edad actual | d_n, m_n, a_n (nacimiento) y d_a, m_a, a_a (actual) | ed_act o e_r | - | ed_act = a_a - a_n; validaciones de mes y día |
| 5. Sueldo del trabajador | h_t (horas trabajadas), p_h (pago por hora) | p_t (pago total) | - | Cálculos según rango de horas (≤40, ≤45, ≤50) |
| 6. Cantidades y ceros | cantidades, valor (por cada cantidad) | ceros, menores, mayores | i (contador) | Contar valores según sean cero, negativos o positivos |
| 7. Ahorros diarios y anuales | ahorro_dia (primer día) | ahorro_anual | dia | ahorro_dia se triplica cada día y se acumula |
| 8. Artículos en descuento | artículos, precio (por cada uno) | total_pagar | descuento, precio_final, item (contador) | Aplicar descuento según precio y acumular el total |
| 9. Función exponencial | x, términos (número de términos) | e^x | término, i | Serie de Taylor para e^x |
| 10. Seno de un ángulo | x (radianes) | seno | término, signo, i | Serie de Taylor para seno(x) |





