## Frente

* **ID**: `Reservar muebles`
* **Título**: Como `Cliente` quiero `reservar muebles` para `realizar un evento`.
* **Reglas de negocio**:
    * Una reserva tiene que tener como mínimo 3 muebles.
    * El pago de la reserva solo se puede realizar con tarjeta de crédito.
---

## Reverso
* Criterios de Aceptación (`Reservar muebles`)

* **Escenario 1**: `Reserva exitosa`
    * Dada `una reserva de 3 unidades de Silla de Madera, cuyo stock actual es 10, y las condiciones necesarias para un pago exitoso`,
    * Cuando `un Cliente ingresa la fecha 20/10/2026, lugar del evento Salón Rodriguez, cantidad de días 5, mobiliario Silla de Madera y cantidad 3, y presiona "Realizar reserva"`
    * Entonces `el sistema redirige al Cliente al pago de la reserva, espera respuesta y da de alta la reserva. Informa en pantala: "Reserva realizada exitosamente! Su número de reserva es: 024A7C"`.
* **Escenario 2**: `Reserva fallida por cantidad insuficiente de muebles`
    * Dada `una reserva de menos de 3 muebles`,
    * Cuando `un Cliente ingresa la fecha 20/10/2026, lugar del evento Salón Rodriguez, cantidad de días 5, mobiliario Silla de Madera y cantidad 2, y presiona "Realizar reserva"`
    * Entonces `la reserva no se realiza en el sistema. Se informa: no se ha podido realizar la reserva. La cantidad de muebles debe ser mayor a 2.".`
* **Escenario 3**: `Reserva fallida por error en pago.`
    * Dado `una reserva de 3 o más muebles y las condiciones no adecuadas para un pago exitoso`,
    * Cuando `un Cliente ingresa la fecha 20/10/2026, lugar del evento Salón Rodriguez, cantidad de días 5, mobiliario Silla de Madera y cantidad 3, y presiona "Realizar reserva"`
    * Entonces `el sistema redirige al Cliente al pago de la reserva, espera respuesta y no da de alta la reserva. Informa en pantala: "No se ha realizado el pago correctamente, la reserva no se pudo efectuar`.
* **Escenario 4:** `Reserva fallida por falta de stock.`
    * Dada `una reserva de 3 unidades de Silla de Madera, cuyo stock actual es 2`,
    * Cuando `un Cliente ingresa la fecha 20/10/2026, lugar del evento Salón Rodriguez, cantidad de días 5, mobiliario Silla de Madera y cantidad 3, y presiona "Realizar reserva"`
    * Entonces `el sistema no realiza ninguna reserva. Informa: No hay stock suficiente del producto Silla de Madera.`

---
