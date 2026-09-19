## Frente

* **ID**: `Verificar vencimiento`
* **Título**: Como `empleado o gerente` quiero `verificar el vencimiento de una factura` para `saber cuánto es el monto final`.
* **Reglas de negocio**:
    * Si la factura tiene su 1er vencimiento vencido, se aplica el recargo
    * Si la factura tiene su 2do vencimiento vencido, no permite su pago

---

## Reverso
* Criterios de Aceptación (`Verificar vencimiento`)

* **Escenario 1**: `Factura no vencida`
    * Dada `la fecha de hoy siendo 9/9/26, y el sistema cuenta con los datos de una factura cuyo 1er vencimiento de la factura es el 10/9/26 y monto original de $5000`,
    * Cuando `el sistema procesa los datos que recuperó de la factura`
    * Entonces `el sistema informa que el monto final es de $5000, sin aplicar ningún recargo`
* **Escenario 2**: `Factura vencida en 1er vencimiento`
    * Dado `Dado que la fecha actual es 10/9/26 y el sistema cuenta con los datos de una factura con 1er vencimiento el 9/9/26, un recargo del 10% y un monto original de $5000`,
    * Cuando `el sistemaprocesa los datos que recuperó de la factura`
    * Entonces `el sistema informa que el monto final es de $5500, aplicando el recargo del 10%`.
* **Escenario 3**: `Factura vencida en 2do vencimiento`
    * Dado `la fecha de hoy siendo 9/9/26, y el sistema cuenta con los datos de una factura cuyo 2do vencimiento de la factura es el 10/9/26`,
    * Cuando `el sistema procesa los datos que recuperó de la factura`
    * Entonces `el sistema informa: "No se puede realizar el pago de la factura, la factura está vencida en ambos vencimientos"`

---
