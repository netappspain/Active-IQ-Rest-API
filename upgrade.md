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

## Componentes a actualizar

Información sobre los sistemas que son candidatos para actualizaciones para la versión ONTAP, el firmware de la placa base, el firmware del disco y el firmware de la bandeja.

### Ejemplo para un único sistema

```shell
curl -X GET "https://api.activeiq.netapp.com/v1/upgrade/summary/level/serial_numbers/id/$serialNumber" \
-H "accept: application/json" -H "authorizationToken: $authToken" | jq .

```

### Ejemplo para todos los sistemas de una empresa

```shell
curl -X GET "https://api.activeiq.netapp.com/v1/upgrade/summary/level/customer/id/$customerID" \
-H "accept: application/json" -H "authorizationToken: $authToken" | jq .

```
