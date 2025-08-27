# Retos de Programación con Memoria EEPROM en Arduino

---

## Reto 1: Contador Persistente de Encendidos

**Objetivo:**  
Programar el Arduino para que cuente cuántas veces se ha encendido el sistema y almacenar este valor en la EEPROM.

**Descripción:**  
Cada vez que el Arduino se energiza, debe:
1. Leer el valor actual del contador desde la EEPROM.  
2. Incrementar el contador en 1.  
3. Guardar el nuevo valor en la EEPROM.  
4. Mostrar el número de encendidos por el puerto serie.  

**Puntos a considerar:**
- Usar `EEPROM.read()` y `EEPROM.write()`.  
- Evitar escribir en cada ciclo del `loop()`, solo al iniciar.  

---

## Reto 2: Menú de Configuración Persistente

**Objetivo:**  
Diseñar un sistema de configuración simple que guarde los parámetros en la EEPROM y los restaure al reiniciar.

**Descripción:**  
- El usuario, a través del puerto serie, debe poder elegir entre 3 opciones de configuración (ejemplo: velocidad de parpadeo de un LED: lenta, media, rápida).  
- La opción seleccionada se guarda en la EEPROM.  
- Al reiniciar el Arduino, debe leer la configuración almacenada y ejecutar el comportamiento correspondiente sin necesidad de volver a configurarlo.  

**Puntos a considerar:**
- Usar `EEPROM.put()` y `EEPROM.get()` para almacenar variables.  
- Crear un menú básico usando `Serial.read()`.  

---