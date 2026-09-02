## Frente

* **ID**: `Realizar check in`
* **Título**: Como `Cliente` quiero `hacer el check in` para `entrar al hotel`.
* **Reglas de negocio**:
    * Los check in únicamente pueden realizarse entre las 10:00 y las 23:59.

---
* Duda escenario 2: tengo que escribir qué se le envió al conserje y a los botones?? o con eso alcanza
* DUDA: escenario 4, el sistema deberia estar en standby?? que pongo en el cuando?? no deberia estar leyendo codigos.
## Reverso
* Criterios de Aceptación (`Realizar check in`)

* **Escenario 1**: `Check in exitoso`
    * Dado `un código de reserva 054AC correspondiente a una reserva para la fecha de hoy (2/9/2026), con la hora actual siendo 20:54`,
    * Cuando `el Cliente ingresa el código 054AC`
    * Entonces `Se asigna la habitación 34. Informa en pantalla "Se le ha asignado la habitación 34 con éxito!". Luego informa a un conserje y a los botones sobre la situación`
* **Escenario 2**: `Check in fallido por código de reserva no correspondiente a una reserva`
    * Dado `un código de reserva 215 no correspondiente a una reserva, con la hora actual siendo 20:54`,
    * Cuando `el Cliente ingresa el código 215`
    * Entonces `No se asigna ninguna habitación. El sistema informa en pantalla: "El código 215 no corresponde a ninguna reserva. Por favor revise su código"`.
* **Escenario 3**: `Check in fallido por código de resreva no corrspondiente a una reserva de hoy`
    * Dado `un código de reserva 054AD correspondiente a una reserva para la fecha de mañana (3/9/2026), con la hora actual siendo 20:54`,
    * Cuando `el Cliente ingresa el código 054AD`
    * Entonces `No se asigna ninguna habitación. El sistema informa en pantalla "El código 054AD corresponde a una reserva para el día 3/9/2026. Por favor regrese ese día entre las 10:00 y las 23:59"`
* **Escenario 4**: `Check in fallido por horario fuera de rango`
    * Dada `la hora actual siendo la 1:00`,
    * Cuando `nada ocurre???` 
    * Entonces `el sistema informa: HORARIO DE CHECK IN: 10:00 - 23:59. Por favor regrese más tarde.`

---

