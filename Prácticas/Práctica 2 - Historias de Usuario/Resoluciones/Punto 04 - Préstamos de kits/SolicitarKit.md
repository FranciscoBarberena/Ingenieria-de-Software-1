## Frente

* **ID**: `Solicitar kit`
* **Título**: Como `Usuario` quiero `solicitar un kit` para `obtener herramientas multimedia`.
* **Reglas de negocio**:
    * Los préstamos no pueden durar más de 3 horas.
    * Un usuario no puede solicitar un préstamo si tiene algún préstamo anterior activo.

---

## Reverso
* Criterios de Aceptación (`Solicitar kit`)

* **Escenario 1**: `Solicitud exitosa`
    * Dado `un Usuario sin préstamos activos, con el nuevo préstamo siendo de 2 horas`,
    * Cuando `el Usuario ingresa: tipo de kit "avanzado", día de retiro "20/10/2026", hora de retiro: "10:00", duración del préstamo (hs): 2, y presiona "Solicitar kit"`
    * Entonces `el sistema acepta la solicutd del kit. Informa en pantalla "Solicitud exitosa!"`
* **Escenario 2**: `Solicitud fallida por préstamo activo`
    * Dado `un Usuario con un préstamo activo`,
    * Cuando `el Usuario ingresa: tipo de kit "avanzado", día de retiro "20/10/2026", hora de retiro: "10:00", duración del préstamo (hs): 2, y presiona "Solicitar kit"`
    * Entonces `el sistema no acepta la soliciud del kit. Informa en pantalla "No se puedo aceptar la solicitud ya que tienes otro préstamo activo"`.
* **Escenario 3**: `Solicitud fallida por duración demasiado larga`
    * Dado `un nuevo préstamo con duración de 4 horas`,
    * Cuando `el Usuario ingresa: tipo de kit "avanzado", día de retiro "20/10/2026", hora de retiro: "10:00", duración del préstamo (hs): 4, y presiona "Solicitar kit"`
    * Entonces `el sistema no acepta la soliciud del kit. Informa en pantalla "No se puedo aceptar la solicitud, la duración máxima de un préstamo es de 3hs."`

---
