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
1. Primero debemos familiarizarnos con los movimientos del robot Epson C4, los cuales explicaremos en la tabla a continuación.

| **Movimiento** | **Descripción**                                                                                                                                                        |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `GO`           | Movimiento rápido a una posición específica sin control de la trayectoria entre la posición actual y la nueva. Ideal para movimientos de posicionamiento rápido.        |
| `MOVE`         | Movimiento lineal controlado hacia una posición definida, asegurando que el brazo se mueva a lo largo de una línea recta. Se utiliza para trayectorias precisas.        |
| `JUMP`         | Movimiento en el que el robot "salta" hacia una posición definida, levantando primero el efector final en la dirección Z y luego moviéndose en el plano horizontal.     |
| `JUMP3CP`      | Movimiento de salto que incluye tres puntos de control, permitiendo mayor flexibilidad en la trayectoria del salto para evitar obstáculos.                              |
| `ARC`          | Movimiento que sigue una trayectoria curva entre dos puntos, útil para operaciones de trazo curvado o tareas que requieren una transición suave.                        |
| `ARC3`         | Similar al movimiento `ARC`, pero con tres puntos de control, permitiendo que el robot trace curvas más complejas con precisión entre varios puntos.                    |
| `PASS`         | Movimiento hacia una posición intermedia sin detenerse, permitiendo que el robot pase por esta posición de manera continua hacia su destino final.                      |
| `CP`           | Movimiento de control continuo, útil para seguir trayectorias complejas donde es importante que las articulaciones mantengan una velocidad constante a lo largo de la ruta. |



2. Una vez que conocemos los movimiento podemos pasara al segundo paso para la elaboración de la práctica es abrir el programa EPSON RC+ y crear un nuevo proyecto.
   
![image](https://github.com/user-attachments/assets/dc677feb-714c-4519-8ccb-f15b9da0af6d)

3. Después de crear el proyecto, comenzamos con la conexión con el robot Epson C4, utilizando la conexión por USB.

![image](https://github.com/user-attachments/assets/3163e851-f70d-4291-837c-a8f62494c90d)


4. Una vez que tenemos conexión con el robot, abrimos el Robot Manager para encender los motores del robot y comenzar con la grabación de los movimientos.

![image](https://github.com/user-attachments/assets/7e367d25-6771-4152-bb61-fc9d1219da58)

5. La práctica consiste en escribir una palabra con un plumón en la garra del robot. Para hacerlo, escribimos la palabra en una hoja de papel; la palabra elegida fue "MIAU". Con este molde lo utilizamos para grabar los movimientos del robot.

![Imagen de WhatsApp 2024-09-29 a las 13 13 11_de34c7a9](https://github.com/user-attachments/assets/5796202c-e6cb-41b4-a1c9-05285db27625)

6. Una vez que grabamos los movimientos, desarrollamos el código para que el robot dibuje esta palabra "MIAU", el cual se muestra a continuación.

```plaintext
Function main
Motor On
Power High
Home
Move m1
Move m2
Move m3
Move m4
Move m5
Home
Move i1
Move i2
Home
Move a1
Move a2
Move a3
Move a4
Move a5
Home
Go u1
Pass u1, u2, u3
Home
Motor Off
Fend



 
