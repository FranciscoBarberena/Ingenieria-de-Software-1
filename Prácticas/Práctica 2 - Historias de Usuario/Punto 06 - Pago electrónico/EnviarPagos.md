## Frente

* **ID**: `Enviar pagos`
* **Título**: Como `Gerente` quiero `enviar los pagos a la central de cobro` para `que estos queden registrados`.
* **Reglas de negocio**:
    * Las transacciones solo pueden enviarse una vez por día.
    * 

---

## Reverso
* Criterios de Aceptación (`Enviar pagos`)

* **Escenario 1**: `Envío exitoso de transacciones`
    * Dada `la clave maestra 123 siendo la correcta, las transacciones de hoy aún sin enviar y las condiciones necesarias para una conexión exitosa con la central de cobro`,
    * Cuando `el gerente ingresa la clave 123 y presiona "Enviar"`
    * Entonces `el sistema envía las transacciones del día a la central de pago. Espera respuesta. Luego marca dichas transacciones como ya enviadas.`
* **Escenario 2**: `Envío fallido por clave incorrecta`
    * Dado `la clave maestra 1234 siendo incorrecta`,
    * Cuando `el gerente ingresa la clave 1234 y presiona "Enviar"`
    * Entonces `el sistema no se conecta con la central. Informa: "La clave ingresada es incorrecta"`.
* **Escenario 3**: `Envío fallido por transacciones ya enviadas`
    * Dado `la clave maestra 123 siendo la correcta y las transacciones de hoy ya enviadas`,
    * Cuando `el gerente ingresa la clave 123 y presiona "Enviar"`
    * Entonces `el sistema no se conecta con la central. Informa: "Las transacciones de hoy ya han sido enviadas. Por favor vuelva mañana"`
* **Escenario 4**: `Envío fallido por error de conexión con la central`
    * Dado `la clave maestra 123 siendo la correcta, las transacciones de hoy aún sin enviar y las condiciones necesarias para una conexión fallida con la central de cobro``,
    * Cuando `el gerente ingresa la clave 123 y presiona "Enviar"`
    * Entonces `el sistema no se conecta con la central y no marca las transacciones como enviadas. Informa: "Hubo un error en la conexión con la central. Inténtelo de nuevo"`

---
