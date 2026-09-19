## Frente

* **ID**: `Solicitar código`
* **Título**: Como `Usuario` quiero `solicitar un código` para `iniciar sesión`.
* **Reglas de negocio**:
    * La cuenta del usuario debe estar activa.

---

## Reverso
* Criterios de Aceptación (`Solicitar código`)

* **Escenario 1**: `Solicitud de código exitosa sin otro código vigente`
    * Dado `un mail pepe@gmail.com ya registrado y activo, que no ha realizado ninguna solicitud de código en los últimos 5 minutos`,
    * Cuando `el usuario ingresa el mail pepe@gmail.com y presiona "Solicitar código"`
    * Entonces `el sistema registra la solicitud, genera el código 123456, con una vigencia máxima de 5 minutos y lo envía al mail pepe@gmail.com. Informa "Su código ha sido enviado al mail ingresado"`
* **Escenario 2**: `Solicitud de código exitosa con otro código vigente`
    * Dado `un mail pepe2@gmail.com ya registrado y activo, que ha realizado una solicitud de código hace 3 minutos`,
    * Cuando `el usuario ingresa el mail pepe2@gmail.com y presiona "Solicitar código"`
    * Entonces `el sistema registra la solicitud, hace que el código generado hace 3 minutos pierda su validez, y genera el nuevo código 123465, con una vigencia máxima de 5 minutos y lo envía al mail pepe2@gmail.com. Informa "Su código ha sido enviado al mail ingresado"`.
* **Escenario 3**: `Solicitud de código fallida por mail no registrado`
    * Dado `un mail pepe3@gmail.com no registrado`,
    * Cuando `el usuario ingresa el mail pepe3@gmail.com y presiona "Solicitar código"`
    * Entonces `el sistema no registra la solicitud. Informa "No se pudo realizar la solicitud. El mail ingresado no se encuentra registrado`
* **Escenario 4**: `Solicitud de código fallida por cuenta inactiva`
    * Dado `un mail pepe4@gmail.com ya registrado e inactivo`,
    * Cuando `el usuario ingresa el mail pepe4@gmail.com y presiona "Solicitar código"`
    * Entonces `el sistema no registra la solicitud. Informa "No se pudo realizar la solicitud. La cuenta correspondiente al mail ingresado se encuenta inactiva"`

---
