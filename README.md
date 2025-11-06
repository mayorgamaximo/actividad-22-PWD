Formulario de Contacto (HTML + JavaScript)

Este proyecto consiste en una página web simple con un formulario de contacto que envía los datos mediante una petición POST en formato JSON a un webhook de n8n.
Está desarrollado sin frameworks, utilizando únicamente HTML, CSS y JavaScript puro.

🚀 Características

Formulario con los campos:

Nombre

Email

Tipo (select con opciones normal y urgente)

Mensaje

Envío de datos vía fetch() en formato JSON.

Validaciones básicas de los campos requeridos.

Muestra mensajes de éxito o error según la respuesta del servidor.

Diseño limpio y adaptable (responsive).

🧩 Estructura del proyecto
/
├── index.html       # Página principal con el formulario y el script embebido
└── README.md        # Este archivo

📤 Ejemplo de datos enviados
{
  "nombre": "Juan Pérez",
  "email": "juan@email.com",
  "tipo": "urgente",
  "mensaje": "Necesito ayuda urgente"
}

🌐 Endpoint configurado

El formulario envía los datos al siguiente webhook de n8n:

https://m4xi.app.n8n.cloud/webhook/formulario-contacto


Puedes modificar este endpoint directamente en el bloque <script> dentro del archivo index.html si deseas usar tu propio flujo de n8n o API personalizada.

⚙️ Cómo probar el proyecto

Clona este repositorio:

git clone https://github.com/mayorgamaximo/actividad-22-PWD/


Abre el archivo index.html en tu navegador.

Completa el formulario y presiona Enviar.

Verás un mensaje de confirmación si el webhook responde correctamente, o un mensaje de error si hay un problema de conexión o validación.

🧠 Notas técnicas

No requiere servidor backend propio; se conecta directamente al webhook.

Usa fetch() con cabeceras:

{
  "Content-Type": "application/json",
  "Accept": "application/json"
}


Compatible con cualquier navegador moderno.

Asegúrate de que tu webhook en n8n tenga CORS habilitado para aceptar solicitudes desde tu dominio o localhost.
