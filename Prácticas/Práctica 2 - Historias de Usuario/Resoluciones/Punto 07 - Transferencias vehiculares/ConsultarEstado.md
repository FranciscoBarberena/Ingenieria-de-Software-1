## Frente

* **ID**: `Consultar estado`
* **Título**: Como `Usuario` quiero `consultar el estado de una transferencia` para `averiguar el dueño actual de un auto`.
* **Reglas de negocio**:
    * Se pueden hacer hasta tres consultas por mes.

---

## Reverso
* Criterios de Aceptación (`Consultar estado`)

* **Escenario 1**: `Consulta exitosa`
    * Dada `la patente FBG 089 correspondiente a un auto cuya transferencia está en el sistema, y esta siendo la primera consulta del mes`,
    * Cuando `el Usuario ingresa la patente FBG 089 y presiona "Consultar"`
    * Entonces `el sistema informa el estado de la transferencia del auto FBG 089, y decrementa la cantidad de consultas restantes en el mes a 2`
* **Escenario 2**: `Consulta fallida por patente no registrada`
    * Dada `la patente FBG 089 no registrada en ninguna transferencia del sistema, y esta siendo la primera consulta del mes`,
    * Cuando `el Usuario ingresa la patente FBG 089 y presiona "Consultar"`
    * Entonces `el sistema informa: "La patente FBG 089 no se encuentra registrada en el sistema", y decrementa la cantidad de consultas restantes en el mes a 2`.
* **Escenario 3**: `Consulta fallida por límite de consultas alcanzado`
    * Dado `que el usuario ya ha consumido su límite de 3 consultas en el mes actual`,
    * Cuando `el Usuario ingresa la patente FBG 089 y presiona "Consultar"`
    * Entonces `el sistema informa: "Límite de consultas por mes alcanzado. Vuelva el mes que viene."`

---
