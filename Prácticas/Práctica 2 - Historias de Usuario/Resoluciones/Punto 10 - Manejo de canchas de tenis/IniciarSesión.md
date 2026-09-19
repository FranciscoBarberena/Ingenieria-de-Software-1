## Frente

* **ID**: `Iniciar sesión`
* **Título**: Como `Usuario` quiero `iniciar sesión` para `resrevar turnos en la cancha de tenis`.
* **Reglas de negocio**:
    * Si el inicio de sesión falla 3 veces, la cuenta del Usuario queda bloqueada.

---

## Reverso
* Criterios de Aceptación (`Iniciar sesión`)

* **Escenario 1**: `Inicio de sesión exitoso`
    * Dado `un mail pedro@gmail.com ya registrado, una contraseña 1234 correspondiente con la asignada y 2 intentos de inicio de sesión fallidos previamente`,
    * Cuando `el Usuario ingresa: mail pedro@gmail.com, contraseña 1234 y presiona "Iniciar sesión"`
    * Entonces `el sistema inicia la sesión y redirige al usuario a la pantalla de inicio`
* **Escenario 2**: `Inicio de sesión fallido por mail no registrado`
    * Dado `un mail pedro2@gmail.com no registrado`,
    * Cuando `el Usuario ingresa: mail pedro2@gmail.com, contraseña 12345 y presiona "Iniciar sesión"`
    * Entonces `el sistema se mantiene en la página de inicio de sesión e informa: "Mail y/o contraseña incorrecta. Revise sus datos"`.
* **Escenario 3**: `Inicio de sesión fallido por contraseña incorrecta`
    * Dado `un mail pipo@gmail.com ya registrado, una contraseña 12345 no correspondiente con la asignada, y 1 intento de inicio de sesión fallido previamente`,
    * Cuando `el Usuario ingresa: mail pipo@gmail.com, contraseña 12345 y presiona "Iniciar sesión"`
    * Entonces `el sistema registra un nuevo intento fallido. Se mantiene en la página de inicio de sesión e informa: "Mail y/o contraseña incorrecta. Revise sus datos"`
* **Escenario 4**: `Inicio de sesión fallido por límite de intentos alcanzado`
    * Dado `un mail pedro4@gmail.com ya registrado, una contraseña 1234 no correspondiente con la asignada y 2 intentos de inicio de sesión fallidos previamente`,
    * Cuando `el Usuario ingresa: mail pedro4@gmail.com, contraseña 1234 y presiona "Iniciar sesión"`
    * Entonces `el sistema no inicia sesión y bloquea la cuenta de pedro4@gmail.com. Informa "Límite de intentos alcanzado, su cuenta ha sido bloqueada"`

---
