# Historias de usuario

**Para qué sirve:** describe todo el trabajo del proyecto, historia por historia. Estas historias se cargan al tablero del equipo.

## Cómo leer este archivo

Una historia de usuario (HU) dice quién necesita algo, qué necesita y para qué. Sus criterios de aceptación indican cuándo está terminada.

| Código | Contenido |
|---|---|
| `HU-DIS-xx` | Análisis y diseño, antes de programar |
| `HU-M01-xx` a `HU-M12-xx` | Funciones de cada [módulo](04-modulos.md) |
| `HU-TEC-xx` | Trabajo técnico exigido por el [curso](02-requisitos-curso.md) o necesario para el producto |

Cada historia termina con estos datos:

- **Entrega:** Diseño, E1, E2 o E3, según el [alcance](03-alcance.md).
- **Dónde:** Web, Teléfono o ambos.
- **Prioridad:** Must (indispensable) o Should (se puede recortar si falta tiempo).
- **Depende de:** historias que deben estar listas antes.
- **Reglas:** `RN` son [reglas de negocio](07-reglas-negocio.md), `D` son [decisiones](08-decisiones-bd.md) y `art.` son artículos del [reglamento](06-marco-normativo.md).

---

## Análisis y diseño

### HU-DIS-01 | Aprobar el alcance

**Como** equipo, **quiero** aprobar los módulos, las entregas y las exclusiones, **para** saber qué vamos a construir.

**Criterios de aceptación:**

- El equipo revisó el alcance y los pendientes que le corresponden.
- La aprobación queda registrada en el tablero.

**Módulo:** Diseño · **Entrega:** Diseño · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** ninguna · **Reglas:** ninguna

### HU-DIS-02 | Documentar los requerimientos funcionales

**Como** equipo, **quiero** listar los requerimientos de cada módulo, **para** tener claro qué operaciones permite el sistema.

**Criterios de aceptación:**

- Cada requerimiento tiene identificador, descripción, actor y prioridad.
- Se indican entradas y resultados esperados.
- Cada requerimiento se relaciona con al menos una HU.

**Módulo:** Diseño · **Entrega:** Diseño · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-DIS-01 · **Reglas:** ninguna

### HU-DIS-03 | Documentar los requerimientos no funcionales

**Como** equipo, **quiero** definir las condiciones de calidad y operación, **para** que sean alcanzables con infraestructura gratuita.

**Criterios de aceptación:**

- Se documentan seguridad, aislamiento entre empresas, auditoría y mantenibilidad.
- Rendimiento y disponibilidad consideran que el servidor gratuito se suspende.
- Se define el tamaño máximo de archivos.
- Se documentan las restricciones del curso.

**Módulo:** Diseño · **Entrega:** Diseño · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-DIS-01 · **Reglas:** D15

### HU-DIS-04 | Validar las reglas de negocio

**Como** equipo, **quiero** revisar y completar las reglas de negocio, **para** que controlen correctamente el sistema.

**Criterios de aceptación:**

- Cada regla es verificable.
- Cada regla se relaciona con sus requerimientos.
- Las reglas marcadas como propuesta quedan confirmadas o ajustadas.

**Módulo:** Diseño · **Entrega:** Diseño · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-DIS-02 · **Reglas:** ninguna

### HU-DIS-05 | Priorizar el backlog

**Como** equipo, **quiero** ordenar las HUs por prioridad y dependencias, **para** saber qué se hace primero.

**Criterios de aceptación:**

- Las prioridades reflejan el tamaño del equipo y el plazo real.
- Se identifican las HUs bloqueadas por pendientes.
- El backlog queda ordenado en el tablero.

**Módulo:** Diseño · **Entrega:** Diseño · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-DIS-02, HU-DIS-16 · **Reglas:** ninguna

### HU-DIS-06 | Elaborar casos de uso

**Como** equipo, **quiero** representar los casos de uso principales, **para** visualizar qué hace cada rol.

**Criterios de aceptación:**

- Un diagrama relaciona los 4 roles con los módulos.
- Se describen los casos de uso principales.

**Módulo:** Diseño · **Entrega:** Diseño · **Dónde:** No aplica · **Prioridad:** Should · **Depende de:** HU-DIS-02 · **Reglas:** ninguna

### HU-DIS-07 | Documentar los flujos principales

**Como** equipo, **quiero** documentar los flujos del producto, **para** entender la secuencia de cada operación.

**Criterios de aceptación:**

- Se documenta registro, inicio de sesión y cambio de empresa.
- Se documenta diagnóstico → matriz de riesgos → plan de trabajo.
- Se documenta accidente → investigación → medidas → revisión de la matriz.
- Se documenta reunión → acta → aprobación → firma.
- Se documenta inspección → hallazgo → tarea.
- Se documenta plantilla → borrador → aprobación → versión vigente.
- Cada flujo indica inicio, resultado, alternativas y errores.

**Módulo:** Diseño · **Entrega:** Diseño · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-DIS-02 · **Reglas:** ninguna

### HU-DIS-08 | Elaborar el diccionario de datos

**Como** equipo, **quiero** definir entidades y atributos, **para** establecer la información que guardará la plataforma.

**Criterios de aceptación:**

- Cada entidad tiene atributos, tipos, llaves primarias y foráneas.
- Se indican los atributos obligatorios y opcionales.
- Cada entidad se clasifica como raíz, global o con `EmpresaId`.

**Módulo:** Diseño · **Entrega:** Diseño · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-DIS-01 · **Reglas:** D1 a D16

### HU-DIS-09 | Definir el aislamiento multiempresa

**Como** equipo, **quiero** definir cómo se separa la información de cada empresa, **para** garantizar que nadie vea datos ajenos.

**Criterios de aceptación:**

- Se listan las tablas con `EmpresaId` y las entidades globales.
- Se documenta el manejo de usuarios en varias empresas.
- Se define cómo se obtiene la empresa activa.
- Se documenta cómo se impiden las referencias entre empresas.

**Módulo:** Diseño · **Entrega:** Diseño · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-DIS-08 · **Reglas:** RN-04, RN-05, RN-06, RN-07, D1, D7, D16

### HU-DIS-10 | Diseñar el diagrama entidad-relación

**Como** equipo, **quiero** elaborar el ERD en tercera forma normal, **para** definir la estructura de la base de datos.

**Criterios de aceptación:**

- Muestra entidades, relaciones, cardinalidades y llaves.
- Las relaciones muchos a muchos usan entidades intermedias.
- Las tablas cumplen 1FN, 2FN y 3FN.
- Las decisiones de normalización quedan documentadas.
- Cada tabla existe en el diccionario de datos.

**Módulo:** Diseño · **Entrega:** Diseño · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-DIS-08, HU-DIS-09 · **Reglas:** D1 a D16

### HU-DIS-11 | Definir restricciones e índices

**Como** equipo, **quiero** definir restricciones e índices, **para** proteger la integridad y optimizar las consultas.

**Criterios de aceptación:**

- Se identifican restricciones de unicidad y campos obligatorios.
- Se documentan las reglas de eliminación y actualización.
- Se identifican índices frecuentes, incluido `EmpresaId`.

**Módulo:** Diseño · **Entrega:** Diseño · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-DIS-10 · **Reglas:** D16

### HU-DIS-12 | Definir los contratos de la API

**Como** equipo, **quiero** definir endpoints y DTOs, **para** acordar cómo se comunican los clientes con el backend.

**Criterios de aceptación:**

- Cada endpoint tiene método, ruta, parámetros, respuestas y códigos HTTP.
- Cada endpoint indica sus requisitos de acceso.
- Los DTOs de entrada y salida están separados de las entidades.
- Hay una estructura uniforme para errores.
- Los contratos sirven para web y teléfono.

**Módulo:** Diseño · **Entrega:** Diseño · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-DIS-02, HU-DIS-10 · **Reglas:** ninguna

### HU-DIS-13 | Diseñar la arquitectura del backend

**Como** equipo, **quiero** definir la arquitectura, **para** separar responsabilidades.

**Criterios de aceptación:**

- Se definen las capas `Domain`, `Application`, `Infrastructure` y `API`.
- Se establecen las dependencias permitidas.
- Se define dónde van los casos de uso, la persistencia y el `DbContext`.
- Se documentan la inyección de dependencias, el manejo de errores y Vertical Slicing.

**Módulo:** Diseño · **Entrega:** Diseño · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-DIS-01 · **Reglas:** ninguna

### HU-DIS-14 | Diseñar autenticación y autorización

**Como** equipo, **quiero** definir el mecanismo de acceso, **para** proteger los recursos.

**Criterios de aceptación:**

- Se definen los claims, incluida la empresa activa.
- Se define cómo se obtiene un token al cambiar de empresa.
- Se resuelve con el catedrático cómo cumplir `EmpresaId` encriptado.
- Se define la estrategia por roles (RBAC).
- Se identifican endpoints públicos y protegidos.
- Se documentan las respuestas 401 y 403.

**Módulo:** Diseño · **Entrega:** Diseño · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-DIS-09 · **Reglas:** RN-03, RN-06, D1

### HU-DIS-15 | Redactar el pitch de 1 página

**Como** equipo, **quiero** resumir SST360 en una página, **para** cumplir el entregable de la Fase 1 del curso.

**Criterios de aceptación:**

- Ocupa una página y define problema, solución, cliente y MVP.
- Coincide con el alcance aprobado.
- Indica que la plataforma prepara a la empresa y no certifica.

**Módulo:** Diseño · **Entrega:** Diseño · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-DIS-01 · **Reglas:** ninguna

### HU-DIS-16 | Configurar el tablero Kanban

**Como** equipo, **quiero** cargar las HUs en GitHub Projects, **para** dar seguimiento al trabajo.

**Criterios de aceptación:**

- Existen el repositorio y su tablero.
- Cada HU es un issue con sus criterios de aceptación.
- Los issues tienen entrega, módulo, prioridad y responsable.

**Módulo:** Diseño · **Entrega:** Diseño · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-DIS-01 · **Reglas:** ninguna

---

## M1. Empresas y acceso

### HU-M01-01 | Registrar mi empresa

**Como** representante de una empresa, **quiero** registrarla, **para** empezar a gestionar su SST.

**Criterios de aceptación:**

- Se crean la empresa, el usuario y su membresía en una sola operación.
- Quien registra queda como Administrador de empresa.
- Un identificador de empresa repetido se rechaza con un mensaje claro.
- La contraseña se guarda con hash, nunca en texto plano.

**Módulo:** M1 · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-TEC-01, HU-TEC-02 · **Reglas:** RN-01, D2

### HU-M01-02 | Iniciar y cerrar sesión

**Como** usuario, **quiero** iniciar y cerrar sesión, **para** acceder de forma segura.

**Criterios de aceptación:**

- Con una sola membresía activa entro directamente a esa empresa.
- Con varias membresías debo elegir una.
- Las credenciales incorrectas reciben un mensaje que no revela qué dato falló.
- Una membresía desactivada no da acceso a esa empresa.

**Módulo:** M1 · **Entrega:** E1 · **Dónde:** Web y teléfono · **Prioridad:** Must · **Depende de:** HU-M01-01, HU-TEC-04 · **Reglas:** RN-02, D1

### HU-M01-03 | Cambiar de empresa

**Como** usuario de varias empresas, **quiero** cambiar de empresa activa, **para** trabajar en cada una sin volver a entrar.

**Criterios de aceptación:**

- Solo veo empresas donde tengo membresía activa.
- Al cambiar, recibo un token con la nueva empresa y mi rol en ella.
- Pedir una empresa ajena devuelve 403.
- Dejan de mostrarse los datos de la empresa anterior.

**Módulo:** M1 · **Entrega:** E1 · **Dónde:** Web y teléfono · **Prioridad:** Must · **Depende de:** HU-M01-02 · **Reglas:** RN-02, RN-03, RN-05, D1

### HU-M01-04 | Agregar usuarios

**Como** Administrador de empresa, **quiero** agregar usuarios, **para** que participen en la gestión.

**Criterios de aceptación:**

- Si el correo ya existe, solo se crea la membresía.
- Si no existe, se crea el usuario y recibe un acceso temporal.
- Elijo su rol al agregarlo.
- Un usuario no puede tener dos membresías en la misma empresa.

**Módulo:** M1 · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M01-02 · **Reglas:** RN-02, D5

### HU-M01-05 | Gestionar roles y membresías

**Como** Administrador de empresa, **quiero** cambiar roles y desactivar membresías, **para** controlar quién accede.

**Criterios de aceptación:**

- Solo afecta a mi empresa.
- Desactivar no borra el historial del usuario.
- La empresa no puede quedar sin Administrador activo.
- Otros roles reciben 403.

**Módulo:** M1 · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M01-04, HU-TEC-05 · **Reglas:** RN-03, RN-08

### HU-M01-06 | Cambiar mi contraseña

**Como** usuario, **quiero** cambiar mi contraseña, **para** proteger mi cuenta.

**Criterios de aceptación:**

- Debo indicar la contraseña actual.
- La nueva cumple la política definida.
- Debo cambiar el acceso temporal al entrar por primera vez.

**Módulo:** M1 · **Entrega:** E1 · **Dónde:** Web y teléfono · **Prioridad:** Should · **Depende de:** HU-M01-02 · **Reglas:** ninguna

### HU-M01-07 | Administrar los catálogos

**Como** Administrador de plataforma, **quiero** mantener sectores, requisitos, preguntas, reglas, peligros y plantillas, **para** actualizar el contenido sin programar.

**Criterios de aceptación:**

- Puedo crear, editar y desactivar elementos.
- Los cambios no alteran diagnósticos ya realizados.
- Otros roles reciben 403.

**Módulo:** M1 · **Entrega:** E3 · **Dónde:** Web · **Prioridad:** Should · **Depende de:** HU-TEC-07 · **Reglas:** D7

### HU-M01-08 | Consultar las empresas registradas

**Como** Administrador de plataforma, **quiero** ver las empresas registradas, **para** conocer el uso de la plataforma.

**Criterios de aceptación:**

- Veo nombre, sector, fecha de registro y número de usuarios.
- No veo su información de SST.

**Módulo:** M1 · **Entrega:** E3 · **Dónde:** Web · **Prioridad:** Should · **Depende de:** HU-M01-01 · **Reglas:** RN-05

---

## M2. Perfil de empresa

### HU-M02-01 | Completar el perfil

**Como** Administrador de empresa, **quiero** registrar sector y datos generales, **para** que la plataforma sepa qué me aplica.

**Criterios de aceptación:**

- Elijo uno de los 4 sectores.
- Puedo actualizar los datos generales.

**Módulo:** M2 · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M01-01, HU-TEC-07 · **Reglas:** RN-09, D7

### HU-M02-02 | Registrar centros de trabajo

**Como** Administrador de empresa, **quiero** registrar mis centros de trabajo, **para** organizar la gestión por lugar.

**Criterios de aceptación:**

- Cada centro tiene nombre, dirección y trabajadores permanentes.
- La empresa puede tener varios centros.
- Un centro con registros asociados se desactiva, no se borra.

**Módulo:** M2 · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M02-01 · **Reglas:** art. 13, D4, D5

### HU-M02-03 | Registrar áreas

**Como** Administrador de empresa, **quiero** registrar las áreas de cada centro, **para** ubicar riesgos, puntos de inspección y responsables.

**Criterios de aceptación:**

- Cada área pertenece a un centro de mi empresa.
- Puedo asignar un Encargado de área.

**Módulo:** M2 · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M02-02 · **Reglas:** RN-07, D3, D4

### HU-M02-04 | Calcular la composición de la comisión

**Como** Responsable SST, **quiero** saber cuántos representantes necesita la comisión, **para** cumplir la ley.

**Criterios de aceptación:**

- Con 10 y 49 trabajadores indica 1 representante por parte.
- Con 50 y 99 indica 2; con 100 y 499, 3; con 500 y 999, 4; con 1000, 5.
- El resultado se calcula y no se guarda.
- Si cambia el número de trabajadores, recuerda comunicarlo a la Secretaría de Trabajo.

**Módulo:** M2 · **Entrega:** E2 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M02-02 · **Reglas:** arts. 12, 14, 17, RN-32

---

## M3. Diagnóstico de contexto

### HU-M03-01 | Responder el formulario de contexto

**Como** Responsable SST, **quiero** responder un formulario sobre mi organización, **para** identificar sus riesgos y qué le falta.

**Criterios de aceptación:**

- Las preguntas dependen del sector.
- Cubre actividades, instalaciones, equipos, sustancias, prácticas y documentación.
- Puedo guardar el avance y continuar después.
- No puedo finalizar con preguntas obligatorias sin responder.
- Finalizado, no se puede editar.

**Módulo:** M3 · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M02-03, HU-TEC-07 · **Reglas:** RN-10, RN-11, RN-12, D8

### HU-M03-02 | Obtener peligros sugeridos

**Como** Responsable SST, **quiero** que el sistema sugiera peligros según mis respuestas, **para** no empezar desde cero.

**Criterios de aceptación:**

- Al finalizar, las reglas del catálogo generan los peligros sugeridos.
- Cada sugerencia indica qué respuesta la originó.
- Las mismas respuestas producen los mismos peligros.
- Agregar una regla al catálogo cambia los resultados sin modificar código.

**Módulo:** M3 · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M03-01 · **Reglas:** art. 46.1.b, RN-14, D7, D9

### HU-M03-03 | Conocer mis brechas

**Como** Responsable SST, **quiero** ver qué requisitos me faltan, **para** saber qué debo resolver.

**Criterios de aceptación:**

- Al finalizar se generan las brechas.
- Cada brecha indica el requisito y la respuesta que la originó.

**Módulo:** M3 · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M03-01 · **Reglas:** RN-14, D8

### HU-M03-04 | Ver mi porcentaje de cumplimiento

**Como** Responsable SST, **quiero** ver mi porcentaje de cumplimiento, **para** medir qué tan preparada está la empresa.

**Criterios de aceptación:**

- Veo el porcentaje total y por grupo de requisitos.
- Se calcula desde las respuestas y no se guarda.
- La fórmula está documentada.

**Módulo:** M3 · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M03-03 · **Reglas:** RN-13

### HU-M03-05 | Repetir el diagnóstico

**Como** Responsable SST, **quiero** repetir el diagnóstico y comparar, **para** comprobar el avance.

**Criterios de aceptación:**

- Cada aplicación queda como registro propio, con su fecha.
- Puedo comparar dos aplicaciones.

**Módulo:** M3 · **Entrega:** E3 · **Dónde:** Web · **Prioridad:** Should · **Depende de:** HU-M03-04 · **Reglas:** RN-12, D8

---

## M4. Matriz de riesgos

### HU-M04-01 | Confirmar los peligros sugeridos

**Como** Responsable SST, **quiero** revisar los peligros sugeridos, **para** dejar en la matriz solo los que aplican.

**Criterios de aceptación:**

- Puedo confirmar o descartar cada sugerencia.
- Al confirmar, indico el área y se crea el riesgo.
- Un peligro sin confirmar no aparece en la matriz.

**Módulo:** M4 · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M03-02 · **Reglas:** RN-17, RN-18, D9

### HU-M04-02 | Agregar riesgos

**Como** Responsable SST, **quiero** agregar riesgos por mi cuenta, **para** incluir lo que el formulario no detectó.

**Criterios de aceptación:**

- Elijo un peligro del catálogo o lo describo.
- Indico el área y la actividad relacionada.

**Módulo:** M4 · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M02-03 · **Reglas:** RN-17, D9

### HU-M04-03 | Evaluar un riesgo

**Como** Responsable SST, **quiero** evaluar probabilidad y severidad, **para** conocer el nivel de cada riesgo.

**Criterios de aceptación:**

- Elijo probabilidad y severidad del 1 al 5, con su explicación visible.
- El sistema calcula el nivel y lo clasifica.
- Se registran evaluador y fecha.

**Módulo:** M4 · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M04-01 · **Reglas:** art. 46.1.b, RN-15, RN-16, D10

### HU-M04-04 | Ver la matriz de riesgos

**Como** Responsable SST, **quiero** ver todos mis riesgos, **para** decidir qué atender primero.

**Criterios de aceptación:**

- Veo una matriz de probabilidad por severidad con los riesgos ubicados.
- Veo también una lista filtrable por centro, área y nivel.
- Puedo abrir el detalle de cada riesgo.

**Módulo:** M4 · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M04-03 · **Reglas:** art. 47.b

### HU-M04-05 | Definir controles

**Como** Responsable SST, **quiero** definir controles, **para** reducir cada riesgo.

**Criterios de aceptación:**

- Cada control indica su tipo y descripción.
- Un riesgo alto o crítico exige al menos un control.
- Se señalan los riesgos altos sin control.

**Módulo:** M4 · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M04-03 · **Reglas:** art. 46.1.e, RN-19, RN-21

### HU-M04-06 | Evaluar el riesgo residual

**Como** Responsable SST, **quiero** evaluar el riesgo con los controles aplicados, **para** saber si bajó.

**Criterios de aceptación:**

- La evaluación residual queda separada de la inicial.
- Veo ambos niveles lado a lado.

**Módulo:** M4 · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Should · **Depende de:** HU-M04-05 · **Reglas:** RN-20, D10

### HU-M04-07 | Consultar el historial de un riesgo

**Como** Responsable SST, **quiero** ver las evaluaciones anteriores, **para** demostrar la evolución.

**Criterios de aceptación:**

- Veo todas las evaluaciones con fecha y autor.
- Una evaluación nueva no borra las anteriores.

**Módulo:** M4 · **Entrega:** E3 · **Dónde:** Web · **Prioridad:** Should · **Depende de:** HU-M04-06 · **Reglas:** art. 47.b, RN-20

---

## M5. Plan de trabajo

### HU-M05-01 | Generar el plan

**Como** Responsable SST, **quiero** convertir riesgos y brechas en tareas, **para** saber qué hacer y en qué orden.

**Criterios de aceptación:**

- Riesgos, controles y brechas producen tareas según las plantillas.
- Las tareas se ordenan por prioridad, empezando por los riesgos más altos.
- Puedo revisar el plan antes de confirmarlo.
- Generarlo dos veces no duplica tareas.

**Módulo:** M5 · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M03-03, HU-M04-05 · **Reglas:** art. 46.1.e, RN-23, D6

### HU-M05-02 | Asignar tareas

**Como** Responsable SST, **quiero** asignar responsable y fecha, **para** que cada tarea tenga dueño.

**Criterios de aceptación:**

- Solo puedo asignar usuarios activos de mi empresa.
- La tarea exige fecha límite.
- Puedo crear tareas manuales.

**Módulo:** M5 · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M05-01 · **Reglas:** RN-07, RN-22, D6

### HU-M05-03 | Atender mis tareas

**Como** Colaborador, **quiero** ver y actualizar mis tareas, **para** informar mi avance.

**Criterios de aceptación:**

- Veo mis tareas asignadas.
- Puedo pasarlas por pendiente, en progreso y completada.
- No puedo cambiar tareas ajenas.

**Módulo:** M5 · **Entrega:** E1 · **Dónde:** Web y teléfono · **Prioridad:** Must · **Depende de:** HU-M05-02, HU-TEC-05 · **Reglas:** RN-24

### HU-M05-04 | Adjuntar evidencia

**Como** responsable de una tarea, **quiero** adjuntar evidencia, **para** demostrar que se hizo.

**Criterios de aceptación:**

- Puedo adjuntar imágenes y PDF dentro del tamaño permitido.
- El archivo queda con fecha y autor.
- Solo usuarios de mi empresa pueden verlo.
- Si la tarea exige evidencia, no se completa sin ella.

**Módulo:** M5 · **Entrega:** E1 · **Dónde:** Web y teléfono · **Prioridad:** Must · **Depende de:** HU-M05-03, HU-TEC-10 · **Reglas:** RN-05, RN-25, D15

### HU-M05-05 | Filtrar el plan

**Como** Responsable SST, **quiero** filtrar tareas, **para** encontrar lo urgente.

**Criterios de aceptación:**

- Puedo filtrar por estado, responsable, origen y fecha.
- Las tareas vencidas se distinguen claramente.

**Módulo:** M5 · **Entrega:** E3 · **Dónde:** Web · **Prioridad:** Should · **Depende de:** HU-M05-02 · **Reglas:** ninguna

---

## M6. Accidentes e incidentes

### HU-M06-01 | Reportar un evento

**Como** Colaborador, **quiero** reportar un accidente o incidente desde donde esté, **para** que se atienda de inmediato.

**Criterios de aceptación:**

- Indico tipo, fecha, hora, área y descripción.
- Puedo adjuntar fotos.
- El sistema registra quién reporta y cuándo.
- Cualquier usuario de la empresa puede reportar.

**Módulo:** M6 · **Entrega:** E2 · **Dónde:** Web y teléfono · **Prioridad:** Must · **Depende de:** HU-M02-03, HU-TEC-10, HU-TEC-15 · **Reglas:** arts. 9.j, 46.1.d, RN-26, RN-27, RN-31

### HU-M06-02 | Registrar a las personas afectadas

**Como** Responsable SST, **quiero** registrar a las personas afectadas, **para** llevar el control de cada caso.

**Criterios de aceptación:**

- Registro nombre, puesto, tipo de lesión y días perdidos.
- La persona no necesita tener cuenta.
- Solo el Responsable SST y la comisión ven estos datos.

**Módulo:** M6 · **Entrega:** E2 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M06-01 · **Reglas:** art. 47.f, RN-30, D11

### HU-M06-03 | Investigar un evento

**Como** Responsable SST, **quiero** registrar causas y conclusiones, **para** entender por qué ocurrió.

**Criterios de aceptación:**

- Registro causas inmediatas y causas de fondo.
- Registro responsables de la investigación y fecha.
- El evento no se cierra sin causas y medidas.

**Módulo:** M6 · **Entrega:** E2 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M06-01 · **Reglas:** arts. 25.d, 46.1.a, RN-28

### HU-M06-04 | Definir medidas correctivas

**Como** Responsable SST, **quiero** convertir las medidas en tareas, **para** evitar que se repita.

**Criterios de aceptación:**

- Cada medida crea una tarea con origen "accidente".
- Desde el evento veo el avance de sus medidas.

**Módulo:** M6 · **Entrega:** E2 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M06-03, HU-M05-02 · **Reglas:** art. 46.1.a, RN-23, D6

### HU-M06-05 | Actualizar la matriz tras un evento

**Como** Responsable SST, **quiero** enlazar el evento con un riesgo, **para** revisar la matriz con lo aprendido.

**Criterios de aceptación:**

- Puedo enlazarlo a un riesgo existente o crear uno nuevo.
- Puedo reevaluar el riesgo enlazado.

**Módulo:** M6 · **Entrega:** E2 · **Dónde:** Web · **Prioridad:** Should · **Depende de:** HU-M06-03, HU-M04-03 · **Reglas:** art. 47.b, D9

### HU-M06-06 | Consultar estadísticas

**Como** Responsable SST, **quiero** ver estadísticas, **para** detectar patrones.

**Criterios de aceptación:**

- Veo eventos por tipo, área y periodo.
- Veo días perdidos por periodo.
- Las cifras se calculan y no muestran datos personales.

**Módulo:** M6 · **Entrega:** E2 · **Dónde:** Web · **Prioridad:** Should · **Depende de:** HU-M06-02 · **Reglas:** arts. 47.e, 47.f, RN-30

---

## M7. Comisión y actas

### HU-M07-01 | Constituir la comisión

**Como** Responsable SST, **quiero** registrar la comisión de un centro, **para** gestionarla en la plataforma.

**Criterios de aceptación:**

- Registro la fecha de constitución y los datos de registro ante la Secretaría.
- Un centro tiene una sola comisión activa.
- Se advierte si pasaron más de 30 días desde el inicio de operaciones.

**Módulo:** M7 · **Entrega:** E2 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M02-04 · **Reglas:** arts. 12, 13, 15, D4

### HU-M07-02 | Registrar los integrantes

**Como** Responsable SST, **quiero** registrar a los integrantes, **para** cumplir la composición legal.

**Criterios de aceptación:**

- Cada integrante indica parte, condición, cargo y periodo.
- Se exige el mismo número de representantes por parte.
- Cada propietario tiene suplente.
- Hay un presidente y un secretario activos.
- Los integrantes son usuarios de la empresa.

**Módulo:** M7 · **Entrega:** E2 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M07-01, HU-M01-04 · **Reglas:** arts. 14, 19, 20, 21, 28.c, RN-32, RN-33, RN-36, D3, D5

### HU-M07-03 | Programar reuniones

**Como** secretario de la comisión, **quiero** programar reuniones, **para** cumplir la reunión mensual.

**Criterios de aceptación:**

- Indico tipo, fecha, lugar y temas.
- La convocatoria queda registrada y visible para los integrantes.
- Una reunión extraordinaria registra su motivo.
- El sistema señala los meses sin reunión ordinaria.

**Módulo:** M7 · **Entrega:** E2 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M07-02 · **Reglas:** arts. 24, 27.a, 32, RN-37

### HU-M07-04 | Registrar asistencia y quórum

**Como** secretario de la comisión, **quiero** registrar la asistencia, **para** verificar el quórum.

**Criterios de aceptación:**

- Marco la asistencia de cada integrante.
- Un suplente solo cuenta si falta su propietario.
- El sistema indica si hay quórum.

**Módulo:** M7 · **Entrega:** E2 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M07-03 · **Reglas:** arts. 14, 23, 27.b, RN-34, RN-35

### HU-M07-05 | Redactar el acta

**Como** secretario de la comisión, **quiero** redactar el acta, **para** dejar constancia de la reunión.

**Criterios de aceptación:**

- Tiene conclusiones de visitas, resultados de investigaciones, actividades educativas y otros temas.
- Queda como borrador editable.
- Solo el secretario puede redactarla.

**Módulo:** M7 · **Entrega:** E2 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M07-04 · **Reglas:** arts. 27.c, 33, D3

### HU-M07-06 | Aprobar y firmar el acta

**Como** integrante de la comisión, **quiero** aprobar y firmar el acta, **para** que quede como registro verificable.

**Criterios de aceptación:**

- El acta pasa por borrador, aprobada y firmada.
- Sin quórum no se aprueba.
- Solo firman los asistentes.
- Un acta firmada no se edita ni se borra por ninguna vía.
- Se puede comprobar que el contenido coincide con su hash.

**Módulo:** M7 · **Entrega:** E2 · **Dónde:** Web y teléfono · **Prioridad:** Must · **Depende de:** HU-M07-05, HU-TEC-15 · **Reglas:** art. 27.c, RN-38, RN-39, RN-40, RN-41, D12

### HU-M07-07 | Convertir acuerdos en tareas

**Como** secretario de la comisión, **quiero** crear tareas desde los acuerdos, **para** dar seguimiento a lo decidido.

**Criterios de aceptación:**

- La tarea queda con origen "acuerdo de reunión" y referencia al acta.

**Módulo:** M7 · **Entrega:** E2 · **Dónde:** Web · **Prioridad:** Should · **Depende de:** HU-M05-02, HU-M07-05 · **Reglas:** RN-23, D6

### HU-M07-08 | Consultar el historial de actas

**Como** usuario de la empresa, **quiero** consultar las actas, **para** tenerlas disponibles ante la autoridad.

**Criterios de aceptación:**

- Veo las actas firmadas por fecha, con búsqueda por periodo.
- Los borradores solo los ve la comisión.

**Módulo:** M7 · **Entrega:** E2 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M07-06 · **Reglas:** arts. 27.e, 33, RN-05

### HU-M07-09 | Renovar la comisión

**Como** Responsable SST, **quiero** registrar nuevos periodos, **para** mantener vigente la comisión.

**Criterios de aceptación:**

- Puedo registrar nuevos integrantes o reelegir a los actuales.
- Se conserva el historial de integrantes anteriores.

**Módulo:** M7 · **Entrega:** E3 · **Dónde:** Web · **Prioridad:** Should · **Depende de:** HU-M07-02 · **Reglas:** arts. 17, 21, RN-36

---

## M8. Inspecciones QR

### HU-M08-01 | Crear puntos de inspección

**Como** Responsable SST, **quiero** crear puntos con su QR, **para** inspeccionar extintores, tableros y otros elementos.

**Criterios de aceptación:**

- Cada punto indica nombre, tipo, área y checklist.
- El sistema genera un QR imprimible.

**Módulo:** M8 · **Entrega:** E2 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M02-03, HU-TEC-07 · **Reglas:** RN-45, D7

### HU-M08-02 | Escanear un punto

**Como** Colaborador, **quiero** escanear el QR, **para** abrir la inspección sin buscar el punto.

**Criterios de aceptación:**

- El teléfono lee el código y abre el punto.
- Sin sesión, me pide iniciarla y regreso al punto.
- Un punto de otra empresa responde como si no existiera.

**Módulo:** M8 · **Entrega:** E2 · **Dónde:** Teléfono · **Prioridad:** Must · **Depende de:** HU-M08-01, HU-TEC-15 · **Reglas:** RN-05

### HU-M08-03 | Llenar el checklist

**Como** Colaborador, **quiero** llenar el checklist, **para** registrar el estado del punto.

**Criterios de aceptación:**

- Respondo cada ítem como conforme, no conforme o no aplica.
- La fecha y hora las fija el servidor.
- Finalizada, la inspección no se puede editar.

**Módulo:** M8 · **Entrega:** E2 · **Dónde:** Teléfono · **Prioridad:** Must · **Depende de:** HU-M08-02 · **Reglas:** arts. 25.b, 47.g, RN-42, RN-46

### HU-M08-04 | Registrar un hallazgo con foto

**Como** Colaborador, **quiero** registrar un hallazgo con foto, **para** dejar evidencia.

**Criterios de aceptación:**

- Puedo tomar la foto con el teléfono.
- Un ítem no conforme exige un hallazgo.
- El hallazgo indica descripción, severidad, fecha y hora.

**Módulo:** M8 · **Entrega:** E2 · **Dónde:** Teléfono · **Prioridad:** Must · **Depende de:** HU-M08-03, HU-TEC-10 · **Reglas:** RN-43, D15

### HU-M08-05 | Generar una tarea desde el hallazgo

**Como** Responsable SST, **quiero** que cada hallazgo genere una tarea, **para** corregirlo.

**Criterios de aceptación:**

- Cada hallazgo crea una tarea con origen "hallazgo".
- Al completar la tarea, el hallazgo se muestra como corregido.

**Módulo:** M8 · **Entrega:** E2 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M08-04, HU-M05-02 · **Reglas:** RN-23, RN-44, D6

### HU-M08-06 | Controlar las visitas mensuales

**Como** Responsable SST, **quiero** ver qué áreas no se visitaron este mes, **para** cumplir las visitas de la comisión.

**Criterios de aceptación:**

- Veo las áreas con y sin visita en el mes.
- Cada visita de comisión registra a sus dos miembros por sector.

**Módulo:** M8 · **Entrega:** E2 · **Dónde:** Web · **Prioridad:** Should · **Depende de:** HU-M08-03, HU-M07-02 · **Reglas:** art. 25.b

---

## M9. Políticas y procedimientos

### HU-M09-01 | Generar un documento

**Como** Responsable SST, **quiero** generar una política o procedimiento desde una plantilla, **para** no empezar desde cero.

**Criterios de aceptación:**

- Veo las plantillas disponibles para mi sector.
- El documento se llena con los datos de la empresa.
- Incluye al menos la política de SST y el procedimiento de investigación de accidentes.
- Queda como borrador.
- Se avisa que la empresa debe revisar el contenido.

**Módulo:** M9 · **Entrega:** E3 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M02-01, HU-TEC-07 · **Reglas:** RN-47, D13

### HU-M09-02 | Editar el borrador

**Como** Responsable SST, **quiero** editar el borrador, **para** adaptarlo a mi empresa.

**Criterios de aceptación:**

- Puedo modificar el contenido.
- Los cambios se guardan sin alterar la plantilla.

**Módulo:** M9 · **Entrega:** E3 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M09-01 · **Reglas:** D13

### HU-M09-03 | Aprobar un documento

**Como** Responsable SST, **quiero** aprobar un documento, **para** dejarlo vigente.

**Criterios de aceptación:**

- La versión aprobada registra aprobador y fecha.
- Una versión aprobada no se puede editar.
- Cada documento tiene una sola versión vigente.

**Módulo:** M9 · **Entrega:** E3 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M09-02 · **Reglas:** RN-48, RN-49, D13

### HU-M09-04 | Crear una versión nueva

**Como** Responsable SST, **quiero** crear una versión nueva, **para** actualizar un documento sin perder el anterior.

**Criterios de aceptación:**

- La versión nueva parte de la vigente y queda como borrador.
- Las versiones anteriores siguen disponibles para consulta.

**Módulo:** M9 · **Entrega:** E3 · **Dónde:** Web · **Prioridad:** Should · **Depende de:** HU-M09-03 · **Reglas:** RN-48, D13

### HU-M09-05 | Consultar los documentos vigentes

**Como** usuario de la empresa, **quiero** consultar los documentos vigentes, **para** conocer las políticas y procedimientos.

**Criterios de aceptación:**

- Veo solo las versiones vigentes.
- Puedo buscar por nombre y descargar en PDF.

**Módulo:** M9 · **Entrega:** E3 · **Dónde:** Web y teléfono · **Prioridad:** Should · **Depende de:** HU-M09-03 · **Reglas:** RN-05

---

## M10. Reportes

### HU-M10-01 | Generar el informe semestral

**Como** Responsable SST, **quiero** generar el informe semestral en PDF, **para** presentarlo a las autoridades de trabajo.

**Criterios de aceptación:**

- Elijo el semestre y el centro de trabajo.
- Incluye reuniones, inspecciones, hallazgos, accidentes y tareas del periodo.
- Usa los datos ya capturados.
- La empresa descarga el PDF y lo presenta.

**Módulo:** M10 · **Entrega:** E3 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M06-01, HU-M07-06, HU-M08-03 · **Reglas:** art. 25.f, RN-50

### HU-M10-02 | Generar el informe anual

**Como** Responsable SST, **quiero** generar el informe anual en PDF, **para** remitirlo en noviembre a la Secretaría de Trabajo, con copia al IHSS.

**Criterios de aceptación:**

- Incluye las actividades del año.
- Recuerda el plazo y la copia al IHSS.
- Usa los datos ya capturados.

**Módulo:** M10 · **Entrega:** E3 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M10-01 · **Reglas:** art. 25.o, RN-50

### HU-M10-03 | Descargar un acta en PDF

**Como** usuario de la empresa, **quiero** descargar un acta firmada, **para** presentarla ante la autoridad.

**Criterios de aceptación:**

- Incluye contenido, asistentes, firmas y hash.
- Solo se descargan actas firmadas.

**Módulo:** M10 · **Entrega:** E3 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M07-06 · **Reglas:** art. 33, D12

### HU-M10-04 | Consultar los informes generados

**Como** Responsable SST, **quiero** ver los informes generados, **para** volver a descargarlos.

**Criterios de aceptación:**

- Veo tipo, periodo, autor y fecha.
- Puedo descargar cada informe de nuevo.

**Módulo:** M10 · **Entrega:** E3 · **Dónde:** Web · **Prioridad:** Should · **Depende de:** HU-M10-01 · **Reglas:** ninguna

---

## M11. Notificaciones

### HU-M11-01 | Ver mis notificaciones

**Como** usuario, **quiero** ver mis notificaciones, **para** saber qué debo atender.

**Criterios de aceptación:**

- Veo las notificaciones de la empresa activa, de la más reciente a la más antigua.
- Puedo marcarlas como leídas.
- Cada notificación lleva a lo que la originó.
- Solo veo las mías.

**Módulo:** M11 · **Entrega:** E3 · **Dónde:** Web y teléfono · **Prioridad:** Must · **Depende de:** HU-M01-02 · **Reglas:** RN-51, D14

### HU-M11-02 | Recibir avisos de tareas

**Como** responsable de una tarea, **quiero** recibir avisos, **para** no incumplir la fecha.

**Criterios de aceptación:**

- Recibo un aviso al ser asignado.
- Recibo otro antes del vencimiento y otro si se vence.
- Un mismo aviso no se repite.

**Módulo:** M11 · **Entrega:** E3 · **Dónde:** Web y teléfono · **Prioridad:** Must · **Depende de:** HU-M11-01, HU-M05-02 · **Reglas:** RN-52

### HU-M11-03 | Recibir avisos de obligaciones

**Como** integrante de la comisión, **quiero** recibir avisos de reuniones, actas e informes, **para** cumplir a tiempo.

**Criterios de aceptación:**

- Recibo un aviso de cada reunión convocada.
- Recibo un aviso de cada acta por firmar.
- El Responsable SST recibe avisos de informes próximos, incluido el de noviembre.
- El Responsable SST recibe un aviso de documentos por aprobar.

**Módulo:** M11 · **Entrega:** E3 · **Dónde:** Web y teléfono · **Prioridad:** Should · **Depende de:** HU-M11-01, HU-M07-03 · **Reglas:** arts. 24, 25.f, 25.o, RN-52

### HU-M11-04 | Recibir alerta de accidente grave

**Como** Responsable SST, **quiero** recibir una alerta inmediata, **para** actuar y convocar a la comisión.

**Criterios de aceptación:**

- Un accidente grave genera una alerta al Responsable SST y a la comisión.
- La alerta permite programar una reunión extraordinaria.

**Módulo:** M11 · **Entrega:** E3 · **Dónde:** Web y teléfono · **Prioridad:** Must · **Depende de:** HU-M11-01, HU-M06-01 · **Reglas:** art. 32, RN-29, RN-52

### HU-M11-05 | Recibir notificaciones por correo

**Como** usuario, **quiero** recibir notificaciones importantes por correo, **para** enterarme aunque no abra la aplicación.

**Criterios de aceptación:**

- Las notificaciones importantes también llegan por correo.
- Un fallo de correo no impide la operación que lo originó.
- Si no se envía, la notificación sigue visible en la aplicación.

**Módulo:** M11 · **Entrega:** E3 · **Dónde:** Web y teléfono · **Prioridad:** Should · **Depende de:** HU-M11-01 · **Reglas:** D14

---

## M12. Panel de avance

### HU-M12-01 | Ver el avance general

**Como** Responsable SST, **quiero** ver un panel general, **para** saber qué tan preparada está la empresa.

**Criterios de aceptación:**

- Muestra porcentaje de cumplimiento, tareas pendientes y tareas vencidas.
- Los datos se calculan a partir de los demás módulos.
- Cada indicador lleva a su detalle.

**Módulo:** M12 · **Entrega:** E3 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M03-04, HU-M05-02 · **Reglas:** RN-13

### HU-M12-02 | Ver el estado de los riesgos

**Como** Responsable SST, **quiero** ver mis riesgos por nivel, **para** priorizar.

**Criterios de aceptación:**

- Muestra el número de riesgos por nivel.
- Señala los riesgos altos o críticos sin control.

**Módulo:** M12 · **Entrega:** E3 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-M12-01, HU-M04-05 · **Reglas:** RN-19

### HU-M12-03 | Ver las obligaciones del mes

**Como** Responsable SST, **quiero** ver mis obligaciones del mes, **para** que no se me pasen.

**Criterios de aceptación:**

- Muestra la reunión mensual, las visitas y los informes próximos.
- En noviembre destaca el informe anual.

**Módulo:** M12 · **Entrega:** E3 · **Dónde:** Web · **Prioridad:** Should · **Depende de:** HU-M12-01, HU-M07-03 · **Reglas:** arts. 24, 25.b, 25.f, 25.o

### HU-M12-04 | Ver la documentación lista

**Como** Responsable SST, **quiero** ver qué documentación tengo, **para** preparar una auditoría.

**Criterios de aceptación:**

- Muestra documentos vigentes, actas firmadas, informes y evidencias por periodo.
- Señala los periodos sin documentación.

**Módulo:** M12 · **Entrega:** E3 · **Dónde:** Web · **Prioridad:** Should · **Depende de:** HU-M12-01, HU-M10-04 · **Reglas:** ninguna

---

## Trabajo técnico

### HU-TEC-01 | Crear la solución con Clean Architecture

**Como** equipo, **quiero** crear la solución .NET por capas, **para** separar responsabilidades.

**Criterios de aceptación:**

- Existen los proyectos `Domain`, `Application`, `Infrastructure` y `API`.
- Las dependencias siguen la arquitectura aprobada.
- Las funcionalidades se organizan por Vertical Slicing.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-DIS-13 · **Reglas:** ninguna

### HU-TEC-02 | Configurar EF Core Code-First

**Como** equipo, **quiero** crear el modelo con EF Core y PostgreSQL, **para** versionar la base de datos.

**Criterios de aceptación:**

- Las entidades coinciden con el ERD aprobado.
- Las migraciones incluyen restricciones e índices.
- La base se crea desde cero con las migraciones.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-TEC-01, HU-DIS-11 · **Reglas:** ninguna

### HU-TEC-03 | Aplicar filtros globales por empresa

**Como** equipo, **quiero** usar `HasQueryFilter`, **para** aislar los datos automáticamente.

**Criterios de aceptación:**

- Toda entidad con `EmpresaId` tiene filtro global.
- La empresa activa sale del token, nunca del cliente.
- Al guardar, `EmpresaId` se asigna desde la empresa activa.
- El uso de `IgnoreQueryFilters` está limitado y justificado.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-TEC-02, HU-TEC-04 · **Reglas:** RN-04, RN-05, RN-06, RN-07, D16

### HU-TEC-04 | Implementar autenticación JWT

**Como** equipo, **quiero** emitir y validar JWT, **para** identificar al usuario y su empresa activa.

**Criterios de aceptación:**

- El token lleva usuario, empresa activa y rol.
- `EmpresaId` viaja como se definió en el diseño.
- Se validan firma, emisor, audiencia y expiración.
- Un token inválido recibe 401.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-DIS-14, HU-TEC-01 · **Reglas:** RN-06, D1

### HU-TEC-05 | Implementar autorización por roles

**Como** equipo, **quiero** proteger los endpoints por rol, **para** que cada usuario haga solo lo permitido.

**Criterios de aceptación:**

- Cada endpoint protegido declara sus roles.
- Un rol no permitido recibe 403.
- Las acciones de la comisión se validan contra el cargo de la persona.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-TEC-04 · **Reglas:** RN-03, D3

### HU-TEC-06 | Validar con FluentValidation

**Como** equipo, **quiero** validar las entradas y centralizar los errores, **para** responder de forma uniforme.

**Criterios de aceptación:**

- Cada comando tiene su validador.
- Un middleware global convierte los errores a la estructura acordada.
- Los errores no exponen detalles internos.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-TEC-01, HU-DIS-12 · **Reglas:** ninguna

### HU-TEC-07 | Cargar los catálogos iniciales

**Como** equipo, **quiero** cargar sectores, requisitos, preguntas, reglas, peligros y plantillas, **para** que el sistema tenga contenido desde el inicio.

**Criterios de aceptación:**

- Cubre los 4 sectores.
- Repetir la carga no duplica datos.
- El contenido usa redacción propia y lo revisa alguien con conocimiento de SST.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-TEC-02 · **Reglas:** D7

### HU-TEC-08 | Probar el aislamiento entre empresas

**Como** equipo, **quiero** pruebas automáticas de aislamiento, **para** demostrar que ninguna empresa accede a datos ajenos.

**Criterios de aceptación:**

- Con dos empresas de prueba, ninguna lista, consulta ni modifica datos de la otra.
- Referenciar un registro de otra empresa se rechaza.
- Cambiar `EmpresaId` en la petición no tiene efecto.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-TEC-03 · **Reglas:** RN-05, RN-06, RN-07, D16

### HU-TEC-09 | Registrar la auditoría de acciones

**Como** equipo, **quiero** registrar las acciones importantes, **para** que la evidencia sea verificable.

**Criterios de aceptación:**

- Se registran usuario, empresa, acción, entidad y fecha.
- El registro no se puede editar desde la aplicación.
- Cubre al menos firmas, aprobaciones, cambios de rol e inspecciones.

**Módulo:** Técnico · **Entrega:** E3 · **Dónde:** No aplica · **Prioridad:** Should · **Depende de:** HU-TEC-03 · **Reglas:** ninguna

### HU-TEC-10 | Configurar el almacenamiento de archivos

**Como** equipo, **quiero** guardar fotos y evidencias en un servicio externo gratuito, **para** no perderlas al reiniciar el servidor.

**Criterios de aceptación:**

- El servicio no requiere pago.
- Se validan tipo y tamaño antes de guardar.
- Los archivos sobreviven a un reinicio del backend.
- Los archivos de una empresa no son accesibles para otra.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-TEC-01, HU-TEC-03 · **Reglas:** RN-05, D15

### HU-TEC-11 | Crear el frontend web por funcionalidades

**Como** equipo, **quiero** organizar el proyecto React por funcionalidades, **para** evitar componentes gigantes.

**Criterios de aceptación:**

- Usa React, TypeScript y Vite.
- Hay carpetas `features/` por módulo.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-DIS-12 · **Reglas:** ninguna

### HU-TEC-12 | Proteger las rutas

**Como** equipo, **quiero** guardias con `react-router-dom`, **para** bloquear a usuarios sin JWT.

**Criterios de aceptación:**

- Sin sesión, una ruta protegida redirige al inicio de sesión.
- Un rol sin permiso no ve esa pantalla.
- Un token vencido cierra la sesión.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-TEC-11, HU-TEC-04 · **Reglas:** ninguna

### HU-TEC-13 | Validar con Zod y React Hook Form

**Como** equipo, **quiero** validar en vivo los campos de la interfaz, **para** dar respuesta inmediata.

**Criterios de aceptación:**

- Usan Zod y React Hook Form con `mode: 'onChange'`.
- Las reglas coinciden con FluentValidation.
- No hay validaciones manuales con `if/else`.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-TEC-11, HU-TEC-06 · **Reglas:** ninguna

### HU-TEC-14 | Centralizar las peticiones HTTP

**Como** equipo, **quiero** interceptores de Axios y un extractor universal de errores, **para** manejar token y fallos en un solo lugar.

**Criterios de aceptación:**

- Cada petición adjunta el JWT como `Bearer`.
- El extractor convierte cualquier error en un mensaje claro.
- Mientras el servidor se reactiva, se muestra un estado de carga.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-TEC-11 · **Reglas:** ninguna

### HU-TEC-15 | Crear la base de la app para teléfono

**Como** equipo, **quiero** crear la aplicación para teléfono, **para** hacer el trabajo de campo.

**Criterios de aceptación:**

- La tecnología está decidida y aceptada por el equipo y el catedrático.
- Funciona en Android y en iPhone, o se documenta la limitación.
- Inicia sesión y consume la misma API que la web.
- Puede usar la cámara del teléfono.

**Módulo:** Técnico · **Entrega:** E2 · **Dónde:** Teléfono · **Prioridad:** Must · **Depende de:** HU-TEC-04, HU-DIS-12 · **Reglas:** ninguna

### HU-TEC-16 | Crear el Dockerfile de la API

**Como** equipo, **quiero** un Dockerfile multi-stage, **para** compilar con el SDK y ejecutar en un runtime ligero de Alpine.

**Criterios de aceptación:**

- Usa una etapa de compilación y una de ejecución.
- La imagen final usa runtime Alpine.
- La generación de PDF y QR funciona dentro de esa imagen.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-TEC-01 · **Reglas:** ninguna

### HU-TEC-17 | Levantar todo con Docker Compose

**Como** equipo, **quiero** un `docker-compose.yml`, **para** levantar el sistema local con un solo comando.

**Criterios de aceptación:**

- Levanta la API, PostgreSQL y el frontend web.
- La API se conecta a la base y aplica migraciones.
- Funciona en una máquina limpia con las instrucciones del repositorio.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-TEC-16 · **Reglas:** ninguna

### HU-TEC-18 | Desplegar la base de datos

**Como** equipo, **quiero** PostgreSQL en Neon o Supabase, **para** tener una base gratuita en la nube.

**Criterios de aceptación:**

- La base tiene migraciones y catálogos cargados.
- Las credenciales no están en el repositorio.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-TEC-02, HU-TEC-07 · **Reglas:** ninguna

### HU-TEC-19 | Desplegar el backend

**Como** equipo, **quiero** publicar la API en Render o Fly.io, **para** exponerla con HTTPS.

**Criterios de aceptación:**

- El servicio compila desde el Dockerfile y está conectado a GitHub.
- La API responde por HTTPS y usa la base en la nube.
- Solo acepta peticiones de los clientes autorizados.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-TEC-16, HU-TEC-18 · **Reglas:** ninguna

### HU-TEC-20 | Desplegar el frontend web

**Como** equipo, **quiero** publicar el cliente en Vercel o Netlify, **para** tener el sistema completo en la nube.

**Criterios de aceptación:**

- Usa la API de producción por HTTPS.
- Las rutas funcionan al recargar la página.
- El flujo principal funciona de punta a punta en producción.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** Web · **Prioridad:** Must · **Depende de:** HU-TEC-11, HU-TEC-19 · **Reglas:** ninguna

### HU-TEC-21 | Automatizar el despliegue

**Como** equipo, **quiero** que cada `git push` a `main` actualice producción, **para** cumplir la integración continua del curso.

**Criterios de aceptación:**

- Un push a `main` actualiza backend y frontend sin pasos manuales.
- El equipo lo demuestra con un cambio real.

**Módulo:** Técnico · **Entrega:** E1 · **Dónde:** No aplica · **Prioridad:** Must · **Depende de:** HU-TEC-19, HU-TEC-20 · **Reglas:** ninguna

### HU-TEC-22 | Distribuir la app para pruebas

**Como** equipo, **quiero** instalar la app en teléfonos reales, **para** probarla y demostrarla.

**Criterios de aceptación:**

- Se puede instalar sin costo en los teléfonos del equipo.
- La app usa la API de producción.

**Módulo:** Técnico · **Entrega:** E2 · **Dónde:** Teléfono · **Prioridad:** Must · **Depende de:** HU-TEC-15, HU-TEC-19 · **Reglas:** ninguna

---

## Resumen

Total: 106 historias: 85 Must y 21 Should. Por entrega: Diseño 16, E1 42, E2 23 y E3 25.

| ID | Historia | Módulo | Entrega | Dónde | Prioridad |
|---|---|---|---|---|---|
| HU-DIS-01 | Aprobar el alcance | Diseño | Diseño | No aplica | Must |
| HU-DIS-02 | Documentar los requerimientos funcionales | Diseño | Diseño | No aplica | Must |
| HU-DIS-03 | Documentar los requerimientos no funcionales | Diseño | Diseño | No aplica | Must |
| HU-DIS-04 | Validar las reglas de negocio | Diseño | Diseño | No aplica | Must |
| HU-DIS-05 | Priorizar el backlog | Diseño | Diseño | No aplica | Must |
| HU-DIS-06 | Elaborar casos de uso | Diseño | Diseño | No aplica | Should |
| HU-DIS-07 | Documentar los flujos principales | Diseño | Diseño | No aplica | Must |
| HU-DIS-08 | Elaborar el diccionario de datos | Diseño | Diseño | No aplica | Must |
| HU-DIS-09 | Definir el aislamiento multiempresa | Diseño | Diseño | No aplica | Must |
| HU-DIS-10 | Diseñar el diagrama entidad-relación | Diseño | Diseño | No aplica | Must |
| HU-DIS-11 | Definir restricciones e índices | Diseño | Diseño | No aplica | Must |
| HU-DIS-12 | Definir los contratos de la API | Diseño | Diseño | No aplica | Must |
| HU-DIS-13 | Diseñar la arquitectura del backend | Diseño | Diseño | No aplica | Must |
| HU-DIS-14 | Diseñar autenticación y autorización | Diseño | Diseño | No aplica | Must |
| HU-DIS-15 | Redactar el pitch de 1 página | Diseño | Diseño | No aplica | Must |
| HU-DIS-16 | Configurar el tablero Kanban | Diseño | Diseño | No aplica | Must |
| HU-M01-01 | Registrar mi empresa | M1 | E1 | Web | Must |
| HU-M01-02 | Iniciar y cerrar sesión | M1 | E1 | Web y teléfono | Must |
| HU-M01-03 | Cambiar de empresa | M1 | E1 | Web y teléfono | Must |
| HU-M01-04 | Agregar usuarios | M1 | E1 | Web | Must |
| HU-M01-05 | Gestionar roles y membresías | M1 | E1 | Web | Must |
| HU-M01-06 | Cambiar mi contraseña | M1 | E1 | Web y teléfono | Should |
| HU-M01-07 | Administrar los catálogos | M1 | E3 | Web | Should |
| HU-M01-08 | Consultar las empresas registradas | M1 | E3 | Web | Should |
| HU-M02-01 | Completar el perfil | M2 | E1 | Web | Must |
| HU-M02-02 | Registrar centros de trabajo | M2 | E1 | Web | Must |
| HU-M02-03 | Registrar áreas | M2 | E1 | Web | Must |
| HU-M02-04 | Calcular la composición de la comisión | M2 | E2 | Web | Must |
| HU-M03-01 | Responder el formulario de contexto | M3 | E1 | Web | Must |
| HU-M03-02 | Obtener peligros sugeridos | M3 | E1 | Web | Must |
| HU-M03-03 | Conocer mis brechas | M3 | E1 | Web | Must |
| HU-M03-04 | Ver mi porcentaje de cumplimiento | M3 | E1 | Web | Must |
| HU-M03-05 | Repetir el diagnóstico | M3 | E3 | Web | Should |
| HU-M04-01 | Confirmar los peligros sugeridos | M4 | E1 | Web | Must |
| HU-M04-02 | Agregar riesgos | M4 | E1 | Web | Must |
| HU-M04-03 | Evaluar un riesgo | M4 | E1 | Web | Must |
| HU-M04-04 | Ver la matriz de riesgos | M4 | E1 | Web | Must |
| HU-M04-05 | Definir controles | M4 | E1 | Web | Must |
| HU-M04-06 | Evaluar el riesgo residual | M4 | E1 | Web | Should |
| HU-M04-07 | Consultar el historial de un riesgo | M4 | E3 | Web | Should |
| HU-M05-01 | Generar el plan | M5 | E1 | Web | Must |
| HU-M05-02 | Asignar tareas | M5 | E1 | Web | Must |
| HU-M05-03 | Atender mis tareas | M5 | E1 | Web y teléfono | Must |
| HU-M05-04 | Adjuntar evidencia | M5 | E1 | Web y teléfono | Must |
| HU-M05-05 | Filtrar el plan | M5 | E3 | Web | Should |
| HU-M06-01 | Reportar un evento | M6 | E2 | Web y teléfono | Must |
| HU-M06-02 | Registrar a las personas afectadas | M6 | E2 | Web | Must |
| HU-M06-03 | Investigar un evento | M6 | E2 | Web | Must |
| HU-M06-04 | Definir medidas correctivas | M6 | E2 | Web | Must |
| HU-M06-05 | Actualizar la matriz tras un evento | M6 | E2 | Web | Should |
| HU-M06-06 | Consultar estadísticas | M6 | E2 | Web | Should |
| HU-M07-01 | Constituir la comisión | M7 | E2 | Web | Must |
| HU-M07-02 | Registrar los integrantes | M7 | E2 | Web | Must |
| HU-M07-03 | Programar reuniones | M7 | E2 | Web | Must |
| HU-M07-04 | Registrar asistencia y quórum | M7 | E2 | Web | Must |
| HU-M07-05 | Redactar el acta | M7 | E2 | Web | Must |
| HU-M07-06 | Aprobar y firmar el acta | M7 | E2 | Web y teléfono | Must |
| HU-M07-07 | Convertir acuerdos en tareas | M7 | E2 | Web | Should |
| HU-M07-08 | Consultar el historial de actas | M7 | E2 | Web | Must |
| HU-M07-09 | Renovar la comisión | M7 | E3 | Web | Should |
| HU-M08-01 | Crear puntos de inspección | M8 | E2 | Web | Must |
| HU-M08-02 | Escanear un punto | M8 | E2 | Teléfono | Must |
| HU-M08-03 | Llenar el checklist | M8 | E2 | Teléfono | Must |
| HU-M08-04 | Registrar un hallazgo con foto | M8 | E2 | Teléfono | Must |
| HU-M08-05 | Generar una tarea desde el hallazgo | M8 | E2 | Web | Must |
| HU-M08-06 | Controlar las visitas mensuales | M8 | E2 | Web | Should |
| HU-M09-01 | Generar un documento | M9 | E3 | Web | Must |
| HU-M09-02 | Editar el borrador | M9 | E3 | Web | Must |
| HU-M09-03 | Aprobar un documento | M9 | E3 | Web | Must |
| HU-M09-04 | Crear una versión nueva | M9 | E3 | Web | Should |
| HU-M09-05 | Consultar los documentos vigentes | M9 | E3 | Web y teléfono | Should |
| HU-M10-01 | Generar el informe semestral | M10 | E3 | Web | Must |
| HU-M10-02 | Generar el informe anual | M10 | E3 | Web | Must |
| HU-M10-03 | Descargar un acta en PDF | M10 | E3 | Web | Must |
| HU-M10-04 | Consultar los informes generados | M10 | E3 | Web | Should |
| HU-M11-01 | Ver mis notificaciones | M11 | E3 | Web y teléfono | Must |
| HU-M11-02 | Recibir avisos de tareas | M11 | E3 | Web y teléfono | Must |
| HU-M11-03 | Recibir avisos de obligaciones | M11 | E3 | Web y teléfono | Should |
| HU-M11-04 | Recibir alerta de accidente grave | M11 | E3 | Web y teléfono | Must |
| HU-M11-05 | Recibir notificaciones por correo | M11 | E3 | Web y teléfono | Should |
| HU-M12-01 | Ver el avance general | M12 | E3 | Web | Must |
| HU-M12-02 | Ver el estado de los riesgos | M12 | E3 | Web | Must |
| HU-M12-03 | Ver las obligaciones del mes | M12 | E3 | Web | Should |
| HU-M12-04 | Ver la documentación lista | M12 | E3 | Web | Should |
| HU-TEC-01 | Crear la solución con Clean Architecture | Técnico | E1 | No aplica | Must |
| HU-TEC-02 | Configurar EF Core Code-First | Técnico | E1 | No aplica | Must |
| HU-TEC-03 | Aplicar filtros globales por empresa | Técnico | E1 | No aplica | Must |
| HU-TEC-04 | Implementar autenticación JWT | Técnico | E1 | No aplica | Must |
| HU-TEC-05 | Implementar autorización por roles | Técnico | E1 | No aplica | Must |
| HU-TEC-06 | Validar con FluentValidation | Técnico | E1 | No aplica | Must |
| HU-TEC-07 | Cargar los catálogos iniciales | Técnico | E1 | No aplica | Must |
| HU-TEC-08 | Probar el aislamiento entre empresas | Técnico | E1 | No aplica | Must |
| HU-TEC-09 | Registrar la auditoría de acciones | Técnico | E3 | No aplica | Should |
| HU-TEC-10 | Configurar el almacenamiento de archivos | Técnico | E1 | No aplica | Must |
| HU-TEC-11 | Crear el frontend web por funcionalidades | Técnico | E1 | Web | Must |
| HU-TEC-12 | Proteger las rutas | Técnico | E1 | Web | Must |
| HU-TEC-13 | Validar con Zod y React Hook Form | Técnico | E1 | Web | Must |
| HU-TEC-14 | Centralizar las peticiones HTTP | Técnico | E1 | Web | Must |
| HU-TEC-15 | Crear la base de la app para teléfono | Técnico | E2 | Teléfono | Must |
| HU-TEC-16 | Crear el Dockerfile de la API | Técnico | E1 | No aplica | Must |
| HU-TEC-17 | Levantar todo con Docker Compose | Técnico | E1 | No aplica | Must |
| HU-TEC-18 | Desplegar la base de datos | Técnico | E1 | No aplica | Must |
| HU-TEC-19 | Desplegar el backend | Técnico | E1 | No aplica | Must |
| HU-TEC-20 | Desplegar el frontend web | Técnico | E1 | Web | Must |
| HU-TEC-21 | Automatizar el despliegue | Técnico | E1 | No aplica | Must |
| HU-TEC-22 | Distribuir la app para pruebas | Técnico | E2 | Teléfono | Must |
