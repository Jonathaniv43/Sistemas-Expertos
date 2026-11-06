# Reglas de negocio

**Para qué sirve:** lista las condiciones que el sistema debe respetar siempre. Cada historia de usuario cita las reglas que le aplican.

Las reglas con artículo vienen del reglamento hondureño, explicado en el [marco normativo](06-marco-normativo.md).

## Multiempresa

| Código | Regla |
|---|---|
| RN-01 | Cada empresa tiene un identificador único |
| RN-02 | Un usuario puede pertenecer a una o varias empresas |
| RN-03 | Un usuario puede tener un rol distinto en cada empresa |
| RN-04 | Todo dato operativo pertenece a una sola empresa |
| RN-05 | Un usuario no puede consultar información de una empresa a la que no pertenece |
| RN-06 | La empresa de cada operación se toma de la sesión autenticada, nunca de lo que envíe el cliente |
| RN-07 | Un registro solo puede relacionarse con registros de su misma empresa |
| RN-08 | Una empresa siempre debe tener al menos un Administrador activo |

## Perfil y diagnóstico

| Código | Regla |
|---|---|
| RN-09 | Cada empresa pertenece a un solo sector |
| RN-10 | Sin sector y sin al menos un centro de trabajo no se puede iniciar el diagnóstico |
| RN-11 | Las preguntas del formulario dependen del sector |
| RN-12 | Un diagnóstico finalizado no se edita; para actualizarlo se aplica uno nuevo |
| RN-13 | El porcentaje de cumplimiento se calcula desde las respuestas y no se guarda |
| RN-14 | Las mismas respuestas siempre producen los mismos resultados |

## Riesgos

| Código | Regla |
|---|---|
| RN-15 | El nivel de riesgo es probabilidad por severidad, cada una en escala de 1 a 5 |
| RN-16 | El resultado se clasifica en: 1–4 bajo, 5–9 medio, 10–14 alto, 15–25 crítico. Esta clasificación es una propuesta por validar |
| RN-17 | Cada riesgo pertenece a un área |
| RN-18 | Un peligro sugerido no forma parte de la matriz hasta que el Responsable SST lo confirme |
| RN-19 | Un riesgo alto o crítico exige al menos un control |
| RN-20 | Cada evaluación se conserva; una nueva no reemplaza a la anterior |
| RN-21 | Cada control indica su tipo: eliminación, sustitución, ingeniería, administrativo o equipo de protección personal |

## Plan de trabajo

| Código | Regla |
|---|---|
| RN-22 | Una tarea necesita responsable activo en la empresa y fecha límite para iniciarse |
| RN-23 | Cada tarea conserva su origen: riesgo, brecha, hallazgo, accidente, acuerdo de reunión o manual |
| RN-24 | Solo el responsable de la tarea o el Responsable SST pueden actualizarla |
| RN-25 | Si la tarea exige evidencia, no se puede completar sin ella |

## Accidentes

| Código | Regla |
|---|---|
| RN-26 | Cada evento se clasifica como accidente, incidente o enfermedad profesional |
| RN-27 | Cualquier usuario de la empresa puede reportar un evento |
| RN-28 | Un evento no se cierra sin causas y medidas correctivas registradas (art. 46.1.a) |
| RN-29 | Un accidente grave genera una alerta y pide programar reunión extraordinaria (art. 32) |
| RN-30 | Los datos de las personas afectadas solo son visibles para el Responsable SST y la comisión |
| RN-31 | La fecha de registro la fija el servidor; la fecha del evento la indica quien reporta |

## Comisión y actas

| Código | Regla |
|---|---|
| RN-32 | La comisión tiene igual número de representantes de cada parte, según la tabla del art. 14 |
| RN-33 | Cada propietario tiene un suplente (art. 14) |
| RN-34 | Un suplente solo cuenta para el quórum si su propietario está ausente (art. 14) |
| RN-35 | El quórum es la mitad más uno de los miembros propietarios (art. 23). Esta interpretación está por confirmar |
| RN-36 | El periodo de los integrantes es de 2 años (art. 21) |
| RN-37 | Debe haber al menos una reunión ordinaria al mes (art. 24) |
| RN-38 | El acta pasa por borrador, aprobada y firmada (art. 27.c) |
| RN-39 | Sin quórum no se puede aprobar el acta |
| RN-40 | Un acta firmada no se puede editar ni borrar; las correcciones se hacen en un acta nueva |
| RN-41 | Cada firma guarda usuario, fecha y hash del contenido, una huella que permite detectar cambios |

## Inspecciones

| Código | Regla |
|---|---|
| RN-42 | La fecha y hora de la inspección las fija el servidor |
| RN-43 | Un ítem no conforme exige registrar un hallazgo |
| RN-44 | Cada hallazgo genera una tarea |
| RN-45 | El código QR no contiene datos de la empresa ni sigue una secuencia adivinable |
| RN-46 | Una inspección finalizada no se puede editar |

## Documentos y reportes

| Código | Regla |
|---|---|
| RN-47 | Un documento generado queda como borrador hasta que el Responsable SST lo apruebe |
| RN-48 | Una versión aprobada no se puede editar; los cambios crean una versión nueva |
| RN-49 | Cada documento tiene una sola versión vigente |
| RN-50 | Los informes usan los datos capturados en el sistema |

## Notificaciones

| Código | Regla |
|---|---|
| RN-51 | Cada notificación tiene un destinatario, y solo esa persona la ve |
| RN-52 | Las notificaciones se generan por eventos del sistema, no manualmente |
