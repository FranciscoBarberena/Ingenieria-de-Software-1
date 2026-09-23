## Frente

* **ID**: Solicitar Turno
* **Título**: Como socio autenticado quiero solicitar un turno para reservar mi lugar en una clase.
* **Reglas de negocio**:
    * El socio debe tener la cuota al día.

---

## Reverso
* Criterios de Aceptación (Solicitar Turno)

* **Escenario 1**: Solicitar turno con éxito
    * Dado un socio del gimnasio con la cuota al día, sin una clase registrada para el 28/9/26 a las 15:00, siendo que hay cupos libres en esa hora, en la sede Gonnet para la clase de tipo "Yoga".
    * Cuando el socio ingresa Sede "Gonnet", tipo de clase "Yoga", día "28/9/26", hora "15:00 hs" y presiona "Solicitar Turno".
    * Entonces el sistema registra la reserva e informa "Reserva Exitosa".
* **Escenario 2**: Solicitud fallida por deuda de cuota
    * Dado un socio del gimnasio sin la cuota al día,
    * Cuando ingresa Sede "Pepe", tipo de clase "Spinning", día "28/9/26", hora "19:00" y presiona "Solicitar turno"
    * Entonces el sistema informa "No se pudo realizar la reserva. Debe tener la cuota al día".
* **Escenario 3**: Solicitud fallida por turno ya reservado
    * Dado un socio con la cuota al día, con una reserva registrada para el día "28/9/26", hora 18:00
    * Cuando el socio ingresa: Sede "Gonnet", tipo "Yoga", día "28/9/26", hora 18:00 y presiona "Solicitar Turno"
    * Entonces el sistema informa "No se pudo realizar la reserva, ya tienes una reserva para el 28/9/26 a las 18:00"
* **Escenario 4**: Solicitud fallida por cupo alcanzado
    * Dado un socio con la cuota al día, siendo que la clase de Yoga en Gonnet a las 18:00 el 10/9/26 no tiene cupos libres
    * Cuando el socio ingresa Sede Gonnet, fecha 10/9/26, hora 18:00, tipo Yoga y presiona "Solicitar Turno"
    * Entonces el sistema informa "No se pudo reservar, clase llena"

