# API de Servicios

La API de servicios de Suite permite interactuar con los datos de servicios registrados en tu cuenta empresarial. A través de estos endpoints, podrás obtener información sobre los servicios existentes o crear nuevos en el sistema.

---

## Endpoints

- [Obtener servicios](/services/endpoints/get-services.md) : ```GET /public/services```
- [Crear un servicio](/services/endpoints/create-service.md) : ```POST /public/services```
- [Actualizar un servicio](/services/endpoints/update-service.md) : ```PATCH /public/services/{id}```
- [Actualizar el estado de un servicio](/services/endpoints/update-status.md) : ```PATCH /public/services/status/{id}```


## Diccionarios

### Estados de los servicios

| Estado                   | ID |
|--------------------------|--------|
| Asignado                 | 1      |
| Pendiente de asignación   | 2      |
| Lanzado a concurso        | 3      |
| Aceptado                 | 4      |
| Rechazado                | 5      |
| En proceso               | 6      |
| En revisión              | 7      |
| Finalizado               | 8      |
| Cancelado                | 9      |
| En petición              | 10     |
| No completado            | 11     |
