# Actualizar Activo

<div style="display: flex; justify-content: space-between;">

<div style="width: 48%;">

### Información de API

- **Endpoint**: `/public/assets/{asset_id}`
- **Método**: `PATCH`
- **Descripción**: Este endpoint actualiza un un activo según los parámetros.


## Referencia de la solicitud:

| Atributo      | Descripción                                                                                               | Tipo de dato | Obligatorio |
|---------------|-----------------------------------------------------------------------------------------------------------|--------------|-------------|
| `asset_type`  | (opcional) Especifica el tipo de activo, permitiendo clasificar el activo bajo un tipo específico.           | String       | No          |
| `reference`   | (opcional) Código de referencia único para el activo.                                                                | String       | No          |
| `name`        | (opcional) Nombre del activo, utilizado para identificarlo fácilmente.                                               | String       | No          |
| `company`     | (opcional) ID de la compañía a la cual pertenece el activo.                                               | String       | No          |
| `form`        | (opcional) Objeto que puede contener información adicional específica sobre el activo, en formato de formulario. | Object       | No          |
   |
| `status`        | (opcional) Estado del activo. └ 0: `Inactivo` └ 1: `Activo` | Entero       | No          |
   |


## Tipo de respuesta: 
```Object { Object }```

</div>

<div style="width: 48%;">

### Ejemplo de la solicitud

```bash
curl -X PATCH \
	https://api-hub.tapptus.com/public/assets/6736861858438f00c80a215c \
	-H 'authorization: Bearer TOKEN' \
	-H 'cache-control: no-cache' \
	-H 'content-type: application/json' \
    -d '{
        "name": "Activo WWWZZZ",
    }'
```

### Ejemplo de la respuesta

```json
{
    "asset": {
        "_id": "6736861858438f00c80a215c",
        "asset_type": "55xs3yroBgTyfqFAN",
        "reference": "12340987",
        "name": "Activo WWWZZZ",
        "form": { },
        "created_at": "2024-11-14T23:22:00.775Z",
        "updated_at": "2024-11-14T23:22:23.679Z",
    }
}
```
</div>
</div>