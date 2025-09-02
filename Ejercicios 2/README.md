# Retos de Interrupciones

---
## Reto 1: Contador con botón (Interrupción externa)
- **Descripción:** Conectar un pulsador al pin **2 (INT0)**. Cada vez que se presione, incrementar un contador.  
- **Requisito extra:** Mostrar el valor en el **puerto serial**.  
- **Objetivo:** Comprender cómo usar interrupciones externas para responder a eventos asincrónicos evitando el *polling*.  

---

## Reto 2: Control de PWM con interrupción
- **Descripción:** Usar `analogWrite()` en un pin PWM para controlar la intensidad de un LED.  
  - Con un botón en el pin **3 (INT1)**, invertir la dirección del cambio:  
    - Si estaba aumentando el brillo, ahora disminuye.  
    - Si estaba disminuyendo, ahora aumenta.  
- **Objetivo:** Combinar **interrupciones externas** con la generación de señales PWM.  

---

## Reto 3: Temporizador interno para parpadeo preciso
- **Descripción:** Usar **Timer1** en modo *CTC* para generar una interrupción cada **500 ms**.  
- En la ISR, invertir el estado de un LED.  
- **Objetivo:** Demostrar cómo los **timers internos** permiten controlar el tiempo sin usar `delay()`.  

---

## Reto 4: Medición de frecuencia de una señal externa
- **Descripción:**  
  - Conectar un sensor que genere pulsos (ej. sensor de efecto Hall, encoder, o un simple botón).  
  - Configurar una interrupción externa en el pin **2** para contar pulsos.  
  - Usar un **timer interno** que genere interrupción cada 1 segundo.  
  - Al cumplirse, calcular y mostrar la frecuencia (pulsos/segundo) en el **monitor serial**.  
- **Objetivo:** Combinar interrupciones **externas** e **internas** para medir frecuencia.  

---

## Reto 5: Sistema de alarma con múltiples interrupciones
- **Descripción:**  
  - Un sensor (ej. PIR o un pulsador) conectado al pin **2** genera una interrupción externa al detectar movimiento.  
  - Al activarse, empieza a sonar un **buzzer** con frecuencia variable usando interrupción por **Timer2**.  
  - La alarma se detiene al presionar otro botón conectado al pin **3 (INT1)**.  
- **Objetivo:** Integrar múltiples fuentes de interrupción (externas e internas) en un sistema con diferentes estados.  

---
