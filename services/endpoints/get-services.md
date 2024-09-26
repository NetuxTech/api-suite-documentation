# Obtener servicios

<div style="display: flex; justify-content: space-between;">

<div style="width: 48%;">

### Información de API

- **Endpoint**: `/public/services`
- **Método**: `GET`
- **Descripción**: Este endpoint retorna los servicios según los filtros aplicados.

## Referencia de la solicitud:

## Referencia de la solicitud:

| Atributo                   | Descripción                                                                           | Tipo de dato  |
|----------------------------|---------------------------------------------------------------------------------------|---------------|
| `execution_date_init`       | (opcional) Fecha de inicio para filtrar los servicios por la fecha de ejecución.      | String (ISO 8601) |
| `execution_date_end`        | (opcional) Fecha de fin para filtrar los servicios por la fecha de ejecución.         | String (ISO 8601) |
| `include_service_type_variables` | (opcional) Indica si se deben incluir variables relacionadas con el tipo de servicio. | Boolean       |
| `init_updated_at`           | (opcional) Fecha de inicio para filtrar por la última actualización de los servicios. | String (ISO 8601) |
| `end_updated_at`            | (opcional) Fecha de fin para filtrar por la última actualización de los servicios.    | String (ISO 8601) |
| `customer`                  | (opcional) ID del cliente asociado al servicio.                                       | String        |
| `final_customer`            | (opcional) ID del cliente final asociado al servicio.                                 | String        |
| `assigned_to`               | (opcional) ID del usuario asignado al servicio.                                       | String        |
| `service_types[]`           | (opcional) IDs de los tipos de servicio para filtrar los servicios.                    |  String |



## Tipo de respuesta: 
```Object { Array[Object, Object, ...] }```

</div>

<div style="width: 48%;">

### Ejemplo de la solicitud

```bash
curl -X GET \
	https://api-hub.tapptus.com/public/services \
	-H 'authorization: Bearer TOKEN' \
	-H 'cache-control: no-cache' \
	-H 'content-type: application/json' \
}'

```

### Ejemplo de la respuesta

```json
{
    "services": [
        {
            "_id": "66ec9ba10a3c0e0db288a6bd",
            "name": "Technical Support - System Setup",
            "description": "System setup and initial configuration for new client",
            "reference": "TS-2024-001",
            "customer": "kov2E5BopbYbtiZx6",
            "contact": "cd2WHZ3iBsMMN5zTP",
            "status": 8,
            "updated_at": "2024-09-19T21:46:49.636Z",
            "private_id": "1912",
            "destination_address": "Cl 44 #10-58, Medellín, Medellín, Antioquia, Colombia",
            "destination_coords": {
                "latitude": 0,
                "longitude": 0
            },
            "service_type": {
                "_id": "rv9RoAdeScEAH9kTY",
                "name": "Technical Assistance",
                "id_color": 13,
                "config_service_duration": {
                    "type": 6,
                    "time_unit": 1,
                    "time_value": 20
                },
                "variables": [],
                "execution_time_duration": 8,
                "color": "#FFC107"
            },
            "assigned_to": "MAtcKu3tkbr8StkHc",
            "execution_date": "2024-09-19T21:35:53.205Z",
            "accepted_date": "2024-09-19T21:46:09.597Z",
            "service_data_extended": null,
            "service_completion_date": "2024-09-19T21:46:48.744Z",
            "service_begin_date": "2024-09-19T21:46:10.995Z",
            "customer_information": {
                "_id": "kov2E5BopbYbtiZx6",
                "nit": "003",
                "name": "Global Tech Solutions"
            },
            "contact_information": {
                "_id": "cd2WHZ3iBsMMN5zTP",
                "name": "Carlos Gonzalez"
            },
            "assigned_to_information": {
                "_id": "MAtcKu3tkbr8StkHc",
                "profile": {
                    "identification": "3452345",
                    "name": "John Cardona",
                    "specialities": [
                        "mEFB6JGx3LRemnzNQ"
                    ],
                    "headquarters": []
                }
            },
            "status_information": {
                "_id": "YDRkctp7SYWSX4AxJ",
                "name": "Completed",
                "color": "#2ab72e"
            }
        },
        {
            "_id": "66ec9985e2526217cc10b8a6",
            "name": "Network Troubleshooting",
            "description": "Diagnose and resolve network issues for corporate client",
            "reference": "NT-2024-002",
            "customer": "xPfhRzFauDsTNsvBd",
            "contact": "ZoDACYo3EX9xJRPHh",
            "status": 8,
            "updated_at": "2024-09-19T21:44:24.839Z",
            "private_id": "1911",
            "destination_address": "Cl 44 #10-58, Medellín, Medellín, Antioquia, Colombia",
            "destination_coords": {
                "latitude": 0,
                "longitude": 0
            },
            "service_type": {
                "_id": "rv9RoAdeScEAH9kTY",
                "name": "Technical Assistance",
                "id_color": 13,
                "config_service_duration": {
                    "type": 6,
                    "time_unit": 1,
                    "time_value": 20
                },
                "variables": [],
                "execution_time_duration": 8,
                "color": "#FFC107"
            },
            "assigned_to": "MAtcKu3tkbr8StkHc",
            "execution_date": "2024-09-19T21:35:53.205Z",
            "accepted_date": "2024-09-19T21:37:09.375Z",
            "service_data_extended": null,
            "service_completion_date": "2024-09-19T21:42:51.950Z",
            "service_begin_date": "2024-09-19T21:37:11.132Z",
            "customer_information": {
                "_id": "xPfhRzFauDsTNsvBd",
                "nit": "875894",
                "name": "Corporate IT Solutions"
            },
            "contact_information": {
                "_id": "ZoDACYo3EX9xJRPHh",
                "name": "Alexander Rios"
            },
            "assigned_to_information": {
                "_id": "MAtcKu3tkbr8StkHc",
                "profile": {
                    "identification": "3452345",
                    "name": "John Cardona",
                    "specialities": [
                        "mEFB6JGx3LRemnzNQ"
                    ],
                    "headquarters": []
                }
            },
            "status_information": {
                "_id": "YDRkctp7SYWSX4AxJ",
                "name": "Completed",
                "color": "#2ab72e"
            }
        }
    ],
    "total": 2,
    "page_size": 20,
    "page": 1
}
```
</div>
</div>