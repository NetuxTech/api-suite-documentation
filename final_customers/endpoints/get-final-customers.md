# Obtener clientes finales

<div style="display: flex; justify-content: space-between;">

<div style="width: 48%;">

### Información de API

- **Endpoint**: `/public/final-customers`
- **Método**: `GET`
- **Descripción**: Este endpoint retorna los clientes finales según los filtros aplicados.

## Referencia de la solicitud:

| Atributo                  | Descripción                                                                                      | Tipo de dato         |
|---------------------------|--------------------------------------------------------------------------------------------------|-----------------------|
| `page`                    | (opcional) Especifica la página de clientes finales a obtener. Cada página retorna hasta 20 clientes por defecto. Si no se especifica `page_size`, el valor por defecto será 1. | Number                |
| `page_size`               | (opcional) Especifica la cantidad de clientes finales a obtener por página. Por defecto será 20, y el máximo puede ser 200. | Number                |
| `final_customers_ids[]`   | (opcional) Lista de IDs de clientes finales específicos para filtrar los resultados.            | Array de Strings      |
| `identifications[]`       | (opcional) Lista de números de identificación para filtrar los clientes finales por identificación específica. | Array de Strings      |

### Filtrado con Parámetros Repetibles

Algunos parámetros como `service_ids[]` y `service_types[]` pueden enviarse **múltiples veces** en la misma solicitud para filtrar por varios ítems.

#### Ejemplo:
```bash
GET /public/final-customers?final_customers_ids[]=1&final_customers_ids[]=2
```

## Tipo de respuesta: 
```Object { Array[Object, Object, ...] }```

</div>

<div style="width: 48%;">

### Ejemplo de la solicitud

```bash
curl -X GET \
	https://api-hub.tapptus.com/public/final-customers \
	-H 'authorization: Bearer TOKEN' \
	-H 'cache-control: no-cache' \
	-H 'content-type: application/json' \
```

### Ejemplo de la respuesta

```json
{
    "final_customers": [
        {
            "_id": "66f141d542ee3b1e40af602",
            "identification_type": "CC",
            "nationality_country": "USA",
            "identification": "1234567890",
            "first_name": "OBI",
            "second_name": "WAN",
            "last_name": "KENOBI",
            "birth_date": "25/12/1997",
            "biological_sex": 1,
            "blood_type": "A+",
            "residence_state": "CO-ANT",
            "residence_city": "Medellín",
            "address": "Carrera 1 # 1 1",
            "regime": "RÉGIMEN CONTRIBUTIVO",
            "phone": "0000000",
            "mobile_phone": "3178925263",
            "id_color": 6,
            "name": "OBI WAN KENOBI",
            "country_information": {
                "_id": "631b6c51d54423efb6c2535d",
                "common_name": "Estados Unidos",
                "iso_alpha3_code": "USA"
            },
            "state_information": {
                "_id": "631b6c68d54423efb6c2587b",
                "iso_state_code": "CO-ANT"
            },
            "city_information": {
                "_id": "631b6c5cd54423efb6c25421",
                "iso_alpha2_code": "CO",
                "municipality_name": "Medellín"
            },
            "health_insurance_information": {
                "_id": "650df864bb81d52e67ab2d04",
                "code": "000000",
                "name": "PARTICULAR"
            },
            "fullname": "OBI WAN KENOBI"
        }
    ],
    "total": 1,
    "page": 1,
    "page_size": 20
}
```
</div>
</div>