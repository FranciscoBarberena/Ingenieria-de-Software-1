## Frente

* **ID**: `Registrar persona`
* **Título**: Como `Persona` quiero `registrarme en el sitio web` para `reservar turnos en canchas de tenis`.
* **Reglas de negocio**:
    * El mail será utilizado como nombre de usuario.
    * Solo se pueden registrar personas mayores de edad.

---

## Reverso
* Criterios de Aceptación (`Registrar persona`)

* **Escenario 1**: `Registro exitoso`
    * Dado `un mail pepe@gmail.com no registrado, y una edad de 18 años`,
    * Cuando `la Persona ingresa: nombre Pepe, apellido Gonzales, mail pepe@gmail.com, edad 18 años, domicilio calle 457, y presiona "Registrarse"`
    * Entonces `el sistema registra a la persona. Luego se genera una contraseña y se envía al mail pepe@gmail.com. Informa: "¡Registro exitoso! Revise su casilla de mail para obtener la contraseña"`
* **Escenario 2**: `Registro fallido por mail ya registrado`
    * Dado `un mail pepeRegistrado@gmail.com ya registrado previamente`,
    * Cuando `la Persona ingresa: nombre Pepe, apellido Gonzales, mail pepeRegistrado@gmail.com, edad 18 años, domicilio calle 457, y presiona "Registrarse"`
    * Entonces `el sistema no registra un nuevo usuario. Informa en pantalla: "La cuenta pepeRegistrado@gmail.com ya se encuentra registrada. Por favor inicie sesión"`.
* **Escenario 3**: `Registro fallido por menoría de edad`
    * Dado `un mail pepe2@gmail.com no registrado, y una edad de 17 años`,
    * Cuando `la Persona ingresa: nombre Pepe, apellido Gonzales, mail pepe2@gmail.com, edad 17 años, domicilio calle 457, y presiona "Registrarse"`
    * Entonces `el sistema no registra un nuevo usuario. Informa en pantalla: "La edad mínima para crear una cuenta es de 18 años.`
      

---
