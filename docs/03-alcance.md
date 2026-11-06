# Alcance

**Para qué sirve:** define qué se construye, en qué orden y qué queda fuera.

MVP significa "producto mínimo viable": la versión más pequeña que ya resuelve el problema para un cliente real.

## Qué incluye

SST360 tiene 12 módulos, descritos en [módulos](04-modulos.md).

| # | Módulo | En una frase |
|---|---|---|
| M1 | Empresas y acceso | Cada empresa tiene su espacio y sus usuarios |
| M2 | Perfil de empresa | Sector, centros de trabajo y áreas |
| M3 | Diagnóstico de contexto | Formulario que sugiere peligros y mide el cumplimiento |
| M4 | Matriz de riesgos | Identificar, evaluar y controlar riesgos |
| M5 | Plan de trabajo | Tareas con responsable, fecha y evidencia |
| M6 | Accidentes e incidentes | Registrar e investigar lo ocurrido |
| M7 | Comisión y actas | Reuniones y actas firmadas de la Comisión Mixta |
| M8 | Inspecciones QR | Inspecciones y hallazgos desde el teléfono |
| M9 | Políticas y procedimientos | Documentos generados con datos de la empresa |
| M10 | Reportes | Informes obligatorios y actas en PDF |
| M11 | Notificaciones | Avisos de lo pendiente |
| M12 | Panel de avance | Vista general de la empresa |

## Web y teléfono

SST360 es multiplataforma, con reparto según el uso:

- **Teléfono, para el trabajo de campo:** inspecciones, reportar accidentes, atender tareas, firmar actas y recibir notificaciones.
- **Web, para todo lo demás:** configuración, diagnóstico, matriz de riesgos, documentos, reportes y panel. La web también incluye las funciones del teléfono.

La tecnología para construirlo se decidirá más adelante.

## Cómo se construye: un MVP en 3 entregas

Antes de escribir código, el equipo completa el diseño (historias HU-DIS). Después, el MVP se construye en 3 entregas, ordenadas según lo que depende de qué.

| Entrega | Módulos | Qué se puede demostrar al terminar |
|---|---|---|
| E1. Base y riesgos | M1 a M5 | Una empresa se registra, llena el formulario, obtiene su matriz de riesgos y su plan de trabajo |
| E2. Operación | M6 a M8 y app para teléfono | Se registran accidentes, la comisión trabaja y se inspecciona con QR desde el teléfono |
| E3. Documentos y seguimiento | M9 a M12 | Se generan políticas e informes, llegan notificaciones y el panel muestra el avance |

### Por qué un solo MVP y no varios

- **El curso califica una sola entrega final.** Lo que quede en un "MVP 2" no suma nota.
- **Las entregas evitan terminar con todo a medias.** Cada una deja algo completo y demostrable.
- **Definen qué recortar.** Las entregas indican qué sacrificar primero.

Si falta tiempo, se recorta en este orden:

1. Historias Should de E3.
2. Historias Should de E2.
3. La app para teléfono, conservando esas funciones en la web adaptada a pantallas pequeñas.

**Advertencia:** el alcance es grande: 12 módulos y dos aplicaciones. Aún falta confirmar cuántas personas hay y cuánto tiempo queda. Si el total no cabe, debe decidirse antes de comenzar E2, no al final. La [rúbrica](02-requisitos-curso.md) premia la calidad de la base técnica más que la cantidad de módulos.

## Fuera de alcance

- Capacitaciones.
- Auditorías internas.
- Normas distintas de ISO 45001 y de la legislación hondureña de SST.
- Envío directo de informes a la Secretaría de Trabajo: la empresa descarga el documento y lo presenta.
- Facturación y planes de pago.
- Trabajo sin conexión a internet.

## Supuestos

- Los clientes son empresas con 10 o más trabajadores permanentes.
- Cada empresa corresponde a un solo sector.
- Hay conexión a internet durante inspecciones y reportes.
- La firma electrónica es la de un usuario autenticado, no una firma avanzada certificada.
- El contenido del formulario, los peligros y las plantillas lo redacta el equipo en cantidad reducida por sector, y debe revisarlo alguien con conocimiento de SST.

## Limitaciones

- **Infraestructura gratuita:** el servicio gratuito de Render se suspende tras 15 minutos sin uso, tarda hasta un minuto en reactivarse y pierde los archivos que tenga guardados. Las fotos y evidencias necesitan un almacenamiento externo.
- **Espacio de base de datos:** el plan gratuito de Neon ronda 1 GB por proyecto. Conviene confirmarlo antes de depender de esa cifra.
- **ISO 45001 tiene derechos de autor:** se cita por número de cláusula y se redacta con palabras propias.
- **Reglamento revisado:** versión reformada publicada en La Gaceta 30,523, del 19 de octubre de 2004. No se comprobó si tiene reformas posteriores.
