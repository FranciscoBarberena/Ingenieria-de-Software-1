## Frente

* **ID**: `Registrar docente`
* **Título**: Como `Docente` quiero `registrarme en el sistema` para `inscribirme a un concurso`.
* **Reglas de negocio**:
    * El mail debe ser único y será utilizado como nombre de usuario.
    * El DNI debe estar entre 12 y 55 millones

---

## Reverso
* Criterios de Aceptación (`Registrar docente`)

* **Escenario 1**: `Registro exitoso`
    * Dado `un DNI 43.455.212 no registrado y un mail pepe@gmail.com no registrado`,
    * Cuando `el Docente ingresa: DNI 43.455.212, mail pepe@gmail.com, nombre pepe, apellido gonzales y presiona "Registrarse"`
    * Entonces ` el sistema crea la cuenta, y envía a la casilla de correo pepe@gmail.com la contraseña asignada 0254`
* **Escenario 2**: `Registro fallido por mail ya registrado`
    * Dado `un mail pepe@gmail.com ya registrado`,
    * Cuando `el Docente ingresa: DNI 43.455.212, mail pepe@gmail.com, nombre pepe, apellido gonzales y presiona "Registrarse"`
    * Entonces `el sistema no crea la cuenta, e informa: "El mail pepe@gmail.com ya se encuentra registrado"`.
* **Escenario 3**: `Registro fallido por DNI ya registrado`
    * Dado `un DNI 43.455.212 ya registrado`,
    * Cuando `el Docente ingresa: DNI 43.455.212, mail pepe@gmail.com, nombre pepe, apellido gonzales y presiona "Registrarse"`
    * Entonces `el sistema no crea la cuenta, e informa: "El DNI 43.455.212 ya se encuentra registrado"`
* **Escenario 4**: `Registro fallido por DNI fuera del rango establecido por el estatuto de la UNLP`
    * Dado `un DNI 56.455.212, fuera del rango de 12-55 millones`,
    * Cuando `el Docente ingresa: DNI 56.455.212, mail pepe@gmail.com, nombre pepe, apellido gonzales y presiona "Registrarse"`
    * Entonces `el sistema no crea la cuenta, e informa: "El DNI del titular de la cuenta debe estar entre los 12 y 55 millones"`

---
