## Frente

* **ID**: `Pagar con tarjeta`
* **Título**: Como `Cliente` quiero `pagar con tarjeta` para `realizar una reserva de muebles`.
* **Reglas de negocio**:
    * Sólo se aceptan números correspondientes a tarjetas de crédito.

---

## Reverso
* Criterios de Aceptación (`Pagar con tarjeta`)
* **Escenario 1**: `Pago exitoso`
    * Dada `la conexión con el servidor del banco exitosa, el número 1234 correspondiente a una tarjeta de crédito y la tarjeta con fondos suficientes para el pago`,
    * Cuando `el Cliente ingresa el número de tarjeta 1234 y presiona “Pagar”`
    * Entonces `el sistema registra el pago y retorna un resultado de éxito.`
* **Escenario 2**: `Pago fallido por número de tarjeta de crédito inexistente`
    * Dado `la conexión con el servidor del banco exitosa y el número 3456 no corresponde a un número de tarjeta de crédito`,
    * Cuando `el Cliente ingresa el número de tarjeta 3456 y presiona “Pagar”`
    * Entonces `el sistema retorna un error por número de tarjeta inexistente.`
* **Escenario 3**: `Pago fallido por fondos insuficientes de tarjeta de crédito`
    * Dada `a conexión con el servidor del banco exitosa, el número de tarjeta 2134 correspondiente a una tarjeta de crédito y sin fondos suficientes para el pago que se solicita hacer`,
    * Cuando `el Cliente ingresa el número de tarjeta 2134 y presiona “Pagar”`
    * Entonces `el sistema retorna un error por fondos insuficientes.`
* **Escenario 4**: `Pago fallido por fallo en la conexión con el servidor externo del banco`
    * Dada `la conexión con el servidor del banco fallida`,
    * Cuando `el Cliente ingresa un número de tarjeta y presiona “Pagar”`
    * Entonces `el sistema retorna un error por conexión no establecida.`
---
