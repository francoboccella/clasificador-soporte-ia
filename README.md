# Clasificador Inteligente de Solicitudes de Soporte con IA

**Proyecto final – Diplomatura en Inteligencia Artificial para No Programadores | UTN (2026)**

## Descripción del proyecto

Desarrollé un prototipo de automatización utilizando Make e inteligencia artificial para optimizar la gestión de correos electrónicos de soporte técnico.

El sistema analiza los mensajes recibidos, identifica su categoría, determina la prioridad de las solicitudes de soporte y genera un resumen del problema. Posteriormente, registra la información en Google Sheets y envía notificaciones al equipo mediante Slack.

## Problema que resuelve

La clasificación manual de correos electrónicos puede generar demoras en la atención, dificultades para identificar solicitudes urgentes y falta de organización en el seguimiento de incidentes.

Este proyecto propone automatizar esas tareas para facilitar la gestión y priorización de solicitudes.

## Tecnologías utilizadas

- **Make:** diseño y orquestación del flujo de automatización.
- **Gmail:** detección y recepción de correos electrónicos.
- **OpenAI (GPT-5 nano):** análisis, clasificación y resumen mediante IA generativa.
- **JSON:** estructuración de los resultados generados por la IA.
- **Google Sheets:** registro y seguimiento de solicitudes.
- **Slack:** envío de notificaciones al equipo de soporte.

## Funcionamiento de la automatización

1. Gmail detecta un nuevo correo electrónico.
2. OpenAI analiza su contenido y lo clasifica como solicitud de soporte, factura, spam u otro.
3. Si corresponde a soporte técnico, determina la prioridad: alta, media, baja o revisión manual.
4. El módulo JSON procesa la respuesta estructurada.
5. Un filtro permite registrar las solicitudes de soporte en Google Sheets.
6. Slack recibe una notificación con la prioridad, el resumen y los datos relevantes de la solicitud.

## Criterios de prioridad

| Prioridad | Criterio |
|---|---|
| Alta | Incidentes que bloquean operaciones importantes. |
| Media | Fallas parciales que permiten continuar operando. |
| Baja | Cambios de contenido o solicitudes sin impacto inmediato. |
| Revisión manual | Información insuficiente para determinar la urgencia. |

## Arquitectura del proyecto

**Gmail → OpenAI → JSON → Google Sheets → Slack**

La solución fue desarrollada mediante un escenario de Make que integra los diferentes servicios.

## Archivos del proyecto

El repositorio contiene un Blueprint en formato JSON con la configuración del escenario de Make, preparado para su revisión técnica.

Para ejecutarlo es necesario importar el escenario en Make, configurar las conexiones correspondientes y seleccionar los recursos de Google Sheets y Slack.

## Estado del proyecto

**Prototipo académico finalizado.**

Desarrollado como trabajo práctico final de la Diplomatura en Inteligencia Artificial para No Programadores de la UTN.

El proyecto demuestra conocimientos prácticos de automatización de procesos, integración de servicios, ingeniería de prompts, procesamiento de datos estructurados y aplicación de inteligencia artificial a problemas operativos.
