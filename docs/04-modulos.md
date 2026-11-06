# Módulos

**Para qué sirve:** describe qué hace cada módulo y dónde se usa.

Las historias detalladas de cada módulo están en [historias de usuario](10-historias-usuario.md).

## M1. Empresas y acceso

**Propósito:** dar a cada empresa un espacio aislado y controlar quién entra.

- Registrar una empresa e iniciar sesión.
- Agregar usuarios y asignar roles.
- Elegir o cambiar de empresa, si el usuario pertenece a varias.
- Administrar los contenidos comunes de la plataforma.

**Se usa en:** web. Iniciar sesión y cambiar de empresa también en teléfono.

## M2. Perfil de empresa

**Propósito:** conocer a la empresa para saber qué le aplica.

- Elegir el sector: oficina administrativa, comercio o tienda, maquila o fábrica, o construcción.
- Registrar centros de trabajo (cada lugar físico) y sus trabajadores permanentes.
- Registrar áreas dentro de cada centro.
- Calcular cuántos representantes necesita la Comisión Mixta.

**Se usa en:** web.

## M3. Diagnóstico de contexto

**Propósito:** entender a la organización para identificar sus riesgos y medir qué le falta.

Es un solo formulario con preguntas según el sector: actividades, instalaciones, equipos, sustancias, trabajo en alturas, prácticas actuales y documentación existente. Corresponde a la idea de "contexto de la organización" de ISO 45001.

Al finalizar, da dos resultados:

1. **Peligros sugeridos,** que pasan a la matriz de riesgos para que el Responsable de SST los confirme.
2. **Porcentaje de cumplimiento y brechas.** Una brecha es algo que la norma o la ley piden y la empresa aún no tiene.

Los resultados salen de reglas guardadas en un catálogo. Por ejemplo: si la empresa responde que trabaja en alturas, se sugiere el peligro de caída. Cada resultado indica qué respuesta lo originó. El diagnóstico se puede repetir para comparar el avance.

**Se usa en:** web.

## M4. Matriz de riesgos

**Propósito:** identificar, evaluar y controlar los riesgos de la empresa.

- Revisar los peligros sugeridos y agregar otros.
- Evaluar cada riesgo por probabilidad y severidad para obtener su nivel.
- Definir controles, de mayor a menor efectividad: eliminar, sustituir, controles de ingeniería, controles administrativos y equipo de protección personal.
- Volver a evaluar con los controles aplicados, lo que da el riesgo residual.
- Ver la matriz completa y su historial.

Un peligro es lo que puede causar daño, como una escalera en mal estado. El riesgo combina qué tan probable es el daño y qué tan grave sería.

**Se usa en:** web.

## M5. Plan de trabajo

**Propósito:** convertir lo detectado en acciones con dueño y fecha.

- Generar tareas desde riesgos y brechas. Otras tareas llegan de hallazgos, accidentes y acuerdos de reunión.
- Asignar responsable y fecha.
- Atender tareas y adjuntar evidencia.
- Filtrar y ver lo vencido.

**Se usa en:** web. Atender tareas y adjuntar evidencia también en teléfono.

## M6. Accidentes e incidentes

**Propósito:** registrar lo ocurrido, entender por qué pasó y evitar que se repita.

- Reportar accidentes, incidentes (lo que estuvo a punto de causar daño) y enfermedades profesionales.
- Registrar a las personas afectadas y los días perdidos.
- Investigar causas y definir medidas correctivas.
- Revisar la matriz de riesgos a partir de lo aprendido.
- Consultar estadísticas.

**Se usa en:** teléfono y web para reportar. Web para investigar y consultar.

## M7. Comisión y actas

**Propósito:** gestionar lo que la ley exige a la Comisión Mixta de Higiene y Seguridad.

- Registrar la comisión y sus integrantes, con su periodo de 2 años.
- Programar reuniones ordinarias y extraordinarias.
- Registrar asistencia y verificar quórum.
- Redactar, aprobar y firmar actas.
- Convertir acuerdos en tareas y consultar el historial.

**Se usa en:** web. Firmar actas también en teléfono.

## M8. Inspecciones QR

**Propósito:** registrar las inspecciones en el sitio, con evidencia.

- Crear puntos de inspección, como un extintor o un tablero eléctrico, con su código QR.
- Escanear el código y llenar su lista de verificación.
- Registrar hallazgos con foto, fecha y hora.
- Generar tareas desde los hallazgos.
- Controlar las visitas mensuales.

**Se usa en:** teléfono. Crear puntos y consultar resultados en web.

## M9. Políticas y procedimientos

**Propósito:** generar la documentación del sistema de gestión sin partir de cero.

- Elegir una plantilla, como la política de SST o un procedimiento de investigación de accidentes.
- Generar el documento con los datos de la empresa.
- Editar el borrador, aprobarlo y publicarlo.
- Crear versiones nuevas y conservar las anteriores.

**Se usa en:** web. Consultar los documentos vigentes también en teléfono.

## M10. Reportes

**Propósito:** generar documentos oficiales con los datos ya capturados.

- Informe semestral a las autoridades de trabajo.
- Informe anual a la Secretaría de Trabajo, con copia al Instituto Hondureño de Seguridad Social (IHSS).
- Actas firmadas en PDF.
- Historial de informes generados.

**Se usa en:** web.

## M11. Notificaciones

**Propósito:** avisar a cada persona lo que debe atender.

- Tareas asignadas y próximas a vencer.
- Reuniones convocadas.
- Informes y obligaciones próximas.
- Accidentes graves.
- Documentos por aprobar y actas por firmar.

Llegan dentro de la aplicación y por correo electrónico.

**Se usa en:** teléfono y web.

## M12. Panel de avance

**Propósito:** mostrar de un vistazo cómo va la empresa.

- Porcentaje de cumplimiento.
- Riesgos por nivel.
- Tareas pendientes y vencidas.
- Obligaciones del mes.
- Documentación lista para una auditoría.

Este módulo no guarda datos propios: lee los de los demás.

**Se usa en:** web.
