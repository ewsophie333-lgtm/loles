# 🚀 Guía de Productividad y Tecnologías: Especial Docencia
### Preparado para: Prof. Loles
**Objetivo:** Transformar la gestión académica diaria mediante la automatización y el uso estratégico de herramientas cloud para recuperar tiempo de calidad docente.

---

## 🛠️ 1. Las Tecnologías (El "Kit" de Herramientas)

### 1.1 GitHub & Codespaces: Tu centro de mando en la nube
No es solo para programadores. Para ti, es una forma de tener tu material siempre listo:
*   **Repositorios:** Carpetas inteligentes para tus apuntes, enunciados y plantillas de exámenes.
*   **Codespaces:** Un entorno de trabajo que se abre en el navegador en 5 segundos. Puedes corregir tareas o probar aplicaciones web de alumnos sin instalar nada en tu ordenador personal.

### 1.2 n8n: Tu asistente personal 24/7
Es el "pegamento" que conecta tus herramientas (Gmail, Google Sheets, Telegram, Drive). n8n trabaja mientras tú das clase, moviendo datos de un sitio a otro según tus reglas.

---

## 🤖 2. Casos de Uso Prácticos (Para tu día a día)

### 2.1 Optimización y Triaje de Correo Electrónico
¿Recibes cientos de correos de alumnos preguntando lo mismo?
*   **El Flujo:** n8n lee tus correos entrantes. Si el asunto contiene "Duda" o "Entrega", lo etiqueta automáticamente en Gmail y lo registra en un panel de control.
*   **Auto-Respuesta Inteligente:** Si detecta palabras clave (ej. "fecha examen"), n8n puede enviar una respuesta automática con el calendario de exámenes, ahorrándote responder manualmente a cada uno.

### 2.2 Sistema de Detección de Plagio y Calidad
Para las entregas de aplicaciones web (IAW) o lenguajes de marcas:
*   **El Flujo:** Cuando un alumno sube su tarea, n8n la recibe, extrae el texto y lo compara con las entregas de otros alumnos o años anteriores usando una IA (como GPT) o scripts de comparación de archivos.
*   **El Resultado:** n8n te envía un informe de "similitud" directamente a tu correo, señalando qué partes son sospechosas antes de que tú abras el archivo.

### 2.3 Gestión Automática de Tutorías
*   **El Flujo:** En lugar de hilos interminables de correos, n8n conecta tu calendario con un formulario. El alumno elige hueco, n8n crea la cita, genera el enlace de la reunión (Meet/Teams) y os envía el recordatorio a ambos.

---

## 🔐 3. Seguridad y Privacidad: El Protocolo MPC

En el ámbito docente manejas datos extremadamente sensibles (DNI, expedientes, salud). El **Multi-Party Computation (MPC)** es tu aliado invisible:

*   **¿Cómo te ayuda?:** Permite realizar cálculos sobre datos de alumnos (ej. estadísticas de aprobados por zona o becas) sin que nadie (ni el informático, ni la plataforma cloud) pueda ver el contenido real de los datos.
*   **Privacidad por Diseño:** Te permite cumplir con la **RGPD** de forma matemática. Podrías comparar tus notas con las de otros centros para ver el nivel medio sin que ningún centro exponga las notas de sus alumnos individuales.

---

## 💡 Tu Nueva Rutina
1.  **Centraliza** tus materiales en GitHub.
2.  **Automatiza** el filtrado de tus correos y dudas con n8n.
3.  **Delega** la vigilancia del plagio y la agenda a flujos de trabajo inteligentes.

---

> [!TIP]
> **Consejo Final:** No intentes automatizarlo todo a la vez. Elige la tarea que más te quita el sueño (ej. "los correos de dudas") y empieza por ahí. La tecnología debe trabajar para ti, no al revés.
