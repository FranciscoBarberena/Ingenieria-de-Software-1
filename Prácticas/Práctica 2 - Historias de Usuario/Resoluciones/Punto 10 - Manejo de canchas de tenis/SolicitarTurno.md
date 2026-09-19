## Frente

* **ID**: `Solicitar turno`
* **Título**: Como `Usuario` quiero `solicitar un turno` para `tener una reserva de una cancha de tenis`.
* **Reglas de negocio**:
    * No se permite reservar un turno con menos de 2 días de antelación a la fecha en que se solicita.
        * **Aclaración: estoy tomando 2 días como equivalente a 48 horas.**

---

## Reverso
* Criterios de Aceptación (`Solicitar turno`)

* **Escenario 1**: `Turno solicitado exitosamente`
    * Dada `la fecha y hora de hoy 5/9/2026 14:45, una fecha y hora solicitada de 7/9/2026 14:45 y la cancha "Monumental" libre en ese horario`,
    * Cuando `el Usuario ingresa: cancha "Monumental", fecha solicitada 7/9/2026, hora solicitada 14:45 y presiona "Solicitar turno"`
    * Entonces `el sistema registra la reserva. Informa "Su turno ha sido registrado con éxito"`
* **Escenario 2**: `Solicitud de turno fallida por cancha ocupada`
    * Dada `una cancha "Bombonera" ocupada en la fecha y hora solicitada de 9/9/2026 14:45`
    * Cuando `el Usuario ingresa: cancha "Bombonera", fecha solicitada 9/9/2026, hora solicitada 14:45 y presiona "Solicitar turno"`
    * Entonces `el sistema no registra la reserva. Informa: "Cancha ocupada, por favor seleccione otro día y horario”`.
* **Escenario 3**: `Solicitud de turno fallida por insuficientes días de antelación`
    * Dada `la fecha y hora de hoy 2/9/2026 14:45, y una fecha y hora solicitada de 4/9/2026 14:44`,
    * Cuando `el Usuario ingresa: cancha "UNO", fecha solicitada 4/9/2026, hora solicitada 14:44 y presiona "Solicitar turno"`
    * Entonces `el sistema no registra la reserva. Informa: "No se pudo realizar la reserva. Todas las reservas se deben realizar con al menos 48 horas de anticipación"`

---
