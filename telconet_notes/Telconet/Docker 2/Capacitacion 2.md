# Docker Swarn

## Levantar un manager 

Seleccionar la maquina virtual que funcionara como manager y ejecutar `sudo docker swarm init` y `docker swarm init --advertise-addr {ip}`
![[Pasted image 20231008211057.png]]
Para unir un worker a un manager ejecutar el comando resaltado

para abandonar un cluster `sudo docker swarm leave --force`

listar nodos `sudo docker node ls`

Conceptos
1. Servicio:  abstrae un conjunto de tareas 
2. Tarea: una unidad de trabajo asignada a un nodo: contenedor que se ejecuta en un nodo

Plano data overlay (manager)

Antes de desplegar un servicio hay que hacer un plano overlay

`sudo docker network create --driver overlay nombreDeLaRed`

Para crear servicios dentro de la red overlay se hace

`sudo docker create service create --name nombreDelServicio --network nombreDeLaRed alpine ping 8.8.8.8`

Se crea una sola replica por defecto si no se especifica

para crear mas replicas correr: 

`sudo docker service update pinger --replicas=8`

para ver los servicios y donde en que tarea estan corriendo ejecutar:

`sudo docker service ls `

ciclo de vida de una tarea