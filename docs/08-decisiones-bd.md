# Decisiones que condicionan la base de datos

**Para qué sirve:** explica las decisiones que hay que tomar antes de dibujar el modelo de datos.

Conceptos usados aquí:

- **Global:** dato común a toda la plataforma; no pertenece a una empresa.
- **`EmpresaId`:** columna que indica a qué empresa pertenece cada registro.

| # | Tema | Decisión recomendada | Por qué |
|---|---|---|---|
| D1 | Usuarios y empresas | El usuario es global y se une a cada empresa mediante una membresía que guarda su rol. La sesión trabaja con una sola empresa activa | Una persona puede estar en varias empresas, y al iniciar sesión aún no se sabe en cuál trabajará |
| D2 | Alta de empresa | Registro propio: quien registra queda como Administrador de empresa | Es el modelo SaaS y no requiere intervención manual |
| D3 | Rol y cargo | Separados: el rol da permisos; presidente, secretario, propietario y suplente son datos de la comisión | Los cargos vencen a los 2 años y no equivalen a permisos |
| D4 | Jerarquía | Empresa → centro de trabajo → área. Cada comisión pertenece a un centro de trabajo | Las constructoras operan en varios sitios, y la ley permite varias comisiones |
| D5 | Trabajadores | Solo tienen cuenta quienes participan. El número de trabajadores permanentes se guarda en cada centro | Evita construir un módulo de personal |
| D6 | Tareas | Una sola entidad Tarea con su origen, para todos los módulos | Unifica seguimiento, evidencia, notificaciones y panel |
| D7 | Catálogos | Globales: sectores, requisitos, preguntas, reglas, peligros y plantillas | Es contenido común que se reutiliza entre empresas |
| D8 | Diagnóstico | Cada aplicación es un registro propio, con dos resultados: peligros sugeridos y brechas | Permite comparar el avance en el tiempo |
| D9 | Peligros y riesgos | El peligro es un catálogo global. El riesgo es de la empresa, enlazado a un peligro y a un área, y empieza como "sugerido" | Dos empresas tienen el mismo peligro con evaluaciones distintas |
| D10 | Evaluaciones | Tabla aparte para las evaluaciones, con su tipo: inicial o residual | Conserva el historial y evita sobrescribir |
| D11 | Accidentes | El evento guarda sus personas afectadas en una tabla aparte, sin exigirles cuenta. El acceso a esa tabla se restringe | Muchos afectados no tendrán cuenta, y son datos sensibles |
| D12 | Actas | Firmada es inmutable. Cada firma guarda usuario, fecha y hash del contenido | La evidencia debe poder verificarse |
| D13 | Documentos | La plantilla es global. El documento es de la empresa y cada versión es un registro propio | Una versión aprobada nunca cambia |
| D14 | Notificaciones | Una fila por destinatario, con su evento de origen y estado de lectura | Cada persona marca lo que ya vio |
| D15 | Archivos | La base de datos guarda los datos del archivo y su enlace. El archivo va en un almacenamiento externo | El servidor gratuito pierde sus archivos al reiniciarse |
| D16 | Integridad entre empresas | Toda relación entre tablas con `EmpresaId` debe quedar dentro de la misma empresa | Filtrar las consultas no impide guardar una referencia cruzada |

## Datos que no se guardan

Para cumplir la tercera forma normal (3FN), estos valores se calculan cuando se necesitan:

- Porcentaje de cumplimiento.
- Nivel de riesgo, a partir de probabilidad y severidad.
- Número de representantes de la comisión.
- Tareas vencidas y estadísticas de accidentes.
