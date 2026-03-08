# Arquitectura Empresarial -- Caso de Estudio Fintech B2C

Este repositorio contiene el desarrollo de una **Arquitectura
Empresarial utilizando el framework TOGAF (ADM)** para un caso de
estudio de una **Fintech B2C enfocada en microcréditos digitales basados
en análisis de datos e integración de múltiples fuentes de
información**.

El objetivo es diseñar una arquitectura que permita **alinear
estrategia, procesos, datos, aplicaciones y tecnología**.

------------------------------------------------------------------------

# Caso de Estudio

La empresa propone una **Fintech digital** que ofrece:

-   Microcréditos rápidos
-   Evaluación automática de riesgo
-   Integración con múltiples fuentes de datos financieros
-   Experiencia digital completa

El sistema debe permitir **tomar decisiones de crédito en tiempo real**
mediante analítica avanzada.

------------------------------------------------------------------------

# Flujo del Proceso de Negocio

``` mermaid
flowchart TD

A[Cliente solicita crédito desde la app] --> B[Captura de datos del cliente]

B --> C[Consulta de fuentes externas]

C --> D[Integración de APIs bancarias]
C --> E[Bureaus de crédito]
C --> F[Datos alternativos]

D --> G[Motor de scoring crediticio]
E --> G
F --> G

G --> H[Evaluación automática]

H -->|Aprobado| I[Desembolso de crédito]
H -->|Rechazado| J[Notificación al cliente]

I --> K[Registro de obligación financiera]
```

------------------------------------------------------------------------

# Arquitectura Empresarial

La arquitectura se organiza en cuatro dominios principales:

-   Arquitectura de Negocio
-   Arquitectura de Datos
-   Arquitectura de Aplicaciones
-   Arquitectura Tecnológica

------------------------------------------------------------------------

# Arquitectura de Negocio

Define los procesos clave del negocio.

``` mermaid
flowchart LR

A[Adquisición de Cliente] --> B[Solicitud de Crédito]

B --> C[Evaluación de Riesgo]

C --> D[Aprobación de Crédito]

D --> E[Desembolso]

E --> F[Gestión de Crédito]
```

------------------------------------------------------------------------

# Arquitectura de Datos

Describe el flujo de información dentro del sistema.

``` mermaid
flowchart TD

A[Datos del Cliente] --> D[Lago de Datos]

B[Datos Bancarios] --> D
C[Datos de Bureaus] --> D

D --> E[Procesamiento de Datos]

E --> F[Modelo de Scoring]

F --> G[Resultado de Evaluación]
```

------------------------------------------------------------------------

# Arquitectura de Aplicaciones

Componentes principales del sistema.

``` mermaid
flowchart TD

A[Aplicación Móvil] --> B[API Gateway]

B --> C[Servicio de Identidad]
B --> D[Servicio de Integración de Datos]
B --> E[Motor de Scoring]
B --> F[Servicio de Créditos]

E --> G[Base de Datos Analítica]

F --> H[Base de Datos Transaccional]
```

------------------------------------------------------------------------

# Arquitectura Tecnológica

Infraestructura que soporta la solución.

``` mermaid
flowchart TD

A[Usuarios] --> B[Internet]

B --> C[API Gateway]

C --> D[Servicios Backend]

D --> E[Contenedores / Microservicios]

E --> F[Base de Datos]

E --> G[Motor de Analítica]

F --> H[Infraestructura Cloud]
G --> H
```

------------------------------------------------------------------------

# Estructura del Repositorio

    ea-fintech-togaf
    │
    ├── preliminary
    ├── architecture-vision
    ├── business-architecture
    ├── data-architecture
    ├── application-architecture
    ├── technology-architecture
    ├── diagrams
    └── models

------------------------------------------------------------------------

# Framework utilizado

Este proyecto sigue el **Architecture Development Method (ADM)** de
TOGAF:

1.  Preliminary
2.  Architecture Vision
3.  Business Architecture
4.  Information Systems Architecture
5.  Technology Architecture
6.  Opportunities & Solutions
7.  Migration Planning
8.  Implementation Governance
9.  Architecture Change Management

------------------------------------------------------------------------

# Objetivo del Proyecto

Diseñar una arquitectura que permita:

-   Decisiones crediticias en tiempo real
-   Integración eficiente de datos
-   Escalabilidad del sistema
-   Seguridad y cumplimiento regulatorio
