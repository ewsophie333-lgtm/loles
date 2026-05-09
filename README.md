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

### 3.3 Casos de Uso en ASIX
*   **Gestión de Claves (Wallets):** Firmar transacciones sin que una sola máquina tenga la clave privada completa.
*   **Auditorías de Privacidad:** Sumar estadísticas de salud o financieras de varios clientes sin violar la RGPD.

---

## 🚀 Fase 4: Proyecto de Integración Práctica

Para consolidar el aprendizaje, propongo este ejercicio:

**"El Notificador Automático de Repositorio"**
*   **Paso 1:** Configurar un Webhook en GitHub que avise cuando alguien haga un *Push*.
*   **Paso 2:** Recibir ese Webhook en n8n.
*   **Paso 3:** Filtrar en n8n (usando un nodo `IF`) si el commit contiene la palabra "error".
*   **Paso 4:** Si es un error, enviar un mensaje automático por Telegram o Email al profesor.

---

## 📚 Recursos Recomendados

| Recurso | Tipo | Enlace |
| :--- | :--- | :--- |
| **GitHub Skills** | Curso Interactivo | [skills.github.com](https://skills.github.com/) |
| **n8n Academy** | Cursos Gratuitos | [academy.n8n.io](https://academy.n8n.io/) |
| **Codespaces Docs** | Documentación Oficial | [docs.github.com/codespaces](https://docs.github.com/en/codespaces) |

---

> [!TIP]
> **Consejo para Loles:** La mejor forma de enseñar n8n es mediante el "aprendizaje basado en problemas". Intenta automatizar una tarea tediosa del día a día (ej. pasar notas de un CSV a una base de datos) y el interés de los alumnos será inmediato.
