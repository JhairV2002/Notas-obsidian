si el proceso es automatico, es decir, se ha encontrado una caja en un radio de 300m el estado pasa a factible, en caso de que no, se hace un proceso manual y el espado pasa a factibilidad en proceso.

una vez dada la factibilidad se procese a convertir en **Orden de trabajo** los servicios ingresados

el departamento de PYL (planificacion) agenda la visita con el cliente a traves de HAL, un sistema que ayuda a escoger el mejor horario.

Se asigna fecha y hora para la visita junto con el departamento de OU (Operacion urbana).

Cuando PYL ya asigna una cuadrilla se crea una tarea automatica (instalacion).

El que corta y activa el producto es middleware (Megadatos).

La cancelacion es cuando se le retira **TODA** la conexion del cliente, se genera una solicitur de retiro de equipo.

primero se ejecuta un job en la base de datos: toma todos los clientes que esten en estado **In-corte** con mas de 45 dias en dicho estado.

Guarda la informacion en las estructuras de Telcos.
(es un proceso masivo)

NAF es el aplicativo de inventario para las solicitudes de retiro o de instalacion 