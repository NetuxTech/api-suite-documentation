# Actualizar Servicio

## Información de API

- **Endpoint**: `/public/services/{serviceId}`
- **Método**: `PATCH`
- **Descripción**: Este endpoint permite actualizar un servicio existente con los parámetros proporcionados.

### Referencia de la solicitud:

| Atributo              | Descripción                                                                 | Tipo de dato        |
|-----------------------|-----------------------------------------------------------------------------|---------------------|
| `name`               | (opcional) Nombre representativo del servicio.                              | String              |
| `reference`          | (opcional) Referencia del servicio, usada para identificarlo.              | String              |
| `description`        | (opcional) Descripción detallada del servicio.                             | String              |
| `service_type`       | (opcional) Tipo de servicio.                                               | String              |
| `customer`           | (opcional) ID del cliente asociado al servicio.                           | String              |
| `contact`            | (opcional) ID del contacto principal para el servicio.                    | String              |
| `assigned_to`        | (opcional) ID del usuario o agente asignado al servicio.                  | String              |
| `execution_date`     | (opcional) Nueva fecha de ejecución del servicio (en formato ISO 8601).   | String (ISO 8601)   |
| `destination_address`| (opcional) Dirección de destino donde se debe realizar el servicio.       | String              |
| `destination_coords` | (opcional) Coordenadas del destino.                                        | Object              |
|                      | └ `latitude` - Latitud del destino.                                       | Number              |
|                      | └ `longitude` - Longitud del destino.                                     | Number              |
| `is_priority`        | (opcional) Indica si el servicio es prioritario (`true`/`false`).         | Boolean             |
| `color_highlight`     | (opcional) Color resaltado del servicio en la UI.                         | String              |

### Nota:
- El campo **execution_date** debe enviarse en formato **ISO 8601** y ajustado a la zona horaria UTC-0.
- Los valores omitidos en la solicitud **no serán modificados** en el servicio.

---

## Tipo de respuesta:

```json
{
    "service": {
        "name": "Instalación de equipo editado",
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
        "customer": "kov2E5BopbYbYtiZx6",
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
        "id": "66f70140feee6400501ac922",
        "color_highlight": "#FFF"
    }
}
