# Documento de Especificación de Requisitos - Caso TicketPass

**Universidad Mariana**
**Ingeniería de Software I**
**Proyecto Transversal - Unidad 2**

**Equipo:**
- Luis Felipe Paredes — Product Owner
- Yeferson Pujimuy — Scrum Master
- Santiago Chamorro — Desarrollador / Equipo de Desarrollo

**Fecha:** 30 de septiembre de 2026


## 1. Contextualización del Proyecto

TicketPass es una plataforma web para la comercialización y gestión de boletería para eventos y festivales de alta concurrencia. El sistema busca reducir los problemas de colapso de servidores, falsificación o duplicación de entradas y dificultades en la configuración de zonas, aforos y precios.

---

## 2. Actores Principales del Sistema

| # | Actor | Descripción |
|:-:|:------|:------------|
| **1** | **Comprador / Fan** | Usuario final que explora el catálogo de eventos, ingresa a la fila virtual, selecciona localidades y efectúa el pago de las entradas. |
| **2** | **Organizador del Evento** | Cliente corporativo encargado de definir la logística comercial, habilitar las zonas del escenario, establecer aforos y consultar reportes de recaudo. |
| **3** | **Logística / Personal de Puerta** | Operador en campo encargado de escanear y validar el acceso de los asistentes en los puntos de entrada mediante dispositivos móviles. |

---

## 3. Matriz de Transformación: Problemas, Necesidades y Requisitos Funcionales

| # | Problema Identificado | Necesidad de Software | Requisito Funcional |
|:-:|:----------------------|:----------------------|:--------------------|
| **1** | Colapso de la plataforma web durante la venta inicial por alta concurrencia de usuarios simultáneos. | Administrar y ordenar el tráfico masivo de peticiones sin saturar la infraestructura. | El sistema debe asignar un turno en fila virtual a los usuarios cuando las peticiones superen las 1.000 solicitudes/minuto. |
| **2** | Falsificación y duplicación de boletas en los puntos de acceso al evento durante la validación manual. | Garantizar la autenticidad e infalsificabilidad de las entradas digitales. | El sistema debe generar un código QR dinámico cifrado que se actualice cada 30 segundos dentro de la aplicación móvil. |
| **3** | Errores humanos y lentitud al configurar manualmente los aforos y precios por localidad para cada concierto. | Digitalizar y centralizar la parametrización de recintos y ofertas comerciales. | El sistema debe permitir parametrizar zonas, límites de aforo y esquemas de precios de forma dinámica antes del lanzamiento comercial. |

---

## 4. Historias de Usuario (Backlog)

> **Nota:** El backlog completo con las 11 Historias de Usuario, su priorización MoSCoW y estimación se encuentra en los archivos:
> - `DOCS/02_priorizacion.md`
> - `DOCS/03_estimacion_y_costos.md`

### Resumen del Backlog

| ID | Historia de Usuario | MoSCoW | SP |
|:--:|:--------------------|:------:|:--:|
| HU01 | Fila virtual para compra de boletos | Must Have | 13 |
| HU02 | Generación de código QR dinámico | Must Have | 5 |
| HU03 | Parametrización de zonas y precios | Must Have | 2 |
| HU04 | Selección de boletos mediante mapa interactivo | Should Have | 8 |
| HU05 | Validación de boletos en punto de acceso | Must Have | 3 |
| HU06 | Registro de usuarios | Must Have | 3 |
| HU07 | Catálogo de eventos | Should Have | 5 |
| HU08 | Pago de boletería | Must Have | 5 |
| HU09 | Historial de compras | Could Have | 3 |
| HU10 | Monitoreo de ventas y recaudo | Should Have | 5 |
| HU11 | Notificaciones de compra | Could Have | 3 |
| | **TOTAL** | | **55 SP** |

---

## 5. Criterios de Aceptación (INVEST)

Cada Historia de Usuario cuenta con mínimo 3 criterios de aceptación verificables mediante casillas de verificación (`- [ ]`), los cuales se encuentran documentados en cada Issue de GitHub.

### Ejemplo — HU01: Fila virtual para compra de boletos

**Como** comprador
**Quiero** ingresar a una fila virtual cuando exista alta demanda
**Para** poder acceder ordenadamente a la compra sin que la plataforma colapse

**Criterios de Aceptación:**
- [ ] El sistema activa la fila virtual cuando la demanda supera el umbral configurado.
- [ ] El usuario recibe un turno y puede consultar su posición.
- [ ] El sistema permite avanzar desde la fila hacia el proceso de compra sin perder el turno.

---

## 6. Roles del Equipo

| Integrante | Rol | Responsabilidades |
|:-----------|:----|:------------------|
| **Luis Felipe Paredes** | Product Owner | Gestionar y priorizar el Product Backlog, representar el valor del producto y definir prioridades. |
| **Yeferson Pujimuy** | Scrum Master | Facilitar Scrum, apoyar al equipo, eliminar impedimentos y promover el cumplimiento del proceso. |
| **Santiago Chamorro** | Desarrollador / Equipo de Desarrollo | Diseñar, construir, probar e integrar las funcionalidades del producto. |

---

## 7. Modelo de Proceso

Se selecciona **Scrum** porque TicketPass es una plataforma comercial que puede desarrollarse de forma iterativa, entregando primero las funcionalidades críticas (MVP) y posteriormente las funcionalidades de experiencia y administración.

- **Velocidad del equipo:** 12 SP por Sprint
- **Duración de cada Sprint:** 2 semanas
- **Duración estimada:** 5 Sprints / 10 semanas

---

## 8. Estimación Global

| Concepto | Valor |
|:---------|:------|
| **Total Story Points** | 55 SP |
| **Factor de conversión** | 8 horas / SP |
| **Esfuerzo total** | 440 horas |
| **Tarifa profesional** | $45.000 COP / hora |
| **Costo estimado total** | $19.800.000 COP |


**Fin del documento.**
