# API de Clientes Finales

La API de Clientes Finales de Suite permite interactuar con los datos de los clientes finales registrados en tu cuenta empresarial. A través de estos endpoints, podrás obtener información sobre los clientes finales y crear nuevos en el sistema.

---

## Endpoints

- [Obtener clientes finales](/final_customers/endpoints/get-final-customers.md) : ```GET /public/final-customers```
- [Crear cliente final](/services/endpoints/create-final-customer.md) : ```POST /public/final-customers```
- [Actualizar cliente final](/services/endpoints/update-final-customer.md) : ```PATCH /public/final-customers```


## Diccionarios

### Tipos de documentos

| Description                             | ID |
|-----------------------------------------|-------|
| Cédula de ciudadanía - CC               | CC    |
| Cédula de extranjería - CE              | CE    |
| Carné diplomático - CD                  | CD    |
| Pasaporte - PA                          | PA    |
| Salvo conducto de permanencia - SC      | SC    |
| Permiso temporal de permanencia - PT    | PT    |
| Permiso especial de permanencia - PE    | PE    |
| Registro civil - RC                     | RC    |
| Tarjeta de identidad - TI               | TI    |
| Certificado de nacido vivo - CN         | CN    |
| Adulto sin identificar - AS             | AS    |
| Menor sin identificar - NS              | NS    |
| Documento extranjero - DE               | DE    |


### Géneros

| Description                   | ID             |
|-------------------------------|----------------|
| Hombre                        | 1              |
| Mujer                         | 2              |
| Indeterminado intersexual     | O              |


### Tipos de sangre

| ID |
|-------------|
| O-          |
| O+          |
| A-          |
| A+          |
| B-          |
| B+          |
| AB-         |
| AB+         |

### Listado de Países
- [Lista de Países](/dictionaries_data/countries.json)

### Listado de Estados / Departamentos
- [Colombia](/dictionaries_data/states/states[CO].json)