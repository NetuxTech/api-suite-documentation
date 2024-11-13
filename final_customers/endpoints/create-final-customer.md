# Crear cliente final

<div style="display: flex; justify-content: space-between;">

<div style="width: 48%;">

### Información de API

- **Endpoint**: `/public/final-customers`
- **Método**: `POST`
- **Descripción**: Este endpoint crea un cliente final según los parámetros.


## Referencia de la solicitud:

| Atributo                 | Descripción                                                                                                                            | Tipo de dato            |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| `identification`         | (obligatorio) Identificación del cliente.                                                                                                | String                   |
| `identification_type`    | (obligatorio) Tipo de identificación del cliente. Ver diccionario en la definición general de la API de clientes finales.                | String                   |
| `first_name`             | (obligatorio) Primer nombre del cliente.                                                                                                 | String                   |
| `second_name`            | (opcional) Segundo nombre del cliente (puede ser nulo).                                                                               | String                   |
| `last_name`              | (obligatorio) Primer apellido del cliente.                                                                                               | String                   |
| `second_last_name`       | (opcional) Segundo apellido del cliente (puede ser nulo).                                                                             | String                   |
| `biological_sex`         | (opcional) Sexo biológico del cliente. Ver diccionario en la definición general de la API de clientes finales.                        | String                   |
| `blood_type`             | (opcional) Tipo de sangre del cliente. Ver diccionario en la definición general de la API de clientes finales.                        | String                   |
| `nationality_country`    | (opcional) País de nacionalidad del cliente. Ver diccionario en la definición general de la API de clientes finales.                  | String (ISO ALPHA3 CODE)                  |
| `residence_state`        | (opcional) Estado de residencia del cliente. Ver diccionario en la definición general de la API de clientes finales.                  | String (ISO STATE CODE)                 |
| `birth_date`             | (opcional) Fecha de nacimiento del cliente (en formato ISO 8601). YYYY-MM-DD                                                                     | String (ISO 8601)        |
| `residence_city`         | (opcional) Ciudad de residencia del cliente.                                                                                          | String                   |
| `address`                | (opcional) Dirección de residencia del cliente.                                                                                       | String                   |
| `health_insurance_code`  | (opcional) Código del seguro de salud del cliente.                                                                                    | String                   |
| `regime`                 | (opcional) Régimen de salud del cliente.                                                                                              | String                   |
| `email`                  | (opcional) Correo electrónico del cliente (validación de formato de correo electrónico).                                              | String                   |
| `phone`                  | (opcional) Teléfono fijo del cliente.                                                                                                 | String                   |
| `mobile_phone`           | (opcional) Número de celular del cliente.                                                                                             | String                   |
| `mobile_phone_indicative`| (opcional) Indicativo del número de celular del cliente.                                                                              | String                   |
| `optional_mobile_phone`  | (opcional) Número de celular alternativo del cliente (puede ser nulo).                                                                | String                   |


## Tipo de respuesta: 
```Object { Object }```

</div>

<div style="width: 48%;">

### Ejemplo de la solicitud

```bash
curl -X POST \
	https://api-hub.tapptus.com/public/final-customers \
	-H 'authorization: Bearer TOKEN' \
	-H 'cache-control: no-cache' \
	-H 'content-type: application/json' \
    -d '{
        "identification": "4353500",
        "identification_type": "CC",
        "first_name": "Jane",
        "last_name": "Rodriguez"
    }'
```

### Ejemplo de la respuesta

```json
{
    "final_customer": {
        "is_removed": false,
        "identification_type": "CC",
        "tags": [],
        "_id": "61dc9df937d6497",
        "id_account": "123",
        "nationality_country": "USA",
        "identification": "1234567891",
        "first_name": "Jane",
        "second_name": "",
        "last_name": "Rodriguez",
        "birth_date": "25/12/1997",
        "biological_sex": 2,
        "blood_type": "A+",
        "residence_state": "ANTU",
        "residence_city": "Medellín",
        "address": "Carrera 1 # 1 1",
        "health_insurance_code": "000000",
        "regime": "RÉGIMEN CONTRIBUTIVO",
        "phone": "0000000",
        "mobile_phone": "3178925263",
        "id_color": 6,
        "created_at": "2024-06-28T19:50:53.833Z",
        "updated_at": "2024-11-13T21:59:32.977Z",
        "__v": 0,
        "email": "jane@email.com",
        "fullname": "Jane Rodriguez"
    }
}
```
</div>
</div>