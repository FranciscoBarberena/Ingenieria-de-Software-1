## Frente

* **ID**: `Realizar check out`
* **Título**: Como `Conserje` quiero `realizar el check out` para `que el Cliente ya no esté registrado en el hotel`.
* **Reglas de negocio**:
    * Solo se puede hacer el check out de habitaciones sin gastos.

---

## Reverso
* Criterios de Aceptación (`Realizar check out`)

* **Escenario 1**: `Check out exitoso`
    * Dado `el número de habitación 34 correspondiente a una habitación ocupada y dicha habitación no teniendo gastos`,
    * Cuando `el Conserje ingresa el número de habitación 34`
    * Entonces `Se realiza el check out. Informa en pantalla: "Se ha realizado el check out con éxito". Informa a las mucamas sobre la situación.`
* **Escenario 2**: `Check out fallido por gastos pendientes`
    * Dado `el número de habitación 34 correspondiente a una habitación ocupada y dicha habitación teniendo gastos`,
    * Cuando `el Conserje ingresa el número de habitación 34`
    * Entonces `No se realiza el check out. Informa en pantalla: "No se pudo realizar el check out porque la habitación 34 tiene gastos pendientes."`
* **Escenario 3**: `Check out fallido por habitación libre`
    * Dado `el número de habitación 35 correspondiente a una habitación libre`,
    * Cuando `el Conserje ingresa el número de habitación 35`
    * Entonces `No se realiza el check out. Informa en pantalla: "No se pudo realizar el check out, la habitación 35 está libre. Por favor revise el número de habitación."`


---

