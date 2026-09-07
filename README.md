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

![Mi Imagen](https://github.com/Sebastian5050942/Toma_notas_Programaci-n/blob/fdd1d3cff4bf816dcae0cbeeed84cb984fe776b9/WAR.drawio.png)

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









