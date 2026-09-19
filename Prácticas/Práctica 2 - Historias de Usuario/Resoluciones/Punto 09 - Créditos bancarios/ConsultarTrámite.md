## Frente

* **ID**: `Consultar trámite`
* **Título**: Como `Cliente` quiero `consultar el estado de mi trámite` para `estimar el tiempo necesario hasta que termine`.
* **Reglas de negocio**:
    * Si un cliente ingresa 3 veces un código inexistente, se le bloquea el acceso al sistema por 24hs.

---

## Reverso
* Criterios de Aceptación (`Consultar trámite`)

* **Escenario 1**: `Consulta exitosa`
    * Dado `un número de comprobante 123 correspondiente a un trámite del banco`,
    * Cuando `el Cliente ingresa el número de comprobante 123, y presiona "Consultar trámite"`
    * Entonces `el sistema retorna un informe con el estado del trámite 123`
* **Escenario 2**: `Consulta fallida por número de comprobante inexistente`
    * Dado `un número de comprobante 1234 no correspondiente a un trámite del banco, y la IP actual hecho una sola consulta fallida el día de hoy 10/9/26`,
    * Cuando `el Cliente ingresa el número de comprobante 1234, y presiona "Consultar trámite"`
    * Entonces `el sistema rechaza la solicitud e informa: "Trámite inexistente"`.
* **Escenario 3**: `Consulta fallida por exceso de consultas inválidas`
    * Dado `un número de comprobante 1234 no correspondiente a un trámite del banco, y la IP actual habiendo hecho 2 consultas fallidas el día de hoy 10/9/26`,
    * Cuando `el Cliente ingresa el número de comprobante 1234, y presiona "Consultar trámite"`
    * Entonces `el sistema rechaza la solicutd, bloquea la IP del cliente por 24hs e informa: "Usted ha excedido el número de consultas inválidas"`.
* **Escenario 4**: `Consulta fallida por IP bloqueada`
    * Dado `un Cliente cuya IP ya había sido bloqueada`,
    * Cuando `el Cliente ingresa el número de comprobante 1234, y presiona "Consultar trámite"`
    * Entonces `el sistema rechaza la solicutd e informa "Usted ha excedido el número de consultas inválidas"`.


---
