# AuraNeuro – Sprint 3

## 5.2.3. Sprint 3

### 5.2.3.1. Sprint Planning 3

El Sprint 3 se centra en el backend del sistema **AuraNeuro**, específicamente en la implementación de los servicios y endpoints REST del subsistema de autenticación y gestión clínica. Este sprint busca establecer la base funcional de la API en C# (.NET Core), garantizando la seguridad, roles, y el acceso controlado a recursos médicos.

#### Sprint Planning Background

| Campo          | Detalle                                                                 |
|----------------|-------------------------------------------------------------------------|
| **Sprint #**   | Sprint 3                                                                |
| **Date**       | 2025-11-05                                                              |
| **Time**       | 10:00 AM – 11:30 AM                                                     |
| **Location**   | Reunión virtual (Zoom) / Oficina central AuraNeuro                     |
| **Prepared by**| Romero Meza, Jhimy                                                      |

**Attendees (planning meeting)**

- Romero Meza, Jhimy — Sprint Lead (Backend)  
- Eduardo F. Chacaliaza Minaya — Product Owner  
- Gutierrez Tume, Jeremy — Lead Dev (Arquitectura / Code Reviews)  
- Fabricio F. Quispe Barzola — Backend Developer  
- Juan José Meza Huanacune — QA / DevOps Support  

---

#### Sprint n – 1 Review Summary

Durante el Sprint 2 se completó la implementación del frontend del subsistema de autenticicación de AuraNeuro. Se desarrollaron las vistas de inicio de sesión, registro (paciente y neurólogo), verificación OTP, e integración visual con Google (OAuth). Todas las vistas fueron validadas con flujos UI funcionales, manejo de errores y diseño responsivo. El Product Owner destacó la calidad visual y consistencia del diseño, y recomendó iniciar la conexión con los servicios reales en el siguiente sprint.

#### Sprint n – 1 Retrospective Summary

El equipo valoró la buena coordinación entre desarrolladores y el cumplimiento de todas las historias planificadas dentro del plazo. Se identificó como mejora para el Sprint 3 fortalecer la integración continua y definir un entorno de staging para pruebas de backend. Además, se acordó mantener reuniones técnicas más cortas pero con acuerdos más claros sobre dependencias y endpoints.

---

#### Sprint Goal & User Stories

**Sprint n Goal**

> Our focus is on habilitar una experiencia integral, segura y fluida para los usuarios de AuraNeuro mediante la implementación del backend que cubre autenticación, gestión completa de usuarios, edición de perfil, visualización de historial médico, administración de recetas, y configuración de disponibilidad y agenda para neurólogos.

We believe it delivers un acceso confiable a la plataforma, una interacción más completa con la información personal y médica del usuario, mayor autonomía en la gestión de su cuenta, y nuevas capacidades para que neurólogos administren sus horarios y emitan recetas, mientras el frontend obtiene endpoints estables, seguros y documentados para construir la experiencia del Sprint 2.

This will be confirmed when el frontend integre correctamente los flujos de autenticación, perfil, gestión de recetas y disponibilidad en el entorno de staging, logrando al menos un 95% de éxito en registro e inicio de sesión, permitiendo consultar y editar el perfil sin errores, visualizar historial médico y recetas según permisos, y alcanzando más del 90% de cobertura en pruebas unitarias e integradas sobre los módulos desarrollados.

---

#### Sprint n Velocity

| Métrica                  | Valor        |
|--------------------------|-------------|
| Planned                  | 28 SP       |
| Committed                | 26 SP       |
| Sum of Story Points      | 26 SP       |

---

### 5.2.3.2. Aspect Leaders and Collaborators

| Team Member (Last Name, First Name) | GitHub Username | Patients | Neurologists | Assessments / Neurological Health | Appointments | Availabilities | Prescriptions | Users / Auth |
|-------------------------------------|-----------------|----------|-------------|-----------------------------------|-------------|----------------|--------------|-------------|
| Romero Meza, Jhimy                  | `jhimyromero`   | C        | C           | L                                 | C           | C              | C            | L           |
| Chacaliaza Minaya, Eduardo F.       | `eduardoFchac`  | C        | C           | C                                 | L           | C              | C            | C           |
| Gutierrez Tume, Jeremy              | `jgutierrez`    | C        | C           | C                                 | C           | L              | C            | C           |
| Fabricio Fabián Quispe Barzola      | `fabricioqfb`   | C        | L           | C                                 | C           | C              | L            | C           |
| Juan José Meza Huanacune            | `juanjosemh`    | L        | C           | C                                 | C           | C              | C            | C           |

> **Leyenda:**  
> - **L** = Leader (Responsable principal)  
> - **C** = Collaborator (Colaborador)

---

### 5.2.3.3. Sprint Backlog 3

En este sprint, el objetivo es consolidar la experiencia integral y segura de los usuarios de AuraNeuro mediante la implementación completa del backend, enfocado en optimizar la autenticación, gestión de usuarios, edición de perfil, historial médico, administración de recetas y configuración de disponibilidad para neurólogos.

Estas funcionalidades garantizarán un acceso confiable a la plataforma, una interacción fluida con la información personal y médica, y una mayor autonomía tanto para pacientes como para neurólogos en la gestión de sus cuentas y horarios. Asimismo, permitirán al frontend consumir endpoints estables, seguros y documentados para integrar los flujos de autenticación, perfil, recetas y agenda en el entorno de staging.

#### Sprint Backlog – Detalle de Historias y Tareas

> Puedes dejar la columna “Assigned To” y “Status” vacías en el repo si las quieres usar como tablero manual.

| Story ID | Story name | Task ID | Task title | Task description | Est. (hrs) | Assigned To | Status |
|----------|------------|---------|------------|-----------------|------------|-------------|--------|
| US01 | Registro de paciente | T01.1 | Implementar modelo Patient y hashing de contraseña | Definir entidad Patient y añadir campo passwordHash; implementar hashing seguro (Argon2/Bcrypt) en el servicio de registro. | 5 | Chacaliaza Minaya, Eduardo F. | In Progress |
| US01 | Registro de paciente | T01.2 | Endpoint POST /api/v1/patients/register | Implementar endpoint REST que reciba DTO, valide duplicados (email/phone) y cree el paciente devolviendo 201 con id. | 4 | Chacaliaza Minaya, Eduardo F. | In Progress |
| US02 | Visualizar perfil del paciente | T02.1 | Servicio: Obtener perfil de paciente por ID | Crear servicio que recupere paciente y mapee a DTO excluyendo campos sensibles. | 3 | Chacaliaza Minaya, Eduardo F. | Done |
| US02 | Visualizar perfil del paciente | T02.2 | Endpoint GET /api/v1/patients/{patientId} | Exponer endpoint protegido que devuelva el perfil; validar permisos (paciente o neurólogo autorizado). | 3 | Chacaliaza Minaya, Eduardo F. | In Progress |
| US04 | Vincular paciente a un neurólogo | T04.1 | Repositorio: persistir vínculo paciente–neurólogo | Implementar método para crear relación patient_neurologists evitando duplicados. | 3 | Gutierrez Tume ,Stanley Jeremy. | Done |
| US04 | Vincular paciente a un neurólogo | T04.2 | Endpoint POST /api/v1/patients/{patientId}/neurologists/{neurologistId} | Endpoint que valida existencia de entidades y crea la solicitud/vínculo en estado requested. | 3 | Chacaliaza Minaya, Eduardo F. | To Review |
| US05 | Crear perfil profesional de neurólogo | T05.1 | Modelo Neurologist y validaciones de licencia | Definir entidad con licenseNumber, specialties, verificationStatus; validar formato de licencia. | 4 | Fabricio Fabián Quispe Barzola | Done |
| US05 | Crear perfil profesional de neurólogo | T05.2 | Endpoint POST /api/v1/neurologists | Endpoint para crear perfil profesional; devuelve 201 Created con neurologistId y verificationStatus. | 3 | Fabricio Fabián Quispe Barzola | Done |
| NEU-002 | Listar pacientes asociados | T-NEU002-1 | Repositorio: Obtener pacientes por neurologistId | Método que retorna pacientes asociados con metadata (assignedAt, status). | 3 | Fabricio Fabián Quispe Barzola | Done |
| NEU-002 | Listar pacientes asociados | T-NEU002-2 | Endpoint GET /api/v1/neurologists/{neurologistId}/patients | Endpoint protegido que devuelve la lista; admite filtro simple ?status=. | 3 | Fabricio Fabián Quispe Barzola | Done |
| NEU-005 | Gestionar solicitudes de asociación | T-NEU005-2 | Endpoint PATCH /api/v1/neurologists/{neurologistId}/requests/{requestId} | Endpoint para aceptar/rechazar solicitud; al aceptar crear relación patient_neurologists. | 4 | Fabricio Fabián Quispe Barzola | To Review |
| ASS-001 | Crear evaluación médica básica | T-ASS001-2 | Endpoint POST /api/v1/patients/{patientId}/assessments | Endpoint protegido para que el neurólogo cree la evaluación y retorne assessmentId. | 3 | jhimyromero | Done |
| ASS-002 | Listar evaluaciones de un paciente | T-ASS002-1 | Repositorio: GetAssessmentsByPatient(patientId) | Método que devuelve resumen de evaluaciones (id, assessedAt, diagnosisPreview, neurologistName). | 3 | jhimyromero | Done |
| ASS-003 | Ver detalle de una evaluación médica | T-ASS003-1 | Repositorio: Obtener evaluación por Id | GetById(assessmentId) que retorna la evaluación completa si no está deleted. | 3 | jhimyromero | Done |
| ASS-003 | Ver detalle de una evaluación médica | T-ASS003-2 | Endpoint GET /api/v1/assessments/{assessmentId} | Endpoint que valida permisos (paciente/creador/admin) y retorna detalle o 404. | 3 | jhimyromero | Done |
| ASS-004 | Editar evaluación médica (propietario) | T-ASS004-2 | Endpoint PATCH /api/v1/assessments/{assessmentId} | Endpoint protegido que recibe cambios parciales y devuelve la evaluación actualizada. | 3 | jhimyromero | Done |
| ASS-005 | Eliminar evaluación médica (soft-delete) | T-ASS005-2 | Endpoint DELETE /api/v1/assessments/{assessmentId} | Endpoint protegido que invoca SoftDelete; solo autor o admin puede ejecutar; devuelve 204. | 2 | jhimyromero | Done |
| APP-001 | Solicitar cita (paciente) | T-APP001-1 | Servicio: Crear cita y validar disponibilidad simple | Crear lógica que valide startAt < endAt, que el neurólogo exista y no haya cita confirmada idéntica. | 4 | Juan José Meza Huanacune | Done |
| APP-001 | Solicitar cita (paciente) | T-APP001-2 | Endpoint POST /api/v1/appointments | Endpoint que crea cita en estado requested y devuelve appointmentId; notifica in-app al neurólogo. | 3 | Juan José Meza Huanacune | Done |
| APP-002 | Ver mis citas (paciente) | T-APP002-1 | Repositorio: Obtener citas por patientId | Implementar GetByPatientId(patientId) con orden por startAt. | 3 |Gutierrez tume,Stanley Jeremy| Done |
| APP-002 | Ver mis citas (paciente) | T-APP002-2 | Endpoint GET /api/v1/patients/{patientId}/appointments | Endpoint protegido que retorna citas del paciente autenticado. | 3 | Juan José Meza Huanacune | Done |
| APP-003 | Listar solicitudes de cita (neurólogo) | T-APP003-1 | Repositorio: Obtener solicitudes por neurologistId | Método para listar citas con estado requested y datos de paciente. | 3 | Juan José Meza Huanacune | Done |
| APP-004 | Confirmar o rechazar solicitud de cita | T-APP004-1 | Servicio: Actualizar estado de cita a confirmed/rejected | Lógica que cambia estado, setea respondedAt y evita colisiones de slots. | 3 | Juan José Meza Huanacune | Done |
| APP-004 | Confirmar o rechazar solicitud de cita | T-APP004-2 | Endpoint PATCH /api/v1/appointments/{appointmentId}/status | Endpoint protegido para que el neurólogo cambie el estado mediante action en body. | 2 | Juan José Meza Huanacune | Done |
| APP-005 | Cancelar cita (paciente o neurólogo) | T-APP005-1 | Servicio: Cancelar cita y registrar metadata | Verificar que quien solicita pertenece a la cita; setear cancelled, cancelledBy, cancelledAt. | 3 | Juan José Meza Huanacune | Done |
| APP-005 | Cancelar cita (paciente o neurólogo) | T-APP005-2 | Endpoint DELETE /api/v1/appointments/{appointmentId} | Endpoint que cancela la cita; devolver 204 si éxito o 403 si falta permiso. | 2 | Juan José Meza Huanacune | Done |
| AVB-001 | Crear franja de disponibilidad | T-AVB001-2 | Endpoint POST /api/v1/neurologists/{neurologistId}/availability | Endpoint protegido para crear franja; validar solapamientos básicos. | 3 | Juan José Meza Huanacune | Done |
| AVB-002 | Listar mis franjas de disponibilidad | T-AVB002-1 | Repositorio: Obtener franjas por neurologistId | Implementar GetByNeurologistId que retorne franjas activas ordenadas. | 2 | Juan José Meza Huanacune | Done |
| AVB-004 | Eliminar franja de disponibilidad | T-AVB004-2 | Endpoint DELETE /api/v1/availability/{slotId} | Endpoint protegido para eliminar la franja; responde 204. | 1.5 | Juan José Meza Huanacune | Done |
| AVB-005 | Consultar franjas disponibles (paciente) | T-AVB005-1 | Servicio: GetAvailableSlots por fecha | Lógica que filtra franjas activas y no ocupadas por citas confirmadas. | 3 | Juan José Meza Huanacune | Done |
| REC-001 | Crear receta electrónica básica | T-REC001-1 | Entidad Prescription y validaciones básicas | Definir entidad con patientId, neurologistId, medicines, issuedAt, signatureHash. | 3 | Fabricio Fabián Quispe Barzola | Done |
| REC-001 | Crear receta electrónica básica | T-REC001-2 | Endpoint POST /api/v1/recipes | Endpoint protegido (NEUROLOGIST) que crea receta y devuelve id; almacenar signatureHash. | 3 | Fabricio Fabián Quispe Barzola | Done |
| REC-002 | Listar recetas del paciente | T-REC002-1 | Repositorio: GetByPatientId para recetas | Método que retorna resumen de recetas por paciente con orden por fecha. | 2 | Gutierrez Tume,Stanley Jeremy | Done |
| REC-002 | Listar recetas del paciente | T-REC002-2 | Endpoint GET /api/v1/patients/{patientId}/recipes | Endpoint protegido que devuelve la lista de recetas del paciente. | 2 | Fabricio Fabián Quispe Barzola | Done |
| REC-003 | Ver detalle de receta | T-REC003-1 | Servicio: Obtener receta completa por id | Obtener receta con medicamentos, dosis, emisor y estado; validar permisos. | 3 | Fabricio Fabián Quispe Barzola | Done |
| REC-003 | Ver detalle de receta | T-REC003-2 | Endpoint GET /api/v1/recipes/{recipeId} | Endpoint que retorna detalle o 403/404 según permisos. | 2 | Fabricio Fabián Quispe Barzola | Done |
| REC-004 | Actualizar receta (corrección menor) | T-REC004-1 | Servicio: UpdatePrescription limitado | Permitir editar campos menores (notes, instructions) solo si estado active. | 3 | Fabricio Fabián Quispe Barzola | Done |
| AUTH-001 | Inicio de sesión con correo/contraseña | T-AUTH001-1 | Servicio Auth: Validación y generación de JWT | Verificar credenciales, usuario activo y generar access token JWT con claims. | 4 | jhimyromero | Done |
| AUTH-001 | Inicio de sesión con correo/contraseña | T-AUTH001-2 | Endpoint POST /api/v1/auth/login | Endpoint que recibe credenciales y devuelve { accessToken, user } o 401. | 2 | jhimyromero | Done |
| AUTH-002 | Inicio de sesión por teléfono mediante OTP | T-AUTH002-1 | Servicio OTP: Validar OTP y autenticar | Verificar código OTP, TTL y estado; generar JWT si es válido. | 3 | jhimyromero | Done |
| AUTH-002 | Inicio de sesión por teléfono mediante OTP | T-AUTH002-2 | Endpoint POST /api/v1/auth/verify-otp | Endpoint que recibe phone + otp y devuelve token si es válido. | 2 | jhimyromero | Done |
| AUTH-003 | Recuperación de contraseña vía token | T-AUTH003-1 | Servicio: Generar token de recuperación | Generar token temporal y guardarlo con TTL; encolar/simular envío por email. | 3 | jhimyromero | Done |
| AUTH-003 | Recuperación de contraseña vía token | T-AUTH003-2 | Endpoint POST /api/v1/auth/reset-password | Endpoint que recibe { token, newPassword } y actualiza hash si token válido. | 2 | jhimyromero | Done |
| AUTH-004 | Cerrar sesión (cliente) / invalidar sesión local | T-AUTH004-2 | Endpoint POST /api/v1/auth/logout | Endpoint que registra evento logout y devuelve 204; cliente limpia auth local. | 1 | jhimyromero | Done |

*(…continúa con el mismo formato para todas las tareas APP-001 .. REC-005 y AUTH-001 .. AUTH-004. Puedes copiar/pegar las filas del documento siguiendo este patrón de tabla.)*

---

### 5.2.3.4. Development Evidence for Sprint Review

Durante este Sprint 3 el equipo centró sus esfuerzos en consolidar la capa de **Web Services** del producto, avanzando decisivamente en la implementación de los módulos que soportan la interacción clínica entre pacientes y neurólogos. Se priorizaron las piezas funcionales que permiten:

- Documentar y consultar evaluaciones médicas  
- Gestionar citas y disponibilidades  
- Emitir y administrar recetas electrónicas  
- Atender los flujos de autenticación necesarios para proteger los accesos  

Estos desarrollos buscan garantizar que los flujos críticos del dominio (registro de evaluación, agendamiento, emisión de receta y autenticación) estén disponibles y sean consumibles por el frontend del Sprint 2.

#### Commits Relevantes

| Repository        | Branch               | Commit Id | Commit Message                                           | Commit Message Body                                                                                                                                                                   | Committed On Date |
|------------------|----------------------|----------|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| Backend-AuraNeuro | `feature/assessments` | a9f4d32  | Implement CRUD endpoints for assessments                | Added AssessmentController, AssessmentService and AssessmentRepository. Implemented Create, Read (list & detail), Update and entity mapping; added DTOs for input/output.             | 2025-11-04        |
| Backend-AuraNeuro | `feature/assessments` | b28e9c1  | Add soft-delete and author-permission checks for assessments | Introduced deleted, deletedAt fields; updated repository queries to ignore soft-deleted records; enforced that only creator or admin can edit/delete; added audit log entries. | 2025-11-05        |
| Backend-AuraNeuro | `feature/appointments` | c83d711  | Implement appointment request and creation flow         | Implemented AppointmentController and AppointmentService with flow to create appointment requests (status=requested), basic availability validation and initial notification enqueue. | 2025-11-06        |
| Backend-AuraNeuro | `feature/appointments` | d97a5b0  | Add confirm/reject and cancellation endpoints for appointments | Added endpoints to update appointment status (confirm/reject) and to cancel appointments; implemented state transitions, respondedAt/cancelledAt metadata and permission checks. | 2025-11-07        |
| Backend-AuraNeuro | `feature/availability` | e42cb1a  | Implement availability CRUD for neurologists            | Added AvailabilitySlot entity, repository and controller; supports create/list/update/delete of availability slots with preliminary overlap checks.                                   | 2025-11-07        |
| Backend-AuraNeuro | `feature/availability` | f0c9de3  | Improve availability validation and overlap detection   | Enhanced overlap detection logic, normalized timezone handling for slots and added constraints to prevent conflicting availabilities for the same neurologist.                         | 2025-11-08        |
| Backend-AuraNeuro | `feature/prescriptions` | a63bd91 | Add prescriptions CRUD and revoke flow                  | Implemented Prescription entity, create/list/detail endpoints, basic signature hash storage and revoke (soft-revoke) behavior with revoked and revokedAt metadata.                    | 2025-11-09        |
| Backend-AuraNeuro | `feature/auth`         | b7a9c00 | Implement JWT auth, OTP login and password recovery     | Added AuthService with JWT generation, OTP verification endpoints, forgot/reset password flows, and basic token blacklist for logout handling.                                        | 2025-11-10        |

---

### 5.2.3.5. Execution Evidence for Sprint Review

Durante este Sprint 3 el equipo completó la implementación y la integración de las piezas funcionales clave que sustentan los flujos clínicos entre pacientes y neurólogos. A nivel de backend se entregaron y estabilizaron los servicios REST versionados (`/api/v1/...`) para:

- Gestión de evaluaciones médicas (crear, listar, ver detalle, editar y soft-delete)  
- Ciclo completo de citas (solicitar, listar, confirmar/rechazar y cancelar)  
- Administración de franjas de disponibilidad de neurólogos  
- Emisión, consulta y revocación básica de recetas  
- Autenticación con emisión de access tokens (JWT), login por OTP y recuperación de contraseña  

Para la Sprint Review se presentarán:

- Capturas de pantalla de las vistas implementadas (Evaluaciones, Citas, Disponibilidad, Recetas y Login/OTP).  
- Un video demostrativo que muestre: registro/login, creación de evaluación, solicitud y confirmación de cita, creación/visualización/revocación de receta y consulta de franjas disponibles.

---

### 5.2.3.6. Services Documentation Evidence for Sprint Review

En el Sprint 3 se completó y publicó la documentación **OpenAPI** de los Web Services desarrollados para soportar los flujos esenciales entre pacientes y neurólogos. La documentación cubre los endpoints versionados `api/v1` implementados en este sprint:

- Assessments  
- Appointments  
- Availability  
- Prescriptions  
- Auth  
- Recursos básicos de `patients` y `neurologists` necesarios para el MVP  

La especificación OpenAPI describe:

- Operaciones (verbos HTTP)  
- Parámetros (path / query / body)  
- Esquemas de request y response  
- Códigos HTTP esperados  
- Ejemplos JSON representativos  

Se expuso via Swagger UI (local):

- Ejemplo local: `http://localhost:5000/swagger/index.html`  
- Ejemplo staging: `https://staging.api.aura-neuro.com/swagger`  

#### Tabla de Endpoints documentados (Sprint 3)

| Endpoint (resource)                             | HTTP Verb | Syntax / Call                                              | Parameters (path / query / body)                                                        | Example Request (JSON / cURL)                                                                                                             | Example Response (status & body)                                                                                      |
|------------------------------------------------|-----------|------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Assessments — Crear evaluación                 | POST      | `POST /api/v1/patients/{patientId}/assessments`           | path: `patientId` (UUID); body: `{ assessedAt, diagnosis, notes }`                      | JSON: `{"assessedAt":"2025-11-11T10:00:00Z","diagnosis":"Migraine","notes":"Follow-up in 2 weeks"}`<br>cURL: `curl -X POST "http://localhost:5000/api/v1/patients/{id}/assessments" -H "Authorization: Bearer <token>" -d '{...}'` | `201 Created { "assessmentId":"uuid", "patientId":"...", "assessedAt":"...", "diagnosis":"...", "createdBy":"neurologistId" }` |
| Assessments — Listar por paciente              | GET       | `GET /api/v1/patients/{patientId}/assessments`            | path: `patientId`; query opcional: `?from=YYYY-MM-DD&to=YYYY-MM-DD`                     | cURL: `curl -X GET "http://localhost:5000/api/v1/patients/{id}/assessments" -H "Authorization: Bearer <token>"`                           | `200 OK [ { "id":"..", "assessedAt":"..", "diagnosis":"..", "neurologistName":"Dr. X" }, ... ]`                       |
| Assessments — Detalle                          | GET       | `GET /api/v1/assessments/{assessmentId}`                  | path: `assessmentId`                                                                    | cURL: `curl -X GET "http://localhost:5000/api/v1/assessments/{aid}" -H "Authorization: Bearer <token>"`                                   | `200 OK { "id":"..", "patientId":"..", "assessedAt":"..", "diagnosis":"..", "notes":"..", "createdBy":".." }` o `404` |
| Assessments — Edit (propietario)               | PATCH     | `PATCH /api/v1/assessments/{assessmentId}`                | path: `assessmentId`; body parcial                                                      | cURL: `curl -X PATCH "http://localhost:5000/api/v1/assessments/{aid}" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"notes":"updated"}'` | `200 OK` recurso actualizado; `403 Forbidden` si no es dueño                                                        |
| Assessments — Soft-delete                      | DELETE    | `DELETE /api/v1/assessments/{assessmentId}`               | path: `assessmentId`                                                                    | cURL: `curl -X DELETE "http://localhost:5000/api/v1/assessments/{aid}" -H "Authorization: Bearer <token>"`                               | `204 No Content` en éxito; `403` si no autorizado                                                                    |
| Appointments — Solicitar cita                  | POST      | `POST /api/v1/appointments`                               | body: `{ patientId, neurologistId, startAt, endAt, reason }`                            | JSON: `{"patientId":"...","neurologistId":"...","startAt":"2025-11-20T09:00:00-05:00","endAt":"2025-11-20T09:30:00-05:00","reason":"Follow-up"}` | `201 Created { "appointmentId":"uuid", "status":"requested", "startAt":"...", "endAt":"..." }`                      |
| Appointments — Listar (paciente)               | GET       | `GET /api/v1/patients/{patientId}/appointments`           | path: `patientId`; query: `?status=confirmed|requested|cancelled`                       | cURL análogo a anteriores                                                                                                                 | `200 OK` lista de citas                                                                                              |
| Appointments — Listar solicitudes (neurólogo)  | GET       | `GET /api/v1/neurologists/{neurologistId}/appointments/requests` | path: `neurologistId`                                                          | cURL ejemplo en Swagger                                                                                                                   | `200 OK` array de solicitudes de cita                                                                               |
| Appointments — Confirmar / Rechazar            | PATCH     | `PATCH /api/v1/appointments/{appointmentId}/status`       | path: `appointmentId`; body: `{ action: "confirm" \| "reject", note?: string }`         | `curl -X PATCH "http://localhost:5000/api/v1/appointments/{id}/status" -d '{"action":"confirm"}' -H "Authorization: Bearer <token>"`      | `200 OK` estado actualizado                                                                                        |
| Appointments — Cancelar                        | DELETE    | `DELETE /api/v1/appointments/{appointmentId}`             | path: `appointmentId`                                                                    | `curl -X DELETE "http://localhost:5000/api/v1/appointments/{id}" -H "Authorization: Bearer <token>"`                                      | `204 No Content`; `403` si usuario no pertenece a la cita                                                          |
| Availability — Crear franja                    | POST      | `POST /api/v1/neurologists/{neurologistId}/availability`  | path: `neurologistId`; body: `{ startAt, endAt, recurrence? }`                          | JSON con timestamps de ejemplo                                                                                                           | `201 Created` slot `{ id, neurologistId, startAt, endAt }` o `409 Conflict` por solapamiento                      |
| Availability — Listar                          | GET       | `GET /api/v1/neurologists/{neurologistId}/availability`   | path: `neurologistId`; query opcional: `?from=&to=`                                      | [Swagger – GetAvailabilities](http://localhost:5000/swagger/index.html#/Availability/GetAvailabilities)                                   | `200 OK [ {id,startAt,endAt,isActive} ]`                                                                           |
| Availability — Actualizar                      | PATCH     | `PATCH /api/v1/availability/{slotId}`                     | path: `slotId`; body parcial `{ startAt?, endAt?, isActive? }`                          | [Swagger – PatchAvailability](http://localhost:5000/swagger/index.html#/Availability/PatchAvailability)                                   | `200 OK` slot actualizado o `409` si hay solapamiento                                                              |
| Availability — Consultar slots disponibles     | GET       | `GET /api/v1/neurologists/{neurologistId}/available-slots?date=YYYY-MM-DD` | path: `neurologistId`; query `date`                                       | [Swagger – GetAvailableSlots](http://localhost:5000/swagger/index.html#/Availability/GetAvailableSlots)                                   | `200 OK` lista de slots disponibles                                                                                |
| Prescriptions — Crear receta                   | POST      | `POST /api/v1/recipes`                                    | body: `{ patientId, medicines:[{name,dose,frequency}], instructions }`                  | JSON de ejemplo con array `medicines`                                                                                                    | `201 Created { "id":"..","issuedAt":"..","signatureHash":".." }`                                                   |
| Prescriptions — Listar por paciente            | GET       | `GET /api/v1/patients/{patientId}/recipes`                | path: `patientId`                                                                        | [Swagger – GetByPatient](http://localhost:5000/swagger/index.html#/Prescriptions/GetByPatient)                                            | `200 OK [ {id,issuedAt,neurologistName,status} ]`                                                                  |
| Prescriptions — Detalle                        | GET       | `GET /api/v1/recipes/{recipeId}`                          | path: `recipeId`                                                                         | [Swagger – GetById](http://localhost:5000/swagger/index.html#/Prescriptions/GetById)                                                     | `200 OK` receta completa (incluye `medicines[]`, `signatureHash`)                                                 |
| Prescriptions — Actualizar (parcial)           | PATCH     | `PATCH /api/v1/recipes/{recipeId}`                        | path: `recipeId`; body parcial                                                           | [Swagger – PatchPrescription](http://localhost:5000/swagger/index.html#/Prescriptions/PatchPrescription)                                  | `200 OK` recurso actualizado o `403` si no es creador                                                             |
| Prescriptions — Revocar                        | PATCH     | `PATCH /api/v1/recipes/{recipeId}/revoke`                 | path: `recipeId`; body: `{ reason }`                                                    | [Swagger – Revoke](http://localhost:5000/swagger/index.html#/Prescriptions/Revoke)                                                       | `200 OK` recurso con `revoked: true`, `revokedAt: ...`                                                            |
| Auth — Login email/password                    | POST      | `POST /api/v1/auth/login`                                 | body: `{ email, password }`                                                              | `curl -X POST "http://localhost:5000/api/v1/auth/login" -d '{"email":"juan@example.com","password":"P@ssw0rd!"}'`                        | `200 OK { accessToken:"...", expiresIn:900, user:{id,email,role} }` o `401 Unauthorized`                         |
| Auth — Send OTP                                | POST      | `POST /api/v1/auth/send-otp`                             | body: `{ phone }`                                                                        | Ver Swagger `/Auth/PostSendOtp`                                                                                                          | `200 Accepted` (enqueued)                                                                                          |
| Auth — Verify OTP                              | POST      | `POST /api/v1/auth/verify-otp`                           | body: `{ phone, otp }`                                                                   | Ver Swagger `/Auth/PostVerifyOtp`                                                                                                        | `200 OK { accessToken:"..." }` o `400/429`                                                                        |
| Auth — Forgot password                         | POST      | `POST /api/v1/auth/forgot-password`                      | body: `{ emailOrPhone }`                                                                 | Ver Swagger `/Auth/PostForgotPassword`                                                                                                   | `202 Accepted` token creado y enviado (simulado)                                                                  |
| Auth — Reset password                          | POST      | `POST /api/v1/auth/reset-password`                       | body: `{ token, newPassword }`                                                           | Ver Swagger `/Auth/PostResetPassword`                                                                                                    | `200 OK` contraseña actualizada                                                                                    |
| Patients — Registro (simplified)               | POST      | `POST /api/v1/patients/register`                         | body: `{ fullName, email?, phone?, password }`                                          | Ver Swagger `/Patients/PostRegister`                                                                                                     | `201 Created { userId: "...", nextAction: "verify_otp" }`                                                         |
| Neurologists — Registro profesional            | POST      | `POST /api/v1/neurologists`                              | body: `{ fullName, email, password, licenseNumber, specialties }`                        | Ver Swagger `/Neurologists/PostCreate`                                                                                                   | `201 Created { neurologistId, verificationStatus:"pending" }`                                                     |

---

### 5.2.3.7. Software Deployment Evidence for Sprint Review

*(Sección reservada para evidencias de despliegue: URLs de staging, capturas, notas de release, etc.)*

---

### 5.2.3.8. Team Collaboration Insights during Sprint

Durante el Sprint 3, el equipo de desarrollo de AuraNeuro mantuvo una comunicación y coordinación continua mediante diversas herramientas colaborativas:

- **Trello** para planificación y seguimiento de tareas (columnas: *Backlog*, *In Progress*, *Code Review*, *Done*).  
- **Discord** para comunicación sincrónica y asincrónica (dailies, resolución de bloqueos, sesiones de pair programming).  
- **GitHub** para control de versiones, commits, issues y pull requests, siguiendo convenciones de ramas (`feature/`, `fix/`, `doc/`).

La revisión de código se realizó de forma sistemática antes de integrar cambios en la rama principal, garantizando calidad y consistencia. Los analytics de GitHub evidencian una distribución equitativa de contribuciones entre los miembros.

La colaboración efectiva entre Trello, Discord y GitHub permitió:

- Cumplir los objetivos del Sprint  
- Mejorar la eficiencia del flujo de trabajo  
- Asegurar la entrega de:  
  - Web Services (API REST con endpoints documentados)  
  - Web Application (módulos de interacción paciente–neurólogo)  
  - Landing Page (sección informativa del sistema AuraNeuro)

---

## 5.3. Validation Interviews

### 5.3.1. Diseño de entrevistas

**Objetivo general**

Validar con usuarios reales (segmentos objetivo) la usabilidad, comprensión y valor percibido de la Landing Page y de la aplicación web (Paciente / Neurólogo) en entornos reales de staging. Detectar fricciones, confirmar hipótesis de conversión y verificar que los flujos críticos funcionan end-to-end.

**Segmentos objetivo**

- Neurólogos / terapeutas — Profesionales que usarán el dashboard clínico, gestionarán pacientes, evaluaciones, citas y recetas.  
- Pacientes o cuidadores — Usuarios que solicitarán citas, consultarán evaluaciones y recetas, y usarán el panel personal.  

---

### Evaluación heurística básica (aplicada post-tarea)

Checklist (por participante):

- Visibilidad del estado del sistema  
- Correspondencia entre el sistema y el mundo real (terminología clínica clara)  
- Control y libertad del usuario (cancelar/editar cita)  
- Consistencia y estándares (nomenclaturas, iconografía)  
- Prevención de errores (validaciones en formularios)  
- Reconocimiento en vez de recuerdo (labels claros)  
- Flexibilidad y eficiencia de uso (atajos para expertos)  
- Estética y diseño minimalista  
- Ayuda y documentación (mensajes de error útiles)  

Registrar observaciones por heurística con severidad: leve / moderada / crítica.

---

### Diseño de Entrevistas — Preguntas y Guion (AuraNeuro)

**Formato de la sesión**

- Duración: 30–45 minutos por participante  
- Modalidad: virtual  
- Registro: video grabado con consentimiento informado  

**Materiales**

- Landing Page final de AuraNeuro  
- Aplicación web funcional (frontend y backend integrados)  
- Guion de entrevista y hoja de observación  

**Estructura general de la sesión**

1. Introducción y consentimiento  
2. Preguntas demográficas y contexto  
3. Exploración libre de la Landing Page  
4. Tareas dirigidas (user flows en Landing y aplicación)  
5. Evaluación heurística y discusión final  

---

### 1. Introducción y consentimiento (moderador)

> “Hola, soy \[nombre del entrevistador/a], miembro del equipo de AuraNeuro. Gracias por participar en esta entrevista de validación. El propósito de esta sesión es comprender tus impresiones y nivel de satisfacción al usar la Landing Page y la aplicación web de AuraNeuro. La sesión será grabada únicamente con fines de análisis interno. ¿Das tu consentimiento para grabar la entrevista y utilizar tus comentarios de manera anónima en el informe final?”

Registrar:

- Consentimiento otorgado: **Sí / No**

---

### 2. Preguntas demográficas y contexto (2–3 min)

- ¿Podrías indicarme tu nombre, edad y distrito donde resides?  
- ¿Cuál es tu ocupación principal? (Médico / Terapeuta / Paciente / Familiar / Otro)  
- ¿Tienes experiencia previa utilizando plataformas de salud digital o telemedicina?  
  - Si responde “Sí”: ¿cuáles y para qué las utilizas?  
- ¿Qué te motiva más: optimizar tu práctica médica o mejorar tu experiencia como paciente?

> **Objetivo:** comprender el perfil del participante y su familiaridad con soluciones digitales de salud.

---

### 3. Exploración libre de la Landing Page (5–7 min)

**Instrucción**

> “Por favor, navega libremente por la Landing Page de AuraNeuro como si la hubieras encontrado por primera vez. Comenta en voz alta lo que vas observando, entendiendo o sintiendo.”

**Observaciones a registrar**

- Secciones más visitadas (Inicio, Características, Planes, etc.)  
- Elementos que generan atención o confusión  
- Tiempos de permanencia por sección  

**Preguntas durante o después de la exploración**

- En una frase: ¿qué crees que ofrece AuraNeuro?  
- ¿Para quién consideras que está dirigida la plataforma?  
- ¿Qué parte del diseño o contenido te generó mayor confianza?  
- ¿Hubo algo que te generó dudas o te pareció poco claro?  
- ¿Qué esperarías que ocurra al hacer clic en “Optimizar mi práctica”?  
- ¿El mensaje principal te motiva a suscribirte o explorar más?

> **Objetivo:** validar la claridad del mensaje, atractivo visual y efectividad del CTA.

---

### 4. Tareas dirigidas (User Flows)

#### 4.A — Landing Page: Suscripción / Registro

**Instrucción**

> “Haz clic en ‘Suscribirse’ y completa el formulario.”

**Observaciones**

- Tiempo en encontrar el CTA  
- Dudas al completar el formulario  
- Percepción de seguridad al ingresar datos  

**Preguntas post-tarea**

- ¿El formulario te pareció claro y fácil de completar?  
- ¿Sentiste confianza al dejar tus datos personales?  
- ¿Cambiarías o eliminarías algún campo del formulario?  
- ¿Qué te motivaría a finalizar el registro en una situación real?  

---

#### 4.B — Aplicación (Rol: Paciente): Solicitar una cita

**Instrucción**

> “Imagina que eres un paciente que desea solicitar una cita para la próxima semana con su neurólogo.”

**Preguntas post-tarea**

- ¿Encontraste fácilmente la opción para agendar una cita?  
- ¿El proceso fue claro desde la selección hasta la confirmación?  
- ¿Cómo evaluarías la rapidez y facilidad del flujo (1–5)?  
- ¿Qué mejorarías para que el proceso sea más intuitivo?  

---

#### 4.C — Aplicación (Rol: Neurólogo): Revisar y confirmar una solicitud

**Instrucción**

> “Ahora imagina que eres un neurólogo. Revisa las solicitudes de cita pendientes y confirma una.”

**Preguntas post-tarea**

- ¿Encontraste rápidamente la solicitud de cita?  
- ¿Fue claro cómo confirmar o rechazar una solicitud?  
- ¿Qué información adicional (por ejemplo, historial del paciente) te gustaría tener antes de confirmar?  

---

#### 4.D — Aplicación (Rol: Paciente): Consultar evaluaciones y recetas

**Instrucción**

> “Desde tu panel, abre el historial de evaluaciones y revisa la última receta médica.”

**Preguntas post-tarea**

- ¿Encontraste la evaluación sin dificultad?  
- ¿La información clínica y las indicaciones fueron comprensibles?  
- ¿Percibes claridad en el formato y lenguaje médico?  
- ¿Qué mejorarías para hacerlo más amigable o visualmente claro?  

---

### 5. Evaluación heurística rápida y discusión final (5–7 min)

Pide al entrevistado calificar del 1 al 5 los siguientes aspectos  
(1 = Muy deficiente, 5 = Excelente):

| Criterio                                             | Calificación (1–5) | Comentario breve |
|------------------------------------------------------|--------------------|------------------|
| Claridad del propósito de AuraNeuro                  |                    |                  |
| Confianza que transmite la plataforma                |                    |                  |
| Facilidad de registro / suscripción                  |                    |                  |
| Facilidad para solicitar o confirmar citas           |                    |                  |
| Claridad de información en secciones “Cómo funciona” y “Planes” |          |                  |

**Preguntas abiertas finales**

- ¿Qué mejorarías en la Landing Page o en la app para hacerla más atractiva o útil?  
- ¿Qué elemento te haría más propenso a registrarte o recomendarla a otros?  
- ¿Te genera alguna preocupación sobre la seguridad o privacidad de los datos en AuraNeuro?  
- En una palabra, ¿cómo describirías tu experiencia general con la plataforma?  

---

## 5.3.2. Registro de Entrevistas

### Segmento 1

- **Responsables:** Juan (1), Jhimy (1)  

**Entrevista N°1**

![Xin](images/xin.jpeg)

- **Entrevistado/a:** Shi Lin, Xin Yu
- **Entrevistador:** Meza Huanacune, Juan José 

**Información del entrevistado**

- Sexo: Masculino
- Edad: 20  
- Residencia: Lima

**Enlace Entrevista:** [Segmento1](https://drive.google.com/drive/folders/1VBndkbpcM_iixfeDW2mb7fPw4qr6-Shi?usp=sharing) 

- YouTube: 

- Inicio: 0:00  
- Duración: 16:18  

**Resumen de Entrevista**

> _(Espacio para redactar el resumen de la entrevista)_  

---

### Segmento 2

- **Responsables:** Eduardo (2), Juan (1)  

**Entrevista N°1**

![Karen](images/karen.png)

- **Entrevistado/a:** Villanueva Castillo, Karen Guadalupe
- **Entrevistador:** Meza Huanacune, Juan José 

**Información del entrevistado: **

- Sexo: Femenino  
- Edad: 26  
- Residencia: Magdalena del Mar - Lima  

**Enlace Entrevista:** [Segmento2](https://drive.google.com/drive/folders/1sv-trro2bY8jTttOsEPvxzbDPJMOhjXc?usp=sharing) 

- YouTube: 

- Inicio: 0:00  
- Duración: 16:18  

**Resumen de Entrevista**

> _(Espacio para redactar el resumen de la entrevista)_  

---

## 5.3.3. Evaluaciones según heurísticas

__

---

## 5.4. Video About-the-Product


__






