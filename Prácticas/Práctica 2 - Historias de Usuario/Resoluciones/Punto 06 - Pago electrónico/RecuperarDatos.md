## Frente

* **ID**: `Recuperar datos`
* **Título**: Como `empleado o gerente` quiero `recuperar los datos de la factura` para `cobrarle al cliente`.
* **Reglas de negocio**:
    * 

---

## Reverso
* Criterios de Aceptación (`Recuperar datos`)

* **Escenario 1**: `Recuperación exitosa`
    * Dado `un código de pago electrónico 123 correspondiente a una factura no pagada, y las condiciones necesarias para una conexión exitosa con la central de pago`,
    * Cuando `el empleado o gerente ingresa el código 123`
    * Entonces `el sistema recupera los datos de la factura (empresa Pepe, nro de cliente 123, 1era fecha de vencimiento 7/8/26, 2da fecha de vencimiento 9/8/26, recargo 10%, y monto original $5000)`
* **Escenario 2**: `Recuperación fallida por código de pago inexistente`
    * Dado `un código de pago electrónico 1234 no correspondiente a una factura, y las condiciones necesarias para una conexión exitosa con la central de pago`,
    * Cuando `el empleado o gerente ingresa el código 1234`
    * Entonces `el sistema no recupera los datos. Informa: el código de pago 1234 no corresponde a ninguna factura`.
* **Escenario 3**: `Recuperación fallida por factura ya pagada`
    * Dado `un código de pago electrónico 12345 correspondiente a una factura ya pagada, y las condiciones necesarias para una conexión exitosa con la central de pago``,
    * Cuando `el empleado o gerente ingresa el código 12345`
    * Entonces `el sistema no recupera los datos. Informa: la factura con código de pago 12345 ya se encuentra pagada`
* **Escenario 4**: `Recuperación fallida por error en la conexión con la central de pago`
    * Dado `las condiciones necesarias para que haya un error en la conexión con la central de pago`,
    * Cuando `el empleado o gerente ingresa el código 1234`
    * Entonces `el sistema no recupera los datos. Informa: Error en la conexión con el servidor.`

---
