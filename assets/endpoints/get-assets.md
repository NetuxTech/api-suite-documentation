# Obtener Activos

<div style="display: flex; justify-content: space-between;">

<div style="width: 48%;">

### Información de API

- **Endpoint**: `/public/assets`
- **Método**: `GET`
- **Descripción**: Este endpoint retorna los activos según los filtros aplicados.

## Referencia de la solicitud:

| Atributo                  | Descripción                                                                                      | Tipo de dato         |
|---------------------------|--------------------------------------------------------------------------------------------------|-----------------------|
| `page`                    | (opcional) Especifica la página de activos a obtener. Cada página retorna un conjunto de activos por defecto. Si no se especifica `page_size`, el valor por defecto será 1. | Number                |
| `page_size`               | (opcional) Especifica la cantidad de activos a obtener por página. Por defecto será 20, y el máximo puede ser 200. | Number                |
| `asset_type`              | (obligatorio) Especifica el tipo de activo a obtener, permitiendo filtrar los resultados por un grupo específico de activos. | String                |
| `assets_ids[]`            | (opcional) Lista de IDs específicos de activos para filtrar los resultados y retornar solo los activos indicados. | Array de Strings      |


### Filtrado con Parámetros Repetibles

Algunos parámetros como `assets_ids[]` puede enviarse **múltiples veces** en la misma solicitud para filtrar por varios ítems.

#### Ejemplo:
```bash
GET /public/assets?assets_ids[]=1&assets_ids[]=2
```

## Tipo de respuesta: 
```Object { Array[Object, Object, ...] }```

</div>

<div style="width: 48%;">

### Ejemplo de la solicitud

```bash
curl -X GET \
	https://api-hub.tapptus.com/public/assets?asset_type=55xs3yroBgTyfqFAN  \
	-H 'authorization: Bearer TOKEN' \
	-H 'cache-control: no-cache' \
	-H 'content-type: application/json' \
```

### Ejemplo de la respuesta

```json
{
    "assets": [
        {
            "_id": "NXyDo5mm",
            "asset_type": "55xs3yroBgTyfqFAN",
            "status": 1,
            "form": {
                "title": "Info dirección",
                "fields": [
                    {
                        "id": 1,
                        "reference": "",
                        "type": "object",
                        "label": "Serial",
                        "typeTextField": 1,
                        "obligatory": false,
                        "icon": "mdi mdi-format-text",
                        "color": "#4CAF50",
                        "isVisibleMobile": true,
                        "idInput": "06298559",
                        "value": "HJOP64KL"
                    }
                ]
            },
            "reference": "12340987",
            "name": "Activo 1",
            "company": "aLFTutJbP",
            "created_at": "2024-11-14T20:52:07.072Z",
            "updated_at": "2024-11-14T20:53:11.538Z"
        }
    ],
    "total": 1,
    "page_size": 20
}
```
</div>
</div>