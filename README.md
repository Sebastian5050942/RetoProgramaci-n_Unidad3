# Clase 18 de Agosto / 2026

## Trabajo en Python:

<img width="694" height="709" alt="image" src="https://github.com/user-attachments/assets/d8e5171b-5a87-4ab8-b6ed-fdb3017dc39e" />


## Programar:

### Primero debemos guardar un nuevo archivo:

<img width="644" height="370" alt="image" src="https://github.com/user-attachments/assets/063c1359-e51b-450c-b44f-91fbec5b2cf2" />

### Después programamos: 

<img width="1360" height="737" alt="image" src="https://github.com/user-attachments/assets/cb7a6eab-402d-4638-8c11-0f77c61cedab" />

- Run Module o F5

## Errores comunes:

- No poner las " de abrir y cerrar

<img width="1353" height="730" alt="image" src="https://github.com/user-attachments/assets/2aeffe6e-414b-4b46-8647-f41e8dba58f8" />

## Iniciar Visual Studio Code:

### 1) Abrir carpeta (Unidad3):

<img width="1181" height="727" alt="image" src="https://github.com/user-attachments/assets/8c92d2ec-2d0e-46b9-a1c3-1d0e86d82f09" />

### 2) Python:

<img width="1193" height="792" alt="image" src="https://github.com/user-attachments/assets/b70ba2af-c100-4054-8d1c-84243582cb93" />

## Código Python (VSC):

Link: https://github.com/Sebastian5050942/Toma_notas_Programaci-n/blob/cb5b8f22df2babed01b9f2b560056f362dddd1cf/Esemar_gtcj/Unidad_3.py

## Ejercicio:

<img width="473" height="596" alt="image" src="https://github.com/user-attachments/assets/56340565-134c-4a9f-a41e-ffa1b541596a" />

### Solucionamos en Python:

<img width="1919" height="1077" alt="image" src="https://github.com/user-attachments/assets/ca922ccc-f532-44e2-bf1b-551552af70bd" />

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/e04da9ca-987a-4941-b862-784942387855" />

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/fec5188e-0fb7-454e-bf80-954eded86366" />

<img width="1918" height="1079" alt="image" src="https://github.com/user-attachments/assets/dcdbf485-bb29-4104-91a6-82aed9e8a304" />

# Trabajo Google Colab

<img width="828" height="717" alt="image" src="https://github.com/user-attachments/assets/e460c25f-aee5-4e0b-8011-65a5bdaa1326" />

# Preguntas

1. ¿Qué es un IDE?
2. ¿Cuál es la diferencia entre los 3 IDEs estudiados en esta actividad?
3. ¿Cuál utilizarás en el resto del curso y por qué?

## Respuestas:

1. Un IDE es un programa el cual tiene como función escribir, ejecutar y editar códigos. Además, nos ayuda a detectar errores.
2. La diferencia entre cada uno de los 3 IDEs en el caso de IDLE, Visual Studio Code y Google Colab la siguiente:
- IDLE: Como tal es una herramienta sencilla para programar y pedir ejecuciones básicas mediante Python
- Visual Studio Code: Es mucho más completa y tienes más capacidades de generar codigos extensos, asi como extensiones.
- Google Colab: Funciona mediante el navegador de Google solo con iniciar sesión y crear un cuaderno y poner una nota ya tienes una creación.
3. Durante el resto del curso yo utilizaría Visual Studio Code, porque como decía anteriormente es una herramienta demasiado completa, en la cual después de completar todo el código podemos verificar mediante una Ejecución si todos los datos que programamos están bien o por el contrario hay que hacer cambios. 

# RETO PROGRAMACIÓN UNIDAD 3

# Fase 1

## 1. Análisis del problema

### Entradas:

| Entrada | Unidad | Descripción |
|---|---|---|
| Presión atmosférica | hPa | Calcular la altitud del cohete |
| Aceleración | m/s² | Determinar el estado del vuelo |
| Temperatura | °C | Evaluar la alerta de temperatura |

### Procesos:

- Recibir la presión, aceleración y temperatura de cada segundo.
- Calcular la altitud actual utilizando la fórmula barométrica.
- Comparar la altitud actual con la altitud anterior para determinar el comportamiento del vuelo.
- Determinar el estado del vuelo.
- Evaluar si la temperatura supera el límite crítico establecido.
- Comparar la altitud actual con la altitud máxima almacenada y actualizarla cuando corresponda.
- Detectar el apogeo cuando la altitud actual sea menor que la altitud previa por primera vez.
- Acumular las temperaturas y contar las lecturas para obtener posteriormente la temperatura promedio.
- Comparar las aceleraciones para conservar la aceleración máxima.
- Repetir el proceso segundo a segundo hasta que la altitud sea menor o igual a cero o el operador finalice la simulación.

### Salidas:

- Altitud actual del cohete.
- Estado del vuelo.
- Alerta de temperatura.
- Altitud máxima alcanzada.
- Detección del apogeo.
- Temperatura promedio.
- Aceleración máxima.

## Diagrama de Flujo

![Mi Imagen](https://github.com/Sebastian5050942/Toma_notas_Programaci-n/blob/a864d2adb16b06df44b3885c6573e04241668ae3/WAR2.drawio.png)

## Pseudocódigo

### 1) Función para calcular la altitud:

FUNCIÓN calcular_altitud(presion_hpa)

   altitud:  $h = 44330 \times \left( 1 - \left( \frac{P}{1013.25} \right)^{0.1903} \right)$
  
RETORNAR altitud

FIN FUNCIÓN

### 2) Función para determinar el estado del vuelo:

FUNCIÓN determinar_estado_vuelo(altitud_actual, altitud_previa, aceleracion)

    SI altitud_actual > altitud_previa ENTONCES
        RETORNAR "Ascenso"

    SINO
        SI aceleracion < 0 
        ENTONCES
            RETORNAR "Apogeo / Caída libre"
        SINO
            RETORNAR "Despliegue de Paracaídas"
        FIN SI
    FIN SI

FIN FUNCIÓN

### 3) Función para evaluar la temperatura:

FUNCIÓN evaluar_alerta_temperatura(temp_celsius)

    SI temp_celsius > limite_temperatura 
    ENTONCES
        RETORNAR VERDADERO
    SINO
        RETORNAR FALSO
    FIN SI

FIN FUNCIÓN

### Pseudocódigo Principal de los 3:

INICIO

    tiempo ← 0
    altitud_previa ← 0
    altitud_maxima ← 0
    temperatura_acumulada ← 0
    cantidad_lecturas ← 0
    aceleracion_maxima ← 0
    apogeo_detectado ← FALSO
    simulacion_activa ← VERDADERO

    MIENTRAS simulacion_activa = VERDADERO

        INGRESAR presión
        INGRESAR aceleración
        INGRESAR temperatura

        altitud_actual ← calcular_altitud(presión)

        estado ← determinar_estado_vuelo(
            altitud_actual,
            altitud_previa,
            aceleración
        )

        alerta ← evaluar_alerta_temperatura(temperatura)

        SI altitud_actual > altitud_maxima ENTONCES
            altitud_maxima ← altitud_actual
        FIN SI

        temperatura_acumulada ← temperatura_acumulada + temperatura
        cantidad_lecturas ← cantidad_lecturas + 1

        SI aceleración > aceleracion_maxima ENTONCES
            aceleracion_maxima ← aceleración
        FIN SI

        SI altitud_actual < altitud_previa Y apogeo_detectado = FALSO ENTONCES
            apogeo_detectado ← VERDADERO
        FIN SI

        MOSTRAR altitud_actual
        MOSTRAR estado
        MOSTRAR alerta

        altitud_previa ← altitud_actual
        tiempo ← tiempo + 1

        SI altitud_actual ≤ 0 ENTONCES
            simulacion_activa ← FALSO
        FIN SI

    FIN MIENTRAS

    temperatura_promedio ← temperatura_acumulada / cantidad_lecturas

    MOSTRAR altitud_maxima
    MOSTRAR temperatura_promedio
    MOSTRAR aceleracion_maxima
    MOSTRAR apogeo_detectado

FIN

# Fase 2

## Link de Código Python hecho en VSC:

https://github.com/Sebastian5050942/RetoProgramaci-n_Unidad3/blob/b34d2df5a204cbdee3f8d509e1685001c947dc94/cohete.py

## Evidencias de cada prueba completada en la Terminal:

<img width="1183" height="640" alt="image" src="https://github.com/user-attachments/assets/959d055e-3e51-4d60-8455-1ed36ffd8635" />

<img width="1169" height="653" alt="image" src="https://github.com/user-attachments/assets/a1f99add-ded6-448b-8137-5514f0f31bb4" />

<img width="1172" height="640" alt="image" src="https://github.com/user-attachments/assets/b24be87d-dccc-4c6d-a799-2dcb360bba80" />

<img width="1168" height="644" alt="image" src="https://github.com/user-attachments/assets/95afb3f4-284c-4428-8873-72949255d9c4" />

<img width="1172" height="630" alt="image" src="https://github.com/user-attachments/assets/88b6b88d-94ab-42ae-8109-d7a4a7cd4166" />

<img width="1169" height="632" alt="image" src="https://github.com/user-attachments/assets/dbd4c858-9a51-4925-a82e-0ce61cafd269" />

<img width="1173" height="644" alt="image" src="https://github.com/user-attachments/assets/ae075f9f-e5de-4232-9f07-fdb372fb4a69" />

<img width="1176" height="640" alt="image" src="https://github.com/user-attachments/assets/41ffd477-cd6a-4d4e-ac3d-f6b265ff139f" />

<img width="1176" height="551" alt="image" src="https://github.com/user-attachments/assets/a0b49dd4-28b7-407e-a7ea-323906e20152" />









