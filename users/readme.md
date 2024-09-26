# API de Usuarios

La API de Usuarios de Suite permite interactuar con los datos de los usuarios registrados en tu cuenta empresarial. A través de estos endpoints, podrás obtener información sobre los usuarios existentes o crear nuevos en el sistema.

---

## Endpoints

- [Obtener usuarios](/users/endpoints/get-users.md) : ```GET /public/users```

## Diccionarios

### Tipos de usuarios

| Tipo de usuario                    | ID |
|------------------------------------|--------|
| Administrador                      | 1      |
| Operador (Usuario de operaciones)  | 2      |
| Recurso (Usuario en campo)         | 4      |
| Interesado (Acceso usuarios externos)  | 5      |


**Nota**: Estos nombres de tipos de usuario pueden variar según la personalización y el uso específico de cuenta en *Suite*.