# Obtener tipos de servicio

<div style="display: flex; justify-content: space-between;">

<div style="width: 48%;">

### Información de API

- **Endpoint**: `/public/service-types`
- **Método**: `GET`
- **Descripción**: Este endpoint retorna los tipos de servicios según los filtros aplicados.

## Referencia de la solicitud:

| Atributo          | Descripción                                                                                                    | Tipo de dato  |
|-------------------|----------------------------------------------------------------------------------------------------------------|---------------|
| `page`            | (opcional) Especifica la página de tipos de servicios a ser obtenidos. Cada página retorna hasta 200 tipos de servicios. Por defecto será 1. | Number        |
| `service_types[]` | (opcional) Lista de IDs de tipos de servicios específicos para obtener detalles de esos tipos de servicios.      | String |

### Filtrado con Parámetros Repetibles

Algunos parámetros como `service_types[]` pueden enviarse **múltiples veces** en la misma solicitud para filtrar por varios ítems.

#### Ejemplo:
```bash
GET /api/service-types?service_types[]=1&service_types[]=2
```


## Tipo de respuesta: 
```Object { Array[Object, Object, ...] }```

</div>

<div style="width: 48%;">

### Ejemplo de la solicitud

```bash
curl -X GET \
	https://api-hub.tapptus.com/public/service-types \
	-H 'authorization: Bearer TOKEN' \
	-H 'cache-control: no-cache' \
	-H 'content-type: application/json' \
```

### Ejemplo de la respuesta

```json
{
    "service_types": [
        {
            "_id": "gmi2asG4pwujvfmQA",
            "name": "Field service",
            "description": "Description sample"
        },
        {
            "_id": "F43gA2c6kfG82PaRm",
            "name": "Support service",
            "description": "Description sample"
        }
    ],
    "total": 2,
    "page_size": 200,
    "page": 1,
}
```
</div>
</div>