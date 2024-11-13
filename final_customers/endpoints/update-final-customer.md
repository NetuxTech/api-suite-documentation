# Actualizar cliente final

<div style="display: flex; justify-content: space-between;">

<div style="width: 48%;">

### Información de API

- **Endpoint**: `/public/final-customers/{id_final_customer}`
- **Método**: `PATCH`
- **Descripción**: Este endpoint actualiza un cliente final según los parámetros.


## Referencia de la solicitud:

| Atributo                 | Descripción                                                                                                                            | Tipo de dato            |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| `identification`         | (opcional) Identificación del cliente.                                                                                                | String                   |
| `identification_type`    | (opcional) Tipo de identificación del cliente. Ver diccionario en la definición general de la API de clientes finales.                | String                   |
| `first_name`             | (opcional) Primer nombre del cliente.                                                                                                 | String                   |
| `second_name`            | (opcional) Segundo nombre del cliente (puede ser nulo).                                                                               | String                   |
| `last_name`              | (opcional) Primer apellido del cliente.                                                                                               | String                   |
| `second_last_name`       | (opcional) Segundo apellido del cliente (puede ser nulo).                                                                             | String                   |
| `biological_sex`         | (opcional) Sexo biológico del cliente. Ver diccionario en la definición general de la API de clientes finales.                        | String                   |
| `blood_type`             | (opcional) Tipo de sangre del cliente. Ver diccionario en la definición general de la API de clientes finales.                        | String                   |
| `nationality_country`    | (opcional) País de nacionalidad del cliente. Ver diccionario en la definición general de la API de clientes finales.                  | String                   |
| `residence_state`        | (opcional) Estado de residencia del cliente. Ver diccionario en la definición general de la API de clientes finales.                  | String                   |
| `birth_date`             | (opcional) Fecha de nacimiento del cliente (en formato ISO 8601).  YYYY-MM-DD                                                                      | String (ISO 8601)        |
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
curl -X PATCH \
	https://api-hub.tapptus.com/public/final-customers/61dc9df937d649022f9 \
	-H 'authorization: Bearer TOKEN' \
	-H 'cache-control: no-cache' \
	-H 'content-type: application/json' \
    -d '{
        "phone": "111222333",
        "blood_type": "A+"
    }'
```

### Ejemplo de la respuesta

```json
{
    "final_customer": {
        "is_removed": false,
        "identification_type": "CC",
        "tags": [],
        "_id": "61dc9df937d649022f9",
        "id_account": "123",
        "nationality_country": "USA",
        "identification": "1234567891",
        "first_name": "OBI2",
        "second_name": "WAN",
        "last_name": "KENOBI",
        "birth_date": "25/12/1997",
        "biological_sex": 1,
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
        "email": "test@gmail.com",
        "fullname": "OBI2 WAN KENOBI"
    }
}
```
</div>
</div>