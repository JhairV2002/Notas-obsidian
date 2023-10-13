
Una tarea es la unidad mas atomica que existe en un cluster
un servicio es un conjunto de tareas que se esta ejecutando en un conjunto de nodos

Se puede utilizar un archivo .yml para swarm

**Stack**: conjunto de servicios que se ejecuta en el cluster

En telconet se hace un stack por proyecto que comparten la misma red

`sudo docker stack deploy -c docker-composer.yml nombreDelStack`

`sudo docker stack rm NombreDelStack`

Actualizar un servicio:

`sudo docker service update NombreDelServicio --replicas=5 `

agregar la seccion deplou al archivo docker-compose.yml

![[Pasted image 20231009143839.png]]

para ejecutar un servicio de forma global (uno en cada nodo) se hace:

**nota:** un servicio replicado no puede pasar a modo global
```yml
deploy:
	mode: global
```
tambien se puede restringir la cantidad de recursos que ocupa un contenedor
```yaml
services:
	nombreDelServicio:
		...
		
```

bajar el stack 
`sudo docker stack down NombreDelStack`
La informacion va codificada en tls
