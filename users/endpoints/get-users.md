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
| `user_ids[]`    | (opcional) Lista de IDs de usuarios específicos para obtener detalles de esos usuarios.                       | Array de String |
| `user_ids`      | (opcional) ID único de un usuario para obtener información específica de un usuario.                          | String        |
| `specialities[]`| (opcional) Lista de especialidades para filtrar usuarios con dichas especialidades.                            |  String |
| `headquarter`   | (opcional) Filtra los usuarios según una sede específica.                                                     | String        |
| `headquarters[]`| (opcional) Lista de sedes para filtrar usuarios asociados a dichas sedes.                                      | String |


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
}'
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