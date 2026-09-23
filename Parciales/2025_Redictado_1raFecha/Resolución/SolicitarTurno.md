## Frente

* **ID**: Solicitar Turno
* **Título**: Como paciente autenticado quiero solicitar un turno para ser atendido.
* **Reglas de negocio**:
    * El paciente debe ser mayor a 18 años
    * Un paciente puede solicitar hasta 1 turno por especialidad por semana

---

## Reverso
* Criterios de Aceptación (Solicitar Turno)

* **Escenario 1**: Solicitud exitosa
    * Dado un paciente con 19 años sin otro turno registrado de especialidad "Pediatría" para la semana del 21/7 - 27/7 y sin otro turno registrado para el 23/7 a las 18:00 hs.
    * Cuando el paciente ingresa, especialidad Pediatría, médico Pepe, día 23/7, hora 18:00 y presiona "Solicitar Turno"
    * Entonces el sistema registra el turno, informa "Turno reservado exitosamente".
* **Escenario 2**: Solicitud fallida por minoría de edad
    * Dado un paciente con 17 años,
    * Cuando el paciente ingresa especialidad Pediatría, médico Pepe, día 18/7, hora 20:00 y presiona "Solicitar Turno"
    * Entonces el sistema informa "Para solicitar un turno, se requiere una edad mayor a 18. Solicitud rechazada".
* **Escenario 3**: Solicitud fallida por límite de turnos de especialidad alcanzado
    * Dado un paciente con un turno de odontología registrado para el 25/7, que está en la semana 21-7 - 27-7 y una fecha de turno 24/7,
    * Cuando el paciente ingresa: especialidad odontología, médico "Juan", día 24/7, hora 18:00 y presiona "Solicitar turno"
    * Entonces el sistema informa "No se solicitó el turno. Solo se puede reservar un turno por especialidad por semana".
* **Escenario 4**: Solicitud fallida por superposición de turnos
    * Dado un paciente con un turno ya reservado para el 20/10 a las 20:00 hs
    * Cuando el paciente ingresa: especialidad oftalmología, médico José, día 20/10, hora 20:00 hs y presiona “Solicitar turno”
    * Entonces el sistema informa: "No se te solicitó el turno. Ya tienes un turno registrado para la fecha y hora ingresadas".
* **Escenario 5**: Solicitud fallida por especialidad no correspondiente al médico
    * Dada una especialidad “dermatología”, no correspondiente al médico José 
    * Cuando el paciente ingresa: especialidad dermatología, médico José, día 20/10, hora 20:00 hs y presiona “Solicitar turno”
    * Entonces el sistema informa: "No se solicitó el turno. El médico José no atiende por dermatología".