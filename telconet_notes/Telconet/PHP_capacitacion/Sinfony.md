
## Controllers

Estan en la ruta **src/AppBundle/Controller** 
![[Pasted image 20231006162332.png]]
de esta forma se retornan vistas o a su vez una respuesta json.
## Servicios

Creacion de servicios en sinfony:
1. Declararlo en services.yml
![[Pasted image 20231006161244.png]]
2. Crear el servicio dentro de **AppBundle/Services/ServiceName.php**

Para poder hacer
## Ver Rutas

sinfony profile

## Sentencias SQL


escribir sentencias sql en general con doctrine (no importa si se cambia de base de datos van a funcionar igual)

Para utilizar doctrine desde la linea de comandos y crear una entidad en php y una tabla en mysql ejecutar:
**No se puede mandar en telcos la linea de comando por tema de seguridad de Oracle**
```bash
php app/console doctrine:generate:entity
```

![[Pasted image 20231006163758.png]]

crea una carpeta Enttiy con la entidad creada  y una carpeta Repository para la conexion a la base de datos 

con el siguiente comando se sincronizara la base de datos con lo que se creo en doctrine 

```bash
php app/console doctrine:schema:update --force
```

Tambien se puede hacer ingenieria inversa para traer las entidades desde la base de datos 

![[Pasted image 20231006170718.png]]

Pra poder hacer peticiones a la base de datos se utiliza la inyeccion de dependencias a traves del archivo .yml

![[Pasted image 20231006171802.png]]
Y dentro del service se recepta la dependencia
![[Pasted image 20231006171833.png]]
Enlazar el repositorio a la entidad
![[Pasted image 20231006172205.png]]

obtener datos de la base 

![[Pasted image 20231006172420.png]]
para poder serializar todo a un formato json que pueda ser consumido hay que realizarlo manualmente o implementanto una clase llamada Serializer al entity 

![[Pasted image 20231006173329.png]]

![[Pasted image 20231006173614.png]]

tambien se puede recuperar datos a trves de querybuilder directamente en el repositorio 

![[Pasted image 20231006174920.png]]![[Pasted image 20231006175316.png]]

Recuperando datos a travez de Native Query

![[Pasted image 20231006175950.png]]
