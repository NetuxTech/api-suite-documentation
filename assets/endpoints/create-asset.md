# Crear Activo

<div style="display: flex; justify-content: space-between;">

<div style="width: 48%;">

### Información de API

- **Endpoint**: `/public/assets`
- **Método**: `POST`
- **Descripción**: Este endpoint crea un un activo según los parámetros.


## Referencia de la solicitud:


| Atributo      | Descripción                                                                                               | Tipo de dato | Obligatorio |
|---------------|-----------------------------------------------------------------------------------------------------------|--------------|-------------|
| `asset_type`  | Especifica el tipo de activo a crear, permitiendo clasificar el activo bajo un tipo específico.           | String       | Sí          |
| `reference`   | Código de referencia único para el activo.                                                                | String       | Sí          |
| `name`        | Nombre del activo, utilizado para identificarlo fácilmente.                                               | String       | Sí          |
| `company`     | (opcional) ID de la compañía a la cual pertenece el activo.                                               | String       | No          |
| `form`        | (opcional) Objeto que puede contener información adicional específica sobre el activo, en formato de formulario. | Object       | No          |
   |


## Tipo de respuesta: 
```Object { Object }```

</div>

<div style="width: 48%;">

### Ejemplo de la solicitud

```bash
curl -X POST \
	https://api-hub.tapptus.com/public/assets \
	-H 'authorization: Bearer TOKEN' \
	-H 'cache-control: no-cache' \
	-H 'content-type: application/json' \
    -d '{
        "name": "Activo XXYYZZ",
        "asset_type": "55xs3yroBgTyfqFAN",
        "reference": "12340987"
    }'
```

### Ejemplo de la respuesta

```json
{
    "asset": {
        "_id": "6736861858438f00c80a215c",
        "asset_type": "55xs3yroBgTyfqFAN",
        "reference": "12340987",
        "name": "Activo XXYYZZ",
        "form": { },
        "created_at": "2024-11-14T23:22:00.775Z",
        "updated_at": "2024-11-14T23:22:23.679Z",
    }
}
```
</div>
</div>