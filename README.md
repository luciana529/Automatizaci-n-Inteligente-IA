🚀 Luciana Ramirez Systems: Automatización Inteligente & IA
Bienvenido al repositorio central de Luciana Ramirez Systems. Aquí documento el desarrollo de ecosistemas de automatización utilizando n8n, IA Generativa y despliegues robustos mediante Docker y ngrok.

📌 Proyecto Destacado: Clasificador de Leads & Agente de Ventas Autónomo
Este flujo resuelve la gestión ineficiente de mensajes entrantes mediante el uso de lógica condicional e Inteligencia Artificial para diferenciar consultas informativas de oportunidades comerciales.

🛠️ Tecnologías Utilizadas
Core: n8n (Desplegado en Docker)

LLMs: OpenAI (GPT-4o) para razonamiento complejo y Google Gemini como soporte.

Canales: Telegram / Web Chat.

Infraestructura: ngrok para túneles seguros y Webhooks.

Integraciones: Gmail API para notificaciones automáticas.

🧠 Arquitectura del Flujo
Trigger de Entrada: Recepción de mensajes en tiempo real vía Telegram/Chat.

Clasificación Semántica: Un Agente de IA actúa como "Portero", analizando la intención del usuario para clasificarla como CHAT (Informativo) o LEAD (Comercial).

Lógica Condicional (Branching): Nodo IF con saneamiento de datos mediante expresiones de JavaScript:

JavaScript
{{ $json.output.trim().toUpperCase() }}
Extracción de Datos (NER): Algoritmo de extracción de información para identificar DNI, CIF, Nombres y Teléfonos explícitos en el texto.

Acción Final: Envío automático de ficha de cliente a Gmail y respuesta personalizada según el perfil del agente.

🛠️ Guía de Configuración Técnica (Self-Hosted)
Para replicar el entorno de Luciana Ramirez Systems, sigo este proceso de despliegue:

Entorno: Docker Desktop para la orquestación del contenedor de n8n.

Arranque del Contenedor:

PowerShell
docker run -it --rm --name n8n -p 5678:5678 -v C:\n8n-data:/home/node/.n8n -e N8N_EDITOR_BASE_URL=https://[TU-URL].ngrok-free.dev -e WEBHOOK_URL=https://[TU-URL].ngrok-free.dev n8nio/n8n start
Exposición: Túnel seguro mediante ngrok: ngrok http 5678.

📈 Desafíos Solucionados
Gestión de Formatos: Superación de errores de parsing en nodos de clasificación antiguos mediante el uso de AI Agents y modelos de respuesta en texto plano.

Control de Rate Limits: Implementación de estrategias de respaldo entre OpenAI y Gemini para garantizar la disponibilidad 24/7.

Integridad de Datos: Uso de esquemas JSON estrictos para evitar alucinaciones en la extracción de documentos de identidad.

📬 Contacto
Luciana Ramirez Systems - luciana.ramirez.systems@gmail.com
Especialistas en flujos de trabajo inteligentes y optimización de procesos.
