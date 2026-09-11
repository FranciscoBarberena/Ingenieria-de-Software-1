## Frente

* **ID**: `Iniciar trámite`
* **Título**: Como `Cliente` quiero `iniciar un trámite` para `pedir un crédito`.
* **Reglas de negocio**:
    * El monto solicitado no puede superar los $400.000.
    * El DNI ingresado debe corresponder a un cliente del banco.

---

## Reverso
* Criterios de Aceptación (`Iniciar trámite`)

* **Escenario 1**: `Inicio de trámite exitoso`
    * Dado `un DNI 44454475 correspondiente a un cliente del banco`,
    * Cuando `el Cliente ingresa: DNI 44454475, nombre Pepe, apellido Gonzales, mail pepe@gmail.com, tipo de crédito "personal", monto solicitado $300.000 y presiona "Iniciar trámite"`
    * Entonces `el sistema almacena el trámite e imprime: "número de comprobante: 0548"`
* **Escenario 2**: `Inicio de trámite fallido por monto demasiado alto`
    * Dado `un DNI 45454475 correspondiente a un cliente del banco`,
    * Cuando `el Cliente ingresa: DNI 45454475, nombre Pepe, apellido Gonzales, mail pepe@gmail.com, tipo de crédito "personal", monto solicitado $400.000 y presiona "Iniciar trámite"`
    * Entonces `el sistema rechaza el inicio de trámite y muestra el mensaje “El monto solicitado excede el límite permitido`.
* **Escenario 3**: `Inicio de trámite fallido por DNI no correspondiente a un Cliente`
    * Dado `un DNI 47454475 no correspondiente a un cliente del banco`,
    * Cuando `el Cliente ingresa: DNI 47454475, nombre Pepe, apellido Gonzales, mail pepe@gmail.com, tipo de crédito "personal", monto solicitado $300.000 y presiona "Iniciar trámite"`
    * Entonces `el sistema rechaza el inicio del trámite y envía un mail a pepe@gmail.com con un instructivo para hacerse cliente del banco. Informa en pantalla: "No se pudo iniciar el trámite ya que usted no es cliente del banco. Por favor revise su mail para hacerse cliente"`

---

