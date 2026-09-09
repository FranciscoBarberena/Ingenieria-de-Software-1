## Frente

* **ID**: `Imprimir listado de inscriptos`
* **Título**: Como `jefe del área de concursos` quiero `imprimir el listado de los docentes inscriptos al concurso de una materia` para `poder enviar dicho listado al secretario administrativo`.
* **Reglas de negocio**:
    * El listado de inscriptos debe seguir el formato del SIU Guaraní

---

## Reverso
* Criterios de Aceptación (`Imprimir listado de inscriptos`)

* **Escenario 1**: `Impresión exitosa`
    * Dada `una materia "Matemática 1" con 20 docentes inscriptos a su concurso`,
    * Cuando `el jefe del área de concursos selecciona matemática 1 y presiona "imprimir listado"`
    * Entonces `el sistema imprime la lista de los 20 docentes inscriptos`
* **Escenario 2**: `Impresión fallida por falta de inscriptos`
    * Dado `una materia "Matemática 2" con 0 docentes inscriptos a su concurso`,
    * Cuando `el jefe del área de concursos selecciona matemática 2 y presiona "imprimir listado"`
    * Entonces `el sistema no imprime nada. Informa en pantalla: "El concurso de Matemática 2 no contiene docentes inscriptos"`.


---
