# Capítulo III: Requirements Specification  

## 3.1. User Stories.  
Lista de Epicas  

| Epic ID | Tipo                         | Descripción (Como / quiero / para)                                                                                      | Nombre de la épica                                   |
|---------|------------------------------|-------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| EP-01   | Funcional                    | Como **usuario (paciente o neurólogo)**, quiero **registrarme e iniciar sesión de forma segura (incluyendo opciones por teléfono y Google)** para **acceder a mi cuenta y servicios personalizados**. | Autenticación y Gestión de Cuentas                   |
| EP-02   | Funcional                    | Como **profesional o paciente**, quiero **editar y consultar mi perfil clínico y datos personales** para **mantener información actualizada y útil en la atención**. | Gestión de Perfiles Médicos y Datos                  |
| EP-03   | Funcional                    | Como **paciente o neurólogo**, quiero **gestionar citas y disponibilidad** para **programar, confirmar y recibir recordatorios de consultas**. | Gestión de Citas y Agenda Médica                     |
| EP-04   | Funcional                    | Como **paciente**, quiero **iniciar videollamadas one-click con mi neurólogo** y mantener comunicación síncrona para **realizar teleconsultas y seguimiento remoto**. | Videollamadas y Teleconsulta                         |
| EP-05   | Funcional                    | Como **paciente y neurólogo**, quiero **comunicarme de forma segura (chat) y gestionar registros clínicos—recetas y datos biométricos** para **dar continuidad al tratamiento**. | Comunicación, Recetas y Registro Clínico             |
| EP-06   | Funcional                    | Como **neurólogo**, quiero **emitir y consultar recetas electrónicas y revisar historial prescriptivo** para **facilitar adherencia y control farmacológico**. | Gestión de Recetas y Tratamientos                    |
| EP-07   | Funcional                    | Como **paciente**, quiero **emparejar y sincronizar mis dispositivos IoT** para **registrar automáticamente biomarcadores en mi historial clínico**. | Monitoreo IoT y Registro de Datos                    |
| EP-08   | Funcional / Seguridad        | Como **sistema clínico**, quiero **detectar anomalías y enviar alertas (incluyendo geolocalización con consentimiento)** para **activar respuestas rápidas ante eventos críticos**. | Alertas, Geolocalización y Respuesta                 |
| EP-09   | No funcional / Seguridad     | Como **administrador del sistema**, quiero **garantizar cifrado, control de accesos, límites OTP y logs de auditoría** para **proteger la confidencialidad y cumplir normativas**. | Privacidad, Seguridad y Cumplimiento                 |
| EP-10   | No funcional / Rendimiento   | Como **usuario**, quiero **tiempos de respuesta y escalabilidad garantizados** para **tener una experiencia fluida incluso con uso concurrente**. | Escalabilidad y Rendimiento                          |
| EP-11   | Funcional / Analítica        | Como **neurólogo**, quiero **recibir análisis e informes generados por IA** sobre series temporales e IoT para **identificar patrones, priorizar pacientes y apoyar decisiones clínicas**. | Analítica con IA y Dashboard Clínico                 |
| EP-12   | Funcional / UX               | Como **usuario (paciente o profesional)**, quiero **personalizar accesibilidad y apariencia de la interfaz** para **adaptarla a mis preferencias y necesidades**. | Usabilidad, Personalización y Accesibilidad          |
| EP-21   | Funcional / Contenido        | Como **visitante**, quiero **encontrar información clara y convincente en la landing (hero, how-it-works, features y sección About)** para **comprender la propuesta de valor y decidir registrarme o contactar**. | Landing — Contenido y CTA principal                  |
| EP-22   | Funcional / UI               | Como **usuario en distintos dispositivos**, quiero **una navegación responsiva y un layout adaptable** para **acceder fácilmente a secciones clave desde desktop y móvil**. | Navegación y Responsive                              |
| EP-23   | Funcional / Conversión       | Como **visitante o responsable comercial**, quiero **canales de contacto y medición (formulario, footer, tracking)** para **comunicarme con el equipo y medir conversiones**. | Contacto, Footer y Analytics                         |
| EP-24   | No funcional / Técnica       | Como **usuario y SEO manager**, quiero **que la landing cargue rápido y tenga meta tags configurados** para **mejorar UX y visibilidad en motores de búsqueda**. | Performance, SEO y Optimización                      |
| EP-25   | Funcional / Contenido        | Como **equipo de marketing**, quiero **un CMS que permita editar contenidos de la landing sin despliegues** para **iterar mensajes, imágenes y CTAs con rapidez**. | CMS y Gestión de Contenido                           |
| EP-26   | No funcional / Legal & UX    | Como **usuario**, quiero **controles de privacidad y accesibilidad (cookies, política, WCAG)** para **tener control sobre mis datos y asegurar acceso básico**. | Privacidad (Cookies) y Accesibilidad                 |




Listas de historias de usuario
<table>
  <tbody>
    <tr>
      <th>ID (HU)</th>
      <th>Título</th>
      <th>Descripción</th>
      <th>Criterios de aceptación</th>
      <th>Epic-ID</th>
    </tr>
    <tr>
      <td>US-01</td>
        <td>Inicio de sesión</td>
        <td>Como usuario (paciente o neurólogo) registrado, quiero iniciar sesión en la plataforma con mis credenciales para acceder de forma segura a mis datos y servicios personalizados.</td>
        <td>
          Escenario A (inicio exitoso): 
          Given que el usuario tiene una cuenta registrada y credenciales válidas. 
          When ingresa correo y contraseña correctos y presiona "Iniciar sesión". 
          Then el sistema autentica al usuario y lo redirige al panel correspondiente.  
          Escenario B (credenciales inválidas): 
          Given que el usuario introduce una contraseña incorrecta. 
          When intenta iniciar sesión. 
          Then el sistema muestra un mensaje de error indicando credenciales inválidas y no permite acceso.
        </td>
        <td>EP-01</td>
    </tr>
    <tr>
      <td>US-02</td>
      <td>Registro de paciente</td>
      <td>Como paciente, quiero registrarme en la plataforma proporcionando mis datos personales básicos para crear una cuenta y usar los servicios de atención neurológica remota.</td>
      <td>
        Escenario A (registro válido): 
        Given que el paciente completa el formulario con datos válidos (email único, contraseña segura). 
        When envía el formulario. 
        Then el sistema crea la cuenta, envía correo de verificación y muestra confirmación.  
        Escenario B (correo ya registrado): 
        Given que el paciente utiliza un correo ya existente. 
        When intenta registrarse. 
        Then el sistema muestra error indicando que el correo ya está en uso y solicita otro.
      </td>
      <td>EP-01</td>
    </tr>
    <tr>
      <tr>
        <td>US-03</td>
        <td>Registro de neurólogo</td>
        <td>Como neurólogo, quiero registrarme en la plataforma proporcionando mis credenciales profesionales (p. ej. número de licencia) para ofrecer consultas remotas.</td>
        <td>
          Escenario A (registro con documentación): Given que el neurólogo ingresa datos válidos y su número de licencia. When envía el formulario. Then la cuenta queda creada en estado “pendiente de verificación” y el equipo admin recibe notificación para validar la licencia.
          Escenario B (licencia inválida): Given que el número de licencia no pasa la validación interna. When intenta registrarse. Then el sistema muestra un mensaje indicando la incompatibilidad y solicita documentación adicional.
        </td>
        <td>EP-01</td>
      </tr>
    <tr>
      <td>US-04</td>
        <td>Datos de usuario</td>
        <td>Como usuario (paciente o neurólogo), quiero actualizar mis datos de perfil personal para mantener mi información actualizada en la plataforma.</td>
        <td>
          Escenario A (actualización correcta): Given que el usuario está autenticado y edita sus datos con formato válido. When guarda los cambios. Then el sistema actualiza el perfil y muestra confirmación.
          Escenario B (datos inválidos): Given que el usuario introduce un email con formato incorrecto. When intenta guardar. Then el sistema valida y muestra errores en los campos inválidos sin persistir cambios.
        </td>
        <td>EP-01</td>
    </tr>
    <tr>
      <td>US-05</td>
      <td>Ver agenda de citas</td>
      <td>Como paciente, quiero consultar mi agenda de citas programadas para visualizar la fecha, hora y neurólogo asignado de cada cita.</td>
      <td>
        Escenario A (con citas): Given que el paciente tiene citas futuras registradas. When accede a la sección “Agenda”. Then el sistema muestra lista/calendario con fechas, horas y profesionales asignados.
        Escenario B (sin citas): Given que el paciente no tiene citas. When abre la agenda. Then el sistema muestra un estado vacío con CTA para solicitar cita.
      </td>
      <td>EP-02</td>
    </tr>  
    <tr>
      <td>US-06</td>
        <td>Solicitar nueva cita</td>
        <td>Como paciente, quiero solicitar una nueva cita con el neurólogo eligiendo una fecha y hora disponibles para recibir atención médica remota.</td>
        <td>
          Escenario A (solicitud exitosa): Given que existen franjas libres en la agenda del neurólogo. When el paciente selecciona una franja y confirma la solicitud. Then el sistema crea la cita en estado “pendiente/confirmación”, envía notificación al paciente y notifica al neurólogo.
          Escenario B (conflicto de horario): Given que otro paciente reservó el mismo turno en paralelo. When el usuario intenta confirmar la cita. Then el sistema informa que la franja ya no está disponible y sugiere alternativas.
        </td>
        <td>EP-02</td>
    </tr>
    <tr>
      <td>US-07</td>
        <td>Definir disponibilidad horaria</td>
        <td>Como neurólogo, quiero configurar mis franjas horarias disponibles en la plataforma para que los pacientes puedan verlas y solicitar citas en esos periodos.</td>
        <td>
          scenario A (guardar franjas válidas): Given que el neurólogo introduce franjas sin solapamientos. When guarda la disponibilidad. Then el sistema la publica y la hace visible a pacientes.
          Escenario B (conflicto/solapamiento): Given que el neurólogo define franjas que se solapan. When intenta guardar. Then el sistema detecta el conflicto y muestra error pidiendo corrección.
        </td>
        <td>EP-02</td>
    </tr>
    <tr>
      <td>US-08</td>
        <td>Consulta por videollamada</td>
        <td>Como paciente, quiero iniciar la videollamada con mi neurólogo en la hora acordada para recibir la consulta médica de forma remota.</td>
        <td>
          Escenario A (conexión exitosa): Given que es la hora de la cita y ambos están autenticados. When el paciente hace clic en “Iniciar videollamada”. Then el sistema establece conexión WebRTC y ambos participantes ven/audio funcionan correctamente.
          Escenario B (médico no conectado): Given que el neurólogo no se ha conectado aún. When el paciente intenta iniciar la sesión. Then el sistema notifica que el profesional aún no está disponible y ofrece reintentar o dejar mensaje.
        </td>
        <td>EP-02</td>
    </tr>
    <tr>
      <td>US-09</td>
        <td>Emitir receta médica electrónica</td>
        <td>Como neurólogo, quiero generar y enviar recetas médicas electrónicas al paciente al finalizar la consulta para que pueda adquirir los medicamentos necesarios.</td>
        <td>
          Escenario A (receta válida enviada): Given que el neurólogo completa campos requeridos (medicamento, dosis, duración). When confirma la receta. Then el sistema guarda la receta en el historial del paciente y notifica al paciente.
          Escenario B (campos incompletos): Given que falta dosis en al menos un medicamento. When intenta guardar. Then el sistema bloquea la emisión y muestra error indicando campos obligatorios.
        </td>
        <td>EP-03</td>
    </tr>
    <tr>
      <td>US-10</td>
        <td>Consultar recetas médicas</td>
        <td>Como paciente, quiero acceder al historial de mis recetas médicas para visualizar y descargar las prescripciones que me ha enviado mi neurólogo.</td>
        <td>
          Escenario A (recetas disponibles): Given que existen recetas emitidas al paciente. When accede a “Recetas”. Then el sistema lista recetas con fecha, médico emisor y opción de descargar PDF.
          Escenario B (sin recetas): Given que no hay recetas registradas. When entra a la sección. Then el sistema muestra mensaje indicando ausencia y sugiere contactar al neurólogo.
        </td>
        <td>EP-03</td>
    </tr>
    <tr>
      <td>US-11</td>
      <td>Chat con el neurólogo</td>
      <td>Como paciente, quiero enviar mensajes de texto a mi neurólogo mediante un chat dentro de la plataforma para aclarar dudas o informar sobre mis síntomas entre consultas.</td>
      <td>
        Escenario A (envío y notificación): Given que el paciente y el neurólogo están activos en la plataforma. When el paciente envía un mensaje en el chat. Then el sistema entrega el mensaje y notifica al neurólogo (push/email según preferencia).
        Escenario B (mensaje vacío): Given que el campo del mensaje está vacío. When el usuario presiona “Enviar”. Then el sistema previene el envío y muestra validación “Ingrese un mensaje”.
      </td>
      <td>EP-04</td>
    </tr>
    <tr>
      <td>US-12</td>
        <td>Visualizar ubicación del paciente</td>
        <td>Como neurólogo, quiero ver la ubicación geográfica aproximada del paciente (con su permiso) durante la consulta para tener contexto en caso de emergencia.</td>
        <td>
          Escenario A (permiso otorgado): Given que el paciente otorgó permiso de geolocalización y la sesión está activa. When el neurólogo solicita ver ubicación. Then el sistema muestra mapa con ubicación aproximada y tiempo de actualización.
          Escenario B (permiso denegado): Given que el paciente no otorgó permiso o lo revocó. When el neurólogo solicita ver ubicación. Then el sistema indica “Ubicación no disponible por falta de permiso”.
        </td>
        <td>EP-05</td>
    </tr>
    <tr>
      <td>US-13</td>
      <td>Integrar dispositivo IoT médico</td>
      <td>Como paciente, quiero conectar mi dispositivo médico IoT a la plataforma para que los datos de salud se registren automáticamente en mi historial médico.</td>
      <td>
        Escenario A (emparejamiento exitoso): Given que el dispositivo es compatible y está en modo emparejamiento. When el paciente inicia emparejamiento desde la web/app y autoriza la conexión. Then la plataforma confirma la vinculación y comienza a recibir datos.
        Escenario B (fallo de emparejamiento): Given que hay interferencia Bluetooth o credenciales del dispositivo inválidas. When intenta emparejar. Then el sistema muestra error paso a paso y sugiere acciones (reintentar, revisar batería, soporte).
      </td>
      <td>EP-05</td>
    </tr>
     <tr>
      <td>US-14</td>
      <td>Alertas automáticas de salud</td>
      <td>Como paciente, quiero recibir alertas automáticas si los datos de mi dispositivo de monitoreo indican valores críticos, para que tanto yo como mi neurólogo podamos actuar.</td>
      <td>
        EEscenario A (alerta crítica): Given que los datos enviados exceden umbrales críticos definidos. When el sistema detecta la anomalía. Then envía alerta inmediata al paciente, al neurólogo y a contactos de emergencia (según configuración) con detalle del evento.
        Escenario B (falsa alarma/umbral ajustado): Given que el dato bordea el umbral pero no supera criterio validado. When el sistema procesa la señal. Then no envía alerta inmediata pero lo marca para revisión y genera nota en el historial para análisis posterior.
      </td>
      <td>EP-05</td>
    </tr>
    <tr>
      <td>US-15</td>
      <td>Seguridad y encriptación</td>
      <td>Como plataforma, la aplicación debe implementar protocolos de seguridad (HTTPS, cifrado) para proteger la información médica de accesos no autorizados.</td>
      <td>
        Escenario A (transmisión segura): Given que el usuario envía datos sensibles por la app web. When se transmite información hacia servidor. Then la comunicación usa HTTPS/TLS y el servidor registra acceso en logs de auditoría.
        Escenario B (intento de acceso no autorizado): Given que existe un intento de login sospechoso (IP anómala). When el sistema detecta patrón inusual. Then bloquea intentos, solicita verificación adicional (2FA) y registra incidente.
      </td>
      <td>EP-05</td>
    </tr>
    <tr>
      <td>US-16</td>
      <td>Rendimiento de la plataforma</td>
      <td>Como paciente o neurólogo, quiero que la plataforma cargue las páginas rápidamente (p. ej., en -2 s) para garantizar una experiencia fluida.</td>
      <td>
        Escenario A (carga under load normal): Given carga promedio de usuarios. When un usuario solicita su dashboard. Then la respuesta se entrega en -2s y la interfaz se renderiza sin errores.
        Escenario B (picos de tráfico): Given tráfico elevado (pruebas de stress). When se realizan múltiples peticiones simultáneas. Then el sistema mantiene respuesta aceptable (-4s en picos) y no presenta fallos críticos; registros de degradación quedan en logs.
      </td>
      <td>EP-06</td>
    </tr>   
    <td>US-17</td>
      <td>Privacidad de datos</td>
      <td>Como paciente o neurólogo, quiero que la plataforma garantice la confidencialidad de mis datos personales y médicos, cumpliendo normativas de privacidad (p. ej. GDPR/HIPAA).</td>
      <td>
        Escenario A (consentimiento válido): Given que un paciente firma consentimiento para uso de datos. When los datos se procesan para atención y/o investigación. Then se aplica anonimización cuando procede y acceso restringido según rol.
        Escenario B (solicitud de eliminación): Given que usuario solicita eliminación de sus datos. When se procesa la solicitud conforme a política. Then los datos personales se borran o anonimizan y se notifica al solicitante.
      </td>
      <td>EP-06</td>
    </tr>
    <tr>
    <td>US-18</td>
      <td>Analítica de salud con IA</td>
      <td>Como neurólogo, quiero que la plataforma utilice IA para analizar datos del paciente y sugerir patrones relevantes para apoyar la toma de decisiones.</td>
      <td>
        Escenario A (informe generado): Given suficientes datos históricos y configuraciones válidas. When se ejecuta análisis IA. Then se genera informe con hallazgos, nivel de confianza y recomendaciones claras para revisión por el neurólogo.
        Escenario B (insuficiencia de datos): Given que hay datos insuficientes o de baja calidad. When se solicita análisis. Then la plataforma notifica que no hay datos suficientes y sugiere recolectar más información antes de ejecutar modelos.
      </td>
      <td>EP-06</td>
    </tr>
    <tr>
      <td>US-19</td>
      <td>Recordatorios de citas</td>
      <td>Como paciente, quiero recibir recordatorios automáticos (email/ push) sobre mis próximas citas para asegurar mi asistencia a tiempo.</td>
      <td>
        Escenario A (recordatorio enviado): Given que existe una cita en 24 horas y el paciente tiene notificaciones habilitadas. When el sistema programa recordatorios. Then envía notificación por los canales configurados y registra entrega.
        Escenario B (usuario pospone cita): Given que recibe recordatorio y decide posponer. When actualiza la cita. Then el sistema actualiza el calendario y envía confirmación de la nueva fecha/hora.
      </td>
      <td>EP-07</td>
    </tr>
    <tr>
      <td>US-20</td>
      <td>Personalización de la interfaz</td>
      <td>Como paciente o neurólogo, quiero personalizar la interfaz (tema oscuro, tamaño de fuente) para adaptarla a mis preferencias de accesibilidad.</td>
      <td>
        Escenario A (aplicar preferencia): Given que el usuario selecciona tema oscuro y tamaño de fuente mayor. When guarda preferencias. Then la UI se aplica inmediatamente y se persisten sus preferencias para próximas sesiones.
        Escenario B (preferencia no aplicable en componente): Given que una vista antigua no soporta cambio de fuente. When aplica nueva preferencia. Then la mayoría de la interfaz cambia y la plataforma muestra nota indicando qué componentes no son totalmente compatibles hasta actualizarse.
      </td>
      <td>EP-07</td>
    </tr>
    <tr>
  <td>US21</td>
  <td>Navegación responsiva</td>
  <td>Como <strong>visitante</strong> en desktop o móvil, quiero una barra de navegación clara y menú hamburguesa en móvil para acceder a secciones (How it works, About, Contact).</td>
  <td>
    <strong>Escenario A (desktop):</strong><br>
    Given usuario en desktop, When ve la cabecera, Then muestra links horizontales y botón destacado de Contact.<br><br>
    <strong>Escenario B (móvil):</strong><br>
    Given usuario en móvil, When pulsa el icono hamburguesa, Then se abre menú vertical con enlaces a secciones y CTA visible.
  </td>
  <td style="text-align:center;">3</td>
</tr>

<tr>
  <td>US22</td>
  <td>Sección “How it works” con pasos</td>
  <td>Como <strong>visitante</strong>, quiero ver pasos visuales (Register → Enter number → Welcome) con capturas para comprender el flujo en 3 pasos.</td>
  <td>
    <strong>Escenario A (contenido visible):</strong><br>
    Given landing cargada, When se desplaza a How it works, Then muestra los 3 pasos con título, descripción e imagen.<br><br>
    <strong>Escenario B (accesibilidad):</strong><br>
    Given lector de pantalla activo, When navega la sección, Then los pasos tienen texto alternativo y semántica para ser leídos correctamente.
  </td>
  <td style="text-align:center;">2</td>
</tr>

<tr>
  <td>US23</td>
  <td>Bloque de Features / Cards</td>
  <td>Como <strong>visitante</strong>, quiero ver tarjetas de beneficios (Telemedicine, Pharmacy/Devices, etc.) con iconos y CTA para explorar cada servicio.</td>
  <td>
    <strong>Escenario A (hover/acción):</strong><br>
    Given usuario en desktop, When pone cursor sobre card, Then la card muestra efecto y enlace "Try" o "Más info".<br><br>
    <strong>Escenario B (clic en card):</strong><br>
    Given usuario hace clic en una card, When confirma la acción, Then lo redirige a la sección interna o abre modal con detalles.
  </td>
  <td style="text-align:center;">3</td>
</tr>

<tr>
  <td>US24</td>
  <td>Sección About / Who we are</td>
  <td>Como <strong>visitante</strong>, quiero leer acerca de la misión y cómo funciona AuraNeuro para evaluar credibilidad antes de registrarme.</td>
  <td>
    <strong>Escenario A (texto visible):</strong><br>
    Given landing cargada, When se desplaza a About, Then el contenido muestra título, párrafos e imágenes correctamente alineados.<br><br>
    <strong>Escenario B (descarga/print):</strong><br>
    Given un usuario desea guardar info, When imprime o guarda página, Then la sección About se muestra de forma adecuada en impresión/PDF.
  </td>
  <td style="text-align:center;">2</td>
</tr>

<tr>
  <td>US25</td>
  <td>Beneficios y “Good for business”</td>
  <td>Como <strong>decisor institucional</strong>, quiero ver beneficios clínicos y comerciales para evaluar el caso de negocio.</td>
  <td>
    <strong>Escenario A (listado):</strong><br>
    Given landing cargada, When llega a Benefits, Then muestra bullets de beneficios para pacientes y empresas.<br><br>
    <strong>Escenario B (cta institucional):</strong><br>
    Given interesado, When pulsa CTA de contacto al final de la sección, Then envía pre-fill indicando interés institucional al formulario.
  </td>
  <td style="text-align:center;">3</td>
</tr>

<tr>
  <td>US26</td>
  <td>Formulario de contacto validado</td>
  <td>Como <strong>visitante</strong>, quiero completar un formulario (nombre, email, teléfono, mensaje) con validaciones para contactar al equipo.</td>
  <td>
    <strong>Escenario A (envío válido):</strong><br>
    Given usuario completa campos obligatorios con formato correcto, When envía formulario, Then se muestra confirmación y correo al equipo se crea/toma en CRM.<br><br>
    <strong>Escenario B (errores de validación):</strong><br>
    Given campo email inválido o campo obligatorio vacío, When intenta enviar, Then se muestran errores y no se envía el formulario.
  </td>
  <td style="text-align:center;">3</td>
</tr>

<tr>
  <td>US27</td>
  <td>Footer con enlaces y redes sociales</td>
  <td>Como <strong>visitante</strong>, quiero ver en el footer enlaces, contacto y redes sociales para seguir o contactar más tarde.</td>
  <td>
    <strong>Escenario A (enlaces funcionan):</strong><br>
    Given landing cargada, When hace clic en un enlace de política o social, Then se abre la página correspondiente o red social en nueva pestaña.<br><br>
    <strong>Escenario B (accesibilidad footer):</strong><br>
    Given navegación por teclado, When tabula hasta footer, Then los enlaces son accesibles y visibles.
  </td>
  <td style="text-align:center;">1</td>
</tr>

<tr>
  <td>US28</td>
  <td>Responsive layout y comportamiento mobile</td>
  <td>Como <strong>usuario móvil</strong>, quiero que la landing se adapte (colapsado, imágenes y texto legible) para una experiencia óptima.</td>
  <td>
    <strong>Escenario A (pantallas pequeñas):</strong><br>
    Given viewport &lt; 768px, When carga la página, Then el diseño se reorganiza (columnas → stack), texto se redimensiona y CTAs siguen visibles.<br><br>
    <strong>Escenario B (pruebas tablet):</strong><br>
    Given tablet, When gira pantalla, Then elementos no se solapan y navegación funciona.
  </td>
  <td style="text-align:center;">3</td>
</tr>

<tr>
  <td>US29</td>
  <td>Performance y optimización de imágenes</td>
  <td>Como <strong>usuario</strong>, quiero que la landing cargue rápido (imágenes optimizadas, lazy-loading) para buena experiencia y SEO.</td>
  <td>
    <strong>Escenario A (carga inicial):</strong><br>
    Given visita primero, When carga la landing, Then el LCP se carga &lt; 2.5s (imágenes optimizadas y lazy load en secciones bajas).<br><br>
    <strong>Escenario B (navegación):</strong><br>
    Given navegación a secciones, When se desplaza, Then imágenes se muestran sin salto de layout (CLS controlado).
  </td>
  <td style="text-align:center;">5</td>
</tr>

<tr>
  <td>US30</td>
  <td>SEO básico y meta tags</td>
  <td>Como <strong>equipo de marketing</strong>, quiero meta tags y OG tags configurados en la landing para mejorar posicionamiento y compartir en redes.</td>
  <td>
    <strong>Escenario A (meta tags):</strong><br>
    Given HTML entregado, When inspecciona head, Then meta title, description y OG tags están presentes y relevantes.<br><br>
    <strong>Escenario B (prueba social share):</strong><br>
    Given URL compartida en redes, When se genera el preview, Then muestra título, descripción e imagen correcta.
  </td>
  <td style="text-align:center;">2</td>
</tr>

<tr>
  <td>US31</td>
  <td>Cookie consent y política de privacidad</td>
  <td>Como <strong>visitante</strong>, quiero aceptar/ rechazar cookies y ver la política de privacidad para control sobre mis datos y geolocalización.</td>
  <td>
    <strong>Escenario A (mostrar consentimiento):</strong><br>
    Given primera visita, When carga la página, Then se muestra banner de cookies con opciones Aceptar/Rechazar y enlace a política.<br><br>
    <strong>Escenario B (rechazo):</strong><br>
    Given usuario rechaza cookies, When navega, Then cookies no esenciales quedan deshabilitadas y no se ejecutan trackers.
  </td>
  <td style="text-align:center;">3</td>
</tr>

<tr>
  <td>US32</td>
  <td>Tracking de eventos y analytics</td>
  <td>Como <strong>product owner</strong>, quiero trackear clicks a CTA, envíos de formulario y scroll depth para medir conversión y optimizar la landing.</td>
  <td>
    <strong>Escenario A (evento CTA):</strong><br>
    Given visitante hace clic en CTA Try, When ocurre el clic, Then se registra evento en analytics (label + page) y se verifica en dashboard.<br><br>
    <strong>Escenario B (form submit):</strong><br>
    Given formulario enviado con éxito, When se confirma envío, Then se dispara evento de conversión con atributos (source/utm).
  </td>
  <td style="text-align:center;">2</td>
</tr>

<tr>
  <td>US33</td>
  <td>Contenidos editables (CMS)</td>
  <td>Como <strong>marketing</strong>, quiero poder editar títulos, textos, imágenes y CTAs desde un CMS para actualizar la landing sin deploy.</td>
  <td>
    <strong>Escenario A (editar hero):</strong><br>
    Given acceso al CMS con permisos, When actualiza título/subtítulo/imagen y publica, Then la landing muestra los cambios inmediatamente.<br><br>
    <strong>Escenario B (rollback):</strong><br>
    Given se publica contenido erróneo, When se solicita rollback, Then se restaura versión anterior desde el CMS.
  </td>
  <td style="text-align:center;">5</td>
</tr>

<tr>
  <td>US34</td>
  <td>Accesibilidad (WCAG 2.1 básico)</td>
  <td>Como <strong>usuario con necesidades de accesibilidad</strong>, quiero que la landing cumpla WCAG 2.1 mínimo (contraste, alt text, keyboard nav).</td>
  <td>
    <strong>Escenario A (contraste):</strong><br>
    Given elementos visuales, When se evalúa contraste, Then colores cumplen ratio mínimo WCAG AA para texto principal.<br><br>
    <strong>Escenario B (navegación por teclado):</strong><br>
    Given navegación sin mouse, When tabula por la página, Then todos los CTAs y links son alcanzables y el foco es visible.
  </td>
  <td style="text-align:center;">3</td>
</tr>
<tr>
      <td>US-35</td>
      <td>Autenticación por número de celular</td>
      <td>Como usuario (paciente o neurólogo) quiero poder registrarme e iniciar sesión usando mi número de celular para acceder de forma rápida y sin contraseña.</td>
      <td>
        <strong>Escenario A (login con teléfono existente):</strong><br>
        Given que el usuario introduce un número de celular registrado y solicita código OTP. <br>
        When recibe e ingresa el OTP correcto dentro del periodo de validez. <br>
        Then el sistema autentica al usuario y lo redirige a su panel.<br><br>
        <strong>Escenario B (registro con teléfono nuevo):</strong><br>
        Given que el número no está registrado en la plataforma. <br>
        When el usuario inicia el flujo de registro introduciendo el número y verifica con OTP. <br>
        Then el sistema crea la cuenta (o completa el registro) tras la verificación y solicita datos faltantes si procede.<br><br>
        <strong>Escenario C (número inválido o formato incorrecto):</strong><br>
        Given que el usuario introduce un número en formato inválido. <br>
        When intenta continuar. <br>
        Then el sistema muestra un error de formato y no envía OTP.
      </td>
      <td>EP-01</td>
    </tr>
    <tr>
      <td>US-36</td>
      <td>Verificación de número de celular (OTP)</td>
      <td>Como usuario quiero verificar mi número de celular mediante un código OTP para confirmar la titularidad y asegurar la autenticación basada en SMS.</td>
      <td>
        <strong>Escenario A (OTP correcto y válido):</strong><br>
        Given que el sistema envió un OTP al número proporcionado y este no ha expirado. <br>
        When el usuario ingresa el OTP correcto. <br>
        Then la verificación se completa, el número queda confirmado y se permite continuar (login o registro).<br><br>
        <strong>Escenario B (OTP incorrecto / reintento):</strong><br>
        Given que el usuario ingresa un OTP incorrecto. <br>
        When lo ingresa nuevamente (hasta límite permitido). <br>
        Then el sistema muestra error, decrementa contador de intentos y permite reintentar hasta el límite; al agotarlo bloquea temporalmente el envío.<br><br>
        <strong>Escenario C (OTP expirado / reenvío):</strong><br>
        Given que el OTP expiró antes de ser usado. <br>
        When el usuario solicita reenvío. <br>
        Then el sistema genera un nuevo OTP y lo envía, registrando timestamp y limitando reenvíos según política.
      </td>
      <td>EP-01</td>
    </tr>
    <tr>
      <td>US-37</td>
      <td>Inicio de sesión con Google (OAuth)</td>
      <td>Como usuario quiero poder autenticarme con mi cuenta de Google para agilizar el acceso y evitar recordar contraseñas.</td>
      <td>
        <strong>Escenario A (primer login con Google - creación de cuenta):</strong><br>
        Given que el usuario elige “Iniciar con Google” y autoriza los permisos básicos (email, nombre). <br>
        When la plataforma recibe el token y verifica el email. <br>
        Then se crea (o completa) una cuenta vinculada a ese email y el usuario queda autenticado; se solicita completar datos faltantes si los hubiera.<br><br>
        <strong>Escenario B (Google email ya asociado a cuenta existente):</strong><br>
        Given que el email de Google ya existe en la plataforma (registro previo). <br>
        When el usuario intenta iniciar con Google. <br>
        Then el sistema propone vincular la cuenta Google al usuario existente tras autenticación adicional (p. ej. ingreso por contraseña o verificación OTP) para evitar duplicados.<br><br>
        <strong>Escenario C (usuario revoca permisos o cancela):</strong><br>
        Given que el usuario cancela el flujo de autorización en Google. <br>
        When retorna al sitio sin token. <br>
        Then la plataforma muestra mensaje de cancelación y permite elegir otro método de ingreso.
      </td>
      <td>EP-01</td>
    </tr>
    <tr>
      <td>US-38</td>
      <td>Consentimiento para uso del número de teléfono y comunicación SMS</td>
      <td>Como usuario quiero dar (y poder revocar) consentimiento explícito para que mi número de celular sea usado en autenticación y para recibir notificaciones/alertas por SMS, cumpliendo privacidad.</td>
      <td>
        <strong>Escenario A (consentimiento otorgado):</strong><br>
        Given que el usuario marca la casilla de consentimiento durante registro o en configuración. <br>
        When se almacena la elección con timestamp y alcance. <br>
        Then el sistema puede enviar OTP y notificaciones por SMS según la preferencia y queda registrada la autorización.<br><br>
        <strong>Escenario B (revocación de consentimiento):</strong><br>
        Given que el usuario revoca el consentimiento desde su cuenta. <br>
        When la acción es confirmada. <br>
        Then la plataforma deja de enviar SMS no esenciales y actualiza la política de comunicación; se notifica al usuario sobre las implicancias (p. ej. perder opción de login por SMS si procede).<br><br>
        <strong>Escenario C (consentimiento requerido y no otorgado):</strong><br>
        Given que el usuario no otorga consentimiento. <br>
        When intenta usar funciones que requieren SMS (OTP, alertas). <br>
        Then el sistema bloquea esas acciones y sugiere métodos alternativos (correo, autenticación social).
      </td>
      <td>EP-09</td>
    </tr>
    <tr>
      <td>US-39</td>
      <td>Protección y límites en el flujo OTP (rate-limiting & fraude)</td>
      <td>Como plataforma quiero implementar límites de envío y verificación de OTP y detección básica de fraude para prevenir abuso y proteger a los usuarios.</td>
      <td>
        <strong>Escenario A (limitación de envíos):</strong><br>
        Given que se han solicitado múltiples OTP desde el mismo número/IP en un corto periodo. <br>
        When se supera el umbral definido. <br>
        Then el sistema bloquea temporalmente nuevos envíos y muestra mensaje de espera con tiempo estimado para reintentar.<br><br>
        <strong>Escenario B (detección de intentos masivos de verificación):</strong><br>
        Given múltiples intentos fallidos de ingreso de OTP desde la misma IP/número. <br>
        When el contador excede el límite. <br>
        Then la cuenta se bloquea temporalmente para verificación manual/recuperación segura y se registra el evento en logs de seguridad.<br><br>
        <strong>Escenario C (registro y notificación al usuario):</strong><br>
        Given que una cuenta sufre bloqueo por actividad sospechosa. <br>
        When ocurre el bloqueo. <br>
        Then el sistema notifica al propietario (por correo o SMS si permitido) e instruye los pasos a seguir para recuperar el acceso.
      </td>
      <td>EP-09</td>
    </tr>
  </tbody>
</table>

## 3.2. Impact Mapping  

El presente apartado muestra los **Impact Maps** elaborados en **UXPressia**, uno por cada segmento objetivo del proyecto **AuraNeuro**.  
Esta técnica permitió vincular los **objetivos estratégicos del negocio digital (Business Goals)** con las **acciones esperadas de los usuarios (Impacts)**, los **entregables del producto (Deliverables)** y las **User Stories** que los harán posibles.  
El análisis se realizó siguiendo el formato propuesto por *Impact Mapping (Gojko Adzic, 2012)*, asegurando que los objetivos cumplan criterios **SMART** (específicos, medibles, alcanzables, relevantes y con tiempo definido).

---

### Metodología de elaboración  
1. Se revisaron los *User Personas* creados previamente para identificar cómo cada uno puede **contribuir a los objetivos del negocio**.  
2. Se definieron **Business Goals medibles** basados en los resultados esperados del MVP.  
3. Se formularon los **Impacts** como comportamientos o acciones observables que los usuarios deberían realizar.  
4. A partir de los *Impacts*, se definieron los **Deliverables**, es decir, las funcionalidades o productos digitales que el equipo de desarrollo debe construir.  
5. Finalmente, se redactaron **User Stories** en formato *“Como [rol], quiero [acción], para [beneficio]”*, que servirán de base para el *Product Backlog*.

---

### Impact Mapping – Segmento 1: Paciente (Epilepsia crónica)

![Impact Mapping - Paciente](./imagesChapter03/impactMapping/Segmento1IM.png)

**Business Goal (SMART):**  
> Alcanzar **500 pacientes activos** que registren de forma continua sus crisis neurológicas en la aplicación durante los **próximos 6 meses**.

**Síntesis:**  
El paciente **Xin Yu Shi Lin** necesita registrar crisis en tiempo real y recibir recordatorios automáticos para mejorar su adherencia al tratamiento.  
Las *User Stories* derivadas priorizan la **automatización del registro** y la **personalización de notificaciones médicas**.  
Esto permitirá medir el progreso del paciente y generar engagement sostenido en la app.

---

### Impact Mapping – Segmento 2: Profesional de la salud (Neuróloga especialista)

![Impact Mapping - Profesional](./imagesChapter03/impactMapping/Segmento2IM.png)

**Business Goal (SMART):**  
> Reducir en **30 %** las consultas presenciales innecesarias de pacientes neurológicos crónicos durante los **próximos 12 meses**.

**Síntesis:**  
La doctora **Karen Villanueva** busca optimizar su tiempo clínico y disponer de datos confiables para decisiones rápidas.  
Las historias de usuario se orientan al **uso de dashboards en tiempo real** y a la **exportación FHIR**, facilitando diagnósticos más precisos y disminuyendo la carga administrativa.

---

### Impact Mapping – Segmento 3: Proveedores IoT  

![Impact Mapping - Proveedores IoT](./imagesChapter03/impactMapping/Segmento3IM.png)

**Business Goal (SMART):**  
> Lograr la **integración de 200 dispositivos IoT activos** (wearables, EEG portátiles) con la plataforma **en los próximos 8 meses**.

**Síntesis:**  
El proveedor **Carlos Paredes** busca escalar sus productos al ecosistema médico mediante integraciones seguras.  
Los impactos propuestos impulsan la **colaboración B2B** a través de APIs y SDKs abiertos, reforzando la interoperabilidad y la validación automática de datos biométricos.

---

### Interpretación general  

| **Dimensión** | **Hallazgo transversal** | **Implicancia para el MVP de AuraNeuro** |
|----------------|---------------------------|-------------------------------------------|
| **Alineación estratégica** | Todos los segmentos contribuyen a objetivos medibles y alcanzables. | Las metas SMART permiten monitorear el progreso de adopción y valor. |
| **Ecosistema conectado** | Los tres actores (paciente, médico, proveedor) dependen de datos sincronizados. | Se debe priorizar interoperabilidad IoT + FHIR desde la primera versión. |
| **Entrega de valor** | Cada Deliverable representa una funcionalidad crítica validada por usuarios. | Los User Stories se convierten en base directa para el *Product Backlog*. |

---

### Conclusión  

El **Impact Mapping** permitió visualizar cómo cada *User Persona* contribuye de manera medible al éxito del negocio digital de **AuraNeuro**.  
Las relaciones entre *Goals–Impacts–Deliverables–User Stories* garantizan que el desarrollo del MVP mantenga **enfoque, trazabilidad y alineación con los resultados clínicos y de negocio**.

---


## 3.3. Product Backlog.

# 🧩 Plataforma AuraNeuro

| Order | User Story Id | Título                            | Descripción (Como... deseo... para...)                                                                                                 | Story Points (1 / 2 / 3 / 5 / 8) |
|-------:|:-------------:|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------:|
| 1     | US01          | Inicio de sesión                  | Como usuario (paciente o neurólogo) deseo iniciar sesión con mis credenciales para acceder de forma segura a mi panel personal.         | 2                                |
| 2     | US02          | Registro de paciente              | Como paciente deseo registrarme con mis datos personales para crear una cuenta y acceder a los servicios de atención remota.            | 3                                |
| 3     | US03          | Registro de neurólogo             | Como neurólogo deseo registrarme aportando credenciales profesionales para ofrecer consultas remotas y ser verificado por el sistema.   | 3                                |
| 4     | US04          | Gestión de perfil                 | Como usuario deseo actualizar mi perfil (foto, contacto, datos) para mantener mi información clínica y de contacto actualizada.         | 2                                |
| 5     | US05          | Ver agenda de citas               | Como paciente deseo ver mi agenda de citas para conocer fechas, horas y el neurólogo asignado.                                         | 2                                |
| 6     | US06          | Solicitar nueva cita              | Como paciente deseo solicitar una nueva cita eligiendo fecha/hora disponible para programar atención remota.                            | 3                                |
| 7     | US07          | Definir disponibilidad horaria    | Como neurólogo deseo configurar mis franjas horarias disponibles para que los pacientes puedan solicitar citas en esos periodos.         | 3                                |
| 8     | US08          | Consulta por videollamada         | Como paciente deseo iniciar la videollamada con mi neurólogo en la hora acordada para realizar la consulta remota en tiempo real.        | 8                                |
| 9     | US09          | Emitir receta médica electrónica  | Como neurólogo deseo generar y enviar recetas electrónicas al paciente para que pueda adquirir los medicamentos prescritos.              | 5                                |
| 10    | US10          | Consultar recetas médicas         | Como paciente deseo acceder a mi historial de recetas para ver, descargar o imprimir las prescripciones recibidas.                       | 2                                |
| 11    | US11          | Chat con el neurólogo             | Como paciente deseo comunicarme por chat con mi neurólogo para aclarar dudas y reportar síntomas entre consultas.                       | 5                                |
| 12    | US12          | Visualizar ubicación del paciente | Como neurólogo deseo ver la ubicación aproximada del paciente (con permiso) para tener contexto en caso de emergencia.                   | 3                                |
| 13    | US13          | Integrar dispositivo IoT médico   | Como paciente deseo emparejar mi dispositivo IoT para que los datos biométricos se registren automáticamente en mi historial clínico.   | 8                                |
| 14    | US14          | Alertas automáticas de salud      | Como paciente (y neurólogo) deseo recibir alertas automáticas cuando los datos IoT indiquen valores críticos para actuar oportunamente. | 8                                |
| 15    | US15          | Seguridad y encriptación          | Como plataforma deseo implementar HTTPS/ TLS y cifrado en reposo para proteger los datos médicos frente a accesos no autorizados.        | 5                                |
| 16    | US16          | Rendimiento de la plataforma      | Como usuario deseo que las páginas críticas carguen rápido (ej. < 2s) para una experiencia fluida y eficiente.                          | 3                                |
| 17    | US17          | Privacidad de datos               | Como usuario deseo que mis datos se manejen conforme a normativas (consentimientos, anonimización, borrado) para proteger mi privacidad. | 5                                |
| 18    | US18          | Analítica de salud con IA         | Como neurólogo deseo que la plataforma analice datos con IA para sugerir patrones o riesgos que apoyen la toma de decisiones.             | 8                                |
| 19    | US19          | Recordatorios de citas            | Como paciente deseo recibir recordatorios automáticos (email/push) sobre mis próximas citas para asegurar mi asistencia.                 | 2                                |
| 20    | US20          | Personalización de la interfaz    | Como usuario deseo personalizar la UI (tema, tamaño de fuente) para adaptar la plataforma a mis preferencias y necesidades de accesibilidad. | 2                             |
| 21    | US21          | Hero con CTA principal            | Como visitante deseo ver un hero claro con título, subtítulo y CTA (Try / Contact) para entender la propuesta y poder actuar rápido.     | 2                                |
| 22    | US22          | Navegación responsiva             | Como visitante en desktop o móvil deseo una barra de navegación clara y menú hamburguesa en móvil para acceder a secciones clave.        | 3                                |
| 23    | US23          | Sección “How it works” con pasos  | Como visitante deseo ver pasos visuales (Register → Enter number → Welcome) con capturas para comprender el flujo en 3 pasos.            | 2                                |
| 24    | US24          | Bloque de Features / Cards        | Como visitante deseo ver tarjetas de beneficios (Telemedicine, Pharmacy/Devices, etc.) con iconos y CTA para explorar cada servicio.     | 3                                |
| 25    | US25          | Sección About / Who we are        | Como visitante deseo leer acerca de la misión y cómo funciona AuraNeuro para evaluar credibilidad antes de registrarme.                  | 2                                |
| 26    | US26          | Beneficios y “Good for business”  | Como decisor institucional deseo ver beneficios clínicos y comerciales para evaluar el caso de negocio.                                  | 3                                |
| 27    | US27          | Formulario de contacto validado   | Como visitante deseo completar un formulario (nombre, email, teléfono, mensaje) con validaciones para contactar al equipo.               | 3                                |
| 28    | US28          | Footer con enlaces y redes sociales | Como visitante deseo ver en el footer enlaces, contacto y redes sociales para seguir o contactar más tarde.                             | 1                                |
| 29    | US29          | Responsive layout y comportamiento mobile | Como usuario móvil deseo que la landing se adapte (colapsado, imágenes y texto legible) para una experiencia óptima.               | 3                                |
| 30    | US30          | Performance y optimización de imágenes | Como usuario deseo que la landing cargue rápido (imágenes optimizadas, lazy-loading) para buena experiencia y SEO.                  | 5                                |
| 31    | US31          | SEO básico y meta tags            | Como equipo de marketing deseo meta tags y OG tags configurados en la landing para mejorar posicionamiento y compartir en redes.        | 2                                |
| 32    | US32          | Cookie consent y política de privacidad | Como visitante deseo aceptar/rechazar cookies y ver la política de privacidad para control sobre mis datos y geolocalización.       | 3                                |
| 33    | US33          | Tracking de eventos y analytics   | Como product owner deseo trackear clicks a CTA, envíos de formulario y scroll depth para medir conversión y optimizar la landing.        | 2                                |
| 34    | US34          | Contenidos editables (CMS)        | Como marketing deseo poder editar títulos, textos, imágenes y CTAs desde un CMS para actualizar la landing sin deploy.                  | 5                                |
| 35    | US35          | Accesibilidad (WCAG 2.1 básico)   | Como usuario con necesidades de accesibilidad deseo que la landing cumpla WCAG 2.1 mínimo (contraste, alt text, keyboard nav).           | 3                                |

---

## Épicas principales

- Épica 1: **Gestión de usuarios y autenticación**
  - Registro de paciente y neurólogo (US02, US03)  
  - Inicio de sesión (US01)  
  - Gestión de perfil (US04)

- Épica 2: **Atención remota y citas médicas**
  - Agenda y solicitud de citas (US05, US06, US07, US19)  
  - Videollamada médica (US08)  
- Chat paciente-neurólogo (US11)

- Épica 3: **Gestión clínica e IoT**
  - Recetas electrónicas (US09, US10)  
  - Integración IoT y alertas automáticas (US13, US14)  
  - Analítica con IA (US18)

- Épica 4: **Seguridad, rendimiento y cumplimiento**
  - Seguridad y privacidad (US15, US17)  
  - Rendimiento (US16, US30)  
  - Accesibilidad (US35)

- Épica 5: **Landing Page informativa y marketing**
  - Hero, navegación y secciones informativas (US21–US26)  
  - Formulario de contacto (US27)  
  - Footer y redes (US28)  
  - SEO, analytics y CMS (US31–US34)

---


