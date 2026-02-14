1. 📬 Agente Autónomo de Telegram & Respuesta InteligenteEste proyecto consiste en un ecosistema de atención automática que utiliza un Agente de IA para procesar y responder mensajes en tiempo real.
Funcionalidad PrincipalRecepción en Tiempo Real: El flujo se activa inmediatamente al recibir un mensaje a través de un Telegram Trigger.
Procesamiento Cognitivo: Utiliza un AI Agent conectado a un modelo OpenAI (GPT-4o) para entender el contexto de la conversación.
Memoria de Sesión: Implementa Simple Memory para mantener el hilo de la conversación con el usuario, permitiendo respuestas coherentes y fluidas.
Acciones Multitarea: El agente no solo responde texto, sino que tiene la capacidad de utilizar herramientas como Gmail para notificar internamente sobre consultas relevantes.
Arquitectura TécnicaTrigger: Telegram Message (Updates: message).I
A Model: OpenAI Chat Model (gpt-4o) con temperatura ajustada a $0,2$ para mayor precisión.
Salida: Envío automático de mensajes de texto personalizados de vuelta al usuario en Telegram.