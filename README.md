Práctica API Segura - Codificación Segura y Certificados

Descripción
API desarrollada en Node.js como parte de la práctica de codificación segura.
Implementa validaciones de datos, protección mediante Helmet y comunicación HTTPS
con certificado autofirmado.

Tecnologías utilizadas

- Node.js
- Express Validator
- Helmet
- HTTPS
- Certificado autofirmado

Instalación

Clonar el repositorio:

```bash
git clone URL_DEL_REPOSITORIO

Instalar dependencias:

npm install
Ejecución

Iniciar el servidor:

npm run dev

El servidor se ejecuta mediante HTTPS en:

https://localhost:3000/salud


Endpoints

POST /api/registro
Endpoint para registrar usuarios.

Validaciones aplicadas:
- El campo `nombre` no puede estar vacío.
- El campo `correo` debe tener un formato válido utilizando `isEmail()`.

Ejemplo de solicitud:
{
  "nombre": "Nayeli",
  "correo": "nayeli@email.com"
}

Respuesta exitosa:
{
  "mensaje": "Usuario registrado correctamente",
  "usuario": {
    "nombre": "Nayeli",
    "correo": "nayeli@email.com"
  }


POST /api/echo
Endpoint para comprobar el funcionamiento de la API.

Validación aplicada:

El campo mensaje no puede estar vacío.

Ejemplo de solicitud:
{
  "mensaje": "Hola API segura"
}

Respuesta exitosa:
{
  "mensaje": "Hola API segura"
}

Si la validación falla, la API devuelve un código HTTP 400 con la lista de errores detectados.



Seguridad implementada
Helmet para agregar encabezados HTTP seguros.
HTTPS mediante certificado autofirmado.
Validación de entradas con express-validator.
Validación de datos para evitar información incorrecta o maliciosa.
Principio de codificación segura aplicado

Se aplica la validación de entradas, ya que todos los datos recibidos por la API
son comprobados antes de ser procesados, reduciendo riesgos de errores,
datos inválidos o ataques mediante entradas manipuladas.