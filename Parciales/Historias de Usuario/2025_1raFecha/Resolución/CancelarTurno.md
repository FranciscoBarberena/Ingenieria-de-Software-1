## Frente

* **ID**: Cancelar Turno
* **Título**: Como socio autenticado quiero cancelar un turno de una clase para no ir a la misma.
* **Reglas de negocio**:
    * Los turnos se deben cancelar con al menos 1h de anticipación

---

## Reverso
* Criterios de Aceptación (Cancelar turno)

* **Escenario 1**: Cancelación exitosa
    * Dado un socio con un turno registrado para el 30/9/26 17:00, con la hora actual siendo las 15:59,
    * Cuando el socio ingresa Fecha 30/9/26, hora 17:00, y presiona "Cancelar Turno"
    * Entonces el sistema elimina el turno e informa "Cancelación de turno exitosa".
* **Escenario 2**: Cancelación fallida por falta de anticipación
    * Dado un socio con un turno registrado para el 3/10/26 a las 20:00 hs, con la hora actual siendo 19:30,
    * Cuando el socio ingresa Fecha 3/10/26, hora 20:00 hs y presiona "Cancelar turno"
    * Entonces el sistema informa "No se pudo cancelar el turno, las cancelaciones se deben hacer con al menos 1h de anticipación".
* **Escenario 3**: "Cancelación fallida por turno inexistente"
    * Dado un socio sin un turno registrado para el 4/10/26 a las 17:00,
    * Cuando el socio ingresa fecha 4/10, hora 17:00 y presiona "Cancelar turno"
    * Entonces el sistema informa "Cancelación fallida, no tienes ningún turno para la fecha y hora ingresados".