1. Inicar las mquinas virtuales con el archivo a importar
2. editar el archivo /etc/hosts y agregar las lineas de las ips de las demas maquinas virtuales
	1. ip nombre.de.la.red.de.la.maquina.virtual
3. Setear las ips estaticas a las maquinas virtuales con nmtui 
	1. ![[Pasted image 20231008204003.png]]
	2. ![[Pasted image 20231008204050.png]]
	3. ![[Pasted image 20231008204121.png]]
	4. Setear a manual ![[Pasted image 20231008204304.png]]
	5. Ir a Show
	6. Setear los diferentes valores que se necesite
		1. Para saber cual es el gateway para la salida a internet se usa `ìp route show` en la parte de default
		2. el dns puede ser el mismo gateway
		3. ![[Pasted image 20231008204654.png]]
	7. Dar click en ok