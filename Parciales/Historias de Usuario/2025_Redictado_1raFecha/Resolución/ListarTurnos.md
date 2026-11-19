## Frente

* **ID**: Listar Turnos
* **Título**: Como médico autenticado quiero ver mis turnos en una fecha para saber mi itinerario.
* **Reglas de negocio**:
    * La fecha debe ser del año actual

---

## Reverso
* Criterios de aceptación (Listar Turnos)

* **Escenario 1**: Listado de turnos exitoso con turnos existentes
    * Dado un médico con turnos registrados para una fecha 20/8/26, con 2026 correspondiente al año actual,
    * Cuando el médico ingresa la fecha 20/8/26 y presiona "Listar Turnos"
    * Entonces el sistema lista todos los turnos activos del médico para el 20/8/26
* **Escenario 2**: Listado de turnos exitoso sin turnos existentes
    * Dado un médico sin turnos registrados para una fecha 10/8/26, con 2026 correspondiente al año actual,
    * Cuando el médico ingresa 10/8/26 y presiona "Listar Turnos"
    * Entonces el sistema imprime "No tiene turnos activos para la fecha".
* **Escenario 3**: Listado fallido por año no corriente
    * Dada una fecha 3/10/25, con 2025 no siendo el año corriente
    * Cuando el médico ingresa 3/10/25 y presiona "Listar Turnos"
    * Entonces el sistema informa "La fecha ingresada debe corresponder al año actual".