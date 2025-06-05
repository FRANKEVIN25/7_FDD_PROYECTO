# “Año de la recuperación y consolidación de la economía peruana”

## UNIVERSIDAD PERUANA CAYETANO HEREDIA  
### Facultad de Ciencias e Ingeniería  
### Fundamentos de Diseño  

---

## INFORME TÉCNICO

**GRUPO 7**

**Jefes de práctica:**
- Umbert Lewis De La Cruz Rodriguez  
- Renzo Jose Chan Rios  
- Victor Alberto Huanambal Sovero  

**Integrantes:**
- Nathalia Silvana Robledo Cerna  
- Frank Jauregui Bendezu  
- Jonathan Suasnabar  
- Antony  

**LIMA - PERÚ**

---

## Ejemplos

---

### 1. Control de Dirección del Motor GA12-N20 con Arduino y L298N

En este sistema se busca controlar la inversión cíclica de la dirección de giro de un motorreductor DC GA12-N20. Esto se dará por la interacción entre el Arduino UNO, que será el control lógico, y un módulo L298N, que será el control de potencia y gestionará la polaridad de la corriente del motor.

El Arduino envía señales a los pines IN1 y IN2 del L298N. Así permitirá girar en un sentido, ya sea horario o antihorario, durante 5 segundos con los comandos. Si es en sentido horario IN1 se activa e IN2 se desactiva, y viceversa si es en sentido antihorario. Para que el motor se detenga durante un segundo, ambos pines deben desactivarse.  

[Ver video](../Videos/EJERCICIO1.mp4)

> Nota: El pin ENA del L298N siempre debe permanecer conectado a 5V para permitir el funcionamiento sin control de velocidad. Se requiere fuente externa de alimentación para el motor.

---

### 2. Control de Dirección y Velocidad del Motor GA12-N20 con Arduino y L298N

A diferencia del sistema anterior, este también busca controlar la **velocidad** del motor GA12-N20. El L298N actuará como puente de potencia y el Arduino enviará señales lógicas a los pines IN1 e IN2, así como una señal PWM al pin ENA para ajustar la velocidad.

Este funcionamiento será alternante: el motor gira en un sentido por 5 segundos, se detiene, y luego gira en sentido contrario por otros 5 segundos. La fuente de alimentación externa debe estar entre 6V y 12V. Este sistema se aplica en áreas como la biomédica, por su flexibilidad y precisión.

[Ver video](../Videos/EJERCICIO2.mp4)

---

### 3. Control de Velocidad del Motor GA12-N20 con Potenciómetro y Arduino

Este sistema permite el ajuste manual de la velocidad del motor GA12-N20 usando un potenciómetro. El potenciómetro actúa como divisor de voltaje; su señal analógica es leída por el Arduino.
El Arduino mapea la lectura del potenciómetro a una señal PWM que regula la potencia que recibe el motor, manteniendo constante el sentido de giro. Necesita una fuente de 6V a 12V.


[Ver video](../Videos/EJERCICIO3.mp4)

---

### 4. Control del Servomotor DS3235 mediante Potenciómetro y PWM

Este sistema controla la posición angular del servomotor DS3235 mediante un potenciómetro. El Arduino transforma el valor analógico en un pulso PWM entre 500 y 2400 µs.

**📷 Foto de materiales**  
*(Agregar imagen aquí)*

La secuencia es: ADC → PWM → Ángulo. El ángulo se muestra en el monitor serial como retroalimentación. El servomotor es alimentado con una fuente externa de 6V a 7.4V.

**📷 Foto del sistema terminado**  
*(Agregar imagen aquí)*  
🎥 *(Agregar video aquí)*

---

### 5. Control de Posición del Servomotor DS3235 con Arduino

El sistema controla con precisión la posición del servomotor DS3235 mediante pulsos PWM. El Arduino envía pulsos entre 500 µs (0°) y 2400 µs (270°).

**📷 Foto de materiales**  
*(Agregar imagen aquí)*

El programa mueve el servo a 0º, 90º, 180º y 270º con intervalos de 5 segundos. El servomotor debe estar conectado a una fuente externa de 6V a 7.4V y compartir tierra con el Arduino.

**📷 Foto del sistema terminado**  
*(Agregar imagen aquí)*  
🎥 *(Agregar video aquí)*

---

### 6. Activación Básica de un Micromotor de Vibración con Arduino

Sistema básico para activar un micromotor de vibración usando un transistor NPN y un Arduino UNO. La señal del pin D3 activa el transistor que permite el flujo de corriente al motor.

**📷 Foto de materiales**  
*(Agregar imagen aquí)*

El motor se activa por 2 segundos y se apaga por 1. Se recomienda un diodo flyback en paralelo con el motor para proteger el transistor de picos de voltaje.

**📷 Foto del sistema terminado**  
*(Agregar imagen aquí)*  
🎥 *(Agregar video aquí)*

---

### 7. Control de Intensidad de Vibración con Potenciómetro y Arduino

Este sistema permite controlar la intensidad de la vibración de un micromotor con un potenciómetro. Usado en biomédica para estímulos táctiles controlados.

**📷 Foto de materiales**  
*(Agregar imagen aquí)*

El Arduino convierte la señal analógica del potenciómetro en una señal PWM que regula la intensidad del motor. Se utiliza un diodo flyback para proteger el transistor.

**📷 Foto del sistema terminado**  
*(Agregar imagen aquí)*  
🎥 *(Agregar video aquí)*

---

## 🔚 Fin del Informe Técnico


