# Crear servicio

<div style="display: flex; justify-content: space-between;">

<div style="width: 48%;">

### Información de API

- **Endpoint**: `/public/services`
- **Método**: `POST`
- **Descripción**: Este endpoint crea un servicio según los parámetros.


## Referencia de la solicitud:

| Atributo              | Descripción                                                 | Tipo de dato        |
|-----------------------|-------------------------------------------------------------|---------------------|
| `name`                | (opcional) Nombre representativo de la solicitud de servicio.           | String              |
| `reference`           | (opcional) Referencia del servicio, usada para identificarlo.           | String              |
| `description`         | (opcional) Descripción detallada del servicio solicitado.               | String              |
| `service_type`        | Tipo de servicio solicitado.                                | String              |
| `customer`            | ID del cliente asociado al servicio.                        | String              |
| `contact`             | ID del contacto principal para el servicio.                 | String              |
| `assigned_to`         | ID del usuario o agente asignado al servicio.               | String              |
| `execution_date`      | Fecha de ejecución del servicio (en formato ISO 8601).       | String (ISO 8601)   |
| `destination_address` | (opcional) Dirección de destino donde se debe realizar el servicio. Por defecto toma la dirección del contacto.     | String              |
| `destination_coords`  | (opcional) Coordenadas del destino, que incluye:                       | Object              |
|                       | └ `latitude` - Latitud del destino.                         | Number              |
|                       | └ `longitude` - Longitud del destino.                       | Number              |
| `is_priority`         | (opcional) Indica si el servicio es prioritario (true/false). Por defecto es False.           | Boolean             |

### Nota:
El campo *execution_date* debe enviarse en formato ISO 8601 y ajustado a la zona horaria UTC-0. Esto significa que cualquier fecha y hora proporcionada, independientemente de la zona horaria en la que se origine, debe ser convertida al formato estándar ISO 8601 en UTC-0 antes de incluirla en la solicitud.

## Tipo de respuesta: 
```Object { Object }```

</div>

<div style="width: 48%;">

### Ejemplo de la solicitud

```bash
curl -X POST \
	https://api-hub.tapptus.com/public/services \
	-H 'authorization: Bearer TOKEN' \
	-H 'cache-control: no-cache' \
	-H 'content-type: application/json' \
    -d '{
        "name": "sample request service",
        "reference": "ref 001",
        "description": "service request for customer",
        "service_type": "rv9RoAdeScEAH9kTY",
        "customer": "kov2E5BopbYbtiZx6",
        "contact": "cd2WHZ3iBsMMN5zTP",
        "assigned_to": "MAtcKu3tkbr8StkHc",
        "execution_date": "2024-10-01T21:04:08.431Z",
        "destination_address": "1234 Elm Street",
        "destination_coords": {
            "latitude": 6.2446,
            "longitude": 75.5916
        },
        "is_priority": true
    }'
```

### Ejemplo de la respuesta

```json
{
    "service": {
        "name": "sample request service",
        "confirmed_by_final_customer": false,
        "is_priority": false,
        "destination_coords": {
            "latitude": 6.2446,
            "longitude": 75.5916
        },
        "is_removed": false,
        "is_suite": true,
        "is_self_scheduled": false,
        "is_legal_terms_accepted_by_final_customer": false,
        "private_id": "1917",
        "execution_date": "2024-10-01T21:04:08.431Z",
        "id_account": "WKTG3GByCq7Aat4nz",
        "assigned_to": "MAtcKu3tkbr8StkHc",
        "service_type": "rv9RoAdeScEAH9kTY",
        "customer": "kov2E5BopbYbtiZx6",
        "contact": "cd2WHZ3iBsMMN5zTP",
        "destination_address": "1234 Elm Street",
        "description": "service request for customer",
        "reference": "ref 001",
        "final_customer": "dPnjP7wd2Soowc3sS",
        "id_author": "dWboLnLqHNvY4MojK",
        "status": 1,
        "profile_type": 4,
        "_id": "66f70140feee6400501ac922",
        "is_reminders_sent": [],
        "future_reminders_sent": [],
        "is_confirmation_sent": [],
        "created_at": "2024-09-27T19:02:24.215Z",
        "updated_at": "2024-09-27T19:02:24.215Z",
        "__v": 0,
        "id": "66f70140feee6400501ac922"
    }
}
```
</div>
</div>