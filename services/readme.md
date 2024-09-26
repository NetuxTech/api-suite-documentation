# API de Servicios

La API de servicios de Suite permite interactuar con los datos de servicios registrados en tu cuenta empresarial. A través de estos endpoints, podrás obtener información sobre los servicios existentes o crear nuevos en el sistema.

---

## Endpoints

- [Obtener servicios](/services/endpoints/get-services.md) : ```GET /public/services```
- [Crear servicios](/services/endpoints/create-service.md) : ```POST /public/services```


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
