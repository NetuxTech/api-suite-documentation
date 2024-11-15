# API Suite NX

¡Bienvenidos! Suite NX permite la captura de datos a través de una interfaz de programación de aplicaciones (API). Esta documentación ha sido creada para guiar a los desarrolladores en la obtención de datos relevantes para integrarlos en sus herramientas empresariales.

**Versión actual de la API:** 3.0.0  
Estamos trabajando continuamente para agregar más funcionalidades.

## ¿Qué puedes hacer con nuestra API?

Puedes integrar tus aplicaciones con nuestra API para crear y obtener datos de:

- **Usuarios** - [Ver más](/users/readme.md)
- **Servicios** - [Ver más](/services/readme.md)
- **Tipos de Servicio** - [Ver más](/service_types/readme.md)
- **Sedes** - [Ver más](/headquarters/readme.md)
- **Clientes y Contactos** - [Ver más](/customers/readme.md)
- **Clientes finales** - [Ver más](/final_customers/readme.md)
- **Activos & Bases de datos** - [Ver más](/assets/readme.md)

**¿Necesitas ayuda?**  
Contáctanos en [soporte@netux.com](mailto:soporte@netux.com) y con gusto te ayudaremos con la integración.

---

## Acerca de la API

Esta API permite capturar datos de servicios ejecutadas por trabajadores en campo. Los administradores pueden asignar y programar tareas y ver detalles de tareas ejecutadas. Nuestra API está basada en REST y devuelve respuestas en formato JSON.

---

## Definiciones clave

### Usuario
Persona registrada en una cuenta de empresa (administrador, operadores y prestadores de servicio) que accede a *Suite* a través de la aplicación web o móvil.

### Operador
Miembro del personal encargado del seguimiento diario de las operaciones. Los operadores asignan nuevos servicios, reciben alertas y monitorean actividades. Sin embargo, la configuración de la cuenta (ej. edición de formularios, creación de usuarios) solo es permitida al administrador.

### Prestador del servicio
Usuarios responsables de realizar la ejecución del servicio asignado.

### Clientes
Clientes o empresas registradas en tu cuenta.

### Contactos
Información de personas asociadas a cada cliente (por ejemplo, personas de contacto asociadas a un cliente).

### Servicios
Tareas asignadas a los prestadores de servicio.


---

## Referencia de la API

Esta sección proporciona una referencia completa de la API HTTP REST, que permite obtener datos de usuarios, servicios, cuentas y contactos.

### API Endpoint

Todos los recursos disponibles a través de la API son accesibles mediante HTTPS desde el siguiente host:

```bash
https://api-hub.tapptus.com/public
```

### Autenticación

Todas las solicitudes a la API requieren autenticación mediante un **TOKEN**, que se puede solicitar mediante una solicitud de soporte.

El token debe incluirse en cada solicitud HTTP/S en el encabezado de petición:

```bash
Authorization: Bearer TOKEN
```

## Códigos de Respuesta

| Código | Nombre                  | Descripción                                                                 |
|--------|-------------------------|-----------------------------------------------------------------------------|
| 200    | OK                      | La solicitud fue exitosa y los datos están en la respuesta.                  |
| 400    | Solicitud errónea        | Hubo un error en la solicitud, por ejemplo, datos faltantes o no válidos.    |
| 401    | No autorizado            | Falta el token de autenticación o es inválido.                               |
| 404    | No encontrado            | El recurso solicitado no fue encontrado.                                     |
| 422    | Entidad no procesada    | El servidor no puede procesar la solicitud debido a la información enviada.  |
| 500    | Error del servidor       | Error interno del servidor. Intenta nuevamente más tarde.                    |


