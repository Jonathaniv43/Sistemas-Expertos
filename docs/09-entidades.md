# Entidades candidatas

**Para qué sirve:** lista los datos principales que guardará SST360. Es el punto de partida del diccionario de datos.

Es una lista conceptual: todavía no incluye atributos ni relaciones. Puede cambiar durante el diseño.

## Tipos de entidad

- **Raíz:** la empresa, de la que depende toda la información.
- **Global:** común a toda la plataforma, sin `EmpresaId`.
- **Con `EmpresaId`:** pertenece a una empresa.

El curso exige `EmpresaId` en las tablas transaccionales principales. Aquí se incluye en todas las de empresa, para que el filtro automático funcione igual en todas y se pueda aplicar la decisión D16.

## Lista

| Tipo | Entidad | Qué guarda | Módulo |
|---|---|---|---|
| Raíz | Empresa | Cada empresa cliente | M1 |
| Global | Usuario | Cuenta de cada persona | M1 |
| Global | Rol | Roles del sistema | M1 |
| Global | Sector | Los 4 sectores | M2 |
| Global | RequisitoNorma | Lo que piden la norma y la ley | M3 |
| Global | PreguntaDiagnostico | Preguntas del formulario | M3 |
| Global | ReglaDiagnostico | Qué respuesta produce qué resultado | M3 |
| Global | Peligro | Catálogo de peligros | M3, M4 |
| Global | PlantillaTarea | Tareas modelo | M3, M5 |
| Global | PlantillaChecklist | Listas de verificación modelo | M8 |
| Global | PlantillaDocumento | Políticas y procedimientos modelo | M9 |
| Con `EmpresaId` | Membresia | Usuario, empresa y rol | M1 |
| Con `EmpresaId` | RegistroAuditoria | Acciones importantes | Todos |
| Con `EmpresaId` | CentroTrabajo | Lugares físicos | M2 |
| Con `EmpresaId` | Area | Áreas de cada centro | M2 |
| Con `EmpresaId` | Diagnostico | Cada aplicación del formulario | M3 |
| Con `EmpresaId` | RespuestaDiagnostico | Respuestas | M3 |
| Con `EmpresaId` | Brecha | Requisitos pendientes | M3 |
| Con `EmpresaId` | RiesgoEmpresa | Riesgos de la empresa | M4 |
| Con `EmpresaId` | EvaluacionRiesgo | Evaluaciones inicial y residual | M4 |
| Con `EmpresaId` | Control | Medidas de cada riesgo | M4 |
| Con `EmpresaId` | Tarea | Tareas de todos los orígenes | M5 |
| Con `EmpresaId` | Archivo | Datos y enlace de evidencias y fotos | M5, M8 |
| Con `EmpresaId` | Accidente | Accidentes, incidentes y enfermedades | M6 |
| Con `EmpresaId` | PersonaAfectada | Personas afectadas y días perdidos | M6 |
| Con `EmpresaId` | InvestigacionAccidente | Causas y conclusiones | M6 |
| Con `EmpresaId` | Comision | Comisión de un centro | M7 |
| Con `EmpresaId` | IntegranteComision | Miembros, cargos y periodos | M7 |
| Con `EmpresaId` | Reunion | Reuniones | M7 |
| Con `EmpresaId` | Asistencia | Asistencia por reunión | M7 |
| Con `EmpresaId` | Acta | Actas | M7 |
| Con `EmpresaId` | FirmaActa | Firmas de cada acta | M7 |
| Con `EmpresaId` | PuntoInspeccion | Elementos con QR | M8 |
| Con `EmpresaId` | Inspeccion | Cada inspección | M8 |
| Con `EmpresaId` | ItemInspeccion | Respuestas del checklist | M8 |
| Con `EmpresaId` | Hallazgo | Problemas encontrados | M8 |
| Con `EmpresaId` | Documento | Políticas y procedimientos de la empresa | M9 |
| Con `EmpresaId` | VersionDocumento | Cada versión | M9 |
| Con `EmpresaId` | Informe | Informes generados | M10 |
| Con `EmpresaId` | Notificacion | Avisos por usuario | M11 |

**M12 no tiene entidades propias:** solo lee datos de los demás módulos.
