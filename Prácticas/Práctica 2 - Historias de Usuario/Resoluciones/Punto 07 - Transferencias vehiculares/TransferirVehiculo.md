## Frente

* **ID**: `Transferir vehículo`
* **Título**: Como `Usuario` quiero `transferir la propiedad de un vehículo` para `que se efectúe una venta`.
* **Reglas de negocio**:
    * El comprador debe ser mayor de 18 años.
    * El vendedor debe ser mayor de 18 años.
    * La patente no debe tener deudas.

---

## Reverso
* Criterios de Aceptación (`Transferir vehículo`)

* **Escenario 1**: `Transferencia exitosa`
    * Dada `la patente FBG 089 correspondiente a un auto sin deudas, el DNI de comprador 1245745 correspondiente a un mayor de 18 años y el DNI de vendedor 1345785 correspondiente a un mayor de 18 años`,
    * Cuando `el Usuario ingresa la patente FBG 089, el DNI de comprador 1245745 y el DNI de vendedor 1345785 y presiona "Transferir"`
    * Entonces `el sistema envía al mail del comprador con DNI 1245745 el código ABC para que realice el pago`
* **Escenario 2**: `Transferencia fallida por deudas pendientes`
    * Dado `la patente FBG 088 correspondiente a un auto con una deuda pendiente`,
    * Cuando `el Usuario ingresa la patente FBG 088, el DNI de comprador 1245745 y el DNI de vendedor 1345785 y presiona "Transferir"`
    * Entonces `el sistema informa: No se puede continuar con la transferencia, el auto FBG 088 tiene una deuda pendiente`.
* **Escenario 3**: `Transferencia fallida por comprador menor de edad`
    * Dado `el DNI de comprador 5245745 correspondiente a un menor de 18 años`,
    * Cuando `el Usuario ingresa la patente FBG 089, el DNI de comprador 5245745 y el DNI de vendedor 1345785 y presiona "Transferir"`
    * Entonces `el sistema informa: No se puede continuar con la transferencia, el DNI del comprador debe corresponder a un mayor de 18 años`
* **Escenario 4**: `Transferencia fallida por vendedor menor de edad`
    * Dado `el DNI de vendedor 5245745 correspondiente a un menor de 18 años`,
    * Cuando `el Usuario ingresa la patente FBG 089, el DNI de comprador 1345785 y el DNI de vendedor 5245745 y presiona "Transferir"`
    * Entonces `el sistema informa: No se puede continuar con la transferencia, el DNI del vendedor debe corresponder a un mayor de 18 años`
* **Escenario 5**: `Transferencia fallida por patente inexistente`
    * Dado `la patente XX 545 RW no correspondiente a ningún auto`,
    * Cuando `el Usuario ingresa la patente XX 545 RW, el DNI de comprador 1245745 y el DNI de comprador 1345785 y presiona "Transferir"`
    * Entonces `el sistema informa: Error: no existe el auto con patente XX 545 RW.`

---
