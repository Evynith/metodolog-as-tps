# TP1.-
## Ejercicio 1
**Describa brevemente qué significan los siguientes términos:**
1. Metodología de desarrollo de software.
2. Modelo de Ciclo de Vida para el desarrollo de software.
3. Etapa dentro de un ciclo de vida.
4. Rol que puede cumplir una persona en el desarrollo de software.
5. Modelo/Diagrama de las características de un sistema de software y sus partes componentes.<br>

**1. Metodologías de desarrollo de software:** Son procesos/metodos que se suelen seguir para lograr diseñar estrategicamente una solución o un programa específico y construir un sistema informático eficiente que cumpla con los requerimientos planteados. Para esto imponen una estructura sobre el desarrollo definiendo reglas, como será la comunicación, la manipulación de modelos y el intercambio de información o datos entre las partes involucradas. Tienen como principal objetivo aumentar la calidad del software que se produce en todas y cada una de sus fases de desarrollo. Es un marco de trabajo usado para estructurar, planificar y controlar el proceso de desarrollo en sistemas de información. <br>
**2. Modelo de Ciclo de Vida​ para el desarrollo de software:** Son modelos que indican las fases/etapas del proceso de desarrollo y el orden en el que se llevarán a cabo, representandolo de forma abstracta y proporcionando información parcial sobre el proceso. De a cuerdo a las características del producto a desarrollar será el ciclo de vida que se debe utilizar. <br>
**3. Etapa​ dentro de un ciclo de vida:** Son las distintas actividades que se realizaran durante el proceso de desarrollo de un software. Como por ejemplo, definir requerimientos, análisis, diseño, implementación y prueba, son etapas separadas.<br>
**4. Rol​ que puede cumplir una persona en el desarrollo de software:** Es la función que una persona desempeña, esta función determina las actividades que a esta persona le corresponderá realizar durante el desarrollo del software encasillandola en un área específica del proyecto.<br>
**5. Modelo/Diagrama ​de las características de un sistema de software y sus partes componentes:** (modelo/diagrama: artefacto) Es una representación de un sistema, muestra los elementos, sus componentes, las interfaces y la dependencia entre estos, su organización.

## Ejercicio 2
**Describa brevemente por qué es importante utilizar una metodología de desarrollo de software.**

Es importante utilizar una metodología de desarrollo de software porque estas aumentan la productividad del proceso, mejoran la gestión, la organización, la comunicación, la repartición de roles, la división de las tareas, adaptan de forma más eficaz el producto final logrando que se acerque más a lo que el cliente busca. Con ellas puede reducirse el número de personas innecesarias involucradas en un proyecto y acortar el tiempo de entrega, reduciendo el gasto.

## Ejercicio 3
**Enumere los modelos de ciclo de vida más comunes, para el desarrollo de software, junto con sus características principales.**

**Ciclo de Vida en Cascada:**
- Considera que las actividades (o etapas) del proceso de desarrollo: Requerimientos, análisis, diseño, implementación y prueba, son etapas separadas que para continuar con la siguiente se debe completar totalmente la anterior.
- La retroalimentación con el cliente se realiza una vez que el producto ha sido terminado.
- Es muy costoso volver a las etapas anteriores para realizar modificaciones por un malentendimiento de los requerimientos.

**Ciclo de Vida Incremental:**
- El software se desarrolla gradualmente, por funcionalidades que incrementan el producto.
- Se aplican pequeños ciclos de vida en cascada.
- Luego de cada ciclo es posible realizar una entrega de software parcial al cliente.
- solo se desarrolla, no se aplica ciclo de vida en cascada (testing, diagrama etc)

**Ciclo de Vida Iterativo:**
- Busca reducir la brecha entre las necesidades del usuario y el producto final.
- Después de cada iteración se le entrega al cliente una versión del sistema.
- El cliente evalúa el proyecto, lo corrige o propone mejoras.
- cada iteración tiene un ciclo de vida en cascada

**Ciclo de Vida Iterativo e Incremental:**
- se desarrolla de a iteraciones, pero no por versiones, sino que por funcionalidades
- luego de cada iteración se charla con el cliente

## Ejercicio 4
**Enumere las etapas de desarrollo de software más comunes que comprenden los diferentes modelos de ciclo de vida existentes para el desarrollo de software. Describa brevemente el propósito de cada una.**

- **Captura de requerimientos:** es donde el cliente expone sus necesidades y requerimientos.
- **Análisis:** se modelan los requerimientos del usuario. Se intenta transformar el lenguaje natural a lenguaje de software
- **Diseño:** se planea una solución al problema, tiene en cuenta como va a ser implementado.
- **Implementación:** se implementa el sistema, se escribe código que permitirá controlar lo que una computadora hará.
- **Testeo:** Tiene como objetivo encontrar defectos. Se valida que el producto es el que el usuario quería y se verifica si funciona correctamente.
- **Mantenimiento:** es donde se actualiza o modifica el sistema si surgen nuevos requerimientos. Es la etapa más difícil del desarrollo.

## Ejercicio 5
**Enumere los roles más comunes que puede cumplir una persona en el desarrollo de software. Describa brevemente las responsabilidades principales de cada uno.**

- **Ingeniero de requerimientos (Documentador):** trabaja con el cliente para realizar el análisis y la especificación del sistema a construir. Está capacitado para obtener claramente todos los requisitos necesarios para el desarrollo del software.
- **Analista:** Estudia el problema (de una complejidad determinada) y lo descompone en subproblemas de menor complejidad. Transforma los requisitos de usuario en requisitos de software.
- **Diseñador:** Es el encargado de generar el diseño arquitectónico y diseño detallado del sistema, basándose en los requisitos funcionales.
- **Arquitecto:** Realizan la gestión de los requisitos no funcionales y definen parte de la arquitectura de Software y la tecnología a utilizar, asegura la calidad del producto.
- **Programador:** Los programadores deben convertir la especificación del sistema en código fuente ejecutable utilizando uno o más lenguajes de programación, así como herramientas de software de apoyo a la programación. No necesita conocer el funcionamiento del sistema, solo se encarga de codificar los módulos a partir de los distintos datos de entrada y salida que se le especifican.
- **Lider de proyecto:** los lideres de proyecto se encargan de organizar las tareas a realizar por los grupos de programadores.
- **Tester:** El tester realiza las tareas de detección y eliminación de los errores y defectos del sistema en construcción.
- **Ingeniero de Manutención:** adapta los sistemas existentes de acuerdo a cambios en su ambiente externo, realiza las mejoras pedidas por los usuarios, y la adaptación del sistema para usos futuros.

## Ejercicio 6
**Enumere los factores que influyen a la hora de elegir un modelo de ciclo de vida para el desarrollo de un sistema.**

- **Características del Sistema:** Complejidad de los requerimientos, dominio de aplicación (estático o cambiante durante el desarrollo del sistema).
- **El cliente:** muchas veces el usuario decide realizar cambios en los requerimientos del sistema cuando el proyecto se encuentra muy avanzado o terminado lo que ocasiona un atraso en el proyecto, por eso es preferible no seguir un ciclo de vida estático sino adaptarse a las características del proyecto.

## Ejercicio 7
**Considere el desarrollo de un sistema cuyo dominio de aplicación es conocido, sus objetivos y requerimientos funcionales son estables y simples de comprender desde un principio, la tecnología a utilizar ya está predeterminada y es bien conocida por el equipo de desarrollo. ¿Qué tipo de modelo de ciclo de vida elegiría para el desarrollo de dicho sistema?.**

Si el sistema es pequeño y tengo que seguir un modelo con esas características elegiría un ciclo de vida en cascada, por la naturaleza tan simple del proyecto.

## Ejercicio 8
**Considere ahora el desarrollo de un sistema cuyo dominio de aplicación no es muy conocido por el equipo de desarrollo. En este caso, el cliente tampoco tiene muy claro qué es lo que quiere, de manera que los objetivos y requerimientos funcionales del sistema son inestables y difíciles de comprender. Además, el equipo de desarrollo va a utilizar una tecnología que le resulta completamente nueva. Discuta qué modelo de ciclo de vida es más apropiado.**

En este caso elegiría un ciclo de vida incremental, ya que es importante poder agregar funcionalidades luego de cada evaluación hecha por el cliente puesto que él no sabe muy bien lo que quiere y puede tener ideas nuevas a integrar en el proyecto durante el desarrollo.
 
