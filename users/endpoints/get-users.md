# Obtener usuarios

<div style="display: flex; justify-content: space-between;">

<div style="width: 48%;">
  
### Información de API

- **Endpoint**: `/public/users`
- **Método**: `GET`
- **Descripción**: Este endpoint retorna los usuarios de la cuenta según filtros


## Referencia de la solicitud:

| Atributo        | Descripción                                                                                                   | Tipo de dato  |
|-----------------|---------------------------------------------------------------------------------------------------------------|---------------|
| `page`          | (opcional) Especifica la página de usuarios a ser obtenidos. Cada página retorna hasta 20 usuarios. Por defecto será 1. | Number        |
| `profile_type`  | (opcional) Filtra los usuarios según el tipo de perfil especificado.                                           | Number        |
| `user_ids[]`    | (opcional) ID de usuario específico para obtener detalles de ese usuario.                       |  String |
| `specialities[]`| (opcional) Especialidad para filtrar usuarios con dicha especialidad.                            |  String |
| `headquarter`   | (opcional) Filtra los usuarios según una sede específica.                                                     | String        |
| `headquarters[]`| (opcional) ID de sede para filtrar usuarios asociados con dicha sede.                                      | String |

### Filtrado con Parámetros Repetibles

Algunos parámetros como `user_ids[]`, `specialities[]` y `headquarters[]` pueden enviarse **múltiples veces** en la misma solicitud para filtrar por varios ítems.

#### Ejemplo:
```bash
GET /api/users?user_ids[]=1&user_ids[]=2
```


## Tipo de respuesta: 
```Object { Array[Object, Object, ...] }```

</div>

<div style="width: 48%;">

### Ejemplo de la solicitud

```bash
curl -X GET \
	https://api-hub.tapptus.com/public/users \
	-H 'authorization: Bearer TOKEN' \
	-H 'cache-control: no-cache' \
	-H 'content-type: application/json' \
```

### Ejemplo de la respuesta

```json
{
    "users": [
        {
            "_id": "JQKkhJ4rToD6TYhX7",
            "username": "prefix.doe",
            "profile": {
                "identification": "123456789",
                "name": "John Doe",
                "profile_type": "4",
                "status": true,
                "specialities": [
                    "mEFB6JGx3LRemnzNQ"
                ]
            }
        },
        {
            "_id": "vfAMA3dSdgAmx6wms",
            "username": "prefix.smith",
            "profile": {
                "identification": "987654321",
                "name": "Jane Smith",
                "profile_type": "4",
                "status": true,
                "headquarters": [
                    "641126f54ef93722dc6a913d",
                    "6464a6bc09f055e107551b86",
                    "jFQewbp6KEL9YDwGv"
                ],
                "specialities": [
                    "mEFB6JGx3LRemnzNQ"
                ]
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