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

## Actualizar el token de acceso

Regenerar tokens usando un token de actualización válido programáticamente.

### Ejemplo

```shell
curl -X POST "https://api.activeiq.netapp.com/v1/tokens/accessToken" \
-H "accept: application/json" -H "Content-Type: application/json" \
-d "{ \"refresh_token\": \"eyJhbGciOi...O4mOTxM\"}" | jq .

{
  "access_token": "eyJhbGciOi...kG2Fxm58",
  "refresh_token": "eyJhbGc...6DHjbQ43"
}
```

Ejemplo de un comando para actualizar el token de acceso y guardar los nuevos tokens de autenticación y de refresco en las variables \$authToken y $refreshToken respectivamente.

```shell
rotateTokens=$(curl -X POST "https://api.activeiq.netapp.com/v1/tokens/accessToken" \
-H "accept: application/json" -H "Content-Type: application/json" \
-d "{ \"refresh_token\": \"$refreshToken\"}" | jq .); set -- $rotateTokens; \
authToken=$(echo $3 | tr -d ',"'); refreshToken=$(echo $5 | tr -d ',"')
```

