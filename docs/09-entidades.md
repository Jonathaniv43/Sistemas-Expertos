# Entidades candidatas

**Para qué sirve:** lista los datos principales que guardará SST360. Es el punto de partida del diccionario de datos.

Es una lista conceptual: todavía no incluye atributos ni relaciones. Puede cambiar durante el diseño.

## Tipos de entidad

- **Raíz:** la empresa, de la que depende toda la información.
- **Global:** común a toda la plataforma, sin `EmpresaId`.
- **Con `EmpresaId`:** pertenece a una empresa.

El curso exige `EmpresaId` en las tablas transaccionales principales. Aquí se incluye en todas las de empresa, para que el filtro automático funcione igual en todas y se pueda aplicar la decisión D15.

## Lista

| Tipo | Entidad | Qué guarda | Módulo |
|---|---|---|---|
| Raíz | Empresa | Cada empresa cliente: razón social, RTN, dirección, actividad económica, rubro y trabajadores permanentes | M1, M2 |
| Global | Usuario | Cuenta de cada persona | M1 |
| Global | Rol | Roles del sistema | M1 |
| Global | Rubro | Los 4 rubros | M2 |
| Global | CategoriaRiesgo | Categorías de riesgo de cada rubro | M3 |
| Global | PreguntaExploratoria | Preguntas de cada categoría, con su peligro asociado | M3 |
| Global | OpcionPregunta | Opciones de respuesta de cada pregunta, indicando cuál revela exposición | M3 |
| Global | Peligro | Catálogo de peligros | M3, M4 |
| Global | PlantillaTarea | Tareas modelo | M4, M5 |
| Global | PlantillaDocumento | Políticas y procedimientos modelo | M9 |
| Con `EmpresaId` | Membresia | Usuario, empresa y rol | M1 |
| Con `EmpresaId` | ConexionGoogle | Cuenta de Google conectada y sus credenciales cifradas | M1 |
| Con `EmpresaId` | RegistroAuditoria | Acciones importantes | Todos |
| Con `EmpresaId` | Area | Áreas de la empresa | M2 |
| Con `EmpresaId` | Encuesta | Cada encuesta, con su formulario y enlace en Google | M3 |
| Con `EmpresaId` | EncuestaCategoria | Categorías elegidas para cada encuesta | M3 |
| Con `EmpresaId` | EncuestaPregunta | Copia de las preguntas enviadas | M3 |
| Con `EmpresaId` | EncuestaOpcion | Copia de las opciones enviadas | M3 |
| Con `EmpresaId` | RespuestaEncuesta | Cada respuesta recibida | M3 |
| Con `EmpresaId` | DetalleRespuesta | Respuesta a cada pregunta | M3 |
| Con `EmpresaId` | RiesgoEmpresa | Riesgos de la empresa | M4 |
| Con `EmpresaId` | EvaluacionRiesgo | Evaluaciones inicial y residual | M4 |
| Con `EmpresaId` | Control | Medidas de cada riesgo | M4 |
| Con `EmpresaId` | Tarea | Tareas de todos los orígenes | M5 |
| Con `EmpresaId` | Archivo | Datos y enlace de evidencias, fotos y actas de constitución | M5, M6, M7, M8 |
| Con `EmpresaId` | Accidente | Accidentes, incidentes y enfermedades profesionales | M6 |
| Con `EmpresaId` | PersonaAfectada | Personas afectadas y días de incapacidad | M6 |
| Con `EmpresaId` | InvestigacionAccidente | Causas y conclusiones | M6 |
| Con `EmpresaId` | Comision | Comisión de la empresa y su acta de constitución | M7 |
| Con `EmpresaId` | IntegranteComision | Miembros, cargos y periodos | M7 |
| Con `EmpresaId` | Reunion | Reuniones | M7 |
| Con `EmpresaId` | Asistencia | Asistencia por reunión | M7 |
| Con `EmpresaId` | Acta | Actas | M7 |
| Con `EmpresaId` | FirmaActa | Firmas de cada acta | M7 |
| Con `EmpresaId` | Equipo | Equipos y productos con su identificador | M8 |
| Con `EmpresaId` | Mantenimiento | Mantenimientos y reparaciones | M8 |
| Con `EmpresaId` | ArticuloEPP | Artículos de equipo de protección personal | M8 |
| Con `EmpresaId` | IngresoEPP | Ingresos al inventario | M8 |
| Con `EmpresaId` | EntregaEPP | Entregas a trabajadores | M8 |
| Con `EmpresaId` | Documento | Políticas y procedimientos de la empresa | M9 |
| Con `EmpresaId` | VersionDocumento | Cada versión | M9 |
| Con `EmpresaId` | Informe | Reportes generados | M10 |
| Con `EmpresaId` | EventoCalendario | Evento de Google Calendar y el registro que lo originó | M11 |

**M12 no tiene entidades propias:** solo lee datos de los demás módulos.

El detalle de cada tabla está en el [modelo de datos](12-modelo-datos.md).
