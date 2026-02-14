🚀 Luciana Ramirez Systems: Ecosistema de Automatización con IA
Bienvenido al repositorio central de Luciana Ramirez Systems. Este proyecto representa una infraestructura completa de operaciones inteligentes, diseñada para automatizar el ciclo de vida del cliente: desde el primer contacto en redes sociales hasta la gestión de citas en el CRM.

🌟 Visión General
Luciana Ramirez Systems utiliza n8n como orquestador principal, integrando modelos de lenguaje avanzado (OpenAI GPT-4o) para transformar interacciones simples en procesos de negocio automatizados y eficientes.

📂 Estructura de Proyectos
En este repositorio encontrarás tres módulos clave:

1. 📬 Agente Autónomo de Telegram
Función: Atención al cliente 24/7 vía Telegram.

Utiliza memoria de sesión para mantener conversaciones fluidas.

Procesa consultas generales y las escala automáticamente a canales internos.

2. 🧠 Triaje y Clasificación de Leads
Función: Inteligencia de enrutamiento para tráfico web.

Un "Agente Portero" analiza la intención del usuario.

Divide el flujo entre un Chatbot Informativo (FAQs desde Google Sheets) y un Agente de Captación persuasivo.

3. 📅 Gestión de Citas y CRM
Función: Conversión final y registro de datos.

Integración con https://www.google.com/search?q=Cal.com para agendamiento automático.

Notificaciones vía Gmail y sincronización en tiempo real con un CRM en Google Sheets.

🛠️ Stack Tecnológico
Orquestador: n8n (Desplegado en Docker).

IA: OpenAI (GPT-4o) & Google Gemini.

Infraestructura: ngrok (Túneles de Webhook seguros).

Integraciones: Telegram API, Google Sheets, Gmail, https://www.google.com/search?q=Cal.com.

🔧 Guía Rápida de Instalación (Entorno Local)
Para poner en marcha el sistema de Luciana Ramirez Systems:

Levantar el contenedor de n8n:

PowerShell
docker run -it --rm --name n8n -p 5678:5678 -v C:\n8n-data:/home/node/.n8n n8nio/n8n start
Exponer el puerto local:

PowerShell
ngrok http 5678
Configurar Webhooks: Actualizar las URLs en los nodos de Telegram y https://www.google.com/search?q=Cal.com con la dirección provista por ngrok.

📈 Resultados Obtenidos
Disponibilidad: Atención inmediata al prospecto 24/7.

Precisión: Reducción de errores de carga de datos mediante el uso de Information Extractors.

Escalabilidad: Capacidad de gestionar múltiples hilos de conversación simultáneamente sin intervención humana.

Desarrollado por Luciana Ramirez Systems Impulsando la eficiencia empresarial mediante el poder de la Inteligencia Artificial.
