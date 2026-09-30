# Estimación Formal, Esfuerzo y Costos - TicketPass

**Universidad Mariana**
**Ingeniería de Software I**
**Proyecto Transversal - Unidad 2**

**Equipo:**
- Luis Felipe Paredes — Product Owner
- Yeferson Pujimuy — Scrum Master
- Santiago Chamorro — Desarrollador / Equipo de Desarrollo

**Fecha:** 30 de septiembre de 2026

---

## 1. Organización del Equipo de Trabajo

| Integrante | Rol | Responsabilidades |
|:-----------|:----|:------------------|
| **Luis Felipe Paredes** | Product Owner (PO) | Representa la voz del cliente. Explica el alcance de cada HU y verifica que la estimación respete las prioridades del negocio. |
| **Yeferson Pujimuy** | Scrum Master | Facilita el proceso Scrum, guía las discusiones de arquitectura, resuelve empates técnicos durante el Planning Poker y elimina impedimentos. |
| **Santiago Chamorro** | Desarrollador | Evalúa el esfuerzo de codificación, integración con base de datos, lógica de negocio y pruebas necesarias para cada funcionalidad. |

---

## 2. Marco Teórico

### 2.1 Story Points (SP)

Un Story Point es una unidad abstracta de medida que evalúa la **Carga Global de Trabajo**:

> **SP = Complejidad Algorítmica + Volumen de Trabajo + Incertidumbre o Riesgo Técnico**

### 2.2 Planning Poker y Secuencia de Fibonacci

Se utiliza la secuencia modificada de Fibonacci: **1, 2, 3, 5, 8, 13, 20** porque la incertidumbre en ingeniería de software no escala linealmente, sino exponencialmente.

### 2.3 Historia Pivote

**HU03 — Parametrización de Zonas y Precios = 2 SP**

Se selecciona como pivote por ser la historia más sencilla, clara y de menor incertidumbre técnica, basada principalmente en operaciones CRUD (Crear, Leer, Actualizar, Eliminar).

### 2.4 Parámetros del Proyecto

| Parámetro | Valor |
|:----------|:------|
| **Factor de conversión (F_c)** | 8 horas / SP |
| **Tarifa profesional (T_h)** | $45.000 COP / hora |

---

## 3. Planning Poker — Justificación de Puntajes

| ID | Historia | SP | Justificación de Estimación |
|:--:|:---------|:--:|:----------------------------|
| HU01 | Fila virtual para compra de boletos | **13** | Muy alta complejidad por concurrencia masiva, colas distribuidas y riesgo de infraestructura. |
| HU02 | Generación de código QR dinámico | **5** | Mayor que la pivote por cifrado simétrico, temporalidad y generación dinámica de imágenes. |
| HU03 | Parametrización de zonas y precios | **2** | **Pivote:** CRUD de zonas, aforos y precios. |
| HU04 | Mapa interactivo del recinto | **8** | Interfaz gráfica interactiva con SVG y actualización de disponibilidad en tiempo real. |
| HU05 | Validación de boletos en punto de acceso | **3** | Cámara, API REST y validación de estado en caché. |
| HU06 | Registro de usuarios | **3** | Autenticación JWT, validación de credenciales y hash de contraseñas. |
| HU07 | Catálogo de eventos | **5** | Consulta, filtros, paginación y disponibilidad de eventos. |
| HU08 | Pago de boletería | **5** | Carrito, reservas temporales, integración con pasarela y cálculo del total. |
| HU09 | Historial de compras | **3** | Consulta de órdenes y recuperación de entradas asociadas. |
| HU10 | Monitoreo de ventas y recaudo | **5** | Consultas agregadas, indicadores y control de acceso por rol. |
| HU11 | Notificaciones de compra | **3** | Generación de confirmación y consulta posterior desde la cuenta. |

---

## 4. Matriz Consolidada de Estimación y Costos

| ID | Historia | MoSCoW | SP | F_c | Esfuerzo (h) | Tarifa | Costo (COP) | Complejidad |
|:--:|:---------|:------:|:--:|:---:|:------------:|:------:|:-----------:|:-----------:|
| HU01 | Fila virtual para compra de boletos | Must Have | 13 | 8 h/SP | 104 h | $45.000 | $4.680.000 | Alta |
| HU02 | Generación de código QR dinámico | Must Have | 5 | 8 h/SP | 40 h | $45.000 | $1.800.000 | Media |
| HU03 | Parametrización de zonas y precios | Must Have | 2 | 8 h/SP | 16 h | $45.000 | $720.000 | Baja |
| HU04 | Mapa interactivo del recinto | Should Have | 8 | 8 h/SP | 64 h | $45.000 | $2.880.000 | Alta |
| HU05 | Validación de boletos en punto de acceso | Must Have | 3 | 8 h/SP | 24 h | $45.000 | $1.080.000 | Baja-Media |
| HU06 | Registro de usuarios | Must Have | 3 | 8 h/SP | 24 h | $45.000 | $1.080.000 | Baja-Media |
| HU07 | Catálogo de eventos | Should Have | 5 | 8 h/SP | 40 h | $45.000 | $1.800.000 | Media |
| HU08 | Pago de boletería | Must Have | 5 | 8 h/SP | 40 h | $45.000 | $1.800.000 | Media |
| HU09 | Historial de compras | Could Have | 3 | 8 h/SP | 24 h | $45.000 | $1.080.000 | Baja-Media |
| HU10 | Monitoreo de ventas y recaudo | Should Have | 5 | 8 h/SP | 40 h | $45.000 | $1.800.000 | Media |
| HU11 | Notificaciones de compra | Could Have | 3 | 8 h/SP | 24 h | $45.000 | $1.080.000 | Baja-Media |
| **TOTAL** | **Backlog completo** | — | **55** | — | **440 h** | — | **$19.800.000** | — |

---

## 5. Fórmulas Aplicadas

### Fórmula 1: Esfuerzo de Desarrollo en Horas

> **E_i = SP_i × F_c**

Donde F_c = 8 horas/SP.

### Fórmula 2: Costo Financiero por Historia

> **C_i = E_i × T_h**

Donde T_h = $45.000 COP/hora.

### Fórmula 3: Sumatorias Totales del Proyecto

> **E_total = Σ E_i**
> **C_total = Σ C_i**

---

## 6. Cálculos Paso a Paso por Historia

### HU01 — Fila virtual para compra de boletos
- **E =** 13 SP × 8 h/SP = **104 horas**
- **C =** 104 h × $45.000 COP/h = **$4.680.000 COP**

### HU02 — Generación de código QR dinámico
- **E =** 5 SP × 8 h/SP = **40 horas**
- **C =** 40 h × $45.000 COP/h = **$1.800.000 COP**

### HU03 — Parametrización de zonas y precios *(Pivote)*
- **E =** 2 SP × 8 h/SP = **16 horas**
- **C =** 16 h × $45.000 COP/h = **$720.000 COP**

### HU04 — Mapa interactivo del recinto
- **E =** 8 SP × 8 h/SP = **64 horas**
- **C =** 64 h × $45.000 COP/h = **$2.880.000 COP**

### HU05 — Validación de boletos en punto de acceso
- **E =** 3 SP × 8 h/SP = **24 horas**
- **C =** 24 h × $45.000 COP/h = **$1.080.000 COP**

### HU06 — Registro de usuarios
- **E =** 3 SP × 8 h/SP = **24 horas**
- **C =** 24 h × $45.000 COP/h = **$1.080.000 COP**

### HU07 — Catálogo de eventos
- **E =** 5 SP × 8 h/SP = **40 horas**
- **C =** 40 h × $45.000 COP/h = **$1.800.000 COP**

### HU08 — Pago de boletería
- **E =** 5 SP × 8 h/SP = **40 horas**
- **C =** 40 h × $45.000 COP/h = **$1.800.000 COP**

### HU09 — Historial de compras
- **E =** 3 SP × 8 h/SP = **24 horas**
- **C =** 24 h × $45.000 COP/h = **$1.080.000 COP**

### HU10 — Monitoreo de ventas y recaudo
- **E =** 5 SP × 8 h/SP = **40 horas**
- **C =** 40 h × $45.000 COP/h = **$1.800.000 COP**

### HU11 — Notificaciones de compra
- **E =** 3 SP × 8 h/SP = **24 horas**
- **C =** 24 h × $45.000 COP/h = **$1.080.000 COP**

---

## 7. Sumatorias Globales

| Concepto | Cálculo | Resultado |
|:---------|:--------|:----------|
| **Total SP** | 13+5+2+8+3+3+5+5+3+5+3 | **55 SP** |
| **E_total** | 55 × 8 | **440 horas** |
| **C_total** | 440 × $45.000 | **$19.800.000 COP** |

---

## 8. Producto Mínimo Viable (MVP)

### 8.1 Historias Must Have

HU01, HU02, HU03, HU05, HU06, HU08

### 8.2 Estimación del MVP

| Concepto | Cálculo | Resultado |
|:---------|:--------|:----------|
| **SP del MVP** | 13+5+2+3+3+5 | **31 SP** |
| **Esfuerzo** | 31 × 8 | **248 horas** |
| **Costo** | 248 × $45.000 | **$11.160.000 COP** |

### 8.3 Historias Postergadas

HU04, HU07, HU09, HU10, HU11 = 24 SP, 192 horas, $8.640.000 COP

---

## 9. Títulos para GitHub Issues

| Issue | Título |
|:-----:|:-------|
| HU01 | `[13 SP] HU01 - Fila virtual para compra de boletos` |
| HU02 | `[5 SP] HU02 - Generación de código QR dinámico` |
| HU03 | `[2 SP] HU03 - Parametrización de zonas y precios` |
| HU04 | `[8 SP] HU04 - Selección de boletos mediante mapa interactivo` |
| HU05 | `[3 SP] HU05 - Validación de boletos en punto de acceso` |
| HU06 | `[3 SP] HU06 - Registro de usuarios` |
| HU07 | `[5 SP] HU07 - Catálogo de eventos` |
| HU08 | `[5 SP] HU08 - Pago de boletería` |
| HU09 | `[3 SP] HU09 - Historial de compras` |
| HU10 | `[5 SP] HU10 - Monitoreo de ventas y recaudo` |
| HU11 | `[3 SP] HU11 - Notificaciones de compra` |

---

