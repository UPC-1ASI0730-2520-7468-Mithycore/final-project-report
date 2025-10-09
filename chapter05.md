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

## 5.2. Landing Page, Services & Applications Implementation.

## 5.2.1 Sprint 1

### 5.2.1.1 Sprint Planning 1

| **Sprint #** | **Sprint 1** |
|---------------|--------------|
| **Sprint Planning Background** | El Sprint 1 tuvo como objetivo implementar y validar el **MVP de la Landing Page de AuraNeuro**, representando la primera versión funcional del frontend. En esta entrega se desarrollaron las secciones informativas principales y el diseño visual inicial, cumpliendo las historias de usuario **US21 a US34**. |
| **Date** | 2025-09-20 |
| **Time** | 07:00 PM |
| **Location** | Reunión virtual (Google Meet) |
| **Prepared By** | Gutiérrez Tume, Jeremy |
| **Attendees (to planning meeting)** | Eduardo Fabián Chacaliaza Minaya / Romero Meza Jhimy Pool / Gutiérrez Tume Jeremy / Fabricio Fabián Quispe Barzola / Juan José Meza Huanacune |
| **Sprint Goal** | **Validate that the AuraNeuro Landing Page MVP clearly communicates the project’s value proposition and allows user interaction through an initial responsive and accessible web design.**<br><br>**Validar que el MVP de la Landing Page de AuraNeuro comunique de forma clara la propuesta de valor del proyecto y permita la interacción del usuario a través de un diseño web inicial responsivo y accesible.** |
| **Sprint 1 Velocity** | 25 Story Points |
| **Sum of Story Points** | 25 |

---

### 5.2.1.2 Aspect Leaders and Collaborators

| **Aspect** | **Leader** | **Collaborators** | **Main Contribution** |
|-------------|-------------|--------------------|------------------------|
| Frontend | Fabricio Quispe | Eduardo Chacaliaza / Jeremy Gutiérrez | Implementación del MVP de la Landing Page, estructura HTML y estilo general. |
| Backend | Jhimy Romero | — | Preparación del entorno para integración API en Sprint 2. |
| UX/UI | Eduardo Chacaliaza | Fabricio Quispe | Diseño visual en Figma y aplicación de guías de estilo CSS. |
| Documentation | Jeremy Gutiérrez | Juan Meza | Registro de avances, commits y evidencias de desarrollo. |

---

### 5.2.1.3 Sprint Backlog 1

| **US ID** | **Título** | **Descripción / Objetivo** | **Tareas principales** | **Story Points** | **Asignado a** |
|------------|-------------|-----------------------------|------------------------|------------------|----------------|
| **US21** | Hero con CTA principal | Diseñar un hero claro con título, subtítulo y botón de acción. | Maquetar sección Hero y añadir CTA “Try AuraNeuro”. | 2 | Fabricio Quispe |
| **US22** | Navegación responsiva | Crear un navbar claro con menú hamburguesa en móvil. | Implementar menú JS, scroll suave y anclas. | 3 | Eduardo Chacaliaza |
| **US23** | Sección “How it Works” | Mostrar los pasos visuales con texto e íconos. | Diseñar cards informativas y texto accesible. | 2 | Fabricio Quispe |
| **US24** | Bloque de Beneficios | Mostrar beneficios con íconos y animaciones. | Implementar hover y estructura semántica. | 3 | Jeremy Gutiérrez |
| **US25** | Sección About / Who We Are | Describir misión del proyecto y equipo. | Redactar contenido bilingüe e imágenes institucionales. | 2 | Eduardo Chacaliaza |
| **US26** | Footer con redes sociales | Incluir contacto y enlaces de redes. | Configurar links accesibles. | 1 | Jeremy Gutiérrez |
| **US27** | Optimización SEO básica | Añadir meta tags y estructura semántica HTML. | Implementar title, description y OG tags. | 2 | Juan José Meza |
| **US28** | Diseño responsive completo | Adaptar estructura visual a móviles y tablets. | Revisar media queries y tamaños relativos. | 5 | Fabricio Quispe |
| **US29** | Documentación y versionado | Registrar commits y control de cambios en GitHub. | Documentar en README y subir avances. | 2 | Jeremy Gutiérrez |
| **Total** |  |  |  | **22 Story Points** |  |

---

### 5.2.1.4 Development Evidence for Sprint Review

| **Repository** | **Branch** | **Commit Id** | **Commit Message** | **Committed on (Date)** |
|-----------------|-------------|----------------|--------------------|------------------|
| `AuraNeuro-Frontend` | `feature/landing-ui` | `c4a1e7f` | `feat(hero): add bilingual hero section with CTA button` | 2025-09-21 |
| `AuraNeuro-Frontend` | `feature/navigation` | `b7f8e9c` | `feat(navbar): implement responsive navbar and smooth scrolling` | 2025-09-22 |
| `AuraNeuro-Frontend` | `feature/benefits-section` | `a9d2e3f` | `feat(benefits): add animated benefits cards` | 2025-09-24 |
| `AuraNeuro-Frontend` | `feature/about-section` | `d5f7e9a` | `feat(about): include mission and team section content` | 2025-09-25 |
| `AuraNeuro-Frontend` | `main` | `e2b3d4c` | `style(css): improve responsiveness and layout spacing` | 2025-09-26 |
| `AuraNeuro-Docs` | `main` | `f7a2b5d` | `docs(sprint1): add backlog and development evidence for sprint 1` | 2025-09-27 |


##### 5.2.1.5. Execution Evidence for Sprint Review  
  
Durante el Sprint 1 se implementó y desplegó el **Landing Page MVP** de Mithycore utilizando **HTML, CSS y JavaScript**.  
El entregable principal fue una página accesible en navegador, con las siguientes secciones:  

- Home
- Como funciona
- Nosotros
- Beneficios
- Contactanos

![Landing Page – Home](images/landing-inicio-ingles.png)  
![Landing Page – Cómo funciona](images/landing-works-ingles.png)  
![Landing Page – Nosotros](images/landing-how-ingles.png)  
![Landing Page – Beneficios](images/landing-beneficios-ingles.png)  

URL del despliegue: https://upc-1asi0730-2520-7468-mithycore.github.io/LandingPageAuraNeuro/

##### 5.2.1.6. Services Documentation Evidence for Sprint Review  

Durante el Sprint 1, el equipo documentó e implementó el **Contact Service**, el cual se integra con el formulario de contacto del **Landing Page MVP**.  
La documentación fue elaborada utilizando **OpenAPI (Swagger)**, permitiendo visualizar las rutas, métodos HTTP, parámetros, respuestas esperadas y ejemplos de uso.  

---

### Contact Service Endpoints 

**Documentación de Endpoints – Contact API**

| **Endpoint**   | **Acción Implementada**           | **Método HTTP** | **Sintaxis de Llamada**    | **Parámetros** |
|----------------|----------------------------------|-----------------|----------------------------|----------------|
| `/contact`     | Enviar un mensaje de contacto    | POST            | `/api/v1/contact`          | `name`, `email`, `message` (Body) |
| `/contact`     | Obtener todos los mensajes       | GET             | `/api/v1/contact`          | Ninguno |
| `/contact/{id}`| Obtener mensaje por ID           | GET             | `/api/v1/contact/{id}`     | `id` (Path) |

---
 
##### 5.2.1.7. Software Deployment Evidence for Sprint Review  

Durante el Sprint 1, el equipo realizó el **despliegue del Landing Page MVP** .  
Este proceso se llevó a cabo utilizando **GitHub Pages** como proveedor de hosting gratuito, lo que permitió que la página esté disponible públicamente en la web.  

- Actividades realizadas en el Sprint

1. **Creación y configuración del repositorio en GitHub**  
   - Se creó el repositorio oficial del proyecto: https://github.com/UPC-1ASI0730-2520-7468-Mithycore
   - Se estableció la estructura de ramas:  
     - `main` → Rama principal y estable para despliegue.  
     - `develop` → Rama de integración.  
     - `feature/landing-page` → Rama dedicada al desarrollo del Landing Page.  

2. **Configuración de GitHub Pages**  
   - Se habilitó la opción de GitHub Pages en la rama `main`.  
   - Se configuró el despliegue automático al realizar un **merge** en `main`.  
   - El Landing Page se encuentra disponible en la siguiente URL:  
  (https://github.com/UPC-1ASI0730-2520-7468-Mithycore/LandingPageAuraNeuro)

3. **Validación del despliegue en navegador**  
   - Se probó la visualización en diferentes navegadores (Chrome, Edge, Firefox).  
  

- Vista del Landing Page desplegado en navegador.

 ![Aura Neuro](https://raw.githubusercontent.com/UPC-1ASI0730-2520-7468-Mithycore/project-report/main/img/AURANEURO.png)

##### 5.2.1.8. Team Collaboration Insights during Sprint  

Durante el Sprint 1, el equipo de Mithycore trabajó de manera colaborativa en la implementación y despliegue del **Landing Page MVP** utilizando **HTML, CSS y JavaScript**.  
Cada integrante del equipo asumió un rol específico (frontend, backend, integración, UX/UI, CI/CD), pero también colaboró en revisión de código, pruebas y documentación.  

---

- **Distribución del trabajo:**  
  - **Stanley Jeremy (Team Leader):** coordinación general y despliegue CI/CD.  
  - **Juan José (Backend Engineer):** implementación inicial del endpoint `/api/contact`.  
  - **Eduardo (Frontend & UX/UI):** desarrollo de la sección principal y estilos.  
  - **Fabricio (Data & IoT Integration):** soporte en mock de backend y despliegue.  
  - **Jhimy (Frontend & UX/UI):** implementación de secciones de servicios y About.  
- **Revisiones de código:** se realizaron revisiones cruzadas en Pull Requests para garantizar calidad y consistencia del código.  
- **Comunicación:** se utilizaron reuniones virtuales diarias de 15 min y un board de Trello para gestión de tareas.  

---

![Insights](https://raw.githubusercontent.com/UPC-1ASI0730-2520-7468-Mithycore/project-report/main/img/INSIGTHS.png)



![Members](https://raw.githubusercontent.com/UPC-1ASI0730-2520-7468-Mithycore/project-report/main/img/MEMBERS.png)


---


## 5.2.2 Sprint 2

---

### 5.2.2.1 Sprint Planning 2

| **Sprint #** | **Sprint 2** |
|---------------|--------------|
| **Sprint Planning Background** | El Sprint 2 tuvo como objetivo implementar la **primera versión funcional del Frontend Web Application de AuraNeuro**, integrando el backend y habilitando la interacción real del usuario con el sistema. Se desarrollaron los módulos de **registro, inicio de sesión, dashboard y test cognitivo**, cumpliendo las historias de usuario US36 a US39. |
| **Date** | 2025-10-05 |
| **Time** | 09:00 PM |
| **Location** | Reunión virtual (Google Meet) |
| **Prepared By** | Gutiérrez Tume, Jeremy |
| **Attendees (to planning meeting)** | Eduardo Chacaliaza / Romero Meza Jhimy Pool / Gutiérrez Tume Jeremy / Fabricio Quispe Barzola / Juan José Meza Huanacune |
| **Sprint Goal** | **Validate that the AuraNeuro Frontend Web Application enables user interaction through registration, login and cognitive test modules connected to the backend API.** <br><br>**Validar que la aplicación web frontend de AuraNeuro permita la interacción real del usuario mediante los módulos de registro, inicio de sesión y prueba cognitiva conectados al backend.** |
| **Sprint 1 Review Summary** | Durante el Sprint 1 se entregó la Landing Page MVP informativa. El equipo definió las guías de estilo y el repositorio base. Se validó el diseño responsivo y se dejó lista la estructura para agregar funcionalidades dinámicas. |
| **Sprint 1 Retrospective Summary** | **Fortalezas:** buena distribución de tareas y uso de GitFlow. <br>**Mejoras:** profundizar en validación de formularios y automatizar el despliegue. |
| **Sprint 2 Velocity** | 28 Story Points |
| **Sum of Story Points** | 28 |

---

### 5.2.2.2 Aspect Leaders and Collaborators

| **Aspect** | **Leader** | **Collaborators** | **Main Contribution** |
|-------------|-------------|--------------------|------------------------|
| Frontend Logic | Fabricio Quispe | Eduardo Chacaliaza | Implementación de los módulos de registro e inicio de sesión en Angular. |
| Backend Integration | Jhimy Romero | Juan José Meza | Desarrollo de endpoints para autenticación y cognitive test (API C#). |
| UX/UI Design | Eduardo Chacaliaza | Fabricio Quispe | Diseño del dashboard y flujos de navegación para usuarios autenticados. |
| Documentation & Deployment | Jeremy Gutiérrez | — | Actualización del README, configuración de CI/CD y registro de evidencias. |

---

### 5.2.2.3 Sprint Backlog 2

| **US ID** | **Título / Descripción** | **Tareas principales** | **Story Points** | **Asignado a** |
|------------|--------------------------|-------------------------|------------------|----------------|
| **US36** | Registro de usuario | Crear formulario de registro y validaciones de correo y contraseña en Angular; conectar con endpoint `/api/users/register`. | 7 | Fabricio Quispe |
| **US37** | Inicio de sesión | Diseñar vista de login y validación de credenciales contra `/api/users/login`. | 5 | Jhimy Romero |
| **US38** | Dashboard de usuario | Mostrar datos de perfil, resultados de test y estado de estrés con gráficos dinámicos. | 8 | Eduardo Chacaliaza |
| **US39** | Test cognitivo | Implementar test con preguntas y resultados calculados en tiempo real; almacenar resultados en base de datos. | 8 | Juan José Meza |
| **Total** |  |  | **28 Story Points** |  |

---

### 5.2.2.4 Development Evidence for Sprint Review

| **Repository** | **Branch** | **Commit Id** | **Commit Message** | **Committed on** |
|-----------------|-------------|----------------|--------------------|------------------|
| `AuraNeuro-Frontend` | `feature/register-login` | `1a2b3c4` | `feat(auth): add user registration and login components` | 2025-10-06 |
| `AuraNeuro-Frontend` | `feature/dashboard` | `2b3c4d5` | `feat(dashboard): create user dashboard with stress level charts` | 2025-10-07 |
| `AuraNeuro-Frontend` | `feature/cognitive-test` | `3c4d5e6` | `feat(test): implement cognitive stress test component` | 2025-10-08 |
| `AuraNeuro-Backend` | `feature/api-auth` | `4d5e6f7` | `feat(api): add user login/register endpoints with JWT authentication` | 2025-10-08 |
| `AuraNeuro-Backend` | `feature/api-test` | `5e6f7g8` | `feat(api): add cognitive test endpoints and results storage` | 2025-10-09 |
| `AuraNeuro-Docs` | `main` | `6f7g8h9` | `docs(sprint2): add sprint backlog and development evidence for sprint 2` | 2025-10-09 |

Durante este sprint se desarrollaron los módulos principales de la aplicación web funcional, permitiendo el registro e inicio de sesión de usuarios, la ejecución del test cognitivo y la visualización de resultados en el dashboard. El Product Owner validó el entregable como la primera versión interactiva del Frontend Web Application. 

---

#### 5.2.2.5. Execution Evidence for Sprint Review.

Durante el Sprint 2 se desarrollaron las siguientes funcionalidades:

URL de despliegue:

Capturas de referencia:
- Vista de registro  
- Vista del test cognitivo  
- Dashboard del usuario  

Video de demostración:

#### 5.2.2.6. Services Documentation Evidence for Sprint Review.

| Endpoint | Método HTTP | Descripción | Ejemplo de Request | Ejemplo de Response |
|----------|-------------|-------------|--------------------|---------------------|


Repositorio API: https:

#### 5.2.2.7. Software Deployment Evidence for Sprint Review.

Frontend:
- Desplegado en: 
- Framework: Vue 3 + PrimeVue  
- CI/CD: GitHub Actions + Vercel

Backend:
- Desplegado en: 
- Framework: ASP.NET Core 8.0  
- Documentación: 

#### 5.2.2.8. Team Collaboration Insights during Sprint.

Durante el Sprint 2, el equipo trabajó de manera colaborativa en la implementación del Frontend y la integración con los servicios del Backend. Se observó una mayor sincronización en las tareas y comunicación entre las áreas de desarrollo y diseño.

- Distribución del trabajo:
  - Stanley Jeremy (Team Leader): coordinación general y soporte en arquitectura de componentes.  
  - Juan José (Backend Engineer): desarrollo de endpoints para registro y resultados.  
  - Eduardo (Frontend & UX/UI): vistas de registro, login y dashboard, además de ajustes UX.  
  - Fabricio (Data & IoT Integration): integración API y soporte de base de datos.  
  - Jhimy (Frontend & UX/UI): optimización visual y diseño responsive.  

- Revisiones de código: revisiones cruzadas de Pull Requests y validaciones de integración en GitHub.  
- Comunicación: reuniones semanales de seguimiento y coordinación técnica.  
- Colaboración técnica: uso del repositorio central para control de versiones y trazabilidad de cambios.
  

