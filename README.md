# Clase 18 de Agosto / 2026

# Actividad # 1 - Ambiente de Desarrollo Integrado (IDE):

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

# Actividad # 2 - De algoritmo a código fuente:

# 1. ¿por qué es útil el pseudocódigo antes de programar?

- El pseudocódigo es útil ya que permite organizar poder tomar un pensamiento de los pasos que debe seguir cada programa antes de escribirlo en Python. Así podemos comprobar si la lógica tiene sentido y asi corregir posibles errores antes de hacer el código.

# 2. Traducir a Python los 5 primeros ejercicios del reto de Unidad 2:

## A) Verificación de peso de despegue

### Pseudocódigo: 

  INICIO
    
     
     Leer peso_total
     Leer peso_maximo

    Si peso_total <= peso_maximo Entonces
        Mostrar "Aeronave lista para despegar"
    Sino
        Mostrar "Debe reducir carga o combustible"
    Fin Si
  FIN

### Python:

<img width="562" height="190" alt="image" src="https://github.com/user-attachments/assets/69139c10-6e50-4d53-85f1-adb7a1c19884" />

## B) Control de temperatura del motor:

### Pseudocódigo: 

INICIO
    
    
    Leer temperatura

    Si temperatura > 100 Entonces
        Mostrar "Peligro: sobrecalentamiento"
    Sino Si temperatura < 50 Entonces
        Mostrar "Motor frío - Calentar antes de operar"
    Sino
        Mostrar "Operación normal"
    Fin Si
FIN

### Python:

<img width="540" height="210" alt="image" src="https://github.com/user-attachments/assets/f3d3ef19-eee1-4696-a00f-0555647688fc" />

## C) Registro de altitudes de vuelo 

### Pseudocódigo: 

INICIO
    
    
    
    Para minuto desde 10 hasta 60, avanzando de 10 en 10
        Leer altitud
        Mostrar altitud
    Fin Para
FIN

### Python:

<img width="625" height="98" alt="image" src="https://github.com/user-attachments/assets/db599450-5013-412b-81cd-7ffb5c2d8dac" />

## D) Control de combustible en pruebas

### Pseudocódigo: 

INICIO
   
    
    tiempo = 0
    Leer combustible

    Mientras combustible >= 10
        Mostrar combustible
        tiempo = tiempo + 1
        Leer combustible
    Fin Mientras

    Mostrar tiempo
FIN

### Python:

<img width="648" height="274" alt="image" src="https://github.com/user-attachments/assets/4f2fab91-1d03-467a-b25e-2e7957cf1f41" />

## E) Detección de turbulencia en trayecto

### Pseudocódigo: 

INICIO
   
    
    
    turbulencias = 0

    Para segundo desde 1 hasta 120
        Leer aceleracion

        Si aceleracion > umbral Entonces
            Mostrar "Turbulencia detectada"
            turbulencias = turbulencias + 1
        Fin Si
    Fin Para

    Mostrar turbulencias
FIN

### Python:

<img width="671" height="354" alt="image" src="https://github.com/user-attachments/assets/17f69982-7523-421a-9c84-3c9d7d1faa82" />

# 3. Pseudocódigo propio

- Escogemos un Pseudocódigo para determinar si un número es par o impar:

INICIO
    
    
    Leer numero

    Si numero MOD 2 = 0 Entonces
        Mostrar "El número es par"
    Sino
        Mostrar "El número es impar"
    Fin Si
FIN

# 4. ¿Cuál es la diferencia entre int(input()) y float(input())?

- La diferencia es que int(input()) sirve para poder convertir el dato ingresado en un número entero, mientras que float(input()) permite convertirlo en un número que puede tener decimales. Por lo cual. se debe utilizar uno u otro dependiendo del tipo de dato que necesite el programa.

# 5. Calcular el promedio de 5 edades

### Pseudocódigo: 


INICIO
    
    
    Leer edad

    Si edad >= 0 Entonces
        Si edad < 6 Entonces
            etapa = "Infancia"
        Sino Si edad < 12 Entonces
            etapa = "Niñez"
        Sino Si edad < 20 Entonces
            etapa = "Adolescencia"
        Sino Si edad < 25 Entonces
            etapa = "Juventud"
        Sino Si edad < 60 Entonces
            etapa = "Adultez"
        Sino
            etapa = "Vejez"
        Fin Si

        Mostrar etapa
    Sino
        Mostrar "Edad inválida"
    Fin Si
FIN

### Python:

<img width="419" height="327" alt="image" src="https://github.com/user-attachments/assets/d5a74731-501e-4d69-8555-fb7991e85a7c" />

# 6. ¿Por qué es importante comentar el código?

Es importante comentar el código ya que los comentarios ayudan a entender qué hace cada parte del programa y facilitan encontrar errores y modificar el código más adelante, especialmente cuando el programa es largo.

# 7. Después de este tutorial, ¿qué puntos crees que deberías reforzar para sentirte más seguro al traducir pseudocódigo a Python?

En mi opinión creo que debería reforzar la forma de pasar las condiciones, los bucles y las variables del pseudocódigo a Python, asi como practicar más para poder identificar qué estructura de Python corresponde a cada paso del pseudocódigo.

# Operadores:

## 1. Pregunta orientadora: ¿Cuántas veces realizas cálculos mentales o tomas decisiones basadas en condiciones? ¿Cómo crees que le enseñamos a una computadora a hacer lo mismo?

En la vida cotidiana realizamos diversos cálculos y tomamos decisiones constantemente a lo largo de los días, por ejemplo, cuando calculamos cuánto dinero necesitamos o decidimos qué hacer dependiendo del clima, por eso, a una computadora le enseñamos a hacer esto mediante operadores que permiten realizar cálculos, comparar valores y evaluar condiciones.

## 2. Cuenta del restaurante

### Python: 

<img width="500" height="327" alt="image" src="https://github.com/user-attachments/assets/4bffa702-d430-4b94-bcdf-b0aab856e672" />

### Ejecución:

<img width="989" height="143" alt="image" src="https://github.com/user-attachments/assets/2c59dc34-b140-40db-926d-5b156e1b4818" />

## 3. Guardián de la montaña rusa

### Python:

<img width="514" height="212" alt="image" src="https://github.com/user-attachments/assets/c7f05d1a-32a2-4d28-a6ea-840c3cb57599" />

### Ejecución:

<img width="958" height="91" alt="image" src="https://github.com/user-attachments/assets/e899a5bc-b9a6-4268-b241-28f304914058" />
<img width="522" height="66" alt="image" src="https://github.com/user-attachments/assets/ed6a3160-2df7-4469-b199-2333c236a6a2" />

# 4. Sistema de becas

### Python:

<img width="650" height="181" alt="image" src="https://github.com/user-attachments/assets/594f0750-5e0e-4524-885b-1a70da9b7c5a" />

### Ejecución:

<img width="512" height="71" alt="image" src="https://github.com/user-attachments/assets/41c592ba-09cb-4451-b6fd-885698a3e23f" />
<img width="522" height="89" alt="image" src="https://github.com/user-attachments/assets/9ea64149-ff4f-42ef-8eed-f201270d2970" />

# 5. Reto Final

### Python:

<img width="607" height="375" alt="image" src="https://github.com/user-attachments/assets/8e644d44-62ff-4708-85f2-c42fb3f4e3b1" />

### Ejecución:

<img width="571" height="70" alt="image" src="https://github.com/user-attachments/assets/91e82aed-34ac-422b-b3db-a11615a28e8a" />

# 6. Pregunta Final: ¿Qué se te dificultó más y cómo lo resolviste?

Lo que más se me dificultó fue poder combinar los operadores aritméticos, relacionales y lógicos en una misma condición.

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

FUNCIÓN 


calcular_altitud(presion_hpa)

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









