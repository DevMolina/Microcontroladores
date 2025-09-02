# Retos de RTOS con Arduino

---

## Reto 1: Parpadeo multitarea (Hello RTOS)

**Objetivo:** Introducir el concepto de tareas concurrentes en RTOS.  

**Descripción:**  
- Crear dos tareas independientes:
  - Tarea 1: Encender y apagar un LED cada 500 ms.  
  - Tarea 2: Encender y apagar otro LED cada 1000 ms.  
- Observar que ambas tareas funcionan sin necesidad de `delay()`.  

---

## Reto 2: Tareas con diferentes prioridades

**Objetivo:** Comprender cómo RTOS asigna CPU a las tareas según su prioridad.  

**Descripción:**  
- Crear tres tareas:
  - Tarea de baja prioridad: parpadeo de LED cada 1000 ms.  
  - Tarea de prioridad media: leer un potenciómetro y mostrar el valor por Serial cada 500 ms.  
  - Tarea de alta prioridad: responder a la pulsación de un botón encendiendo un LED inmediatamente.  
- Comparar qué pasa si todas las tareas tienen la misma prioridad vs. cuando se asignan prioridades distintas.  

---

## Reto 3: Sincronización con semáforos

**Objetivo:** Introducir el control de acceso a recursos compartidos.  

**Descripción:**  
- Dos tareas intentan escribir en la pantalla LCD o en el puerto Serial (recurso compartido).  
- Usar un **semáforo binario** o un **mutex** para que solo una tarea acceda al recurso a la vez.  
- Mostrar en la salida Serial qué tarea está escribiendo y verificar que no haya mensajes mezclados.  

---

## Reto 4: Colas de mensajes para comunicación entre tareas

**Objetivo:** Entender cómo las tareas se comunican de manera ordenada.  

**Descripción:**  
- Crear una **tarea de lectura de sensor** (por ejemplo, temperatura con un DHT11).  
- Esta tarea envía los valores a través de una **cola** a otra tarea.  
- La **tarea de procesamiento** recibe los datos de la cola y:
  - Los muestra en Serial.  
  - Enciende un LED si la temperatura pasa cierto umbral.  
- Implementar además una tarea de "monitoreo" que corra en paralelo y muestre un "sistema en funcionamiento".  

---
