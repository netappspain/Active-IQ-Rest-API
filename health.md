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

## Estado de los sistemas

Información sobre sistemas con riesgos.

### Ejemplo para un único sistema

```shell
curl -X GET "https://api.activeiq.netapp.com/v1/health/details/level/serial_numbers/id/$serialNumber" \
-H "accept: application/json" -H "authorizationToken: $authToken" | jq .
```

### Ejemplo para todos los sistemas de una empresa

```shell
curl -X GET "https://api.activeiq.netapp.com/v1/health/details/level/customer/id/$customerID" \
-H "accept: application/json" -H "authorizationToken: $authToken" | jq .

```
