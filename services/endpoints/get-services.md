# Obtener servicios

<div style="display: flex; justify-content: space-between;">

<div style="width: 48%;">

### Información de API

- **Endpoint**: `/public/services`
- **Método**: `GET`
- **Descripción**: Este endpoint retorna los servicios según los filtros aplicados.

## Referencia de la solicitud:

| Atributo                   | Descripción                                                                           | Tipo de dato  |
|----------------------------|---------------------------------------------------------------------------------------|---------------|
| `page`          | (opcional) Especifica la página de servicios a ser obtenidos. Cada página retorna hasta 20 servicios por default en caso no de especificar page_size. Por defecto será 1. | Number        |
| `page_size`          | (opcional) Especifica la cantidad de servicios a ser obtenidos por página. Por defecto será 20 y como máximo puede ser retornado 200 | Number        |
| `service_ids[]`             | (opcional) ID del servicio           |  String |
| `execution_date_init`       | (opcional) Fecha de inicio para filtrar los servicios por la fecha de ejecución.      | String (ISO 8601) |
| `execution_date_end`        | (opcional) Fecha de fin para filtrar los servicios por la fecha de ejecución.         | String (ISO 8601) |
| `init_updated_at`           | (opcional) Fecha de inicio para filtrar por la última actualización de los servicios. | String (ISO 8601) |
| `end_updated_at`            | (opcional) Fecha de fin para filtrar por la última actualización de los servicios.    | String (ISO 8601) |
| `reference` | (opcional) Referencia del servicio. | String       |
| `customer`                  | (opcional) ID del cliente asociado al servicio.                                       | String        |
| `final_customer`            | (opcional) ID del cliente final asociado al servicio.                                 | String        |
| `assigned_to`               | (opcional) ID del usuario asignado al servicio.                                       | String        |
| `service_types[]`           | (opcional) IDs de los tipos de servicio para filtrar los servicios.                    |  String |
| `include_service_type_variables` | (opcional) Indica si se deben incluir variables relacionadas con el tipo de servicio. | Boolean       |
| `include_service_extended_data` | (opcional) Indica si se deben incluir en la respuesta el flujo de servicio extendido. | Boolean       |
| `include_service_summary_data` | (opcional) (opcional) Indica si se deben incluir en la respuesta los datos de resumen de servicio. | Boolean       |
| `include_service_review_data` | (opcional) Indica si se deben incluir en la respuesta el flujo de revisión de servicio. | Boolean       |

### Filtrado con Parámetros Repetibles

Algunos parámetros como `service_ids[]` y `service_types[]` pueden enviarse **múltiples veces** en la misma solicitud para filtrar por varios ítems.

#### Ejemplo:
```bash
GET /public/services?service_ids[]=1&service_ids[]=2
```

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
            "service_extended_data": {...},
            "service_summary_data": {...},
            "service_review_data": {...},
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
            },
            "headquarter_information": {
                "_id": "65dc149037d649022d77dbb3",
                "is_removed": false,
                "is_default": true,
                "name": "Medellín",
                "reference": "001",
                "id_color": 19,
                "destination_address": "Torre Médica cosultorio 13",
                "phone": "6040000000",
                "id_account": "65d",
                "created_at": "2024-02-26T04:33:20.650Z",
                "updated_at": "2024-02-26T04:36:09.900Z",
                "__v": 0,
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
            "service_extended_data": null,
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
            },
            "final_customer_information": {
                "_id": "1234567890abcdef12345678",
                "identification_type": "CC",
                "identification": "123456789",
                "destination_address": "HILLS 72",
                "first_name": "JOHN",
                "last_name": "DOE",
                "second_name": "",
                "second_last_name": "SMITH",
                "birth_date": "01/01/1990",
                "biological_sex": "Hombre",
                "blood_type": "A+",
                "health_insurance_code": "EPS999",
                "email": "john.doe@example.com",
                "mobile_phone": "3001234567",
                "name": "JOHN DOE SMITH",
                "fullname": "JOHN DOE SMITH",
                "nationality_country": "",
                "optional_mobile_phone": "",
                "residence_city": "",
                "residence_state": "",
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