# Capítulo II: Requirements Elicitation & Analysis

## 2.1. Competidores.

### 2.1.1. Análisis competitivo.  

En esta sección se presentan algunos competidores relevantes en el ámbito del monitoreo neurológico y la telemedicina, así como un análisis de las características que nuestra plataforma IoT busca superar.  

<table>
  <tr>
    <th colspan="22">Competitive Analysis Landscape</th>
  </tr>
  <tr>
    <td colspan="1">¿Por qué llevar a cabo el análisis?</td>
    <td colspan="17">El análisis competitivo es esencial para entender el mercado, identificar oportunidades que nos diferencien y anticipar amenazas. Permite ajustar la estrategia para ganar ventaja sobre la competencia y asegurar el éxito del producto.</td>
  </tr>
  <tr>
    <td colspan="2"></td>
    <td>startup<br><img src="" alt=""></td>
    <td>Ceribell<br><img src="" alt=""></td>
    <td>Empatica (Embrace/EmbracePlus)<br><img src="" alt=""></td>
    <td>NeuroPace (RNS)<br><img src="" alt=""></td>
</tr>
  <tr>
    <td rowspan="2">Perfil</td>
    <td>Overview</td>
    <td>Plataforma web + IoT + IA para monitoreo neurológico continuo, gestión de pacientes, agenda y teleconsultas; alertas con geolocalización (con consentimiento).</td>
    <td>EEG portátil orientado a diagnóstico rápido en entornos hospitalarios (UCI / emergencias).</td>
    <td>Wearable biomédico (pulseras) para monitorización continua; orientado a investigación y monitoreo ambulatorio de epilepsia.</td>
    <td>Sistema implantable de neuromodulación con detección y respuesta adaptativa para epilepsia refractaria.</td>
</tr>
  <tr>
  <td>Ventaja competitiva ¿Qué valor ofrece a los clientes?</td>
    <td>Gestión clínica completa (registro, agenda, teleconsulta), monitoreo 24/7, alertas y ubicación para respuesta rápida; análisis longitudinal con IA.</td>
    <td>Diagnóstico rápido en situaciones agudas; reducción de tiempo a diagnóstico en emergencias.</td>
    <td>Recolección continua y validada de biométricos para investigación y monitoreo domiciliario.</td>
    <td>Terapia activa: detecta actividad anómala y entrega estimulación; solución terapéutica implantable.</td>
    </tr>
<tr>
    <td rowspan="2">Perfil de Marketing</td>
    <td>Mercado Objetivo</td>
    <td>Pacientes crónicos, neurólogos, clínicas, aseguradoras, cuidadores.</td>
    <td>Hospitales, UCI, equipos de emergencias.</td>
    <td>Investigadores, centros clínicos y pacientes con epilepsia ambulatoria.</td>
    <td>Pacientes con epilepsia farmacorresistente candidatos a implante; neurocirujanos.</td>
  </tr>
  <tr>
  <td>Estrategias de Marketing</td>
    <td>Pilotos con clínicas/aseguradoras, marketing B2B a neurólogos, alianzas con asociaciones de pacientes, contenido científico (casos de uso/papers), campañas digitales dirigidas a cuidadores y profesionales, conferencias médicas.</td>
    <td>Marketing B2B directo a hospitales y UCIs; publicaciones clínicas y demostraciones en entornos de emergencias; ferias médicas hospitalarias.</td>
    <td>Alianzas con universidades e investigadores; marketing dirigido a pacientes y familias (comunidad epilepsia); publicaciones científicas y colaboraciones en estudios clínicos.</td>
    <td>Comunicación dirigida a especialistas (neurocirujanos, epileptólogos), publicaciones en revistas clínicas y presentaciones en congresos; relaciones con centros de referencia.</td>
    </tr>
<tr>
    <td rowspan="3">Perfil de Producto</td>
    <td>Productos y Servicios</td>
    <td>Plataforma web + app móvil: registro clínico, agenda, teleconsultas (WebRTC), ingestión de datos IoT, detección de eventos (IA), alertas (incl. ubicación con consentimiento), dashboard clínico, módulo de investigación/exportes.</td>
    <td>Dispositivo EEG portátil + software de análisis para diagnóstico rápido en hospital; entrenamiento clínico y soporte.</td>
    <td>Wearable (pulsera) + plataforma de datos para monitorización continua (actividad, ritmo cardiaco, eventos), APIs para investigación y dashboard.</td>
    <td>Sistema implantable (neurostimulación adaptativa RNS) + plataforma de seguimiento clínico para equipo médico.</td>
  </tr>
  <tr>
  <td>Precios y Costos</td>
    <td>Modelo mixto: suscripción institucional (clínicas/hospitals) y/o por paciente; paquetes piloto con descuento; posible tarifa añadida por integración y soporte. Costos: desarrollo backend, hosting seguro, integraciones, licencias de video, soporte IoT.</td>
    <td>Venta de hardware y licencias de software; costo alto por equipo hospitalario; mantenimiento y soporte.</td>
    <td>Venta del dispositivo + suscripción a la plataforma/datos; coste medio (dispositivo + servicio).</td>
    <td>Alto coste único por dispositivo + coste quirúrgico e implante; seguimiento y mantenimiento clínico.</td>
  </tr>
<td>Canales de distribución (Web y/o Móvil)</td>
    <td>Web + App móvil (iOS/Android); ventas directas B2B (equipos clínicos/aseguradoras); integraciones API con sistemas hospitalarios; portales para pacientes y profesionales.</td>
    <td>Principalmente reposicionamiento en hospitales (venta directa y distribuidores); software para estaciones clínicas (desktop).</td>
    <td>Web para gestión y móvil para pacientes; venta online para consumidores y a través de centros de investigación.</td>
    <td>Soporte hospitalario especializado — implante y seguimiento en centros referencia; plataforma web para seguimiento.</td>
<tr>
    <td rowspan="4">Análisis SWOT</td>
    <td>Fortalezas</td>
    <td>Solución integral que combina gestión clínica (agenda, teleconsulta), monitorización IoT, alertas y análisis IA; enfoque en coordinación y respuesta rápida (geolocalización con permiso).</td>
    <td>Rápida capacidad diagnóstica en entorno crítico; solución probada para emergencias hospitalarias.</td>
    <td>Sensores validados para investigación; aceptación entre académicos y pacientes; diseño cómodo para uso ambulatorio.</td>
    <td>Terapia demostrada para epilepsia resistente; eficacia clínica documentada; seguimiento especializado.</td>
  </tr>
  <tr>
  <td>Debilidades</td>
    <td>Necesidad de validación clínica y adopción por profesionales; dependencia de integración con hardware de terceros; riesgo de falsas alarmas de IA; requisitos regulatorios.</td>
    <td>Enfoque limitado al hospital (no para monitoreo domiciliario ni teleconsulta); alto coste de implementación.</td>
    <td>Menor foco en gestión clínica (agenda/teleconsulta); posible limitación en la integración de flujo clínico hospitalario.</td>
    <td>Muy invasivo y caro; limitada población objetivo; altos requisitos regulatorios y quirúrgicos.</td>
    </tr>
  <tr>
<td>Oportunidades</td>
    <td>Alianzas con fabricantes de wearables y hospitales; mercado de telemedicina en crecimiento; convenios con aseguradoras por reducción de costos; ampliar a manejo de Parkinson, caídas y rehabilitación.</td>
    <td>Extender uso en más UCIs y servicios de emergencias; integración con plataformas de triage hospitalario.</td>
    <td>Expandir integraciones con plataformas de telemedicina (ej. AuraNeuro), paquetes para programas de salud pública e investigación a gran escala.</td>
    <td>Ampliar indicaciones terapéuticas, integraciones con plataformas de manejo de epilepsia y ofrecer datos para investigación longitudinal.</td>
</tr>
  <tr>
<td>Amenazas</td>
    <td>Competidores con dispositivos validados que ofrezcan plataforma propia; regulación y barreras legales por geolocalización/datos; entrantes con fuerte financiación..</td>
    <td>Competencia de otros equipos portátiles y soluciones de monitorización avanzada; presión para certificaciones y soporte.</td>
    <td>Competencia de wearables generalistas (Apple, Fitbit) y necesidad de demostrar ventaja clínica; adopción limitada fuera de investigación.</td>
    <td>Nuevas terapias no invasivas o avances en fármacos; costes y barreras regulatorias; alternativas de neuromodulación menos invasivas.</td>
</tr>
</table>

---

### 2.1.2. Estrategias y tácticas frente a competidores

## 2.2. Entrevistas.

### 2.2.1. Diseño de entrevistas.

Muy buenos días/tardes/noches, estamos contentos de que haya aceptado esta entrevista. Somos estudiantes de la carrera de Ingeniería de Software e Informática de la UPC. A nombre del grupo desarrollador de la Plataforma IoT para la Optimización de la Atención Neurológica, queremos conversar con usted sobre las dificultades y necesidades que enfrentan los pacientes con enfermedades neurológicas y los profesionales de la salud que los atienden.  

Nuestro objetivo es conocer su experiencia y su perspectiva, ya que buscamos validar y mejorar nuestro producto. Esta plataforma integra dispositivos IoT que recolectan datos neurológicos en tiempo real (EEG, EMG, actividad motora, calidad del sueño, etc.) con inteligencia artificial para generar reportes, alertas predictivas y facilitar el seguimiento remoto por parte de los médicos. Sus respuestas serán muy valiosas para construir una solución útil, accesible y empática.  

---

### Segmento #1: Pacientes con enfermedades neurológicas crónicas  

**Preguntas complementarias:**  
- ¿Cuál es tu nombre completo?  
- ¿Cuántos años tienes?  
- ¿Dónde resides actualmente?  
- ¿Vives solo o acompañado?  
- ¿Tienes algún diagnóstico neurológico específico?  
- ¿Has recibido tratamiento o seguimiento médico especializado anteriormente?  
- ¿Qué dispositivos tecnológicos usas con mayor frecuencia? 
- ¿Qué navegador web utilizas normalmente? 
- ¿Cuáles son los métodos que utilizas más para autenticarte o logearte en plataformas?  

**Preguntas principales:** *Obtener información sobre el impacto de la enfermedad, necesidades, expectativas y aceptación de nuevas tecnologías*  
- ¿Cómo ha impactado tu condición en tu vida diaria o en la de tus familiares?  
- ¿Qué dificultades enfrentas actualmente para llevar un control de tu enfermedad?  
- ¿Qué tan útil consideras que sería contar con un sistema que envíe alertas tempranas sobre crisis o anomalías?  
- ¿Qué información te gustaría poder consultar en una aplicación?  
- ¿Qué tan dispuesto estarías a usar dispositivos IoT para mejorar tu seguimiento médico?  
- ¿Cuáles serían tus principales preocupaciones respecto al uso de esta tecnología?  

 
### Segmento #2: Psicólogos clínicos / Neuropsicólogos  

**Preguntas complementarias:**  
- ¿Cuál es su nombre completo?  
- ¿Cuántos años tiene?  
- ¿Dónde ejerce actualmente su profesión? (clínica, hospital, consultorio privado, universidad, etc.)  
- ¿Cuántos años de experiencia tiene en el área de neurología / salud mental?  
- ¿Cuál es su especialidad o campo principal de trabajo? (neurología, neuropsicología, psicología clínica, terapia de rehabilitación, etc.)  
- ¿Con qué frecuencia atiende a pacientes con enfermedades neurológicas crónicas?  
- ¿Qué dispositivos tecnológicos utiliza con mayor frecuencia en su práctica profesional? (ejemplo: laptop, tablet, smartphone, dispositivos médicos digitales)  
- ¿Qué software o plataformas médicas emplea habitualmente? (ejemplo: historias clínicas electrónicas, Epic, Cerner, otros)  
- ¿Qué navegador web utiliza normalmente para su trabajo? (ejemplo: Chrome, Safari, Edge, Opera)  
- ¿Cuáles son los métodos que utiliza más para autenticarse en sistemas o plataformas profesionales? (ejemplo: correo institucional, Gmail, SMS, autenticación en dos pasos, otros)  

**Preguntas principales (Segmento 2 – Profesionales de la salud):**  
- ¿Cómo realiza actualmente el seguimiento de sus pacientes con epilepsia u otras condiciones neurológicas?  
- ¿Qué tan útil considera contar con una plataforma que integre registros de crisis, calidad de sueño y datos biométricos en tiempo real?  
- ¿Qué marcas o sistemas le generan más confianza para trabajar con este tipo de soluciones?  
- ¿Le sería útil acceder a los registros de sus pacientes desde una aplicación web conectada a la nube?  
- ¿Qué comunidades científicas sigue para mantenerse actualizado en este tema?  
- ¿Cómo cree que estas herramientas digitales impactarían en el sistema de salud en general?  
- ¿Cómo visualiza el futuro de la neurología con IoT y plataformas digitales integradas?  

### Segmento #3: Proveedores IoT

**Preguntas complementarias:**  
- ¿Cuál es el nombre de su empresa o marca?  
- ¿Cuál es su nombre completo y cargo dentro de la empresa?  
- ¿Cuántos años de experiencia tiene su empresa en el desarrollo de dispositivos IoT para el sector salud?  
- ¿Qué tipo de dispositivos IoT produce o distribuye actualmente? (ejemplo: bandas EEG, wearables, relojes inteligentes, sensores implantables, otros)  
- ¿En qué mercados o regiones tienen mayor presencia?  
- ¿Cuáles son los principales clientes a los que venden sus soluciones? (hospitales, clínicas, investigadores, aseguradoras, pacientes directamente)  
- ¿Qué dispositivos tecnológicos utilizan con mayor frecuencia en su operación diaria? (ejemplo: servidores, plataformas cloud, aplicaciones de monitoreo)  
- ¿Qué software o plataformas emplean para la gestión y seguridad de datos recolectados por sus dispositivos?  
- ¿Qué navegador web utilizan normalmente para el trabajo administrativo o de integración de plataformas?  
- ¿Cuáles son los métodos más utilizados para autenticar usuarios en sus dispositivos o plataformas? (ejemplo: correo institucional, Gmail, SMS, autenticación en dos pasos, biometría)  

**Preguntas principales:**  
- ¿Cómo desarrollan actualmente sus dispositivos IoT aplicados a la salud neurológica y cuáles son sus principales funcionalidades?  
- ¿Qué tan capacitado considera que está su equipo en la integración de dispositivos IoT con plataformas digitales de salud, como historias clínicas electrónicas o dashboards médicos?  
- ¿Qué marcas, certificaciones o estándares internacionales considera fundamentales para que los profesionales de la salud confíen en sus dispositivos? 
- ¿Le sería útil contar con alianzas estratégicas que permitan acceder a los datos de sus dispositivos desde aplicaciones web o plataformas en la nube utilizadas por médicos y hospitales?  
- ¿En qué comunidades profesionales o foros online participa su empresa para mantenerse actualizada sobre tendencias y regulaciones de IoT en el sector salud?  
- ¿Cómo cree que la adopción de dispositivos IoT impactará en hospitales, clínicas y aseguradoras que atienden a pacientes neurológicos?  
- ¿Cómo visualiza el futuro de los dispositivos IoT aplicados a la neurología en los próximos 5 a 10 años?  

---  

**Despedida:** 
Muchas gracias por tu tiempo hoy. Tu opinión y las ideas que compartiste nos ayudarán mucho a mejorar nuestro producto. Apreciamos tu sinceridad y disposición para participar. Si necesitas más información, no dudes en contactarnos. ¡Gracias!

### 2.2.2. Registro de entrevistas.

**Segmento 1**

<table>
  <tr>
    <th colspan="2">Entrevistado N° 1</th>
  </tr>
  <tr>
    <td colspan="2" style="text-align: center;">
      <img src="" width="90%" style="text-align: center;"/>
    </td>
  </tr>
  <tr>
    <td><b>Nombre y Apellido:</b>Cesar Aaron Cornejo</td>
    <td><b>Edad:</b> 21</td>
  </tr>
  <tr>
    <td><b>Residencia:</b> Lima - San Juan de Lurigancho</td>
    <td><b>Sexo:</b> Masculino</td>
  </tr>
  <tr>
    <td><b>Instante de inicio:</b> 0:10</td>
    <td><b>Duración:</b>  4:21 </td>
  </tr>
  <tr>
    <td><b>Link de entrevista:</b> </td>
    <td>https://upcedupe-my.sharepoint.com/:v:/g/personal/u202320574_upc_edu_pe/EZxZ3WlYjT1Cp7yqP_OKdSIBRR0IFKAnrzwQjBEJNXY9YQ?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=j1Yf0B</td>
  </tr>
  <tr>
    <td colspan="2">
      <b>Resumen de entrevista:</b><br>
      - El entrevistado se llama **Cesar Aaron Cornejo**, tiene 21 años, vive en Lima y está diagnosticado con epilepsia.  
      - Su principal dificultad es la **imprevisibilidad de las crisis**, lo que genera ansiedad en él y preocupación en su familia.  
      - Actualmente lleva un **registro manual** de sus episodios, pero reconoce que es incompleto y poco confiable.  
      - Considera muy útil contar con **alertas tempranas** que detecten anomalías en tiempo real, para actuar con mayor seguridad.  
      - Le gustaría consultar en una app móvil registros de crisis, calidad del sueño y factores desencadenantes, con **gráficos y estadísticas claras**.  
      - Tiene **confianza en wearables** como Garmin y Fitbit, y aceptaría sensores implantables si son seguros y certificados.  
      - Valora que su neuróloga pueda **acceder a sus datos desde una plataforma web** conectada a la historia clínica.  
      - Ha participado en **comunidades online** de pacientes, lo que le ha dado apoyo emocional.  
      - Cree que estas herramientas digitales le darían **independencia, seguridad y tranquilidad familiar**.  
    </td>
  </tr>
</table>

<table style="width: 100%">
  <tr>
    <th colspan="2">Entrevistado N° 2</th>
  </tr>
  <tr>
    <td colspan="2" style="text-align: center;">
      <img src="" width="90%" style="text-align: center;"/>
    </td>
  </tr>
  <tr>
    <td><b>Nombre y Apellido:</b> Xin Yu Shi Lin</td>
    <td><b>Edad:</b> 25</td>
  </tr>
  <tr>
    <td><b>Residencia:</b> Lima - Perú</td>
    <td><b>Sexo:</b> Maculino</td>
  </tr>
  <tr>
    <td><b>Instante de inicio:</b> 0:05</td>
    <td><b>Duración:</b> 4:22</td>
  </tr>
  <tr>
    <td><b>Link de entrevista:</b> </td><
    <td>https://upcedupe-my.sharepoint.com/:v:/g/personal/u202320442_upc_edu_pe/EVgqZffZGQtFmtniG8D9sCMBK5K39T_bMbQSLhM_WlAlsg?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=h8BhtU</td>
  </tr>
  <tr>
    <td colspan="2">
      <b>Resumen de entrevista:</b><br>
      - El entrevistado se llama Xin Yu Shi Lin, tiene 25 años, vive en Lima y está diagnosticado con epilepsia.  
      - Su mayor preocupación es sufrir una crisis en el trabajo y no poder avisar a tiempo.  
      - Actualmente lleva un control incompleto, anotando de manera poco confiable o recordando de memoria.  
      - Considera muy útil contar con alertas tempranas que anticipen crisis y den seguridad a su familia.  
      - Le gustaría usar una app móvil con registros claros, gráficos de evolución y recordatorios de medicación.  
      - Está dispuesto a usar dispositivos IoT como relojes inteligentes (ej. Fitbit Ionic), siempre que sean seguros.  
      - Sus principales preocupaciones son fallas técnicas y la protección de datos personales.  
      - Participa en comunidades de apoyo como la Asociación Peruana de Epilepsia, lo que le ha dado orientación y acompañamiento.  
      - Sus habilidades digitales son básicas en smartphones y medias en laptops, con uso frecuente de WhatsApp, Gmail y SMS. 
    </td>
  </tr>
</table>

<table style="width: 100%">
  <tr>
    <th colspan="2">Entrevistado N° 3</th>
  </tr>
  <tr>
    <td colspan="2" style="text-align: center;">
      <img src="" width="90%" style="text-align: center;"/>
    </td>
  </tr>
  <tr>
    <td><b>Nombre y Apellido:</b> Eduardo Gabriel Díaz Veliz</td>
    <td><b>Edad:</b> 27</td>
  </tr>
  <tr>
    <td><b>Profesión:</b>Ingeniero de telecomunicaciones – Desarrollador de soluciones IoT para salud</td>
    <td><b>Sexo:</b> Masculino</td>
  </tr>
  <tr>
    <td><b>Instante de inicio:</b> 0:10</td>
    <td><b>Duración:</b> 4:47</td>
  </tr>
  <tr>
    <td><b>Link de entrevista:</b> ...</td>
    <td>https://upcedupe-my.sharepoint.com/:v:/g/personal/u202320574_upc_edu_pe/EYkNwKwupDNBubgFbxYToRcBjpdK5VuueGVGPPJ4TGq2NA?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=eZbHLJ</td>
  </tr>
  <tr>
    <td colspan="2">
      <b>Resumen de entrevista:</b><br>
      - El entrevistado es **Eduardo Gabriel Díaz Veliz**, ingeniero de telecomunicaciones de 27 años.  
- Se especializa en **infraestructura IoT aplicada a la salud neurológica**.  
- Ha trabajado con **pulseras biométricas y EEG portátiles**.  
- Identifica como retos la **conectividad deficiente en provincias** y la **falta de estandarización** de dispositivos.  
- Confía en **Empatica, NeuroSky** y **Fitbit Health Solutions**.  
- Domina **LoRaWAN, 4G/5G, Wi-Fi industrial, Azure IoT, AWS, Python y Grafana**.  
- Su **frustración** es la falta de presupuesto y personal capacitado para escalar pilotos en hospitales.  
- Su **objetivo** es implementar soluciones IoT accesibles en hospitales públicos sin comprometer la seguridad y calidad de los datos.  

    </td>
  </tr>
</table>

**Segmento 2**

<table style="width: 100%">
  <tr>
    <th colspan="2">Entrevistado N° 1</th>
  </tr>
  <tr>
    <td colspan="2" style="text-align: center;">
      <img src="" width="90%" style="text-align: center;"/>
    </td>
  </tr>
  <tr>
    <td><b>Nombre y Apellido:</b> Karen Guadalupe Villanueva Castillo</td>
    <td><b>Edad:</b> 27</td>
  </tr>
  <tr>
    <td><b>Profesión:</b> Neuróloga especialista </td>
    <td><b>Sexo:</b> Femenino</td>
  </tr>
  <tr>
    <td><b>Instante de inicio:</b> 0:04</td>
    <td><b>Duración:</b> 6:58</td>
  </tr>
  <tr>
    <td><b>Link de entrevista:</b> </td>
    <td>https://upcedupe-my.sharepoint.com/:v:/g/personal/u202320574_upc_edu_pe/EQiEyBrJx-JGoHK_l4x45sYBAWGLVSJzu40JYMV2arNWBA?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=dL6y9t</td>
  </tr>
  <tr>
    <td colspan="2">
      <b>Resumen de entrevista:</b><br>
      - La entrevistada es **Karen Guadalupe Villanueva Castillo**, neuróloga especialista de 27 años.  
      - Señala que actualmente depende de registros manuales de los pacientes, lo que dificulta diagnósticos precisos.  
      - Considera muy valiosa una plataforma que integre **datos de crisis, sueño y biometría en tiempo real**.  
      - Confía en software clínico como **Epic** y **Cerner**, y en dispositivos de monitoreo de **Medtronic** y **Empatica**.  
      - Valora el acceso remoto a datos de pacientes mediante aplicaciones web en la nube.  
      - Forma parte de comunidades científicas como la **ILAE** y la **AAN**.  
      - Opina que estas herramientas reducirán costos hospitalarios, mejorarán la prevención y harán más eficiente al sistema de salud.  
      - Visualiza la neurología del futuro como **preventiva, personalizada y soportada por IoT**.
    </td>
  </tr>
</table>

<table style="width: 100%">
  <tr>
    <th colspan="2">Entrevistado N° 2</th>
  </tr>
  <tr>
    <td colspan="2" style="text-align: center;">
      <img src="" width="90%" style="text-align: center;"/>
    </td>
  </tr>
  <tr>
    <td><b>Nombre y Apellido:</b> Nicol Buendía</td>
    <td><b>Edad:</b> 26</td>
  </tr>
  <tr>
    <td><b>Profesión:</b> Terapeuta en rehabilitación neurológica</td>
    <td><b>Sexo:</b> Femenino</td>
  </tr>
  <tr>
    <td><b>Instante de inicio:</b> 0:33</td>
    <td><b>Duración:</b> 7:50</td>
  </tr>
  <tr>
    <td><b>Link de entrevista:</b> </td><
    <td>https://upcedupe-my.sharepoint.com/:v:/g/personal/u202320574_upc_edu_pe/ERy66J4mXqlEjW4IcsmtsVwBdu-vmnMGzi9ZldbU61cQnQ?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=YYQLlB</td>
  </tr>
  <tr>
    <td colspan="2">
      <b>Resumen de entrevista:</b><br>
      <td>- La entrevistada es **Nicol Buendía**, terapeuta en rehabilitación neurológica de 26 años.  
      - Señala que el seguimiento actual depende de observaciones presenciales y reportes familiares.  
      - Considera muy útil una plataforma que integre **actividad motora, crisis y sueño en tiempo real**.  
      - Confía en plataformas como **Rehametrics** y **MindMotion**, y en dispositivos de **Empatica** y **NeuroPace**.  
      - Destaca la importancia de un **dashboard en la nube** para colaboración con neurólogos y familiares.  
      - Forma parte de comunidades como la **WFNR** y la **Sociedad Española de Neurorrehabilitación**.  
      - Opina que estas herramientas reducirían hospitalizaciones y facilitarían terapias en casa.  
      - Visualiza la rehabilitación del futuro como **personalizada, digital e integrada con IoT**. </td>
    </td>
  </tr>
</table>

<table style="width: 100%">
  <tr>
    <th colspan="2">Entrevistado N° 1</th>
  </tr>
  <tr>
    <td colspan="2" style="text-align: center;">
      <img src="" width="90%" style="text-align: center;"/>
    </td>
  </tr>
  <tr>
    <td><b>Nombre y Apellido:</b> Carlos Paredes</td>
    <td><b>Edad:</b> ...</td>
  </tr>
  <tr>
    <td><b>Profesión:</b> Ingeniero electrónico – Proveedor de soluciones IoT</td>
    <td><b>Sexo:</b> Masculino</td>
  </tr>
  <tr>
    <td><b>Instante de inicio:</b> 0:09</td>
    <td><b>Duración:</b> 13:09</td>
  </tr>
  <tr>
    <td><b>Link de entrevista:</b> ...</td>
    <td>https://upcedupe-my.sharepoint.com/:v:/g/personal/u202320574_upc_edu_pe/EabaC7sEU_9GrDDU69Xv9owBK49d_g1TTHwcW7RoBKtmZg?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=CKbOGC</td>
  </tr>
  <tr>
    <td colspan="2">
      <b>Resumen de entrevista:</b><br>
      - El entrevistado es **Carlos Paredes**, ingeniero electrónico de 32 años, proveedor de soluciones IoT.  
      - Explica que desarrolla proyectos con **sensores biométricos, wearables y EEG portátiles**.  
      - Señala como reto principal la **interoperabilidad** de datos y la **seguridad** bajo normas como HIPAA.  
      - Confía en dispositivos de **Empatica, Medtronic y NeuroSky**.  
      - Domina **protocolos IoT (MQTT, BLE, Wi-Fi seguro)** y plataformas como **AWS IoT, Grafana y Power BI**.  
      - Considera que una alianza con startups como **Mithycore** puede agilizar pilotos y soluciones personalizadas.  
      - Menciona como **frustración** la resistencia institucional por falta de presupuesto o desconocimiento.  
      - Su **objetivo** es integrar IoT con historias clínicas electrónicas y telemedicina para dar soporte en tiempo real a médicos y pacientes.  
    </td>
  </tr>
</table>

### 2.2.3. Análisis de entrevistas.

## 2.3. Needfinding.  

### 2.3.1. User Personas.  

En esta parte del informe presentamos a los User Personas construidos a partir de entrevistas y análisis de los segmentos objetivo de Mythicore. Estas representaciones ficticias, pero basadas en datos reales, nos permiten comprender mejor cómo piensan, qué esperan y qué problemas enfrentan nuestros usuarios. Con esta información, el equipo puede diseñar una solución alineada a necesidades auténticas y no solo a supuestos.

User Persona – Segmento 1: Paciente(epilepsia crónica):  

![User Persona - Paciente](./imagesChapter02/userPersona/userperson-segmentopaciente.png)

User Persona - Segmento 2: Profesionales de la salud(neurólogos):

![User Persona - Neuropsicólogo](./imagesChapter02/userPersona/userperson-segmentoprofesional.png)

User Persona - Segmento 3: Proveedores IoT:

![User Persona - Neuropsicólogo](./imagesChapter02/userPersona/userperson-segmentoproovedor.png)


### 2.3.2. User Task Matrix.

La siguiente matriz relaciona a los roles de usuario de la plataforma **Mythicore** con las principales tareas que realizan.  
Cada tarea está asociada a una **prioridad** (Alta, Media, Baja) y una **frecuencia de uso** (Alta, Media, Baja).  
Esto permite identificar qué funciones son críticas para cada segmento objetivo.

| Rol / Usuario | Tarea | Descripción | Prioridad | Frecuencia |
|---------------|-------|-------------|-----------|------------|
| **Paciente** | Usar dispositivo IoT | El paciente utiliza los sensores para registrar datos neurológicos. | Alta | Alta |
| **Paciente** | Revisar reportes de adherencia | El paciente consulta sus métricas de uso y evolución. | Media | Media |
| **Paciente** | Recibir recordatorios | El paciente recibe notificaciones para mantener la adherencia al tratamiento. | Alta | Alta |
| **Paciente** | Participar en teleconsulta | El paciente asiste a consultas virtuales con su médico desde la plataforma. | Alta | Media |
| **Paciente** | Consultar ensayos clínicos | El paciente revisa información sobre estudios relevantes a su condición. | Media | Baja |
| **Médico** | Visualizar datos IoT | El médico consulta las señales neurológicas capturadas en tiempo real. | Alta | Alta |
| **Médico** | Recibir alertas predictivas | El médico recibe notificaciones de crisis o riesgos detectados por la IA. | Alta | Alta |
| **Médico** | Consultar dashboard de riesgos | El médico revisa el estado de riesgo de todos sus pacientes. | Alta | Media |
| **Médico** | Atender teleconsultas | El médico realiza consultas virtuales con pacientes integrando datos IoT. | Alta | Media |
| **Médico** | Exportar reportes a EHR | El médico genera exportaciones en formato FHIR para integrarlas al sistema clínico. | Media | Baja |
| **Visitante (Landing Page)** | Revisar información general | El visitante accede al sitio para conocer misión, visión y beneficios de la plataforma. | Alta | Alta |
| **Visitante (Landing Page)** | Explorar servicios | El visitante consulta la sección de telemedicina y farmacia/dispositivos. | Media | Media |
| **Visitante (Landing Page)** | Revisar sección “Quiénes somos / Qué hacemos” | El visitante comprende la identidad y propuesta de valor del proyecto. | Media | Baja |
| **Visitante (Landing Page)** | Usar formulario de contacto | El visitante envía sus datos para recibir más información. | Alta | Media |
| **Developer (API)** | Registrar pacientes vía API | El developer usa el endpoint para crear pacientes en la plataforma. | Alta | Alta |
| **Developer (API)** | Consultar datos de monitoreo | El developer obtiene información neurológica desde la API en formato JSON. | Alta | Alta |
| **Developer (API)** | Manejar errores de la API | El developer recibe mensajes de error descriptivos en caso de requests inválidos. | Alta | Media |

### 2.3.3. User Journey Mapping.  

User Journey Mapping – Segmento 1: Paciente(epilepsia crónica):

![User Journey Mapping - Paciente](./imagesChapter02/userJourney/Segmento1JM.png)

User Journey Mapping - Segmento 2: Profesionales de la salud(neurólogos):

![User Journey Mapping - Neuropsicólogo](./imagesChapter02/userJourney/Segmento2JM.png)

User Journey Mappinga - Segmento 3: Proveedores IoT:

![User Journey Mapping - Proveedores](./imagesChapter02/userJourney/Segmento3JM.png)


### 2.3.4. Empathy Mapping.  

PACIENTES:

Empathy Mapping – Segmento 1: Paciente(epilepsia crónica):

![Empathy Mapping - Paciente](./imagesChapter02/empathyMapping/Segmento1EM.png)

Empathy Mapping - Segmento 2: Profesionales de la salud(neurólogos):

![Empathy Mapping - Neuropsicólogo](./imagesChapter02/empathyMapping/Segmento2EM.png)

Empathy Mapping - Segmento 3: Proveedores IoT:

![Empathy Mapping - Proveedores](./imagesChapter02/empathyMapping/Segmento3EM.png)

## 2.4. Big Picture EventStorming.  

El Big Picture Event Storming es una técnica colaborativa que nos permitió visualizar el dominio completo de nuestra solución, identificando actores, eventos clave, problemas, dudas, sistemas externos y oportunidades. A través de esta dinámica, el equipo logró comprender de manera compartida el flujo de procesos en la atención neurológica digital y cómo nuestra plataforma Mythicore puede integrarse para resolver brechas críticas.  

**Big Picture Event Storming - Leyenda de Colores**    
![BigPicture](./imagesChapter02/bigPicture/bigpicture1.png) 

**Big Picture Event Storming - Mapa General**   
![BigPicture](./imagesChapter02/bigPicture/bigpicture2.png) 

## 2.5. Ubiquitous Language.  

Este glosario define los términos clave que usamos en el proyecto para mantener un **lenguaje común** entre el equipo de desarrollo, los médicos especialistas y los demás stakeholders.    

| Term (English) | Definición (Español) |
|----------------|-----------------------|
| **Patient (Paciente)** | Persona diagnosticada con una enfermedad neurológica crónica, como epilepsia o Parkinson, que utiliza la plataforma para registrar, monitorear y compartir información de su condición. |
| **Neurologist (Neurólogo/a)** | Médico especialista en el diagnóstico y tratamiento de enfermedades neurológicas, encargado de revisar la información registrada por los pacientes y ajustar tratamientos. |
| **Caregiver (Cuidador/Familiar)** | Persona cercana al paciente que brinda apoyo en el manejo diario de la enfermedad y puede recibir alertas tempranas en situaciones de crisis. |
| **Seizure (Crisis epiléptica)** | Episodio súbito generado por actividad eléctrica anormal en el cerebro, caracterizado por convulsiones, pérdida de conciencia u otros síntomas neurológicos. |
| **Crisis log (Registro de crisis)** | Historial digital donde el paciente documenta la fecha, hora, duración y características de cada crisis. |
| **Biometric data (Datos biométricos)** | Señales fisiológicas obtenidas mediante dispositivos IoT (ej. ritmo cardíaco, actividad cerebral, calidad del sueño) que permiten un seguimiento objetivo de la salud del paciente. |
| **Wearable device (Dispositivo vestible/IoT)** | Tecnología portátil (reloj inteligente, sensor EEG, pulsera médica) que mide y transmite datos biométricos del paciente. |
| **EEG – Electroencephalogram (Electroencefalograma)** | Examen que registra la actividad eléctrica cerebral a través de sensores en el cuero cabelludo; utilizado para diagnosticar y monitorear epilepsia y otras condiciones neurológicas. |
| **Health Record (Historia clínica electrónica)** | Documento digital que almacena la información médica del paciente, accesible por el neurólogo para evaluar evolución y tratamientos. |
| **Alert (Alerta temprana)** | Notificación automática que advierte al paciente, familiares o médicos sobre una crisis inminente o anomalía detectada por los sensores. |
| **Medication adherence (Adherencia al tratamiento)** | Grado en el que el paciente sigue correctamente la toma de medicamentos prescritos por el neurólogo. |
| **Sleep quality (Calidad de sueño)** | Indicador de descanso del paciente, medido por dispositivos IoT, que influye directamente en la frecuencia de crisis. |
| **Dashboard (Panel de control clínico)** | Interfaz visual que muestra estadísticas, gráficos y tendencias de la evolución del paciente, accesible para médicos y pacientes. |
| **Scientific community (Comunidad científica)** | Organismos y grupos de investigación internacionales (ej. ILAE, AAN) que validan y difunden prácticas y tecnologías para el tratamiento de enfermedades neurológicas. |
| **Support group (Grupo de apoyo)** | Comunidad de pacientes que comparte experiencias, consejos y acompañamiento sobre el manejo de su condición neurológica. |
| **Data privacy (Privacidad de datos)** | Principio que garantiza la protección de la información médica y biométrica del paciente frente a accesos no autorizados. |

---
