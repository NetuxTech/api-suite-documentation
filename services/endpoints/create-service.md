# Obtener servicios

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
| `destination_address` | Dirección de destino donde se debe realizar el servicio.     | String              |
| `destination_coords`  | Coordenadas del destino, que incluye:                       | Object              |
|                       | └ `latitude` - Latitud del destino.                         | Number              |
|                       | └ `longitude` - Longitud del destino.                       | Number              |
| `timezone`            | Zona horaria del destino en formato UTC (p.ej., -5 para EST).| Integer             |
| `is_priority`         | (opcional) Indica si el servicio es prioritario (true/false).           | Boolean             |



## Tipo de respuesta: 
```Object { Array[Object, Object, ...] }```

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
            "latitude": 40.7128,
            "longitude": -74.0060
        },
        "timezone": -5,
        "is_priority": true
    }'
```

### Ejemplo de la respuesta

```json

```
</div>
</div>