# TP5.-
**Lista de Conceptos Tratados: Actor; Caso de Uso; Especificación de Casos de Uso; Curso básico y alternativos de un Caso de Uso; Generalización/Especialización de Actores; Relaciones entre Casos de Uso: Generalización, Extensión, e Inclusión.**

## Ejercicio 5.1 
**Considere el siguiente diagrama de casos de uso.**

![Diagrama](/assets/Screenshot_20220815_163841.png "Red celular")

**Nombre cada uno de los elementos de notación o sintaxis que están presentes en dicho diagrama. ⮚ Describa brevemente qué interpreta de dicho diagrama.**

**Actores:** Son los que activan/inician los casos de uso, en este caso hay 2, cliente y red celular. Cumplen un rol <br>
**casos de uso:** son cada una de las funcionalidades del sistema<br>
**relaciones:** muestran que hay una relación, puede ser de activación (actor - CU), de inclusión o de extensión (entre CUs) --activación != relación <br>
**relación de extensión:** se da cuando un CU no puede solucionar una funcionalidad por sí mismo, se representa demostrando la condición por la cual es activada
Como no incluye descripción no se puede saber a ciencia cierta cual es el actor secundario, pero aun asi es facil de interpretar.
Un cliente requiere usar un sistema de celular el cual incluye enviar mensajes, atender y recibir llamadas y la posibilidad de hacer llamadas grupales. En caso de hacer una llamada grupal, esta funcionalidad va a requerir que cuando se quieran agregar receptores se les haga una llamada.
La red celular será actor secundario de cada una de los CU ya que es quien provee el servicio.

## Ejercicio 5.2 (Caso de Estudio: Telecompras) 

**Identifique actores y casos de uso para el sistema de procesamiento de órdenes de compra, a partir de la narrativa descrita. Construya el diagrama de casos de uso correspondiente. 
⮚ Especifique de forma breve, en un párrafo, cada uno de los casos de uso en su diagrama. ⮚ Extienda la siguiente especificación, que describe el flujo normal de eventos en un caso de uso del sistema, para incorporar flujos alternativos o lo que considere faltante.**

**Nombre de Caso de Uso:** “Ingresar Orden de Compra” <br>
**Descripción:** Este caso de uso describe el proceso por medio del cual un cliente ingresa una orden de compra al sistema. <br>
**Actor Principal:** Cliente <br>
**Actores Secundarios:** Sistema de Control de Inventario, Sistema Financiero <br>
**Trigger:** El caso de uso comienza cuando el cliente desea ingresar una orden de compra <br>
**Flujo de Eventos Flujo Normal o Básico:** <br>
1) El caso de uso comienza cuando el cliente desea ingresar una orden de compra. 
2) El sistema solicita el ingreso de los datos de una orden de compra (datos personales y códigos de productos) personales
3) El cliente ingresa sus datos personales (nombre, dni, y dirección donde quiere recibir los productos siendo ordenados). 
3.1) El sistema solicita el ingreso de los códigos de producto 
4) El cliente ingresa los códigos de productos que quiere ordenar. 
5) Por cada código de producto ingresado 
a. El sistema obtiene información del producto (descripción, stock y precio por unidad), interactuando con el sistema de inventario. 
b. El sistema presenta la descripción, stock y el precio por unidad del producto. 
c. El cliente ingresa la cantidad requerida de dicho producto. 
d. El sistema calcula el total a cobrar para dicho producto (= precio unitario x cantidad) 
e. El sistema acumula el total para el producto en el total de la orden de compra. fin iteración 
f. fin iteración 
5.1) El sistema solicita los datos de pago
6) El cliente ingresa información de su tarjeta de crédito para el pago de la orden (número y dirección de recibo de facturas). 
6.1) El sistema verifica la tarjeta ingresada con el sistema financiero
7) El sistema crea la orden con un número unívoco. 
8) El sistema registra la orden en estado pendiente. 
9) El sistema carga a la cuenta de la correspondiente tarjeta el total de la orden de compra, interactuando con el sistema financiero. 
10) El sistema registra la orden en estado confirmada. 
11) El sistema presenta el número de la orden al cliente, y el caso de uso termina. 
12) El caso de uso finaliza
flujo alternativo: 
6.1) El sistema verifica la tarjeta ingresada con el sistema financiero
	6.2) la tarjeta es rechazada
6.3) El sistema muestra un error
6.4) vuelve al punto 5.1

**flujo alternativo:** <br>
5)c. El cliente ingresa la cantidad requerida de dicho producto. <br>
	c.1) no hay stock <br>
	c.2) fin de la iteración <br>

**⮚ Especifique de forma detallada el caso de uso correspondiente a la cancelación de una orden de compra. Incluya flujo de eventos básico, y alternativos.**

**Nombre de Caso de Uso:** “Cancelar Orden de Compra” <br>
**Descripción:** Este caso de uso describe el proceso por medio del cual un cliente cancela una orden de compra al sistema luego de haberla hecho.  <br>
**Actor Principal:** Cliente <br>
**Actores Secundarios:** Sistema de Control de Inventario, Sistema Financiero <br>
**Trigger:** El caso de uso comienza cuando el cliente desea cancelar una orden de compra <br>
**Flujo de Eventos Flujo Normal o Básico:** <br>
1) El caso de uso comienza cuando el cliente desea cancelar una orden de compra. 
2) El sistema solicita el ingreso de los datos personales
3) El cliente ingresa sus datos personales (nombre, dni, y dirección donde quiere recibir los productos siendo ordenados). 
4) El sistema lista las órdenes de compra de ese cliente. Por cada orden se detallan los productos, la cantidad de cada uno y el precio **LO DEL LISTADO QUIZÁS NO VAYA, EL SISTEMA DEBE PEDIR DATOS Y EL USUARIO INGRESARLOS, EL DESARROLLADOR LUEGO ELIGE SI MOSTRAR COMO LISTA Y SI EL USUARIO LO SELECCIONA O INGRESA EL DATO
4.1) El cliente indica cual quiere cancelar
4.2) El sistema revisa con la empresa de transporte que la orden no haya sido despachada
5) Por cada código de producto ingresado 
a. El sistema obtiene información del producto (cantidad)
b. El sistema revierte stock de ese producto, interactuando con el sistema de inventario. 
f. fin iteración 
6) El sistema reembolsa el monto total mediante el sistema bancario 
8) El sistema registra la orden en estado cancelado. 
11) El sistema informa que ha sido cancelada
12) El caso de uso finaliza
flujo alternativo: 
4.2) El sistema revisa con la empresa de transporte que la orden no haya sido despachada
	4.3) la orden ha sido despachada
4.4) El sistema muestra un error 
4.5) caso de uso finaliza

**Precondición :** que el cliente haya hecho al menos una orden de compra <br>

draw.io

## Ejercicio 5.3 (Caso de Estudio: Biblioteca) 
**⮚ Identifique actores y casos de uso a partir de la narrativa descripta. Construya el diagrama de casos de uso correspondiente.**

draw.io

**⮚ Especifique de forma detallada, los casos de uso correspondientes: al préstamo de un ejemplar de libro a un socio; y a la devolución de un ejemplar. Incluya flujo de eventos básico, y alternativos. 
(pedir libro, devolver libro, consultar disponibilidad)**

**Nombre del caso de uso:** pedir libro <br>
**Descripción:** Este caso de uso describe el proceso por medio del cual un socio puede pedir prestado un libro de la biblioteca <br>
**Actor principal:** socio <br>
**Trigger:** el caso de uso comienza cuando el socio quiere retirar un libro <br>
**Curso básico:** <br>
1) el caso de uso comienza cuando el socio quiere retirar un libro
2) el sistema verifica que el socio no esté suspendido
<br> ptoExt <br>
3) el sistema muestra la cantidad y fecha de devolución según el tipo de socio
4) el sistema solicita el número de ejemplares a retirar
5) el socio ingresa un número de ejemplares a retirar
6) el sistema asigna un numero de prestamo
7) el sistema le asigna una fecha de dia limite al préstamo
8) el sistema actualiza el stock de ese ejemplar
<br>fin del caso de uso

**Curso alternativo:** <br>
2) el sistema verifica que el socio no esté suspendido <br>
	2.1) el socio está suspendido <br>
	2.2) el sistema muestra un mensaje de error <br>
	2.3) fin del caso de uso <br>
**Curso alternativo:** <br>
9) el sistema verifica el número de ejemplares del préstamo según stock y tipo de socio (dividir en 2, stock y tipo de socio son dos cosas distintas) <br>
	9.1) el socio ingresó más cantidad de la que puede retirar <br>
	9.2)el sistema muestra un error <br>
	9.3) vuelve al punto 5) <br>
**Suposición:** el socio está logueado (para saber su tipo), sino debe pedir el tipo de usuario

**Nombre del caso de uso:** consultar disponibilidad <br>
**Actor primario:** socio <br>
**Trigger:** el caso de uso comienza cuando el socio requiere consultar la disponibilidad de un libro <br>
**Curso básico:** <br>
1) El sistema solicita el código único del libro a prestar
2) el socio ingresa el código
3) el sistema verifica cuáles ejemplares de ese libro no están en mantenimiento
4) el sistema muestra la cantidad disponibles de ejemplares
<br>fin del caso de uso

**Curso alternativo:**
        3) el sistema verifica cuáles ejemplares de ese libro no están en mantenimiento <br>
	3.1) no hay ejemplares disponibles <br>
	3.2) el sistema muestra un mensaje de indisponibilidad <br>
	3.3) fin del caso de uso <br>
**Casos de uso extendidos:**
Extiende a “pedir libro” , cuando el socio quiere saber la disponibilidad de un libro

**Nombre del caso de uso:** devolver libro <br>
**Descripción:** Este caso de uso describe el proceso por medio del cual un socio devuelve un libro <br>
**Actor principal:** socio <br>
**Trigger:** el caso de uso comienza cuando el socio quiere devolver un libro <br>
**Curso básico:**
1) el caso de uso comienza cuando el socio quiere devolver un libro
2) el sistema solicita el numero de prestamo (si esta logueado el sistema puede mostrar el listado y el usuario debe elegir) **LO DEL LISTADO QUIZÁS NO VAYA, EL SISTEMA DEBE PEDIR DATOS Y EL USUARIO INGRESARLOS, EL DESARROLLADOR LUEGO ELIGE SI MOSTRAR COMO LISTA Y SI EL USUARIO LO SELECCIONA O INGRESA EL DATO
3) el sistema repone el stock de cada uno de los ejemplares devueltos
4) el sistema revisa la fecha de devolución
5) el sistema asigna el préstamo como devuelto
<br> fin del caso de uso

**Curso alternativo:**
4) el sistema revisa la fecha de devolución <br>
4.1) la devolución se hizo luego de la fecha asignada <br>
4.2) el sistema revisa que tipo de socio es <br>
4.2) el sistema marca al socio como suspendido según su tipo <br>
4.3) el sistema muestra un aviso de suspensión <br>
4.3) el curso continua en el punto 5) <br>

**Suposición:** el socio está logueado (para saber su tipo), sino debe pedir el tipo de usuario

## Ejercicio 5.4 (Caso de Estudio: Cajero Automático)
**Identifique actores y casos de uso a partir de la operatoria descripta para un cajero automático. Construya el diagrama de casos de uso correspondiente. 
⮚ Especifique en detalle los casos de uso correspondientes a: la extracción de un monto de dinero de una cuenta; al depósito de un monto de dinero en una cuenta; y a la transferencia de un monto entre dos cuentas de un mismo cliente y un mismo banco.**

draw.io

**Nombre del caso de uso:** extraer dinero <br>
**Descripción:** Este caso de uso describe el proceso por medio del cual un cliente del banco puede extraer dinero de su cuenta <br>
**Actor principal:** cliente <br>
**Actor secundario:** sistema consorcio bancario <br>
**Trigger:** el caso de uso comienza cuando el cliente quiere retirar dinero de su cuenta <br>
**Curso básico:**
1) [INCLUDE] Obtener monto involucrado
2) el sistema corrobora que el monto ingresado no exceda al saldo actual
3) el sistema consulta el dinero disponible en el cajero (monto y tipos de  billetes)
4) el sistema verifica que el monto ingresado sea múltiplo del valor de los billetes que el cajero entrega
5) el sistema verifica que puede entregar esa cantidad de dinero
6) el sistema le entrega el dinero por el monto ingresado al cliente
7) [INCLUDE] Registrar operación
<br> fin del caso de uso

**Curso alternativo:** 
2) el sistema corrobora que el monto ingresado no exceda al saldo actual <br>
	2.1) el monto excede el saldo de la cuenta <br>
	2.2) el sistema devuelve un mensaje <br>
	2.3) vuelve al punto 1) <br>

**Curso alternativo:**
3) el sistema consulta el dinero disponible en el cajero (monto y tipos de  billetes) <br>
	3.1) el cajero no tiene dinero <br>
	3.2) el sistema muestra un mensaje de error <br>
	3.3) fin del caso de uso <br>

**Curso alternativo:**
4) el sistema verifica que el monto ingresado sea múltiplo del valor de los billetes que el cajero entrega <br>
	4.1) el monto ingresado no corresponde con lo que puede entregar el cajero <br>
	4.2) el sistema muestra las opciones posibles <br>
	4.3) el cliente elige una de las opciones <br>
	4.4) vuelve al punto 5) <br>

**Curso alternativo:**
5) el sistema verifica que puede entregar esa cantidad de dinero
	5.1) el cajero no tiene dinero suficiente <br>
	5.2) el sistema muestra un mensaje de error <br>
	5.3) fin del caso de uso <br>

**Precondición:** la cuenta debe tener suficiente saldo para realizar un retiro de dinero, el cajero debe tener dinero <br>
**Suposiciones:** El cliente ya está ingresado en el sistema con una cuenta válida <br>
**Casos de uso incluidos:** Obtener monto involucrado, Registrar operación <br>

**Nombre del caso de uso:** depositar dinero <br>
**Descripción:** Este caso de uso describe el proceso por medio del cual un cliente del banco puede depositar dinero en su cuenta <br>
**Actor principal:** cliente <br>
**Actor secundario:** sistema consorcio bancario <br>
**Trigger:** el caso de uso comienza cuando el cliente quiere depositar dinero en su cuenta <br>
**Curso básico:**
1) [INCLUDE] Obtener monto involucrado
2) el sistema muestra un mensaje de que se realizó la acción de manera satisfactoria
3) [INCLUDE] Registrar operación
<br> fin del caso de uso

**Suposiciones:** El cliente ya está ingresado en el sistema con una cuenta válida <br>
**Casos de uso incluidos:** Obtener monto involucrado, Registrar operación


**Nombre del caso de uso:** transferir dinero <br>
**Descripción:** Este caso de uso describe el proceso por medio del cual un cliente del banco puede transferir dinero a otra cuenta <br>
**Actor principal:** cliente <br>
**Actor secundario:** sistema consorcio bancario <br>
**Trigger:** el caso de uso comienza cuando el cliente quiere depositar dinero en su cuenta <br>
**Curso básico:**
1) [INCLUDE] Obtener monto involucrado
2) el sistema corrobora que el monto ingresado no exceda al saldo actual
3) el sistema pregunta al cliente el tipo de cuenta (propia o ajena)
4) el cliente elije cuenta propia
5) el sistema le lista las cuentas a las cuales puede transferir (con número de cuenta)
6) el cliente elige
7) el sistema muestra un mensaje de que se realizó la acción de manera satisfactoria
8) [INCLUDE] Registrar operación
<br> fin del caso de uso

**Curso alternativo:**
2) el sistema corrobora que el monto ingresado no exceda al saldo actual <br>
	2.1) el monto excede el saldo de la cuenta <br>
	2.2) el sistema devuelve un mensaje <br>
	2.3) vuelve al punto 1) <br>

**Curso alternativo:**
3) el sistema pregunta al cliente el tipo de cuenta (propia o ajena) <br>
	3.1) el cliente elige cuenta ajena <br>
	3.2) el sistema consulta el número de cuenta <br>
	3.3) el usuario ingresa un número de cuenta <br>
	3.4) el sistema valida que exista esa cuenta <br>
	3.5) vuelve al paso 7) <br>
	**Curso alternativo:**
		3.4) el sistema valida que exista esa cuenta <br>
			3.4.1) el numero ingresado no es un cliente válido <br>
			3.4.2) el sistema muestra un error <br>
			3.4.3) vuelve al punto 3.2) <br>

**Precondición:** la cuenta debe tener suficiente saldo para realizar una transferencia <br>
**Suposiciones:** El cliente ya está ingresado en el sistema con una cuenta válida <br>
**Casos de uso incluidos:** Obtener monto involucrado, Registrar operación <br>
*obtener monto involucrado tendría un curso alternativo de error en caso que no se pueda obtener el monto, y registrar operación hace que se manden todos los datos al sistema bancario, se trae de ahi el codigo de registro e imprime el ticket

## Ejercicio 5.5 
**Considere nuevamente los ejercicios 5.2 a 5.4 de este trabajo práctico. ⮚ Revise, y extienda de ser necesario, sus diagramas y especificaciones de casos de uso para: a) Expresar, si fuera posible, relaciones entre los casos de uso existentes. b) Abstraer o especializar casos de uso, o bien factorizar comportamiento común o variantes en nuevos casos de uso.**

hecho!
 
