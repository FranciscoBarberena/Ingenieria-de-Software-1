## Frente

* **ID**: `Visualizar estadísiticas`
* **Título**: Como `Gerente` quiero `ver las estadísticas de los impuestos y servicios cobrados` para `mejorar mi entendimiento sobre mis clientes`.
* **Reglas de negocio**:
    * Los montos se deben informar agrupando por empresa

---

## Reverso
* Criterios de Aceptación (`Visualizar estadísiticas`)

* **Escenario 1**: `Visualización exitosa`
    * Dada `la clave maestra 123 siendo la correcta y la fecha de hoy siendo 5/10/26`,
    * Cuando `el Gerente ingresa la clave 123, y el rango de fechas: 3/8/26 - 3/9/26`
    * Entonces `el sistema informa los montos y la cantidad de cobros realizados, agrupando por empresa`
* **Escenario 2**: `Visualización fallida por clave maestra incorrecta`
    * Dado `la clave maestra 1234 siendo incorrecta`,
    * Cuando `el Gerente ingresa la clave 1234, y el rango de fechas: 3/8/26 - 3/9/26`
    * Entonces `el sistema informa: "La clave ingresada es incorrecta"`
* **Escenario 3**: `Visualización fallida por rango de fechas imposible`
    * Dada `la clave maestra 123 siendo la correcta`,
    * Cuando `el Gerente ingresa la clave 123, y el rango de fechas: 3/9/26 - 3/8/26`
    * Entonces `el sistema informa: "Error en el rango de fechas. La fecha inicial no puede ser posterior a la fecha final"`
* **Escenario 4**: `Visualización fallida por rango de fechas futuro`
    * Dado `la clave maestra 123 siendo la correcta y la fecha de hoy siendo 5/5/26`,
    * Cuando `el Gerente ingresa la clave 123, y el rango de fechas: 6/5/26 - 6/6/26`
    * Entonces `el sistema informa: "Error en el rango de fechas. El rango no puede estar en el futuro"`

---
