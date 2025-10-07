# Capítulo V: Product Implementation, Validation & Deployment

### 5.1. Software Configuration Management  
#### 5.1.1. Software Development Environment Configuration  
Esta sección detalla las herramientas utilizadas durante el desarrollo del software, organizadas según las distintas fases del proyecto.

*Project Management

-Google Meet: https://meet.google.com/

-Plataforma utilizada para realizar reuniones virtuales con los miembros del equipo. Permite compartir pantalla, imágenes, texto y video, todo en tiempo real. Es compatible con navegadores web, dispositivos móviles y computadoras, y solo requiere una cuenta activa para su uso.

-Product UX/UI Design

-UXpressia: https://uxpressia.com/

Fue clave para construir perfiles detallados de usuarios, mapear sus emociones, metas y comportamientos mediante herramientas como User Personas, Journey Maps y Empathy Maps.

-Figma: https://www.figma.com/ Plataforma colaborativa de diseño usada para crear wireframes y mockups. Su facilidad para compartir y editar en tiempo real la convirtió en una herramienta fundamental en el desarrollo de interfaces visuales.

*Software Development

-Landing Page

Se desarrolló la landing page con tecnologías como HTML5, CSS3 y JavaScript, apoyados en Bootstrap para lograr un diseño responsivo y acelerar el desarrollo de una interfaz adaptable a diversos dispositivos.

*IDE’s de desarrollo

-Visual Studio Code: https://code.visualstudio.com/

Usamos este IDE por su rendimiento, facilidad de uso y herramientas integradas para la edición, depuración y control de versiones. Fue esencial para implementar la landing page de forma ágil y ordenada.

-GitHub: https://github.com/

Plataforma para alojar el repositorio del proyecto y gestionar el control de versiones del código fuente y la documentación, facilitando la colaboración y el seguimiento de cambios.

*Software Deployment

-GitHub Pages

Utilizamos GitHub Pages para desplegar la landing page de forma gratuita y directamente desde el repositorio del proyecto. Esta herramienta permite alojar sitios estáticos fácilmente, integrándose con el flujo de trabajo de GitHub y facilitando una publicación continua con cada cambio en el repositorio.

*Software Documentation

-Canva: https://www.canva.com/

Empleamos Canva para la creación de material visual y presentaciones gráficas del proyecto. Su interfaz sencilla e intuitiva permite diseñar documentos importantes que ayudan a comunicar ideas de forma clara y profesional.

-Markdown:

Un lenguaje de marcado ligero y sencillo para crear documentos con formato, empleándose para redactar la documentación del proyecto de manera clara y estructurada.

#### 5.1.2. Source Code Management  

El equipo gestiona el código fuente utilizando **GitHub** como plataforma de control de versiones.  

- **Landing Page**: https://github.com/UPC-1ASI0730-2520-7468-Mithycore/LandingPageAuraNeuro

#### Workflow de Versionado – GitFlow
Para el control de versiones se aplica la estrategia **GitFlow**.La organización de ramas es la siguiente:

- **`main`**: contiene el código estable y liberado en producción.  
- **`develop`**: integra el trabajo de todas las features y sirve como base para la preparación de releases.  
- **Feature branches**: creados a partir de `develop` para nuevas funcionalidades. 
- **Release branches**: creados a partir de `develop` cuando se prepara una nueva versión estable. 
- **Hotfix branches**: creados a partir de `main` para resolver errores críticos detectados en producción. 

#### Convenciones de Commits
Se adoptó el estándar **Conventional Commits** para los mensajes de commit, garantizando claridad y trazabilidad.

Esto permite generar changelogs automáticos y facilita la integración continua.  

---

#### 5.1.3. Source Code Style Guide & Conventions  

En el proyecto **AuraNeuro**, se adoptaron convenciones de código para mantener consistencia, legibilidad y mantenibilidad. Todos los identificadores, clases, variables y comentarios se escriben en **inglés**. Las guías aplicadas se basan en estándares reconocidos para HTML, CSS, JavaScript y C#.

## 1. HTML
- Uso de HTML semántico: `<header>`, `<main>`, `<section>`, `<footer>`, `<article>`
- Clases e IDs en **kebab-case**: `hero-content`, `contact-form`, `navbar-container`
- Comentarios: `<!-- Comentario -->`
- Imágenes siempre con `alt` descriptivo

## 2. CSS
- Archivo principal: `Styles.css`
- Clases e IDs en **kebab-case**
- Variables CSS: `--variable-name`
- Responsividad con media queries

## 3. JavaScript
- Variables: `camelCase`
- Constantes: `UPPER_SNAKE_CASE`
- Funciones descriptivas; manejadores con prefijo `onEvent`
- `"use strict";` al inicio de scripts

## 4. C# (Backend – ASP.NET Core)
En el desarrollo del backend de AuraNeuro, se empleó C# con el framework ASP.NET Core, siguiendo las convenciones oficiales de Microsoft para mantener un código limpio, modular y mantenible.  
Estas guías garantizan la consistencia en la estructura de clases, métodos y nomenclatura de archivos dentro del API RESTful del proyecto.

- Naming conventions:
  - **Classes & Methods:** PascalCase → `PatientController`, `GetAllRecords()`
  - **Variables & Parameters:** camelCase → `patientId`, `recordList`
  - **Constants:** UPPER_SNAKE_CASE → `MAX_ATTEMPTS`
- File organization:
  - Estructura por capas: *Controllers*, *Models*, *Services*, *Data*
  - Separación de responsabilidades para mejorar mantenibilidad y testing.
- Comments:
  - XML documentation comments (`///`) para describir clases y métodos públicos.
- Framework guidelines:
  - Se siguieron las **Microsoft C# Coding Conventions** y las **ASP.NET Core Engineering Guidelines**.

#### 5.1.4. Software Deployment Configuration  

La aplicación se desplegará en la nube mediante:

-Vercel para el Landing Page.

-Azure o AWS para el backend con API RESTful y base de datos.

-Contenedores Docker para mantener consistencia en los entornos. 

## 5.2. Landing Page, Services & Applications Implementation.

### 5.2.1. Sprint 1

#### 5.2.1.1. Sprint Planning 1.

<table>
  <tbody>
    <tr>
     <td>Sprint #</td>
     <td>Sprint n</td>
    </tr>
    <tr>
     <td>Sprint Planning Background</td>
    </tr>
    <tr>
     <td>Date</td>
     <td>YYYY-MM-DD</td>
    </tr>
    <tr>
     <td>Time</td>
     <td>HH:MM AM/PM</td>
    </tr>
    <tr>
     <td>Location</td>
     <td>
     (Descripción de la ubicación de la reunión, física ovirtual)
     </td>
    </tr>
    <tr>
     <td>Prepared By</td>
     <td>Jiménez Rosas, Arturo Eduardo</td>
    </tr>
    <tr>
     <td>
     Attendees (to planning
      meeting)
    </td>
     <td>Jiménez Rosas, Arturo Eduardo / Rodríguez Peña,Jorge Andrés / …
     </td>
    </tr>
    <tr>
     <td>Sprint n – 1 Review Summary</td>
     <td>
     (Resumen del Sprint anterior, en términos de resultados alcanzados a nivel de productos de software, opiniones de miembros y feedback de product owner.)</td>
    </tr>
    <tr>
     <td>Sprint n – 1 Retrospective Summary</td>
     <td>(Resumen del Sprint anterior, en términos de opiniones de miembros del equipo sobre aciertos u oportunidades de mejora en su forma de trabajo)</td>
    </tr>
    <tr>
     <td>Sprint Goal & User Stories</td>
    </tr>
    <tr>
     <td>Sprint n Goal</td>
     <td> (Definir el Goal del Sprint n y la métrica de
cumplimiento.)</td>
    </tr>
    <tr>
     <td>Sprint n Velocity</td>
     <td>(Definir el Velocity establecido para el Sprint n, es
decir cuántos Story Points puede aceptar el equipo
para este Sprint n.)</td>
    </tr>
    <tr>
     <td>Sum of Story Points</td>
     <td></td>
    </tr>
  </tbody>
</table>

#### 5.2.1.2. Aspect Leaders and Collaborators.

#### 5.2.1.3. Sprint Backlog 1.

#### 5.2.1.4. Development Evidence for Sprint Review.

#### 5.2.1.5. Execution Evidence for Sprint Review.

#### 5.2.1.6. Services Documentation Evidence for Sprint Review.

#### 5.2.1.7. Software Deployment Evidence for Sprint Review.

#### 5.2.1.8. Team Collaboration Insights during Sprint.

### 5.2.2. Sprint 2

#### 5.2.2.1. Sprint Planning 2.

| Sprint # | Sprint 2 |
|-----------|-----------|
| **Sprint Planning Background** | El Sprint 2 tiene como objetivo implementar la primera versión funcional de la Aplicación Web AuraNeuro, centrada en desarrollar los flujos iniciales del Frontend, la integración de servicios del Backend y la validación de la experiencia de usuario. |
| **Date** | 2025-10-01 |
| **Time** | 07:00 PM |
| **Location** | Reunión virtual (Google meet) |
| **Prepared By** | Stanley Jeremy Gutierrez Tume |
| **Attendees (to planning meeting)** | Romero Meza Jhimy Pool / Eduardo Fabian Chacaliaza Minaya / Gutierrez Tume, Jeremy / Fabricio Fabián Quispe Barzola / Juan José Meza Huanacune |
| **Sprint 1 Review Summary** | Durante el Sprint 1 se logró desarrollar y desplegar el Landing Page MVP del proyecto AuraNeuro. Se validó la propuesta de valor y la comunicación visual del producto, asegurando su responsividad y accesibilidad. Se documentaron los endpoints del servicio de contacto y se estableció el flujo de despliegue con GitHub Pages y Vercel. |
| **Sprint 1 Retrospective Summary** | El equipo identificó mejoras en la coordinación técnica, estableció reuniones intersemanales para sincronización de avances y estandarizó los mensajes de commits mediante Conventional Commits. Se decidió iniciar el desarrollo del Frontend principal en el siguiente Sprint. |
| **Sprint Goal** | Desarrollar la primera versión funcional de la Aplicación Web AuraNeuro, que permita el registro, inicio de sesión y ejecución de una prueba cognitiva básica conectada con servicios de Backend. Se busca validar la integración inicial del Frontend y Backend, garantizando una experiencia de usuario fluida y funcional. |
| **Sprint 2 Velocity** | 27 Story Points |
| **Sum of Story Points** | 27 |

#### 5.2.2.2. Aspect Leaders and Collaborators.

Se identificaron los siguientes aspectos clave del Sprint:  
- User Authentication (Registro e Inicio de Sesión)  
- Cognitive Test Module (Módulo de Pruebas Cognitivas)  
- Frontend Navigation (Sistema de Navegación)  
- API Integration (Integración de Servicios REST)  
- UI Enhancements (Ajustes de Interfaz y Estilo)  

Cada aspecto fue asignado a un líder (L) responsable de su entrega y a uno o más colaboradores (C) encargados del soporte técnico y revisión del desarrollo.

| Team Member (Last Name, First Name) | Role | GitHub Username | User Authentication | Cognitive Test Module | Frontend Navigation | API Integration | UI Enhancements |
|-------------------------------------|------|-----------------|---------------------|----------------------|---------------------|-----------------|-----------------|
| Gutierrez Tume, Stanley Jeremy | Team Leader | `Stan-gt213891` | L | C | C | C | C |
| Meza Huanacune, Juan José | Backend Engineer | `JuanMHZ1250` | C | C | L | C | C |
| Chacaliaza Minaya, Eduardo Fabián | Frontend & UX/UI Engineer | `educmz` | C | C | L | L | L |
| Quispe Barzola, Fabricio Fabián | Data & IoT Integration Engineer | `BrooklynKarmis` | C | L | C | L | C |
| Romero Meza, Jhimy Pool | Frontend & UX/UI Engineer | `jhimyromeromeza` | C | C | C | C | L |

#### 5.2.2.3. Sprint Backlog 2.

El Sprint 2 se centró en la implementación del Frontend funcional de AuraNeuro y su integración con los servicios básicos del Backend.  
El objetivo principal fue entregar una versión que permitiera el registro de usuarios, inicio de sesión y ejecución de una prueba cognitiva con resultados visibles.

| Sprint # | User Story | Work-Item / Task | Descripción | Estimación (Horas) | Assigned To | Status |
|----------|------------|------------------|-------------|---------------------|-------------|--------|
| Sprint 2 | US07.1 – Registro de usuario | T2.1 | Implementar vista y formulario de registro con validaciones de datos. | 8h | Eduardo | Done |
| Sprint 2 | US07.2 – Inicio de sesión | T2.2 | Crear vista de login y conexión con API de autenticación. | 8h | Eduardo | Done |
| Sprint 2 | US08.1 – Módulo de prueba cognitiva | T2.3 | Integrar API de preguntas y flujo de evaluación. | 10h | Fabricio | In Progress |
| Sprint 2 | US09.1 – Dashboard de resultados | T2.4 | Diseñar e implementar la vista de resultados del test cognitivo. | 6h | Juan José | To Review |
| Sprint 2 | US10.1 – UI/UX Enhancements | T2.5 | Ajustar estilos, tipografía y diseño responsivo general. | 5h | Jhimy | Done |

#### 5.2.2.4. Development Evidence for Sprint Review.

| Repository | Branch | Commit Id | Commit Message | Committed on (Date) |
|------------|--------|-----------|----------------|---------------------|
| aura-frontend | feature/auth | b23c4df | feat: add login and signup view with router guard | 22/09/2025 |
| aura-backend  | feature/api-tests | f92a11a | test: add endpoint for user cognitive results | 23/09/2025 |
| aura-frontend | feature/dashboard | 7a11cc9 | feat: create dashboard with score charts | 24/09/2025 |

#### 5.2.2.5. Execution Evidence for Sprint Review.

Durante el Sprint 2 se desarrollaron las siguientes funcionalidades:
- Registro e inicio de sesión de usuarios.  
- Ejecución del test cognitivo desde el Frontend mediante API REST.  
- Visualización de resultados en un Dashboard.  
- Interfaz responsiva validada en diferentes dispositivos.  

URL de despliegue: https://aura-frontend.vercel.app  

Capturas de referencia:
- Vista de registro  
- Vista del test cognitivo  
- Dashboard del usuario  

Video de demostración:

#### 5.2.2.6. Services Documentation Evidence for Sprint Review.

#### 5.2.2.7. Software Deployment Evidence for Sprint Review.

#### 5.2.2.8. Team Collaboration Insights during Sprint.

## 5.3. Validation Interviews.

### 5.3.1. Diseño de Entrevistas.

### 5.3.2. Registro de Entrevistas.

### 5.3.3. Evaluaciones según heurísticas

## 5.4. Video About-the-Product.
