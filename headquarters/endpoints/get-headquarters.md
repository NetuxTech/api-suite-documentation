# Obtener headquarters

<div style="display: flex; justify-content: space-between;">

<div style="width: 48%;">

### Información de API

- **Endpoint**: `/public/headquarters`
- **Método**: `GET`
- **Descripción**: Este endpoint retorna las sedes (headquarters) según los filtros aplicados.

## Referencia de la solicitud:

| Atributo         | Descripción                                                                                                  | Tipo de dato  |
|------------------|--------------------------------------------------------------------------------------------------------------|---------------|
| `page`           | (opcional) Especifica la página de sedes a ser obtenidas. Cada página retorna hasta 200 sedes. Por defecto será 1. | Number        |
| `headquarters[]` | (opcional) Lista de IDs de sedes específicas para obtener detalles de esas sedes.                             | String |
| `headquarters`   | (opcional) ID único de una sede para obtener información específica de esa sede.                              | String        |

## Tipo de respuesta: 
```Object { Array[Object, Object, ...] }```

</div>

<div style="width: 48%;">

### Ejemplo de la solicitud

```bash
curl -X GET \
	https://api-hub.tapptus.com/public/headquarters \
	-H 'authorization: Bearer TOKEN' \
	-H 'cache-control: no-cache' \
	-H 'content-type: application/json' \
}'
```

### Ejemplo de la respuesta

```json
{
    "headquarters": [
        {
            "is_default": true,
            "_id": "641126f54ef93722dc6a913d",
            "name": "General",
            "reference": "001",
            "id_color": 7,
            "address": "Miami, Florida, EE. UU.",
            "phone": "55555554",
            "related_service_types": [],
            "id": "641126f54ef93722dc6a913d"
        },
        {
            "is_default": false,
            "_id": "jFQewbp6KEL9YDwGv",
            "name": "Central",
            "reference": "002",
            "address": "Medellín, Antioquia, Colombia",
            "id_color": 5,
            "phone": "000000001",
            "related_service_types": [
                {
                    "headquarters": [
                        "jFQewbp6KEL9YDwGv"
                    ],
                    "_id": "gmi2asG4pwujvfmQA",
                    "name": "Service"
                }
            ],
            "id": "jFQewbp6KEL9YDwGv"
        }
    ],
    "page_size": 200,
    "total": 2,
    "page": 1
}
```
</div>
</div>