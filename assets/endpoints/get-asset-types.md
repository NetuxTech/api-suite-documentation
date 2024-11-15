# Obtener Tipos de Activos

<div style="display: flex; justify-content: space-between;">

<div style="width: 48%;">

### Información de API

- **Endpoint**: `/public/asset-types`
- **Método**: `GET`
- **Descripción**: Este endpoint retorna los tipos de activos según los filtros aplicados.

## Referencia de la solicitud:

| Atributo                  | Descripción                                                                                      | Tipo de dato         |
|---------------------------|--------------------------------------------------------------------------------------------------|-----------------------|
| `page`                    | (opcional) Especifica la página de activos a obtener. Cada página retorna un conjunto de activos por defecto. Si no se especifica `page_size`, el valor por defecto será 1. | Number                |
| `page_size`               | (opcional) Especifica la cantidad de activos a obtener por página. Por defecto será 20, y el máximo puede ser 200. | Number                |


## Tipo de respuesta: 
```Object { Array[Object, Object, ...] }```

</div>

<div style="width: 48%;">

### Ejemplo de la solicitud

```bash
curl -X GET \
	https://api-hub.tapptus.com/public/asset-types  \
	-H 'authorization: Bearer TOKEN' \
	-H 'cache-control: no-cache' \
	-H 'content-type: application/json' \
```

### Ejemplo de la respuesta

```json
{
    "asset_types": [
        {
            "is_removed": false,
            "_id": "AwN2WefbgcsL3khbQ",
            "name": "Equipos",
            "id_form": "P3N5cB2pWsvbm2gKH",
            "id_account": "WKTG3GByCq7Aat4nz",
            "created_at": "2019-10-22T21:31:00.977Z",
            "updated_at": "2019-10-22T21:31:00.977Z",
            "version": 1
        },
        {
            "is_removed": false,
            "_id": "nY3gEHzo5pxiD8QCK",
            "name": "Materiales",
            "id_form": null,
            "id_account": "WKTG3GByCq7Aat4nz",
            "created_at": "2019-10-24T19:46:34.288Z",
            "updated_at": "2024-02-02T15:25:58.480Z",
            "version": 3,
            "geolicalization_active": false
        }
    ],
    "total": 2,
    "page": 1,
    "page_size": 20
}
```
</div>
</div>