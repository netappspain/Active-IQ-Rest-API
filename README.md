# Active IQ Rest API
Ejemplos Rest API para el acceso a información de NetApp Active IQ

* [Uso de variables en los ejemplos](README.md)
* [Actualizar el token de acceso](token.md)
* [Número de sistemas](systems.md)
* [Estado de los sistemas](health.md)
* [Información de la capacidad](/capacity.md)
* [Información de la eficiencia](/efficiency.md)
* [Componentes a actualizar](/upgrade.md)
* [Información de rendimiento](/performance.md)

## Uso de variables en los ejemplos

Los ejemplos están basados en la el uso de variables de una shell. Se muestran en todos los ejemplos la información para un único sistema basado en el número de serie del equipo con la variable $serialNumber, y para todos los sistemas que una misma empresa tenga con la variable \$customerID. Ésta última se corresponde con el identificador que NetApp tiene de cada cliente, y que puede conocerse a través de la URL al acceder al Active IQ de cada cliente a través de un navegador web.

https://mysupport.netapp.com/myautosupport/dist/index.html#/pages/dashboard/customer/1000000

La autenticación de todas las llamadas API se realizan usando el token con la variable \$authToken, y el refresco del token se realiza con la variable $refreshToken.

Estas cuatro variables se inicializan en primer lugar desde la shell con el valor correspondiente.

```shell
customerID=1000000

serialNumber=600000000000

authToken=eyJhbGciOi...kG2Fxm58

refreshToken=eyJhbGc...6DHjbQ43
```


