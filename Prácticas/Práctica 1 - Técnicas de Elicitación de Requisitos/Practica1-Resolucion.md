# Práctica 1

## Obtención de los requerimientos

### Parte 1. Definiciones

1. Un requierimiento o requisito del cliente es una característica o habilidad del sistema, que tiene la meta de satisfacer el objetivo del mismo.
2. Los requisitos pueden ser funcionales o no funcionales:
    * **Funcionales**: Son enunciados acerca de servicios que el sistema debe proveer, de cómo debería reaccionar el sistema a entradas particulares y de cómo debería comportarse el sistema en situaciones específicas. En algunos casos, también explican lo que **no** debe hacer el sistema.
    * **No funcionales**: Son limitaciones sobre servicios o funciones que ofrece el sistema. Incluyen restricciones tanto de temporización y del proceso de desarrollo, como impuestas por los estándares. Los requerimientos no funcionales se suelen aplicar al sistema como un todo, más que a características o a servicios individuales del sistema.
        * Ejemplos: rendimiento, seguridad y uso de almacenamiento.
3. Un *stakeholder* es una persona que se ve afectada por el sistema, ya sea de manera directa o indirecta.
4. Las fuentes más importantes para obtener información sobre los requerimientos son:
    * Documentos
    * Los propios *stakeholders*
    * Especifiaciones de sistemas similares, es decir, que cumplen un objetivo parecido al nuestro.
5. Los tres puntos de vista genéricos en un proyecto de *software* son:
    * **Interactuadores**: personas o sistemas que interaccionan directamente con el sistema. Puede que afecten los requisitos del mismo.
    * **Indirectos**: *stakeholders* que no interactúan directamente con el sistema, pero influyen en los requisitos del mismo.
    * **Dominio**: son las características y restricciones del ambiente que afectan los requisitos del sistema. Serían como las "reglas del juego".
6. Tres ejemplos de posibles problemas en la comuncación con el cliente serían:
    * Dificultad del cliente para expresar claramente las necesidades.
    * Realización de simplificaciones excecisvas por parte del desarrollador.
    * Falta de entendimiento del dominio por parte del desarrollador.
### Parte 2. Situaciones

#### Punto A

1. En un sistema de registro de asistencia a través de técnicas biométricas (huella digital) de estudiantes universitarios para la cátedra de Ingeniería I. Este sistema se alimentará de un listado otorgado por la oficina de alumnos de la facultad. Además, necesita la autorización del Jefe de Trabajos Prácticos del turno correspondiente para luego los alumnos poder registrar el presente. También, el profesor a cargo de la materia podrá consultar y listar el estado de cada alumno perteneciente a su cátedra. El sistema sólo se utilizará en el ámbito de la facultad de Informática y deberá adecuarse a la reglamentación sobre privacidad de los datos en el ámbito de la misma. 
    * **DUDAS:**
        * **que pasa con la oficina de alumnos? participan en la creacion del sistema pero no se ven afectados por la implementación del mismo**
        * **Las fuentes de informacion se refiere a la fuente de requerimientos? no incluiria siempre a los interactuadores directos? ya que ellos usan el sistema, obtener feedback de ellos sería la mejor manera de entender los requierimientos**
        * **La reglamentración (el dominio) cuenta como fuente de info. para los requerimientos?**
    * **Stakeholders**: Los estudiantes de la cátedra, los JTPs, los profesores y la oficina de alumnos.
    * **Puntos de vista**: 
        * Interactuadores: Los estudiantes y los profesores
        * Indirectos: La oficina de alumnos y los JTPs. No interactúan con el sistema, pero deben proveer el listado en el que el mismo se basa, o autorizar su uso en el caso de los JTPs.
        * Dominio: La reglamentación sobre privacidad de datos de la Facultad de Informática.
    * **Fuentes de información:** Para obtener información sobre los requerimientos del sistema, se le podría preguntar a los interactuadores directos.

2. Se desea desarrollar un sistema para gestionar y administrar la atención de pacientes en una clínica privada especializada en tratamientos alérgicos. Cuando un paciente nuevo es ingresado a la clínica, el empleado registra todos sus datos personales, posteriormente un enfermero registra los controles y realiza las anotaciones habituales (temperatura, presión, peso, reacciones alérgicas etc.). Luego, el paciente es derivado con alguno de los doctores de la clínica, quién registra qué tratamientos deberá realizar. El médico también se encarga de registrar si el paciente debe quedar internado y debe mantener su historia clínica durante el período que dure el tratamiento. Se sabe que el director de la clínica puede consultar las historias clínicas de todos los pacientes. El sistema debe adecuarse a las normativas impuestas por el ministerio de salud de la provincia de Bs As.
    * **Stakeholders**: Los pacientes, los empleados que registran los datos, los enfermeros, los doctores, el director de la clínica.
    * **Puntos de vista**: 
        * Interactuadores: Los empleados, doctores, enfermeros y el director de la clínica
        * Indirectos: Los pacientes. No interactúan con el sistema, pero sus datos se registran en él, por lo que se ven afectados por su correcto o incorrecto funcionamiento.
        * Dominio: Las normativas del ministerio de la salud de la provincia de Buenos Aires.
    * **Fuentes de información:** Para obtener información sobre los requerimientos del sistema, se le podría preguntar a los interactuadores directos.

#### Punto B

* En la situación A, podría suceder que los profesores deseen un sistema en el que la asistencia únicamente se contabilice si el alumno se mantuvo en la totalidad de la clase. Es decir, tendrían que apoyar su huella tanto al principio como al final de la misma. En cambio, los alumnos podrían preferir un sistema más flexible, en el que solo se requiera apoyar la huella en una de las 2 ocasiones.
* En la situación B, podría suceder que un paciente sienta vergüenza ante alguna consulta médica. En ese caso, desearía que sus datos solo sean accesibles a los médicos, enfermeros y empleados con los que interactúa directamente, y que estos no sean visibles al director de la clínica. Por el contrario, dicho director podría desear tener acceso a la mayor cantidad posible de información, para poder administrar sus recursos de una mejor manera.

## Entrevistas
 

