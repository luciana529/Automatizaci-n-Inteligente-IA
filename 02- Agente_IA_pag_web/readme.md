🧠 Agente Inteligente de Triaje y Captación Web - Luciana Ramirez Systems
Este proyecto presenta una solución avanzada de atención al cliente automatizada mediante el uso de múltiples Agentes de IA especializados y lógica de enrutamiento dinámico. El sistema actúa como un filtro inteligente que separa consultas generales de oportunidades de venta reales.

🚀 Descripción del Flujo
A diferencia de un bot lineal, este ecosistema utiliza un modelo de clasificación para dirigir al usuario hacia el experto más adecuado según su mensaje inicial.

🛠️ Componentes Clave
Entrada de Datos (Trigger): Se activa mediante un Webhook de chat cuando el usuario envía un mensaje.

Agente Clasificador: Actúa como el "cerebro" inicial. Su única función es determinar si el usuario necesita información general o si tiene intención de compra.

Lógica Condicional (Nodo If): Un nodo de control que evalúa el output del clasificador y bifurca el camino del flujo.

Especialistas de IA:

Chat Bot Web: Un agente enfocado en soporte y FAQs, conectado a una base de conocimientos en Google Sheets (preguntas_frecuentes) para dar respuestas precisas.

Captación de Leads: Un agente persuasivo diseñado para recolectar datos del cliente y enviarlos automáticamente vía Gmail al equipo de ventas.

⚙️ Especificaciones Técnicas
Motor de IA: OpenAI Chat Model (GPT-4o) para todos los agentes, garantizando un razonamiento de nivel superior.

Gestión de Memoria: Implementación de Simple Memory en cada etapa para que los agentes recuerden el contexto de la conversación actual.

Configuración de Respuesta: Los modelos están ajustados con una temperatura de 0,2 para minimizar alucinaciones y mantener un tono profesional constante.

📋 Requisitos para el Despliegue
Para replicar este entorno de Luciana Ramirez Systems, es necesario:

Contenedor Docker activo con la imagen oficial de n8n.

Túnel de ngrok para la recepción de webhooks externos.

Credenciales configuradas para OpenAI, Google Sheets y Gmail.