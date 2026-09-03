# Reto Programación Unidad 3

## 1. Análisis del problema

### Entradas:

- Presión atmosférica en hPa.
- Aceleración en m/s².
- Temperatura en °C.
- Tiempo en segundos.

### Procesos:

- Calcular la altitud del cohete usando la presión.
- Determinar el estado del vuelo.
- Evaluar si la temperatura supera el límite establecido.
- Actualizar la altitud máxima.
- Detectar el apogeo.
- Calcular la temperatura promedio.
- Determinar la aceleración máxima.
- Repetir el proceso cada segundo hasta que el cohete aterrice o el operador termine la simulación.

### Salidas:

- Altitud actual del cohete.
- Estado del vuelo.
- Alerta de temperatura.
- Altitud máxima alcanzada.
- Detección del apogeo.
- Temperatura promedio.
- Aceleración máxima.

## Diagrama de Flujo

![Mi Imagen](https://github.com/Sebastian5050942/Toma_notas_Programaci-n/blob/daee28b6dd139c489bb16c3fd42840c0f287254d/Diagrama%20sin%20t%C3%ADtulo.drawio.png)

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



