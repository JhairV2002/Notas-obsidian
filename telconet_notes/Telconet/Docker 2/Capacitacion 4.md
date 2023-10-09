Ciclo de vida de un servicio 
![[Pasted image 20231009002339.png]]
Servicio como solo lectura (por serguridad el servicio debe ser solo de lectura)
`sudo docker service update nombreDelServicio --read-only `
Eliminar un servicio:
`sudo docker service rm NombreDelServicio`
Crear un servicio y exponer el puerto 
`sudo docker service create --punlish 8080:8080 --replicas 3 NombreDeLaIMagenDelContenedor`
Balancear
`sudo docker service create --punlish 8080:8080 --replicas 3 NombreDeLaIMagenDelContenedor`

Se pude tener el mismo puerto externo pero el puerto interno del contenedor debe ser diferente
ejm: 
- 8080:80
- 8081:80
Se mapea el puerto 80 a los servicios en el puerto 8080 8081
