## Capítulo I: Introducción  

### 1.1.1. Descripción de la Startup

**Startup:** Mithycore  
**Producto:** AuraNeuro

**Elevator pitch:**  
AuraNeuro transforma datos obtenidos de dispositivos IoT y wearables en información clínica útil para pacientes neurológicos y sus neurólogos. Permite registrar crisis, hábitos y eventos relevantes, analizando tendencias que facilitan decisiones médicas con foco en adherencia y bienestar.

**Misión**  
Conectar a pacientes neurológicos, profesionales de la salud y dispositivos IoT a través de una plataforma accesible y segura que convierta los datos biométricos en decisiones clínicas útiles, mejorando la adherencia terapéutica y la calidad de vida.

**Visión**  
Ser la referencia latinoamericana en soluciones digitales de neuro-salud basadas en datos, integrando IoT, análisis inteligente y diseño inclusivo para transformar la relación entre paciente y médico en un proceso continuo y colaborativo.

### Objetivo general

Desarrollar una **plataforma digital de monitoreo neurológico continuo** que integre **dispositivos IoT** y **analítica de datos** para transformar los registros biométricos en información clínica útil, fortaleciendo la comunicación entre paciente y especialista y mejorando la **adherencia terapéutica** en enfermedades neurológicas crónicas.

### Objetivos específicos

- **OE1:** Implementar un sistema de registro y visualización de datos neurológicos (crisis, sueño, adherencia) accesible para pacientes y cuidadores.  
- **OE2:** Desarrollar un **panel clínico** para neurólogos que consolide datos en tiempo real y facilite decisiones médicas basadas en evidencia.  
- **OE3:** Integrar sensores IoT y protocolos seguros de comunicación (MQTT/HTTPS) que garanticen la transmisión confiable de información biométrica.  
- **OE4:** Asegurar la **interoperabilidad con sistemas clínicos** bajo estándares internacionales (**HL7–FHIR**) y almacenamiento cifrado.  
- **OE5:** Validar la adopción de la plataforma mediante **pruebas piloto** con usuarios reales, midiendo adherencia, satisfacción y reducción de reingresos hospitalarios.

**Propuesta de valor por actor**
- **Pacientes y cuidadores:** registro digital de crisis y síntomas, recordatorios de medicación y visualización de avances en su tratamiento.  
- **Profesionales de salud:** panel web con métricas de evolución (tendencias de sueño, frecuencia de crisis, adherencia a tratamientos) para optimizar decisiones clínicas.  
- **Proveedores IoT:** integración mediante API para envío seguro de señales biométricas (EEG, PPG, HRV) con documentación y entorno de pruebas.

**Diferenciadores**
- Enfoque en **outcomes de salud** (reducción de episodios, mejora en adherencia terapéutica) más que en funcionalidades.  
- Diseño centrado en la accesibilidad y facilidad de uso para pacientes con limitaciones motoras o cognitivas.  
- Integración transparente con dispositivos IoT, priorizando seguridad y privacidad de los datos.

**Privacidad y ética**  
AuraNeuro maneja información biomédica con criterios éticos y de privacidad basados en HIPAA e ISO 27001. Todos los registros son tratados con consentimiento informado y cifrado en tránsito y almacenamiento. 

#### 1.1.2. Perfiles de integrantes del equipo  

| Foto | Nombre y Código | Rol | Descripción |
|------|-----------------|-----|-------------|
| ![Stanley](./imagesTeam/stanley.jpg) | **Stanley Jeremy Gutierrez Tume (U202118152)** | **Product Lead & Scrum Facilitator** | Estudiante de Ingeniería de Software y **líder general del equipo Mithycore**. Facilita las ceremonias Scrum, gestiona el roadmap del proyecto y coordina la integración de entregables. Lidera la definición de **GitFlow**, **Convencional Commits** y **SemVer**. Supervisa la documentación del Capítulo I y la creación del repositorio inicial. <br>**Evidencia TB1:** coordinación de tareas y despliegue base de la Landing Page. |
| ![Juan José](./imagesTeam/juan.jpg) | **Juan José Meza Huanacune (U202320574)** | **Backend Engineer & API Owner (.NET Core)** | Responsable del diseño e implementación de **servicios web en ASP.NET Core**, aplicando principios de arquitectura limpia, seguridad y documentación con **Swagger/OpenAPI**. Lidera la estructura técnica del backend y colabora con la integración IoT. <br>**Evidencia TB1:** diseño de la estructura inicial del backend, lineamientos de versionado y configuración del repositorio técnico. |
| ![Eduardo](./imagesTeam/eduardo.jpg) | **Eduardo Fabián Chacaliaza Minaya (U202324129)** | **Frontend & UX/UI Engineer (PrimeVue / Figma)** | Dirige el diseño de la interfaz y la experiencia de usuario. Responsable de la creación del **design system**, la accesibilidad (**a11y**) y la internacionalización (**i18n**, en_US/es_419). Utiliza **Figma** y **PrimeVue** para garantizar consistencia visual. <br>**Evidencia TB1:** diseño inicial del Landing Page y lineamientos visuales aplicados al prototipo. |
| ![Fabricio](./imagesTeam/fabricio.jpg) | **Fabricio Fabián Quispe Barzola (U202320442)** | **Data & IoT Integration Engineer** | Especialista en procesamiento de datos y conexión de sensores IoT. Lidera la construcción de artefactos de investigación (**5W2H**, benchmark, entrevistas y análisis). Colabora en la integración entre hardware y servicios cloud. <br>**Evidencia TB1:** diagnóstico de la problemática inicial y documentación del entorno IoT con fuentes referenciadas. |
| ![Jhimy](./imagesTeam/JhimyRomeroMeza.png) | **Romero Meza Jhimy Pool (U202321510)** | **Frontend Developer & Landing Owner (Vue + PrimeVue)** | Encargado de la maquetación responsive de la **Landing Page** y del frontend principal. Asegura el cumplimiento de buenas prácticas **RWD**, optimización de rendimiento y soporte **i18n**. Implementa los componentes base de **PrimeVue**. <br>**Evidencia TB1:** despliegue funcional de la Landing Page y organización del repositorio de assets. |

**Champions transversales del equipo Mithycore**
- **a11y/i18n:** Eduardo & Jhimy  
- **Seguridad y privacidad:** Stanley & Juan José  
- **Gestión de artefactos Lean UX:** Fabricio (UXPressia) & Eduardo (Figma)

## 1.2. Solution Profile  

### 1.2.1. Antecedentes y problemática  

Las enfermedades neurológicas como la epilepsia, el Parkinson y el Alzheimer representan un reto creciente para los sistemas de salud.  
En América Latina, la atención continúa siendo fragmentada: los diagnósticos suelen realizarse en fases avanzadas y los pacientes carecen de seguimiento continuo.  
Aunque la OMS estima más de **50 millones de personas con epilepsia** a nivel mundial (OMS, 2020), cerca del **70 % podría controlar sus crisis** con detección temprana y adherencia adecuada.  

Actualmente, los pacientes dependen de anotaciones manuales o consultas esporádicas. Los especialistas reciben información incompleta, y los dispositivos de monitoreo existentes son **costosos o poco accesibles**, lo que genera **falta de continuidad en la atención** y **decisiones clínicas basadas en datos insuficientes**.

**AuraNeuro**, iniciativa de la startup **Mithycore**, surge para **facilitar el seguimiento neurológico de manera continua, accesible y segura**, aprovechando el potencial de los dispositivos IoT y la analítica avanzada de datos.  
A continuación, se presenta el análisis **5W+2H** que sustenta la problemática identificada.

---

#### Análisis 5W + 2H  

| **Pregunta** | **Descripción (AuraNeuro – Mithycore)** |
|---------------|------------------------------------------|
| **What (Qué)** | En la atención neurológica ambulatoria **no existe un registro continuo y centralizado** de crisis, sueño, adherencia y eventos relevantes. La información llega **tardía, fragmentada y subjetiva**, lo que dificulta **ajustar tratamientos de forma oportuna**. |
| **When (Cuándo)** | El problema se presenta **entre consultas médicas** (semanas o meses), durante **episodios críticos** (crisis epilépticas o alteraciones cognitivas) y en **rutinas diarias** donde se requieren datos continuos para observar tendencias. |
| **Where (Dónde)** | Ocurre en el **hogar del paciente** (uso de wearables o sensores), en **consultorios, hospitales y teleconsultas**, principalmente en **Latinoamérica urbana**, donde la conectividad y la digitalización son parciales. |
| **Who (Quién)** | **Pacientes adultos (20–65 años)** con diagnóstico o sospecha de epilepsia (segmento inicial) y, en fases posteriores, Parkinson o deterioro cognitivo. Involucra también a **neurólogos, terapeutas, cuidadores, instituciones de salud** y **proveedores IoT** (EEG, EMG, PPG, HRV). |
| **Why (Por qué)** | 1) **Dependencia de registros subjetivos** y poco confiables. <br>2) **Baja interoperabilidad** entre dispositivos IoT y sistemas clínicos (**EHR/HL7-FHIR**). <br>3) **Ausencia de analítica en tiempo real** para emitir alertas útiles. <br>4) **Limitaciones de acceso y usabilidad** para pacientes con discapacidad motora o cognitiva. |
| **How (Cómo)** | **AuraNeuro** propone: <br>• Una **aplicación móvil** para registrar síntomas y recibir alertas. <br>• **Sensores IoT** que transmiten datos biométricos (EEG, HRV, sueño) hacia la nube. <br>• Un **dashboard clínico** con métricas y exportación a EHR (**FHIR/PDF**). <br>• Seguridad basada en **cifrado en tránsito y almacenamiento**, control de acceso y **consentimiento informado**. |
| **How much (Cuánto)** | **Metas del piloto (6–9 meses):** <br>• ≥ **4 registros por semana** por usuario activo. <br>• Reducción ≥ **15 %** en reingresos hospitalarios. <br>• ≥ **60 %** de consultas con historial digital exportado. <br>• **Latencia P95 < 500 ms** y **> 99 %** de mensajes IoT sin pérdida. <br>• ≥ **2 integraciones IoT** y **1 FHIR** activas. |

---

#### Declaración de Problema de Negocio (Box 1 – Lean UX Canvas)

> **AuraNeuro**, producto de **Mithycore**, busca resolver la brecha en el seguimiento neurológico ambulatorio.  
> Los pacientes carecen de una plataforma accesible para registrar sus crisis y hábitos, y los médicos no pueden analizar datos de forma integrada ni oportuna.  
> Esta situación conduce a **diagnósticos tardíos** y **baja adherencia terapéutica**.  
> **¿Cómo podríamos mejorar la recolección y visualización de datos neurológicos para facilitar decisiones médicas basadas en evidencia**, **medido por una mayor frecuencia de registro y una reducción en hospitalizaciones evitables?**

---

#### Métricas de éxito (Impact → Outcome)

| **Tipo de métrica** | **Indicador** | **Objetivo esperado** |
|----------------------|---------------|------------------------|
| **Impact metric** | Reducción de hospitalizaciones evitables por pacientes neurológicos | Disminuir ≥ 20 % en 6 meses. |
| **Outcome metric** | Frecuencia de registro de crisis y síntomas en la app | ≥ 4 registros por semana por usuario activo. |
| **Outcome metric** | Porcentaje de consultas médicas con datos digitales completos | ≥ 60 % de consultas con historial exportado. |
| **Leading metric** | Número de proveedores IoT integrados (SDK/API) | ≥ 2 integraciones validadas en 3 meses. |

### 1.2.2. Lean UX Process  

> En esta sección aplicamos el **Lean UX Process** según *Lean UX 3rd Edition*, estructurado en los siguientes componentes: **Problem Statements, Assumptions, Hypothesis Statements** y **Lean UX Canvas**.  
> Se utiliza el formato oficial recomendado en el curso y en el libro (*Gothelf & Seiden, 2021*).

---

#### 1.2.2.1. Lean UX Problem Statement  

El **Problem Statement** describe el contexto actual, las limitaciones y la oportunidad que busca resolver la solución digital.  
Se formula respondiendo a los cuatro elementos clave indicados en *Lean UX (3rd Edition)*: **context**, **problem**, **impact**, y **measure of success**.

---

**Lean UX Problem Statement (English):**

> The current state of **neurological health monitoring** depends on **occasional clinical evaluations** and **manual symptom reports**.  
> This leads to **delayed diagnoses**, **fragmented information**, and **low treatment adherence** among patients with neurological disorders.  
> We believe that by providing a **continuous, data-driven monitoring experience** that connects patients and neurologists through IoT devices and analytics, we can **improve diagnostic accuracy and patient engagement**.  
> We’ll know this is true when we observe **a measurable reduction in hospital readmissions**, **an increase in weekly patient activity**, and **greater clinical data completeness**.

---

**Traducción (referencial):**

> El estado actual del **monitoreo neurológico** depende de **evaluaciones clínicas ocasionales** y **reportes manuales de síntomas**.  
> Esto genera **diagnósticos tardíos**, **información fragmentada** y **baja adherencia terapéutica** entre los pacientes con trastornos neurológicos.  
> Creemos que al ofrecer una **experiencia de monitoreo continuo basada en datos**, que conecte a pacientes y neurólogos mediante dispositivos IoT y analítica, podremos **mejorar la precisión diagnóstica y la participación del paciente**.  
> Sabremos que esto es cierto cuando observemos **una reducción medible en reingresos hospitalarios**, **un aumento en la actividad semanal de los usuarios** y **una mayor completitud de datos clínicos**.

---

#### 1.2.2.2. Lean UX Assumptions  

Según *Lean UX (3rd Edition)*, las **assumptions** se agrupan en cuatro tipos:

1. **Business Assumptions** — sobre la viabilidad y objetivos del negocio.  
2. **User Assumptions** — sobre quiénes son los usuarios y qué necesitan.  
3. **Value Assumptions** — sobre el valor que la solución les genera.  
4. **Feature Assumptions** — sobre qué características permitirán entregar ese valor.

---

**Lean UX Assumptions (English):**

**a) Business Assumptions**  
- Healthcare institutions need digital solutions that reduce hospital readmissions and monitoring costs.  
- A subscription-based or SaaS model can be sustainable in the Latin American health sector.  
- Demonstrable clinical improvement (adherence, fewer crises) will drive adoption by doctors and institutions.

**b) User Assumptions**  
- Patients with neurological disorders find it difficult to consistently log symptoms without digital support.  
- Neurologists require continuous and visual data to make informed decisions.  
- Caregivers are motivated to help patients track and share relevant information if the process is simple and reliable.

**c) Value Assumptions**  
- Real-time insights increase trust and engagement among patients and clinicians.  
- Continuous monitoring enables early detection and better adherence to treatment.  
- Data-driven reports save time for medical professionals and reduce uncertainty for patients.

**d) Feature Assumptions**  
- Dashboards with visual trends help neurologists understand patient progress quickly.  
- Notifications and alerts encourage patients to maintain adherence.  
- Easy-to-use logging interfaces promote frequent interaction and data accuracy.

---

**Traducción (referencial):**

**a) Supuestos de Negocio**  
- Las instituciones de salud necesitan soluciones digitales que reduzcan los reingresos hospitalarios y los costos de monitoreo.  
- Un modelo de suscripción o SaaS puede ser sostenible en el sector salud latinoamericano.  
- Las mejoras clínicas demostrables (adherencia, reducción de crisis) impulsarán la adopción por parte de médicos e instituciones.

**b) Supuestos de Usuario**  
- Los pacientes con trastornos neurológicos tienen dificultades para registrar sus síntomas de forma constante sin apoyo digital.  
- Los neurólogos requieren datos continuos y visuales para tomar decisiones informadas.  
- Los cuidadores están motivados a apoyar el seguimiento si el proceso es simple y confiable.

**c) Supuestos de Valor**  
- Las visualizaciones en tiempo real aumentan la confianza y el compromiso entre pacientes y clínicos.  
- El monitoreo continuo permite una detección temprana y una mejor adherencia al tratamiento.  
- Los reportes basados en datos ahorran tiempo a los profesionales de salud y reducen la incertidumbre en los pacientes.

**d) Supuestos de Funcionalidad**  
- Los tableros con tendencias visuales ayudan a los neurólogos a entender rápidamente la evolución del paciente.  
- Las notificaciones y alertas fomentan la adherencia terapéutica.  
- Las interfaces simples promueven la interacción frecuente y la precisión en el registro.

---

#### 1.2.2.3. Lean UX Hypothesis Statements  

Cada hipótesis se formula conforme al patrón estándar del libro:

> **We believe that [this outcome] will be achieved if [these users] attain [this benefit].**  
> We will know this is true when we observe [this measurable result].

---

**Lean UX Hypothesis Statements (English):**

**a) Business Hypothesis**  
> We believe that **hospitals and neurologists** will adopt AuraNeuro if it **reduces patient readmissions and saves monitoring costs**.  
> We’ll know this is true when we see **pilot programs or institutional partnerships** with measurable cost reductions.

**b) User Hypothesis**  
> We believe that **patients with neurological disorders** will use AuraNeuro regularly **if it helps them visualize progress and receive useful alerts**.  
> We’ll know this is true when we see **consistent weekly usage (≥4 sessions)** and **positive feedback on alert relevance**.

**c) Value Hypothesis**  
> We believe that **continuous IoT monitoring and data-driven insights** will lead to **fewer emergency visits and better treatment adherence**.  
> We’ll know this is true when we observe a **decrease in readmission rates (≥15%)** and **increased patient adherence metrics**.

**d) Feature Hypothesis**  
> We believe that **simple symptom logging, alert notifications, and clinician dashboards** will enable **better collaboration and decision-making**.  
> We’ll know this is true when we observe **more complete patient records** and **active clinician dashboard usage**.

---

**Traducción (referencial):**

**a) Hipótesis de Negocio**  
> Creemos que los **hospitales y neurólogos** adoptarán AuraNeuro si **reduce los reingresos hospitalarios y los costos de monitoreo**.  
> Sabremos que esto es cierto cuando veamos **programas piloto o alianzas institucionales** con reducciones de costos medibles.

**b) Hipótesis de Usuario**  
> Creemos que los **pacientes con trastornos neurológicos** usarán AuraNeuro regularmente **si les ayuda a visualizar su progreso y recibir alertas útiles**.  
> Sabremos que esto es cierto cuando observemos **uso semanal constante (≥4 sesiones)** y **retroalimentación positiva sobre la relevancia de las alertas**.

**c) Hipótesis de Valor**  
> Creemos que el **monitoreo IoT continuo y los reportes basados en datos** conducirán a **menos visitas de emergencia y mejor adherencia al tratamiento**.  
> Sabremos que esto es cierto cuando observemos **una disminución en los reingresos (≥15%)** y **mayores métricas de adherencia**.

**d) Hipótesis de Funcionalidad**  
> Creemos que el **registro simple de síntomas, las alertas y el panel clínico** permitirán **una mejor colaboración y toma de decisiones**.  
> Sabremos que esto es cierto cuando veamos **registros de pacientes más completos** y **uso activo del panel por parte de los médicos**.

---

#### 1.2.2.4. Lean UX Canvas – AuraNeuro  

El siguiente cuadro resume los principales componentes del **Lean UX Canvas (v2)** aplicados a AuraNeuro, conforme al formato de *Lean UX 3rd Edition*.

| **Box** | **Component** | **Summary (English)** | **Traducción (Español)** |
|----------|----------------|------------------------|----------------------------|
| **1** | **Business Problem** | Neurological monitoring depends on occasional checkups and manual reports. Existing solutions are expensive and disconnected. | El monitoreo neurológico depende de evaluaciones esporádicas y reportes manuales. Las soluciones actuales son costosas y poco integradas. |
| **2** | **Business Outcomes** | Reduce hospital readmissions and monitoring costs; increase clinical efficiency and patient engagement. | Reducir reingresos y costos; aumentar eficiencia clínica y compromiso del paciente. |
| **3** | **Users & Customers** | Adult patients (20–65) with neurological disorders, neurologists, and caregivers. | Pacientes adultos (20–65), neurólogos y cuidadores. |
| **4** | **User Outcomes & Benefits** | Patients detect anomalies early; doctors access continuous data for informed decisions. | Los pacientes detectan anomalías tempranas; los médicos acceden a datos continuos para decisiones informadas. |
| **5** | **Solutions** | IoT-based sensors connected to an app and clinician dashboard for alerts, trends, and reports. | Sensores IoT conectados a una app y un panel clínico para alertas, tendencias y reportes. |
| **6** | **Assumptions** | Business, User, Value, and Feature assumptions guiding MVP validation. | Supuestos de negocio, usuario, valor y funcionalidad que guían la validación del MVP. |
| **7** | **Hypotheses** | See Section 1.2.2.3 — measurable hypotheses for validation. | Ver sección 1.2.2.3 — hipótesis medibles para validar valor, adopción y efectividad. |
| **8** | **Experiments** | Conduct MVP pilot with 20 patients and 5 doctors over 8 weeks; measure usage frequency, alert accuracy, and satisfaction. | Ejecutar piloto MVP con 20 pacientes y 5 médicos durante 8 semanas; medir frecuencia de uso, precisión de alertas y satisfacción. |

---

**Conclusión:**  
El *Lean UX Process* aplicado a **AuraNeuro** permite conectar las necesidades reales de los usuarios con los objetivos del negocio mediante hipótesis medibles y experimentos iterativos.  
El equipo **Mithycore** usará estos artefactos como guía para las fases de validación y desarrollo incremental.

---

## 1.3. Segmentos Objetivo

El proyecto **AuraNeuro**, desarrollado por **Mithycore**, se centra en tres segmentos principales de usuarios identificados a través de investigación exploratoria y entrevistas iniciales.

---

### 1.3.1. Segmentos Objetivo #1 — Pacientes neurológicos  

- **Perfil:** Adultos de 20 a 65 años con diagnóstico o riesgo de epilepsia, Parkinson o deterioro cognitivo.  
- **Necesidades / Problemas:** Falta de monitoreo continuo, dificultad para registrar síntomas, baja adherencia al tratamiento y ansiedad por la imprevisibilidad de los eventos neurológicos.  
- **Contexto de Uso:** Entorno doméstico y sesiones de telemedicina, donde los pacientes necesitan registrar síntomas y recibir alertas de forma sencilla y confiable.  
- **Hallazgo Clave:** Los pacientes dependen de anotaciones manuales o la memoria, lo que genera información incompleta durante las consultas médicas.  
- **Beneficio con AuraNeuro:** Monitoreo en tiempo real mediante biosensores IoT, alertas automáticas para detección temprana y reportes accesibles que mejoran la adherencia y la confianza del paciente.

---

### 1.3.2. Segmentos Objetivo #2 — Profesionales de la salud  
 
- **Perfil:** Neurólogos, psicólogos y fisioterapeutas que trabajan en hospitales o clínicas privadas, de entre 25 y 55 años.  
- **Necesidades / Problemas:** Fuentes de datos fragmentadas, dificultad para evaluar la evolución del paciente y sobrecarga de información sin métricas estandarizadas.  
- **Contexto de Uso:** Entornos clínicos y plataformas de teleconsulta donde se requiere información visual, precisa y actualizada para apoyar la toma de decisiones.  
- **Hallazgo Clave:** Los especialistas buscan tableros integrados que consoliden la evolución del paciente y permitan exportar reportes médicos estandarizados.  
- **Beneficio con AuraNeuro:** Un panel clínico con datos biométricos y de comportamiento en tiempo real (sueño, frecuencia de crisis, adherencia), interoperable con sistemas clínicos (**HL7–FHIR**).

---

### 1.3.3. Segmentos Objetivo #3 — Proveedores de dispositivos IoT 
 
- **Perfil:** Empresas que desarrollan wearables médicos, sensores EEG/EMG y plataformas de datos biométricos interesadas en integrarse al sector salud.  
- **Necesidades / Problemas:** Falta de interoperabilidad, baja visibilidad en el mercado clínico y necesidad de canales seguros para transmisión de datos.  
- **Contexto de Uso:** Ecosistemas B2B orientados al desarrollo y la integración mediante APIs o SDKs.  
- **Hallazgo Clave:** Muchos proveedores IoT en Latinoamérica carecen de una plataforma de referencia para validar las aplicaciones clínicas de sus dispositivos.  
- **Beneficio con AuraNeuro:** Un marco de colaboración que permite la integración segura mediante API, amplía su alcance comercial y garantiza compatibilidad con estándares médicos (**HL7–FHIR**, **ISO 27001**).

---

**Conclusión:**   
Estos tres segmentos conforman un ecosistema digital conectado donde cada actor genera y recibe valor.  
Con este enfoque, **Mithycore** posiciona a **AuraNeuro** como una plataforma colaborativa **B2B2C (Business–to–Business–to–Consumer)** que fortalece la continuidad del cuidado neurológico en Latinoamérica.

---

