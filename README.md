# 🎓 Ruta de Aprendizaje: GitHub, Codespaces y n8n
### Preparado para: Prof. Loles
**Objetivo:** Dominar la automatización de flujos de trabajo, el desarrollo en la nube y la computación segura (MPC) para entornos educativos y profesionales.

---

## 🏗️ Fase 1: Ecosistema GitHub & Cloud Development

GitHub ha dejado de ser solo un "almacén de código" para convertirse en una plataforma de desarrollo completa.

### 1.1 Fundamentos de Git (Lo esencial)
*   **Concepto de Ramas (Branches):** Por qué nunca trabajar directamente en `main` en proyectos colaborativos.
*   **El Ciclo de Vida:** `Add` -> `Commit` -> `Push` -> `Pull Request`.
*   **Gestión de Conflictos:** Cómo resolver discrepancias cuando dos personas editan la misma línea.

### 1.2 GitHub Codespaces (El futuro del aula)
Codespaces elimina el clásico problema de "en mi ordenador no funciona".
*   **Configuración de Entornos:** Uso de archivos `.devcontainer` para preinstalar extensiones de VS Code y lenguajes (Python, Node, PHP).
*   **Port Forwarding:** Cómo exponer puertos locales (ej. 8000) a URLs públicas seguras para demostraciones.
*   **Secrets:** Gestión de variables de entorno seguras para no exponer contraseñas en el repositorio.

---

## 🤖 Fase 2: Automatización con n8n

n8n es una herramienta de automatización "fair-code" que permite conectar aplicaciones mediante nodos visuales.

### 2.1 Conceptos Core
*   **Nodos:** Cada bloque es una función (Trigger, Acción, Transformación).
*   **JSON Data:** Entender cómo fluye la información entre nodos (la estructura de "objetos").
*   **Expressions:** El uso de JavaScript básico para manipular datos entre pasos.

### 2.2 Flujos de Trabajo (Workflows)
1.  **Triggers:** Ejecución por horario (Cron), Webhooks (peticiones externas) o eventos de apps (GitHub, Telegram).
2.  **Lógica:** Uso del nodo `IF` para bifurcar el flujo y `Merge` para combinar datos de distintas fuentes.
3.  **HTTP Request:** El nodo más potente para conectar con cualquier API que no tenga un nodo oficial.

---

## 🔐 Fase 3: Introducción a MPC (Secure Multi-Party Computation)

Para un nivel avanzado de ciberseguridad, es vital entender cómo procesar datos sin verlos.

### 3.1 ¿Qué es MPC?
El **Multi-Party Computation** es un subcampo de la criptografía que permite a varias partes calcular conjuntamente una función sobre sus entradas, manteniendo dichas entradas privadas.
*   **Principio de "Caja Negra":** Varias personas ponen datos en una caja virtual; la caja da el resultado final, pero nadie ve los datos de los demás.
*   **Sin Terceros de Confianza:** No hace falta un "servidor central" que lo sepa todo; la confianza se distribuye matemáticamente.

### 3.2 ¿Cómo funciona el protocolo? (Simplificado)
1.  **Secret Sharing (Reparto de Secretos):** Un dato (ej. el número 10) se divide en "pedazos" aleatorios (shares) como 4, 3 y 3. Por separado, no dicen nada.
2.  **Computación Distribuida:** Cada nodo realiza cálculos matemáticos sobre su pedazo.
3.  **Reconstrucción:** Solo cuando los nodos combinan sus resultados parciales se obtiene la respuesta correcta (ej. la suma total de salarios sin que nadie sepa el salario de su compañero).

### 3.3 Casos de Uso Educativos (LMSGI e IAW)

Para que los alumnos de ASIX lo entiendan en sus módulos:

*   **En IAW (Implantación de Apps Web):** Configurar el despliegue de una aplicación de forma que las claves de la base de datos o los tokens de API estén fragmentados. Si un atacante vulnera el servidor web, **no podrá obtener la clave completa**, ya que solo reside una "pieza" (share) en esa máquina.
*   **En LMSGI (Lenguaje de Marcas):** Imaginad que cada alumno tiene un archivo XML con sus notas privadas. Usando MPC, podríamos calcular la nota media de toda la clase y la desviación típica **sin que nadie (ni siquiera el profesor o el sistema) vea nunca las notas individuales** de cada archivo XML. Solo se revela el resultado final agregado.
*   **Votaciones y Evaluaciones:** Realizar encuestas de satisfacción o evaluaciones entre pares (peer-review) donde los votos son totalmente anónimos y privados hasta que se alcanza el quorum para mostrar el resultado.

---

## 🚀 Fase 4: Proyecto de Integración Práctica

Para consolidar el aprendizaje, propongo este ejercicio diseñado para ahorrar tiempo en la gestión docente:

**"Gestor Inteligente de Tutorías y Dudas"**

*   **Paso 1:** Crear un formulario sencillo (Google Forms o Typeform) donde los alumnos marquen su asistencia o dejen dudas sobre la clase.
*   **Paso 2:** Configurar n8n para que escuche cada nueva respuesta del formulario.
*   **Paso 3:** Usar un nodo `IF` en n8n: 
    *   Si el alumno marca la duda como **"Urgente"**, n8n envía una notificación inmediata a tu **Telegram** o móvil.
    *   Si es una duda normal, n8n la guarda automáticamente en un **Google Sheets** organizado por temas.
*   **Paso 4:** n8n genera un correo electrónico automático de confirmación al alumno indicándole que su duda ha sido recibida y será tratada en la próxima sesión.

---

## 📚 Recursos Recomendados

| Recurso | Tipo | Enlace |
| :--- | :--- | :--- |
| **GitHub Skills** | Curso Interactivo | [skills.github.com](https://skills.github.com/) |
| **n8n Academy** | Cursos Gratuitos | [academy.n8n.io](https://academy.n8n.io/) |
| **Codespaces Docs** | Documentación Oficial | [docs.github.com/codespaces](https://docs.github.com/en/codespaces) |

---

> [!TIP]
> **Consejo para Loles:** La automatización no es solo tecnología, es **libertad**. Al delegar las tareas repetitivas (asistencia, organización de dudas, avisos) a n8n, recuperas tiempo valioso para lo que realmente importa: la mentoría directa y la calidad de la enseñanza. Empieza automatizando un solo proceso pequeño y verás cómo la clase se vuelve mucho más dinámica.
