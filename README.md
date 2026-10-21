
[![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=l23212178-sys/MSFP2)

# Práctica 2: Modelado y control del sistema cardiovascular mediante el modelo Windkessel

## Información del estudiante

Osmar Ediel Armenta Medina \[23212178]; l23212178@tectijuana.edu.mx

Modelado de Sistemas Fisiológicos

Ingeniería Biomédica

## Docente

Dr. Paul Antonio Valle Trujillo; paul.valle@tectijuana.edu.mx

Departamento de Ingeniería Eléctrica y Electrónica, Tecnológico Nacional de México/IT Tijuana, Blvd. Alberto Limón Padilla s/n, Tijuana, C.P. 22454, B.C., México.

## Descripción de la asignatura

El modelado de sistemas fisiológicos permite representar y analizar matemáticamente el comportamiento de procesos biológicos, así como estudiar su respuesta ante diferentes condiciones y estrategias de control. En Ingeniería Biomédica, estas herramientas relacionan los principios de los circuitos eléctricos, las ecuaciones diferenciales y el control clásico con el funcionamiento de los sistemas del cuerpo humano.

En esta práctica se aplica el modelo Windkessel de cuatro elementos para describir la dinámica del sistema cardiovascular mediante una analogía entre presión arterial y voltaje, y entre flujo sanguíneo y corriente eléctrica. Se utilizan MATLAB, Simulink, Simscape Electrical y Python para comparar las respuestas de tres condiciones cardiovasculares y evaluar controladores PID mediante simulaciones in silico.

## Objetivos

1. Cuaderno computacional de MATLAB y su versión exportada [.mlx y .pdf].
2. Modelo de Simulink [.slx].
3. Código desarrollado en Python [.py].
4. Señal de entrada utilizada en las simulaciones [.xlsx].
5. Análisis matemático: ecuaciones, función de transferencia, polos, estabilidad y error en estado estacionario [.pdf].
6. Figuras de las simulaciones de los casos normotenso, hipotenso e hipertenso en MATLAB y Python [.pdf].
7. Capturas de los parámetros y las respuestas de los controladores PID para los casos hipotenso e hipertenso [.png].
8. Diagrama biológico del sistema cardiovascular y su relación con el modelo Windkessel [.jpeg].

## Descripción detallada del sistema

El modelo Windkessel de cuatro elementos representa el comportamiento dinámico del sistema arterial mediante un circuito eléctrico equivalente. La impedancia característica Z describe la oposición al flujo en la región proximal de las arterias, la capacitancia C representa la distensibilidad arterial, la resistencia R representa la resistencia periférica y la inductancia L modela los efectos inerciales de la sangre en movimiento.

El sistema es de segundo orden, debido a que contiene dos elementos independientes de almacenamiento de energía, C y L. La presión arterial Pa(t) se considera la entrada y la presión Pp(t) sobre la distensibilidad arterial se utiliza como salida. Las variables de estado son FL(t) y Pp(t).

Se analizan tres condiciones cardiovasculares: hipotensa, normotensa e hipertensa. La condición normotensa se utiliza como referencia, mientras que los otros dos modelos representan los casos que se desean controlar. Los parámetros Z, L y R permanecen constantes y únicamente cambia la distensibilidad arterial C.

| Parámetro | Hipotenso | Normotenso | Hipertenso | Unidades |
|---|---:|---:|---:|---|
| Z | 0.010 | 0.010 | 0.010 | mmHg·s/ml |
| L | 0.001 | 0.001 | 0.001 | mmHg·s²/ml |
| R | 1.000 | 1.000 | 1.000 | mmHg·s/ml |
| C | 3.500 | 1.500 | 1.000 | ml/mmHg |

Para comparar los modelos se utiliza una misma señal de excitación aleatoria en el intervalo de 0 a 15 segundos. Posteriormente, se implementan dos sistemas de control independientes con controladores PID, uno para el caso hipotenso y otro para el hipertenso, buscando que sus respuestas se aproximen a la del individuo normotenso.

Las simulaciones y los controladores tienen únicamente fines académicos y no constituyen una recomendación terapéutica.

Palabras clave: Sistema cardiovascular; Modelo Windkessel; Controlador PID; Presión arterial; Modelado matemático; Simulación in silico.

## Lista de archivos incluidos en el repositorio

1. Cuaderno computacional de MATLAB [.mlx].
2. Modelos de Simulink [.slx] para las tres condiciones cardiovasculares y sus sistemas de control.
3. Modelo eléctrico equivalente mediante Simscape Electrical.
4. Código fuente de Python [.py].
5. Análisis matemático: ecuaciones diferenciales, espacio de estados, funciones de transferencia, estabilidad y error en estado estacionario.
6. Tabla de parámetros de los modelos hipotenso, normotenso e hipertenso.
7. Señal de excitación utilizada para las simulaciones.
8. Ganancias y capturas de la sintonización de los controladores PID.
9. Figuras y resultados de las simulaciones en lazo abierto y cerrado [.pdf y .png].
10. Diagrama biológico del sistema cardiovascular.
11. Archivo de citación del repositorio [CITATION.cff].

## Referencias

[1] P. A. Valle, Syllabus para Modelado de Sistemas Fisiológicos. Tijuana, B.C., México: Tecnológico Nacional de México / Instituto Tecnológico de Tijuana, 2026, sección 5.4, pp. 76–86. https://biomath.xyz/course/

[2] M. C. Khoo, Physiological Control Systems: Analysis, Simulation, and Estimation, 2nd ed. Piscataway, New Jersey, USA: IEEE Press, 2018.

[3] F. C. Hoppensteadt and C. S. Peskin, Modeling and Simulation in Medicine and the Life Sciences, 2nd ed. New York, USA: Springer, 2002.

[4] J. E. Hall, Guyton and Hall Textbook of Medical Physiology, 14th ed. Philadelphia, USA: Elsevier, 2021.

[5] K. Ogata, Ingeniería de Control Moderna, 5a ed. Ciudad de México, México: Pearson Educación, 2010.

[6] N. S. Nise, Control Systems Engineering, 8th ed. Hoboken, New Jersey, USA: John Wiley & Sons, 2020.
