## Frente

* **ID**: Crear Clase
* **Título**: Como administrador autenticado quiero crear una clase para expandir mi negocio.
* **Reglas de negocio**:
    * Por sala solo se puede dar 1 clase
    * Cada instructor puede dar hasta 3 clases por día

---

## Reverso
* Criterios de aceptación (Crear Clase)

* **Escenario 1**: Creación de clase exitosa
    * Dado una sala 9 sin clases el 30/9 14:00 hs y un DNI de instructor 48 888 888 con 2 clases asignadas a ese día
    * Cuando el administrador ingresa Sede Gonnet, tipo Yoga, número de sala 9, DNI de instructor 48 888 888, capacidad maxima 20, día 30/9, hora 14:00 hs y presiona "Crear Clase"
    * Entonces el sistema registra la creación de la clase informa "Clase creada exitosamente".
* **Escenario 2**: Creación Fallida Por sala ocupada
    * Dada una sala 8 con una clase agendada para el 15/10 18:00hs
    * Cuando el administrador ingresa Sede Gonnet, tipo Yoga, número sala 8, DNI 40 000 000, capacidad 20, día 15/10, hora 18:00 y presiona "Crear clase"
    * Entonces el sistema informa "No se pudo crear la clase la sala 8 está ocupada en el horario ingresado"
* **Escenario 3**: Creación fallida por instructor sobrecargado
    * Dado un DNI de instructor 30 000 000 con 3 clases asignadas para el 15/12/26
    * Cuando el admin. ingresa "Sede Gonnet", tipo "yoga", número de sala 8, DNI 30 000 000, capacidad 20, día 15/12/26, hora 19:00 y presiona "Crear clase"
    * Entonces el sistema informa "No se pudo crear la clase, el instructor 30 000 000 ya tiene 3 clases asignadas para el 15/12"