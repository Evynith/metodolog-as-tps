# TP4.-
## Ejercicio 1 
**Para cada una de las siguientes afirmaciones discuta e indique si esta es Verdadera o Falsa.**

- **Los artefactos de Scrum son el product backlog, el Sprint backlog, el Increment y las user stories.**

falso, las user histories son elementos que contiene el sprint baclog

- **La priorización del product backlog es responsabilidad del equipo de desarrollo.**

falso, esto lo hace el PO con el cliente(stakeholders) ya que es éste ultimo elq ue decide como se desarrolla la aplicacion

- **Los elementos del product backlog deben tener un grado similar de detalle.**

falso, el product backlog se va modificando a medida que pasan las iteraciones, por lo que las mas cercanas a desarrollar son las mas detalladas, mientras que las mas lejanas no necesitan aun tal grado de desarrollo.

- **El Sprint Backlog es el conjunto de items del Product Backlog seleccionados para el Sprint.**

verdadero

- **Increment es la suma de todos los items del Product Backlog completados durante un Sprint.**

falso, es el producto que quedó desarrollado al terminar de aplicar todas las tareas(items) de ese sprint y de sprints anteriores.

## Ejercicio 2 (Caso de Estudio: Telecompras)

> como cliente quiero poder ver los todos productos ofrecidos para tener un panorama de lo que hay en stock

> como cliente quiero poder acceder a un producto para obtener información de un producto en particular <br>
>> **criterio de aceptación:** deberá tener código, descripción, precio, cantidad disponibles (stock), etc

> como cliente quiero recibir el catálogo de productos para tener una noción de los productos diariamente <br>
	>> **criterio de aceptación:** deberá ser diario y deberá enviarse por correo

> como cliente quiero poder crear una orden de compra para que todos los productos que compré me lleguen juntos <br>
	>> **criterio de aceptación:**  se deberá poder pagar con tarjeta de crédito (único medio)

> como cliente quiero poder presentar una queja para que me den una solución a mi problema <br>
	>> **criterio de aceptación:** se debe permitir elegir que tipo de problema representa

> como cliente quiero poder cancelar una orden para no recibir la compra <br>
	>> **criterio de aceptación:** una vez hecho se debe hacer un reintegro del dinero pagado

> como agente quiero poder ver las órdenes de compra confirmadas para armar y empaquetar los productos de dicha orden

> como agente quiero poder determinar a logística del paquete para poder enviarse <br>
	>> **criterio aceptación:** se debe permitir seleccionar la empresa de envío para que se encargue del mismo

> como gerente de relaciones quiero poder recibir las quejas de los clientes para poder dar soluciones posibles

## Ejercicio 3 (Caso de Estudio: Biblioteca)
> como administrador quiero concederle un nivel de usuario diferente según los datos que nos proporcionan al loguearse los mismos usuarios para que tengan distintos privilegios <br>
		>> **criterio de aceptación:** el administrador debe poder verificar estos datos con una página externa de la facultad a la que pertenecen, los tipos serán: docente, no docente y estudiante 

> como socio quiero poder ver cuáles son mis condiciones de préstamo para tener en cuenta mis opciones <br>
		>> **criterio de aceptación:** las condiciones serán asociadas a el tipo de usuario, definirán la duración y el numero a ejemplares a retirar

> como socio quiero pode elegir qué tipo de usuario seré para tener los beneficios de este <br>
		>> **criterio de aceptación:** debe poder por medio de un formulario completar una serie de datos relacionados al tipo de usuario que declara ser

> como bibliotecario quiero poder suspender a un usuario que cometió infracción para no prestarle más libros <br>
		>> **criterio de aceptación:**  debe recibir notificaciones ante una devolución tardía, libro devuelto en mal estado o falsificación de datos, cada tipo de socio tendrá suspensiones diferentes según corresponda serán más o menos días

> como bibliotecario debo poder cargar el estado de un libro para penalizar por roturas a un usuario o avisar la disponibilidad de un libro <br>
		>> **criterio de aceptación:** si un bibliotecario carga un libro roto le llegara a este mismo luego un aviso de quien fue el usuario que lo ha devuelto en ese estado, si un libro está en mantenimiento el sistema lo sacara de las opciones de préstamo

> como bibliotecario quiero poder cargar libros para que puedan estar entre las opciones de disponibilidad de préstamo <br>
		>> **criterio de aceptación:** cada libro debe tener un numero identificador, isbn, titulo, autor y editorial en la que fue publicado con su fecha
        
> como usuario quiero poder ver una lista de ejemplares disponibles para el préstamo para saber cuáles puedo retirar

## Ejercicio 4 (Caso de Estudio: Cajero Automático)
> como cliente quiero poder realizar operaciones en cajeros automáticos para no tener que ir presencialmente al banco (EPIC)
>> **criterio de aceptación:** puede hacerlas en cualquiera de la red de bancos asociados

> como cliente quiero poder consultar saldo de mi cuenta para saber de cuanto efectivo dispongo
>> **criterio de aceptación:** se especificará cuanto le resta por poder sacar durante el día

> como cliente quiero poder consultar los movimientos de mi cuenta para tener un seguimiento de mi dinero
>> **criterio de aceptación:** se podrá elegir entre una fecha específica o solo los últimos

> como cliente quiero poder depositar dinero en mi cuenta para tener más dinero disponible en ella
>> **criterio de aceptación:** se contará la cantidad depositada y se actualizará el monto de dinero disponible en la cuenta

> como cliente quiero poder extraer dinero de mi cuenta para usarla físicamente
>> **criterio de aceptación:**  una vez extraído se actualizará el monto actual del cliente restándole lo extraído. No se deberá poder exceder el saldo de la cuenta. Deberá ser múltiplo del valor de los billetes.

> como cliente quiero poder transferir dinero de una cuenta a otra para pasar dinero 
>> **criterio de aceptación:** puede ser entre cuentas de diferente cliente o del mismo. Deberá ser el monto a transferir menor o igual que el dinero disponible en la cuenta.

> como cliente quiero poder registrarme como cliente valido para poder utilizar los cajeros (EPIC??)
		>> **criterio de aceptación:** el proceso es identificar la tarjeta ingresada en el cajero y verificar que el código ingresado pertenece a un banco del consorcio, el cajero debe guardar el numero de la tarjeta para relacionarla con las cuentas disponibles del usuario, el código ingresado se puede poner hasta 3 veces de haberse equivocado luego se retendrá la tarjeta.
Deberá tener un número de cuenta único asignado.

> como cliente quiero recibir un recibo de la operación efectuada para constatar el hecho
	>> **criterio de aceptación:** deberá registrarse además la operación en el sistema

## Ejercicio 5 - aplicación online para la serie Games of Thrones®.

> Como usuario quiero poder ver la lista de capítulos existentes de la serie para tener un panorama de lo que es la serie

> Como usuario quiero poder acceder a un capítulo en específico para ver los detalles del mismo
>> **criterio de aceptación:** el mismo deberá tener nombre, sinopsis, foto/s , video/s promocionales y la lista de personajes que aparecen

> Como usuario quiero poder seleccionar a un personaje para ver su información
>> **criterio de aceptación:** esta consta de biografía, nombre y escudo de su casa, fotos del mismo y capítulos en los que aparece.

> Como usuario quiero poder ver el listado de personajes que aparecen en toda la serie para poder acceder a cada uno sin buscarlo en los capítulos específicos
>> **criterio de aceptación:** se deberá poder acceder a ellos como en cada capitulo

> Como usuario quiero poder suscribirme para tener veneficios/ para poder recibir alertas irá unida a la de abajo
>> **criterio de aceptación:** se deberá ingresar un email y/o número de teléfono móvil

>Como usuario quiero poder recibir alertas de capítulos nuevos
>> **criterio de aceptación:** deberá enviarse 1hs antes de que salga el capítulo. 

## Ejercicio 6 - diario “La Pulga” - mundial Rusia 2018
> Como usuario quiero ver los partidos que se jugarán para tener un seguimiento de los mismos
>> **criterio de aceptación:** deben listarse en orden cronológico. Deberá indicar hora, estadio y ciudad donde se desarrollará cada uno. Deberá estar dentro de una sección llamada “calendario de partidos”

> Como usuario quiero elegir que se me notifique cuando un partido ya finalizó para mantenerme informado. 
>> **criterio de aceptación:** se deberá chequear cada 30 min la finalización de partidos mediante la app “MatchesScore”. En caso que haya finalizado se indica el resultado en la lista de partidos y se le manda la notificación al usuario.

> Como usuario quiero ver noticias de todo el mundial para tener un conocimiento más general del mundial
>> **criterio de aceptación:** Deberá estar dentro de una sección de “noticias” y deberán ser las mismas que están publicadas en el sitio web del diario.  
