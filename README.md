# Práctica 5

## Integrantes:
- **Luis Fernando Duarte Reséndiz**
- **Mauricio Alberto Gómez Arroyo**
- **Diego Brandon Guzmán Sierra**
- **Bryan Hiadim Vera Hernández**

## Introducción:
Los brazos robóticos han revolucionado la industria moderna, permitiendo una automatización avanzada en una variedad de procesos. Equipados con una variedad de juntas, motores y controladores programables, estos dispositivos pueden realizar tareas repetitivas con alta precisión y eficiencia, lo que los hace indispensables en campos como la fabricación, la automoción, la electrónica y la logística.

Uno de los modelos más conocidos de la industria, el Epson C4 es un brazo robótico compacto de alto rendimiento diseñado para brindar flexibilidad y precisión en entornos industriales. Este modelo es ideal para espacios pequeños y capaz de manejar una variedad de aplicaciones de automatización.

El robot utiliza diferentes tipos de movimientos, como:

- Movimientos lineales: Perfectos para dibujar líneas rectas o seguir trayectorias predefinidas con precisión.
- Movimientos angulares: Ideales para ajustar la orientación del brazo, permitiendo rotar la herramienta en ángulos precisos para escribir caracteres o figuras curvas.
- Interpolación circular: Este tipo de movimiento es útil para dibujar curvas o círculos, permitiendo al Epson C4 seguir trayectorias circulares suaves.
  
Al programar el brazo para escribir en el suelo, se puede integrar una herramienta de escritura (como un marcador o una tiza) en su extremo, y mediante la programación adecuada, el Epson C4 puede trazar letras, símbolos o cualquier patrón requerido. Su precisión y capacidad para seguir trayectorias complejas le permiten realizar esta tarea con gran exactitud, haciendo uso de todos sus tipos de movimiento para adaptarse a los requerimientos específicos del diseño.

## Instrucciones.
1.Primero debemos de familiarizarnos con los movimientos del robot epson C4, los cales explicaremos en la tabla a continuacion.

| **Movimiento** | **Descripción**                                                                                                                                                        | **Trayectoria**  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| `GO`           | Movimiento rápido a una posición específica sin control de la trayectoria entre la posición actual y la nueva. Ideal para posicionamiento rápido.                        | ───────────>     |
| `MOVE`         | Movimiento lineal controlado hacia una posición definida, asegurando que el brazo se mueva a lo largo de una línea recta.                                               | ───────────>     |
| `JUMP`         | Movimiento en el que el robot "salta" hacia una posición definida, levantando primero el efector en la dirección Z, luego moviéndose en el plano horizontal.            | ^───>            |
| `JUMP3CP`      | Movimiento de salto con tres puntos de control, permitiendo mayor flexibilidad en la trayectoria para evitar obstáculos.                                                | ^───o───>        |
| `ARC`          | Movimiento que sigue una trayectoria curva entre dos puntos, útil para operaciones de trazo curvado o transiciones suaves.                                              | ⌒                |
| `ARC3`         | Similar a `ARC`, pero con tres puntos de control, permitiendo curvas más complejas entre varios puntos.                                                                 | ⌒⌒               |
| `PASS`         | Movimiento hacia una posición intermedia sin detenerse, permitiendo que el robot pase por esta posición de manera continua hacia su destino final.                      | ─o─────>          |
| `CP`           | Movimiento de control continuo para seguir trayectorias complejas, manteniendo una velocidad constante a lo largo de la ruta.                                           | ∼~~~~~~~~∼       |


2. El segundo paso para la elaboración de la práctica es abrir el programa EPSON RC+ y crear un nuevo proyecto.
   
![image](https://github.com/user-attachments/assets/dc677feb-714c-4519-8ccb-f15b9da0af6d)

2. Despues de crear el proyecto 
 
