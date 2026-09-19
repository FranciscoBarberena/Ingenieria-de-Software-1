## Frente

* **ID**: `Iniciar sesión`
* **Título**: Como `Usuario` quiero `iniciar sesión` para `entrar a mi cuenta`.
* **Reglas de negocio**:

---

## Reverso
* Criterios de Aceptación (`Iniciar sesión`)

* **Escenario 1**: `Inicio de sesión exitoso`
    * Dado `un código 123456 vigente y correspondiente al mail ingresado`,
    * Cuando `el Usuario ingresa el código 123456 y presiona "Iniciar sesión"`
    * Entonces `el sistema accede a la aplicación, y registra la fecha y hora del inicio de sesión`
* **Escenario 2**: `Inicio de sesión fallido por código expirado`
    * Dado `un código 654321 expirado, previamente correspondiente al mail ingresado`,
    * Cuando `el Usuario ingresa el código 654321 y presiona "Iniciar sesión"`
    * Entonces `el sistema no inicia la sesión. Informa "No se pudo iniciar sesión. Su código es incorrecto o expiró"`.
* **Escenario 3**: `Inicio de sesión fallido por código incorrecto`
    * Dado `un código 798456, nunca correspondiente al mail ingresado`,
    * Cuando `el Usuario ingresa el código 798456 y presiona "Iniciar sesión"`
    * Entonces `el sistema no inicia la sesión. Informa "No se pudo iniciar sesión. Su código es incorrecto o expiró"`.

---
