## Frente

* **ID**: `Inscribir a concurso`
* **Título**: Como `Docente` quiero `inscribirme a un concurso` para `conseguir un cargo de docencia`.
* **Reglas de negocio**:
    * Un docente no puede inscribirse a más de 3 concursos.

---

## Reverso
* Criterios de Aceptación (`Inscribir a concurso`)

* **Escenario 1**: `Inscripción exitosa`
    * Dado `un Docente 1234@gmail.com que no se ha inscripto a ningún concurso`,
    * Cuando `el docente selecciona el concurso "Matemática 1" y presiona "Inscribirse"`
    * Entonces `el sistema registra la inscripción e imprime el comprobante de inscripción`
* **Escenario 2**: `Inscripción fallida por límite de inscripciones alcanzado`
    * Dado `un Docente ya inscripto a 3 concursos (Matemática 1, 2 y 3)`,
    * Cuando `el docente selecciona el concurso "Matemática 4" y presiona "Inscribirse"`
    * Entonces `el sistema no registra la inscripicón. Informa: Error: Límite de inscripciones a concursos ya alcanzado`.
* **Escenario 3**: `Inscripción fallida por inscripción ya realizada`
    * Dado `un docente inscripto en el concurso Matemática 1`,
    * Cuando `el docente selecciona el concurso "Matemática 1" y presiona "Inscribirse"`
    * Entonces `el sistema no registra la inscripción. Informa: "Error: ya estás inscripto al concurso de Matemática 1"`


---
