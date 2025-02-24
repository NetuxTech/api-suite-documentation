# Cambio de Estado del Servicio

## Información de API

- **Endpoint**: `/public/services/status/{serviceId}`
- **Método**: `PATCH`
- **Descripción**: Permite actualizar el estado de un servicio existente.

### Referencia de la solicitud:

| Atributo  | Descripción                                       | Tipo de dato |
|-----------|---------------------------------------------------|-------------|
| `status`  | Nuevo estado del servicio. Ver valores permitidos. | Number      |

### Estados Permitidos para Cambio:

| Estado        | ID  |
|--------------|----:|
| **Finalizado** (`FINISH`) | `8` |
| **Cancelado** (`CANCELLED`) | `9` |

**Nota:** Solo se permiten cambios a los estados `8 (Finalizado)` o `9 (Cancelado)`.  
Cualquier otro valor generará un error de validación.

---

### Ejemplo de la solicitud

```bash
    curl --location --request PATCH 'https://api-hub.tapptus.com/public/services/status/CZnPJSzZmsmFYT5rk' \
    --header 'Content-Type: application/json' \
    --header 'Authorization: Bearer TOKEN' \
    --data '{
        "status": 9
    }'
```

## Respuestas

### Respuesta Exitosa (200 OK)

```json
{
    "service": {
        "_id": "BYkt5tgoyYTYXRNzL",
        "name": "Mantenimiento Maquina 1",
        "is_priority": false,
        "customInfo": {},
        "description": "Descripción 1",
        "destination_address": "Cartagena, Cartagena Province, Bolivar, Colombia",
        "destination_coords": {
            "latitude": 10.3910485,
            "longitude": -75.4794257
        },
        "execution_date": "2020-01-28T05:00:00.000Z",
        "customer": "FmZnSMkbyBWM6Lh9X",
        "contact": "tJHwLfBQefaGeodwX",
        "service_type": "GjiKyKHm8DLYkAbnf",
        "createdByResource": false,
        "status": 9,
        "assigned_to": "kAdPGNxq5jgYipN3k",
        "created_by": "Xd9FFcdeLnAv8Ft6q",
        "is_removed": false,
        "id_account": "WKTG3GByCq7Aat4nz",
        "timezone": -5,
        "created_at": "2020-01-27T20:00:01.063Z",
        "updated_at": "2025-02-24T20:58:07.099Z",
        "app": {
            "idApp": "ZtJYWQMiSjkHNexN3",
            "hasChange": false
        },
        "private_id": "0122",
        "profile_type": 4,
        "isEnabled": true
    }
}
```