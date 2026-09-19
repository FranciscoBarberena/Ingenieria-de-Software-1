## Frente

* **ID**: `Mostrar listado`
* **Título**: Como `Gerente` quiero `pedir un listado de créditos aprobados entre fechas` para `conocer el estado de mi negocio`.
* **Reglas de negocio**:


---

## Reverso
* Criterios de Aceptación (`Mostrar listado`)

* **Escenario 1**: `Solicitud exitosa`
    * Dado `la fecha de hoy 10/9/26, y que existen 3 créditos aprobados entre el 4/7/26 y el 4/8/26`,
    * Cuando `el Gerente ingresa el rango de fechas: 4/7/26 - 4/8/26 y presiona "Mostrar listado"`
    * Entonces `el sistema muestra una lista de los 3 créditos aprobados`
* **Escenario 2**: `Solicitud fallida por falta de créditos en el rango`
    * Dado `que no hubo solicitudes de créditos aprobadas entre el 4/4/26 y el 4/5/26`,
    * Cuando `el Gerente ingresa el rango de fechas: 4/4/26 - 4/5/26 y presiona "Mostrar listado`
    * Entonces `el sistema informa: "No hay créditos aprobados en las fechas ingresadas"`.
* **Escenario 3**: `Solicitud fallida por rango de fechas imposible`
    * Dado `?????????`,
    * Cuando `evento`
    * Entonces `resultado`
* **Escenario 4**: `títuloEscenario`
    * Dado `contexto`,
    * Cuando `evento`
    * Entonces `resultado`
* **Escenario 5**: `títuloEscenario`
    * Dado `contexto`,
    * Cuando `evento`
    * Entonces `resultado`
* **Escenario 6**: `títuloEscenario`
    * Dado `contexto`,
    * Cuando `evento`
    * Entonces `resultado`
* **Escenario 7**: `títuloEscenario`
    * Dado `contexto`,
    * Cuando `evento`
    * Entonces `resultado`
* **Escenario 8**: `títuloEscenario`
    * Dado `contexto`,
    * Cuando `evento`
    * Entonces `resultado`
* **Escenario 9**: `títuloEscenario`
    * Dado `contexto`,
    * Cuando `evento`
    * Entonces `resultado`
* **Escenario 10**: `títuloEscenario`
    * Dado `contexto`,
    * Cuando `evento`
    * Entonces `resultado`

---
