# Plan de Proyecto y Modelos - LicorExpress

**Universidad Mariana**
**Ingeniería de Software I**
**Proyecto Transversal - Unidad 2**

**Equipo:**

- [Santiago chamorro] — Product Owner
- [Pujimuy yeferson ] — Desarrollador / Equipo de Desarrollo
- [luis felipe paredes] — Desarrollador / Equipo de Desarrollo.

**Fecha:** 30 de septiembre de 2026

---

## 1. Marco Teórico y Fundamentos Metodológicos

### 1.1 ¿Qué es un Proceso de Software?

Un Proceso de Software es el conjunto estructurado de actividades de ingeniería (Análisis de Requisitos, Diseño de Arquitectura, Construcción de Código, Pruebas y Despliegue) ejecutadas de forma metódica para construir productos funcionales de alta calidad.

### 1.2 Cuadro Comparativo de Modelos de Proceso

| Modelo | Filosofía de Trabajo | Manejo del Cambio | Ideal Para... |
|:-------|:---------------------|:------------------|:--------------|
| **Cascada** | Lineal y secuencial. No se avanza sin congelar la fase previa. | Muy rígido y costoso. | Sistemas críticos o regulados (médico, aeronáutico). |
| **Incremental** | El sistema se divide en módulos y se entrega por partes funcionales. | Moderadamente flexible. | Proyectos con componentes independientes bien definidos. |
| **Espiral (Boehm)** | Guiado por identificación, análisis y mitigación de riesgos técnicos. | Muy adaptativo según riesgos. | Proyectos complejos con alto nivel de innovación. |
| **Scrum (Ágil)** | Iterativo e incremental. Trabajo en bloques fijos (Sprints de 2 semanas). | Altamente adaptativo. | Software comercial, startups y entornos variables. |

---

## 2. Selección y Justificación del Modelo de Proceso

Para LicorExpress se selecciona **Scrum (Marco Ágil)**.

### 2.1 Justificación

LicorExpress es una **plataforma comercial** con necesidad de lanzar un Producto Mínimo Viable (MVP) al mercado en el menor tiempo posible para validar ventas y domicilios, dejando funcionalidades avanzadas para incrementos posteriores.

En particular:

- La funcionalidad de **verificación de edad (HU01, 5 SP)** es crítica por cumplimiento legal y debe entregarse en el primer Sprint.
- El **seguimiento en tiempo real (HU08, 8 SP)** representa un esfuerzo considerable que **no impide la operación básica**, por lo que se posterga para una fase de extensión.
- El **pago electrónico (HU05, 8 SP)** y la **asignación de domiciliarios (HU07, 8 SP)** son críticos para el recaudo y deben entregarse en los primeros Sprints.

Scrum permite iterar, recibir retroalimentación y ajustar el alcance sin comprometer el lanzamiento comercial.

### 2.2 Pilares de Scrum

| Pilar | Aplicación en LicorExpress |
|:------|:---------------------------|
| **Transparencia** | El Product Backlog en GitHub Issues es visible para todo el equipo. |
| **Inspección** | Revisiones diarias del avance en el Sprint Board. |
| **Adaptación** | Re-priorización del backlog según feedback del negocio. |

### 2.3 Roles de Scrum

| Rol | Integrante | Responsabilidades |
|:----|:-----------|:------------------|
| **Desarollador** | [Luis felipe paredes] | Gestiona, prioriza y aclara la Pila de Producto (Product Backlog). |
| **Scrum Master** | [Santiago chamorro] | Líder servidor que elimina impedimentos y asegura la aplicación de Scrum. |
| **Equipo de Desarrollo** | [Yeferson pujimuy] | Profesional multifuncional que realiza análisis, diseño, codificación y pruebas. |

### 2.4 Artefactos de Scrum

- **Product Backlog:** Los 11 Issues en GitHub, ordenados por prioridad MoSCoW.
- **Sprint Backlog:** Subconjunto de Issues seleccionados para cada Sprint.
- **Incremento:** Software funcional entregado al final de cada Sprint.

### 2.5 Eventos o Ceremonias de Scrum

| Evento | Descripción |
|:-------|:------------|
| **Sprint Planning** | Selección de historias según prioridad y capacidad (12 SP). |
| **Daily Standup** | Reunión diaria de 15 min para sincronizar avance y bloqueos. |
| **Sprint Review** | Presentación del incremento y recepción de feedback. |
| **Sprint Retrospective** | Identificación de mejoras para el siguiente Sprint. |

---

## 3. Fórmulas de Planificación

### Fórmula 1: Velocidad del Equipo (V)

> **V = Puntos de Historia comprometidos por Sprint [SP/Sprint]**

### Fórmula 2: Duración en Sprints del MVP

> **n_Sprints = Σ SP Must Have ÷ V**

*(Si el resultado tiene decimales, se redondea hacia arriba.)*

### Fórmula 3: Tiempo Total de Desarrollo en Semanas

> **T_semanas = n_Sprints × Duración del Sprint (semanas)**

---

## 4. Parámetros del Proyecto LicorExpress

| Parámetro | Valor |
|:----------|:------|
| **Backlog completo** | 60 SP (11 Historias de Usuario) |
| **Historias Must Have (MVP)** | HU01, HU02, HU03, HU04, HU05, HU06, HU07 |
| **SP del MVP** | 39 SP |
| **Historias Should Have** | HU08, HU09, HU11 |
| **Historias Could Have** | HU10 |
| **Velocidad del equipo (V)** | 12 SP / Sprint |
| **Duración de cada Sprint** | 2 semanas |
| **Factor de conversión** | 8 horas / SP |
| **Tarifa profesional** | $45.000 COP / hora |

---

## 5. Cálculos del Plan de Proyecto

### 5.1 Cálculo de Sprints para el MVP

> **n_Sprints = 39 SP ÷ 12 SP/Sprint = 3.25 → 4 Sprints**

### 5.2 Cálculo del Tiempo de Desarrollo del MVP

> **T_semanas = 4 Sprints × 2 semanas = 8 semanas**

### 5.3 Cálculo de Sprints para el Proyecto Completo

> **n_Sprints = 60 SP ÷ 12 SP/Sprint = 5.0 → 5 Sprints**

### 5.4 Cálculo del Tiempo Total del Proyecto

> **T_semanas = 5 Sprints × 2 semanas = 10 semanas**

---

## 6. Distribución de Sprints (sin dividir historias)

> **Regla:** Ninguna Historia de Usuario se divide entre Sprints.

| Sprint | Trabajo Planificado | SP | Horas | Costo |
|:------:|:--------------------|:--:|:-----:|:------|
| **Sprint 1** (Sem. 1-2) | HU03 (3) + HU02 (5) + HU10 (3) | **11 SP** | 88 h | $3.960.000 |
| **Sprint 2** (Sem. 3-4) | HU01 (5) + HU06 (5) | **10 SP** | 80 h | $3.600.000 |
| **Sprint 3** (Sem. 5-6) | HU04 (5) + HU05 (8) | **13 SP** | 104 h | $4.680.000 |
| **Sprint 4** (Sem. 7-8) | HU07 (8) + HU11 (5) | **13 SP** | 104 h | $4.680.000 |
| **Sprint 5** (Sem. 9-10) | HU08 (8) + HU09 (5) | **13 SP** | 104 h | $4.680.000 |
| **TOTAL** | **Proyecto completo** | **60 SP** | **480 h** | **$21.600.000** |

### 6.1 Detalle de cada Sprint

#### Sprint 1 (Semanas 1-2) · Capacidad: 12 SP

| Historia | SP |
|:---------|:--:|
| HU03 - Registro e inicio de sesión | 3 |
| HU02 - Catálogo de productos por categorías | 5 |
| HU10 - Historial de pedidos del cliente | 3 |
| **Carga** | **11 SP** |

- **Esfuerzo:** 11 × 8 = **88 horas**
- **Costo:** 88 × $45.000 = **$3.960.000 COP**

#### Sprint 2 (Semanas 3-4) · Capacidad: 12 SP

| Historia | SP |
|:---------|:--:|
| HU01 - Verificación de mayoría de edad | 5 |
| HU06 - Gestión de inventario y stock | 5 |
| **Carga** | **10 SP** |

- **Esfuerzo:** 10 × 8 = **80 horas**
- **Costo:** 80 × $45.000 = **$3.600.000 COP**

#### Sprint 3 (Semanas 5-6) · Capacidad: 12 SP

| Historia | SP |
|:---------|:--:|
| HU04 - Carrito de compras | 5 |
| HU05 - Pago electrónico y contra entrega | 8 |
| **Carga** | **13 SP** |

- **Esfuerzo:** 13 × 8 = **104 horas**
- **Costo:** 104 × $45.000 = **$4.680.000 COP**

#### Sprint 4 (Semanas 7-8) · Capacidad: 12 SP

| Historia | SP |
|:---------|:--:|
| HU07 - Asignación de pedidos a domiciliarios | 8 |
| HU11 - Reportes de ventas y stock | 5 |
| **Carga** | **13 SP** |

- **Esfuerzo:** 13 × 8 = **104 horas**
- **Costo:** 104 × $45.000 = **$4.680.000 COP**

#### Sprint 5 (Semanas 9-10) · Capacidad: 12 SP

| Historia | SP |
|:---------|:--:|
| HU08 - Seguimiento del pedido en tiempo real | 8 |
| HU09 - Verificación de edad en la entrega | 5 |
| **Carga** | **13 SP** |

- **Esfuerzo:** 13 × 8 = **104 horas**
- **Costo:** 104 × $45.000 = **$4.680.000 COP**

---

## 7. Resumen Ejecutivo y Comercial Consolidado

### 7.1 MVP (Must Have)

| Concepto | Valor |
|:---------|:------|
| **Historias Must Have** | HU01, HU02, HU03, HU04, HU05, HU06, HU07 |
| **SP del MVP** | 39 SP |
| **Esfuerzo** | 312 horas |
| **Sprints requeridos** | 4 Sprints |
| **Duración** | 8 semanas |
| **Costo del MVP** | **$14.040.000 COP** |

### 7.2 Extensión (Should Have + Could Have)

| Concepto | Valor |
|:---------|:------|
| **Historias postergadas** | HU08, HU09, HU10, HU11 |
| **SP de extensión** | 21 SP |
| **Esfuerzo** | 168 horas |
| **Sprints adicionales** | 1 Sprint |
| **Duración adicional** | 2 semanas |
| **Costo de extensión** | **$7.560.000 COP** |

### 7.3 Proyecto Completo

| Concepto | Valor |
|:---------|:------|
| **Total SP** | 60 SP |
| **Esfuerzo total** | 480 horas |
| **Sprints totales** | 5 Sprints |
| **Duración total** | 10 semanas |
| **Costo total** | **$21.600.000 COP** |

---

## 8. Cronograma Visual

| Semana | Sprint | Historias | SP | Costo |
|:------:|:------:|:----------|:--:|:------|
| 1-2 | Sprint 1 | HU03, HU02, HU10 | 11 | $3.960.000 |
| 3-4 | Sprint 2 | HU01, HU06 | 10 | $3.600.000 |
| 5-6 | Sprint 3 | HU04, HU05 | 13 | $4.680.000 |
| 7-8 | Sprint 4 | HU07, HU11 | 13 | $4.680.000 |
| 9-10 | Sprint 5 | HU08, HU09 | 13 | $4.680.000 |
| **TOTAL** | **5 Sprints** | **11 historias** | **60** | **$21.600.000** |

---

## 9. Conclusiones

El backlog de LicorExpress contiene **11 Historias de Usuario** con un total de **60 Story Points**, equivalentes a **480 horas** y **$21.600.000 COP** bajo los parámetros establecidos por la asignatura.

El **MVP** está compuesto por **7 historias Must Have**, con **39 SP**, **312 horas** y **$14.040.000 COP**, y requiere **4 Sprints (8 semanas)**.

El **proyecto completo** requiere **5 Sprints (10 semanas)** con un presupuesto total de **$21.600.000 COP**.

La planificación con Scrum permite entregar valor de forma iterativa, priorizando las funcionalidades críticas del negocio (legalidad, recaudo y operatividad) y postergando las de experiencia de usuario sin comprometer la operación comercial.

---
