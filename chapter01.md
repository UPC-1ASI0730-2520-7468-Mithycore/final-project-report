# Capitulo I: Introducción

## 1.1. Startup Profile  

### 1.1.1. Descripción de la Startup  

Mythicore desarrolla AuraNeuro, una plataforma digital para atención neurológica que combina dispositivos IoT (sensores biomédicos portátiles), procesamiento de señales y analítica de Inteligencia Artificial para ofrecer monitoreo continuo, alertas tempranas y reportes clínicos accionables. El objetivo es complementar la atención clínica (no sustituirla) permitiendo intervenciones más oportunas, reducir hospitalizaciones evitables y mejorar la calidad de vida de pacientes con enfermedades neurológicas crónicas.

**Misión**  
Mythicore —a través de la plataforma web AuraNeuro— tiene la misión de ofrecer atención neurológica personalizada y accesible mediante la integración segura de dispositivos IoT y analítica de inteligencia artificial. Buscamos complementar la práctica clínica aportando datos objetivos y continuidad en el seguimiento, facilitando teleconsultas y respuestas rápidas ante eventos críticos, siempre respetando la privacidad, el consentimiento informado y las buenas prácticas médicas, con el fin de reducir hospitalizaciones evitables y mejorar la calidad de vida de las personas con enfermedades neurológicas.

**Objetivo general**  
Desplegar y validar en un periodo piloto un MVP funcional de la plataforma web AuraNeuro que demuestre la viabilidad técnica y clínica de la integración IoT → analítica → workflow clínico (registro, agenda, videollamadas y alertas con geolocalización autorizada), evidenciando mejoras en la continuidad del cuidado y la toma de decisiones médicas basadas en datos objetivos.

Lograr que, durante el piloto, al menos el 70 % de los pacientes participantes generen datos válidos de manera continua (horas/día definidas) y que el 80 % de los profesionales implicados utilicen activamente las funciones de agenda y teleconsulta; además, documentar que un porcentaje significativo de casos (meta inicial 15–20 %) derive en una acción clínica (ajuste de tratamiento, citación o intervención) sustentada por la información aportada por la plataforma.

### 1.1.2. Perfiles de integrantes del equipo  

| Foto | Nombre y Código | Rol | Descripción |
|------|-----------------|-----|-------------|
| ![Stanley](imagesTeam/stanley.jpg) | **Stanley Jeremy Gutierrez Tume (U202118152)** | **Team Leader** | Estudiante de Ingeniería de Software, asume el rol de *Team Leader*. Su enfoque colaborativo le permite asignar tareas de manera eficiente, mientras que sus habilidades técnicas en HTML y CSS respaldan la capacidad para materializar ideas. Busca constantemente oportunidades de crecimiento y aprendizaje, y está comprometido con impulsar la innovación y el éxito en entornos de desarrollo de software. |
| ![Juan José](imagesTeam/juan.jpg) | **Juan José Meza Huanacune (U202320574)** | **Backend Engineer** | Estudiante de Ingeniería de Software, asume el rol de *Backend Engineer*. Tiene experiencia en arquitecturas backend con C#, Java y Python, además del manejo de bases de datos relacionales. Su capacidad de organización, liderazgo y aplicación de metodologías ágiles le permite coordinar tareas y asegurar el cumplimiento de objetivos del equipo. |
| ![Eduardo](imagesTeam/eduardo.jpg) | **Eduardo Fabián Chacaliaza Minaya (U202324129)** | **Frontend & UX/UI Engineer** | Estudiante de Ingeniería de Software, desempeña el rol de *Frontend & UX/UI Engineer*. Domina HTML5, CSS3 y JavaScript, junto con frameworks modernos como Vue.js y React. Se especializa en diseño de interfaces accesibles y centradas en el usuario, aportando creatividad y una visión enfocada en la experiencia de usuario para lograr aplicaciones intuitivas y atractivas. |
| ![Fabricio](imagesTeam/fabricio.jpg) | **Fabricio Fabián Quispe Barzola (U202320442)** | **Data & IoT Integration Engineer** | Estudiante de Ingeniería de Software, cumple el rol de *Data & IoT Integration Engineer*. Cuenta con conocimientos en machine learning, procesamiento de datos y analítica con Python y R, además de experiencia en la integración de dispositivos IoT. Su aporte principal es implementar soluciones inteligentes que conecten sensores y servicios en la nube, garantizando un flujo de datos seguro y en tiempo real. |
| ![Jhimy](./imagesTeam/JhimyRomeroMeza.png) | **Romero Meza Jhimy Pool (U202321510)** | **Frontend & UX/UI Engineer** | Estudiante de Ingeniería de Software, cumple el rol de UX/UI Designer & Frontend Engineer. Cuenta con conocimientos en diseño de interfaces, experiencia de usuario y desarrollo frontend con tecnologías modernas. Su aporte principal es la conceptualización y creación de wireframes, mockups y prototipos interactivos, asegurando que la experiencia del usuario sea clara, intuitiva y alineada con los objetivos del proyecto. Además, garantiza la coherencia visual del sistema y facilita la transición entre la fase de diseño y desarrollo.  |

---

## 1.2. Solution Profile  

### 1.2.1. Antecedentes y problemática  

Las enfermedades neurológicas —como epilepsia, Parkinson y Alzheimer— constituyen un desafío creciente para los sistemas de salud. Muchos diagnósticos llegan en etapas avanzadas por la ausencia de monitoreo continuo y la dependencia de consultas médicas espaciadas. Esta realidad provoca tratamientos poco personalizados, hospitalizaciones evitables y una pérdida significativa en la calidad de vida de los pacientes.

La integración de Internet of Things (IoT) y analítica de Inteligencia Artificial (IA) ofrece la oportunidad de transformar la atención neurológica mediante monitoreo en tiempo real, detección temprana de eventos clínicos y soporte a la telemedicina. Sin embargo, las soluciones actuales suelen ser fragmentadas, costosas o de difícil acceso, lo que amplía la brecha entre la tecnología disponible y las necesidades reales de pacientes y profesionales.

AuraNeuro, producto de la startup Mythicore, responde a esa necesidad proponiendo un sistema de monitoreo neurológico continuo que captura biomarcadores con dispositivos IoT, los procesa con algoritmos de IA y presenta la información en una plataforma accesible para especialistas y pacientes.

What — ¿Cuál es el problema?

La falta de monitoreo continuo en pacientes neurológicos provoca diagnósticos tardíos, tratamientos poco ajustados y aumentos innecesarios de hospitalizaciones. La información clínica se basa con frecuencia en reportes subjetivos y episodios puntuales, lo que impide intervenciones oportunas y personalizadas.

Who — ¿Quiénes están involucrados y quiénes sufren el problema?

Involucrados: pacientes con enfermedades neurológicas crónicas o en rehabilitación, neurólogos y especialistas, hospitales, clínicas y aseguradoras.

Afectados: pacientes que dependen de consultas médicas periódicas y carecen de datos objetivos entre evaluaciones; especialistas que necesitan evidencia continua para tomar decisiones clínicas más precisas.

Where — ¿Dónde ocurre el problema?

El problema surge en la atención tradicional: dentro de hospitales y clínicas durante citas programadas, y fuera de estos entornos en el hogar del paciente, donde no existe continuidad ni integración fiable de los datos recolectados entre visitas.

When — ¿Cuándo sucede el problema?

Entre citas médicas y, con especial gravedad, en momentos críticos como crisis epilépticas, episodios de pérdida aguda de memoria o fases de deterioro cognitivo progresivo. El problema es constante: la falta de datos continuos impide la detección temprana y la gestión proactiva las 24 horas del día.

Why — ¿Cuál es la causa raíz?

Dependencia de registros subjetivos (anamnesis) en lugar de mediciones objetivas.

Ausencia de herramientas tecnológicas accesibles y asequibles para monitoreo continuo.

Fragmentación de los datos clínicos entre distintos proveedores y plataformas, que dificulta la interpretación longitudinal por parte del especialista.

How — ¿Cómo y en qué condiciones se necesita la solución?

En la rutina del paciente: mediante sensores portátiles conectados a una app móvil que capture biomarcadores relevantes de forma continua.

En la consulta: especialistas acceden a un panel web con datos procesados por IA (patrones, alertas y reportes históricos) para apoyar decisiones clínicas.

Acceso y adopción: a través de alianzas con programas de salud digital, recomendaciones médicas y convenios con hospitales y aseguradoras; los usuarios prefieren interfaces móviles intuitivas y paneles web claros con notificaciones y reportes accionables.

Propuesta de valor (breve)

- AuraNeuro centraliza y estructura datos biomédicos continuos para ofrecer:

- Detección temprana de cambios clínicos relevantes.

- Reportes objetivos que mejoran la toma de decisiones médicas.

- Reducción de hospitalizaciones evitables y personalización del tratamiento.

- Mejora en la calidad de vida y empoderamiento del paciente mediante información accesible y en tiempo real.
---


### 1.2.2. Lean UX Process  

A continuación se presenta el Lean UX Process aplicado a AuraNeuro / Mythicore, organizado en Problem Statements, Assumptions, Hypothesis Statements y un Lean UX Canvas pensado para un informe académico y validación temprana.

#### 1.2.2.1. Lean UX Problem Statements  

Domain (dominio):
Atención neurológica continua para enfermedades crónicas (epilepsia, Parkinson, enfermedades neurodegenerativas) apoyada por IoT y analítica de IA.

**Customer segments (segmentos de cliente):**

- Pacientes adultos (20–65+) con diagnóstico confirmado o en riesgo de episodios neurológicos.

- Neurólogos y equipos clínicos (hospitales, clínicas privadas).

- Aseguradoras y programas de salud que buscan reducir costos por hospitalizaciones evitables.

**Pain points (dolores principales):**

- Falta de monitoreo objetivo y continuo entre consultas.

- Diagnósticos y ajustes terapéuticos basados en información subjetiva (anamnesis).

- Retrasos en la detección de crisis (p. ej. crisis epilépticas) que aumentan riesgo y costos.

- Fragmentación de datos clínicos entre dispositivos y sistemas hospitalarios.

**Gap (brecha identificada):**
No existe, en el mercado objetivo, una solución asequible y accesible que combine sensores portátiles validados, procesamiento de señales en tiempo real y reportes clínicos accionables integrados para la toma de decisiones neurológicas.

**Vision / Strategy (visión y estrategia):**
Visión: ofrecer monitoreo neurológico continuo y accesible que permita detección temprana y personalización del tratamiento.
Estrategia: empezar por un segmento clínico inicial (por ejemplo, pacientes con epilepsia vinculados a centros neurólogos aliados), validar modelos de IA para eventos detectables, luego escalar a otros diagnósticos y alianzas con aseguradoras.

**Initial segment (segmento inicial recomendado):**
Pacientes adultos con epilepsia controlada de forma insuficiente o con episodios recurrentes, atendidos en clínicas neurológicas urbanas dispuestas a participar en pilotos clínicos.

    #### 1.2.2.2. Lean UX Assumptions  

    #### 1.2.2.3. Lean UX Hypothesis Statements  

    #### 1.2.2.4. Lean UX Canvas  

## 1.3. Segmentos objetivo  

Esta sección describe los segmentos objetivo asociados al dominio del problema con características demográficas, motivaciones, barreras y la información estadística que sustentaría el análisis en un informe académico.

**Segmento A — Primario: Pacientes adultos con enfermedades neurológicas**

Perfil demográfico y clínico

- Edad: típicamente 20–65+ años (dependiendo de la enfermedad; Alzheimer predomina en >65).

- Condición: epilepsia, Parkinson temprano-intermedio, personas con deterioro cognitivo leve o en rehabilitación post-evento neurológico.

- Ubicación: inicialmente en áreas urbanas con acceso a clínicas neurológicas.

- Nivel socioeconómico: variable; enfoque inicial en clínicas que atiendan a población con cobertura o con recursos para pilotos.

Comportamiento y necesidades

- Necesitan monitoreo objetivo entre citas.

- Buscan reducir crisis y mejorar calidad de vida.

- Valoran confidencialidad y facilidad de uso.

- Barreras a la adopción

- Reticencia por usar dispositivos 24/7.

- Preocupaciones sobre privacidad de datos y costos.

- Falta de confianza en nuevas tecnologías médicas.

- Estadística de sustento (qué incluir en informe académico):

- Prevalencia local y/o nacional de la(s) condición(es) objetivo (p. ej. tasa de epilepsia por 1,000 hab.).

- % de pacientes con crisis recurrentes o mal control (si disponible).

Penetración de smartphones en el grupo etario objetivo.
(Nota: reemplace con cifras locales actualizadas — fuentes recomendadas: OMS, ministerio de salud local, INEI o similar.)

**Segmento B — Secundario: Neurólogos y equipos clínicos**

Perfil profesional

- Neurólogos, neurofisiólogos, enfermeras de neurología y coordinadores de cuidado.

- Centrados en hospitales y clínicas privadas/ públicas con servicio neurológico.

Necesidades

- Datos objetivos y longitudinales para orientar diagnósticos y ajustar terapias.

- Herramientas que reduzcan carga administrativa y mejoren la priorización de casos.

Barreras

- Carga de trabajo y resistencia a incorporar nuevas plataformas.

- Necesidad de evidencia clínica y validación antes de usar como herramienta de decisión.

- Estadística de sustento (qué incluir):

- Número de neurólogos por 100,000 habitantes en la región.

Tiempo promedio de consulta y número de pacientes por neurólogo (si disponible).
(Fuentes: sociedades médicas nacionales, registros de salud pública.)
