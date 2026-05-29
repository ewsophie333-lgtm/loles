# Guia de Productividad para Docencia

Preparado para: Prof. Loles

Objetivo: Reducir la carga de tareas repetitivas y recuperar tiempo para la docencia real, sin caer en la trampa de automatizar por automatizar.

---

## INDICE

1. El kit basico
2. Casos practicos para el dia a dia
   - Correo administrativo y del centro
   - Como detectar codigo generado por IA en examenes
3. Seguridad y privacidad de los datos del alumnado
4. Recursos para aprender a tu ritmo
5. Por donde empezar

---

## 1. EL KIT BASICO

### GitHub y Codespaces

No es solo para informaticos. Para un profesor de FP o Bachillerato es util porque:

+---------------+--------------------------------+----------------------------------+
|  CONCEPTO     |  QUE ES                        |  PARA QUE TE SIRVE               |
+---------------+--------------------------------+----------------------------------+
| Repositorios  | Carpetas con historial         | Guardas apuntes, examenes y      |
|               | de cambios                     | plantillas. Si borras algo,      |
|               |                                | lo recuperas.                    |
+---------------+--------------------------------+----------------------------------+
| Codespaces    | Entorno de trabajo en          | Abrelo desde el navegador.       |
|               | el navegador                   | Corrige proyectos de alumnos     |
|               |                                | sin instalar nada.               |
+---------------+--------------------------------+----------------------------------+
| Commits       | Registro de cada cambio        | Ves como ha trabajado el alumno. |
|               |                                | 500 lineas de golpe = sospechoso.|
+---------------+--------------------------------+----------------------------------+

Ventaja real: no dependes del ordenador del centro ni del tuyo propio. Todo esta en la nube.

### n8n: automatizacion sin complicaciones

n8n conecta servicios que normalmente no se hablan: Gmail, Google Sheets, Telegram, Drive. Funciona con reglas que tu defines.

Ejemplo sencillo: cuando llega un email de la secretaria, n8n lo etiqueta y te crea una tarea con la fecha limite. Tu no tienes que estar pendiente de la bandeja de entrada cada hora.

---

## 2. CASOS PRACTICOS PARA EL DIA A DIA

### Correo administrativo y del centro

Como docente en un instituto publico espanol, recibes constantemente: convocatorias de reuniones de departamento, actas, mensajes de secretaria, boletines de notas, comunicados de la direccion, etc.

CLASIFICACION INTELIGENTE

    Correo entrante (Gmail / Outlook)
              |
              v
         [ Flujo n8n ]
              |
      +-------+-------+
      |               |
      v               v
  PRIORIDAD ALTA    PRIORIDAD BAJA
  (Direccion /      (Boletines /
   Secretaria)       Generales)
      |               |
      v               v
  Etiqueta roja     Resumen diario
  + Tarea urgente     por Telegram
                      a la hora que tu elijas

Un flujo de n8n puede:

1. Leer tus correos entrantes
2. Detectar si el remitente es direccion, secretaria o jefatura de estudios
3. Asignar prioridad y crear una tarea en tu gestor (Todoist, Google Tasks) con el plazo
4. Los correos de poca urgencia se acumulan y te llega un solo resumen diario por Telegram

Esto evita que estes pendiente del movil durante las clases.

---

### Como detectar codigo generado por IA en examenes

En modulos como IAW, Lenguaje de Marcas o programacion de FP, los alumnos usan ChatGPT o Copilot para resolver examenes practicos. Esto no es ayuda, es trampantojo.

ESTRATEGIAS QUE FUNCIONAN

1. ANALISIS CON n8n + MODELO DE LENGUAJE

    Entrega de examen
    (GitHub / Formulario)
            |
            v
      [ Flujo n8n ]
            |
            v
      { Analisis GPT-4 }
            |
            v
    Informe de patrones
    sospechosos
            |
            v
      Revision humana
      y decision final

El flujo recibe el codigo y lo envia a un modelo con instrucciones especificas: "Analiza este codigo e identifica patrones tipicos de generacion automatica o inconsistencias con el nivel del alumno". El resultado es una orientacion, NO una sentencia firme. Tu decides.

2. HISTORIAL DE GIT

Exige que los examenes se entreguen via GitHub. Revisa los commits:

    +-------------------------+-------------------------+
    |   TRABAJO REAL          |   CODIGO PEGADO DE IA   |
    +-------------------------+-------------------------+
    | Commits graduales       | Un solo commit masivo   |
    | con mensajes            | con todo perfecto       |
    | descriptivos            | de golpe                |
    +-------------------------+-------------------------+
    | Evolucion visible       | Sin evolucion logica    |
    | del codigo              |                         |
    +-------------------------+-------------------------+
    | Commits en horario      | Actividad a horas       |
    | de clase                | inusuales               |
    +-------------------------+-------------------------+

3. CODESPACES EN DIRECTO

Con Live Share puedes entrar a la sesion del alumno mientras trabaja y ver como construye la logica. Tambien puedes revisar el historial de comandos de la terminal.

ADVERTENCIA IMPORTANTE

Estas herramientas son orientativas. La decision final siempre es humana. No se trata de crear un clima de vigilancia punitiva, sino de mantener la equidad para quienes si estudian. Un falso positivo puede perjudicar a un alumno que si ha trabajado.

---

## 3. SEGURIDAD Y PRIVACIDAD DE LOS DATOS DEL ALUMNADO

En un centro educativo espanol manejas datos sensibles: DNI, expedientes academicos, datos de salud, becas, situacion socioeconomica. La LOPD y el RGPD se cumplen, no son sugerencias.

MULTI-PARTY COMPUTATION (MPC)

Es un protocolo que permite hacer calculos sobre datos sin que nadie vea el contenido real. Ni el informatico del centro, ni la plataforma en la nube.

+----------------+---------------------------+---------------------------+
|    ESCENARIO   |         SIN MPC           |          CON MPC          |
+----------------+---------------------------+---------------------------+
| Estadisticas   | Expones notas             | Calculos sobre datos      |
| de aprobados   | individuales al           | cifrados. Nadie ve        |
| por zona       | informatico / plataforma  | el contenido real.        |
+----------------+---------------------------+---------------------------+
| Comparacion    | Cada centro expone        | Comparacion del nivel     |
| entre centros  | sus datos completos       | medio sin revelar notas   |
|                |                           | individuales.             |
+----------------+---------------------------+---------------------------+
| Becas y        | Riesgo de filtracion      | Cumplimiento matematico   |
| ayudas         | de datos sensibles        | de la normativa.          |
+----------------+---------------------------+---------------------------+

Ejemplos practicos:

- Comparar tasas de aprobados entre centros para ver el nivel medio sin que ningun centro exponga las notas individuales de sus alumnos.
- Procesar estadisticas de becas sin que los datos personales queden expuestos en servidores externos.

---

## 4. RECURSOS PARA APRENDER A TU RITMO

Todos gratuitos y orientados a la practica.

GITHUB Y CODESPACES

+----------------------------+---------------------------------------------+
|         RECURSO            |              DESCRIPCION                    |
+----------------------------+---------------------------------------------+
| GitHub Skills (oficial)    | Retos practicos paso a paso. Recomendado    |
|                            | para docentes: "Introduction to GitHub".    |
+----------------------------+---------------------------------------------+
| GitHub Education           | Recursos exclusivos para profesores,        |
|                            | incluyendo GitHub Classroom.                |
+----------------------------+---------------------------------------------+

n8n

+----------------------------+---------------------------------------------+
|         RECURSO            |              DESCRIPCION                    |
+----------------------------+---------------------------------------------+
| n8n Academy (oficial)      | Cursos por niveles (basico, intermedio,     |
|                            | avanzado) con certificaciones.              |
+----------------------------+---------------------------------------------+
| Plantillas de flujos       | Automatizaciones predisenadas que clonas    |
| para educacion             | en un clic.                                 |
+----------------------------+---------------------------------------------+

INTELIGENCIA ARTIFICIAL APLICADA A LA DOCENCIA

+----------------------------+---------------------------------------------+
|         RECURSO            |              DESCRIPCION                    |
+----------------------------+---------------------------------------------+
| Documentacion n8n + OpenAI | Guia para triaje de correos y               |
|                            | analisis de codigo.                         |
+----------------------------+---------------------------------------------+
| Google AI Essentials       | Basico pero util para entender como         |
| (Coursera)                 | redactar instrucciones eficientes.          |
+----------------------------+---------------------------------------------+

---

## 5. POR DONDE EMPEZAR

No intentes montarlo todo de golpe. Elige el problema que mas te quita tiempo o paciencia.

    +----------------------+
    |  1. CENTRALIZA       |
    |  tus materiales      |
    |  en GitHub           |
    +----------+-----------+
               |
               v
    +----------------------+
    |  2. AUTOMATIZA       |
    |  el filtrado de      |
    |  correos con n8n     |
    +----------+-----------+
               |
               v
    +----------------------+
    |  3. REVISA           |
    |  el historial de     |
    |  commits para        |
    |  detectar plagio     |
    +----------------------+

Algunos ejemplos reales para empezar:

- "Me vuelvo loca con los emails de la secretaria"
- "No se si este codigo lo ha hecho el alumno o ChatGPT"

Empieza por uno. Monta el flujo. Cuando funcione, pasa al siguiente.

La tecnologia debe quitarte trabajo, no anadirlo.

---

CONSEJO FINAL

La IA es una herramienta. En el aula, el criterio humano del docente sigue siendo lo unico que no se puede automatizar. Usa estas herramientas para liberarte de las tareas repetitivas y dedicar ese tiempo a lo que realmente importa: ensenar.
