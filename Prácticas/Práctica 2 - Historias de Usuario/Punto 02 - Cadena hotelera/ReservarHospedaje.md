## Frente

* **ID**: `Reservar hospedaje`
* **Título**: Como `Usuario` quiero `reservar un hospedaje` para `irme de viaje`.
* **Reglas de negocio**:
    * La fecha de ingreso debe estar dentro de los 90 días de la fecha actual.
    * Las estadías no pueden durar más de 15 días.

---

* Duda: pongo la fecha de hoy? ya que dice que tiene que ser dentro de 90 dias desde la fecha actual.
* Qué pasa con el pago? enunciado no da detalles
* Tiene que haber un orden de prioridades en los criterios de aceptacion?? No entiendo como se define cuando 2 criterios no se cumplen a la vez

## Reverso
* Criterios de Aceptación (`Reservar hospedaje`)

* **Escenario 1**: `Reserva exitosa`
    * Dada `la fecha de hoy 2/9/2026, la fecha de ingreso 10/9/2026, la fecha de egreso 17/9/2026 y el hotel elegido "Hotel Morales" con espacio`,
    * Cuando `el Usuario ingresa: fecha de ingreso 10/9/2026, fecha de egreso 17/9/2026, hotel elegido "Hotel Morales" y cantidad de huéspedes 4`
    * Entonces `el sistema envía un *mail* con el código de reserva 0874BD y un enlace para continuar con el pago.`
* **Escenario 2**: `Reserva fallida por fecha de ingreso muy lejana`
    * Dada `la fecha de hoy 2/9/2026 y la fecha de ingreso 10/9/2027`,
    * Cuando `el Usuario ingresa: fecha de ingreso 10/9/2027, fecha de egreso 17/9/2027, hotel elegido "Hotel Morales" y cantidad de huéspedes 4`
    * Entonces `No se realiza la reserva. Informa: "No se ha podido realizar la reserva. La fecha de ingreso debe estar dentro de los 90 días de la fecha actual."`.
* **Escenario 3**: `Reserva fallida por estadía demasiado larga`
    * Dada `la fecha de hoy 2/9/2026, la fecha de ingreso 10/9/2026 y la fecha de egreso 17/10/2026`,
    * Cuando `el Usuario ingresa: fecha de ingreso 10/9/2026, fecha de egreso 17/10/2026, hotel elegido "Hotel Morales" y cantidad de huéspedes 4`
    * Entonces `No se realiza la reserva. Informa: "No se ha podido realizar la reserva. Las estadías no pueden durar más de 15 días."`
* **Escenario 4**: `Reserva fallida por hotel lleno`
    * Dado `el hotel elegido "Hotel Morales" sin espacio`,
    * Cuando `el Usuario ingresa: fecha de ingreso 10/9/2026, fecha de egreso 17/9/2026, hotel elegido "Hotel Morales" y cantidad de huéspedes 4`
    * Entonces `No se realiza la reserva. Informa: "No se ha podido realizar la reserva. El hotel elegido "Hotel Morales" está lleno"`

---
