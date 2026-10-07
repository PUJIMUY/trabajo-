# Estimación Formal, Esfuerzo y Costos - LicorExpress

**Universidad Mariana**
**Ingeniería de Software I**
**Proyecto Transversal - Unidad 2**

**Equipo:**
- [Santiago chamorro] — Product Owner
- [Pujimuy yeferson ] — Desarrollador / Equipo de Desarrollo
- [luis felipe paredes] — Desarrollador / Equipo de Desarrollo
**Fecha:** 30 de septiembre de 2026

---

## 1. Organización del Equipo de Trabajo

| Integrante | Rol | Responsabilidades |
|:-----------|:----|:------------------|
| **[luis felipe paredes riascos]** | Desarrollador | Representa la voz del cliente. Explica el alcance de cada HU y verifica que la estimación respete las prioridades del negocio. |
| **[Santiago chamorro marinez]** | Scrum Master | Facilita el proceso Scrum, guía las discusiones de arquitectura, resuelve empates técnicos durante el Planning Poker y elimina impedimentos. |
| **[Pujimuy yeferson]** | Desarrollador | Evalúa el esfuerzo de codificación, integración con base de datos, lógica de negocio y pruebas necesarias para cada funcionalidad. |

---

## 2. Marco Teórico

### 2.1 Story Points (SP)

Un Story Point es una unidad abstracta de medida que evalúa la **Carga Global de Trabajo**:

> **SP = Complejidad Algorítmica + Volumen de Trabajo + Incertidumbre o Riesgo Técnico**

### 2.2 Planning Poker y Secuencia de Fibonacci

Se utiliza la secuencia modificada de Fibonacci: **1, 2, 3, 5, 8, 13, 21** porque la incertidumbre en ingeniería de software no escala linealmente, sino exponencialmente.

### 2.3 Historia Pivote

**HU03 — Registro e inicio de sesión = 3 SP**

Se selecciona como pivote por ser la historia más sencilla, clara y de menor incertidumbre técnica, basada principalmente en operaciones CRUD de autenticación.

### 2.4 Parámetros del Proyecto

| Parámetro | Valor |
|:----------|:------|
| **Factor de conversión (F_c)** | 8 horas / SP |
| **Tarifa profesional (T_h)** | $45.000 COP / hora |

---

## 3. Planning Poker — Justificación de Puntajes

| ID | Historia | SP | Justificación de Estimación |
|:--:|:---------|:--:|:----------------------------|
| HU01 | Verificación de mayoría de edad | **5** | Validación de documento, foto, OCR y reglas legales. |
| HU02 | Catálogo de productos por categorías | **5** | Consulta, filtros, paginación y control de stock en tiempo real. |
| HU03 | Registro e inicio de sesión | **3** | **Pivote:** CRUD de usuarios con autenticación JWT. |
| HU04 | Carrito de compras | **5** | Persistencia, validación de stock y cálculo del total. |
| HU05 | Pago electrónico y contra entrega | **8** | Integración con pasarela, múltiples métodos y estados de transacción. |
| HU06 | Gestión de inventario y stock | **5** | CRUD con alertas de stock mínimo y movimientos. |
| HU07 | Asignación de pedidos a domiciliarios | **8** | Algoritmo de cercanía, notificaciones y reasignación. |
| HU08 | Seguimiento del pedido en tiempo real | **8** | WebSockets, mapas y actualización cada 10 segundos. |
| HU09 | Verificación de edad en la entrega | **5** | Captura de documento en móvil, validación y registro. |
| HU10 | Historial de pedidos del cliente | **3** | Consultas paginadas y filtros. |
| HU11 | Reportes de ventas y stock | **5** | Consultas agregadas, gráficos y exportación. |

---

## 4. Matriz Consolidada de Estimación y Costos

| ID | Historia | MoSCoW | SP | F_c | Esfuerzo (h) | Tarifa | Costo (COP) | Complejidad |
|:--:|:---------|:------:|:--:|:---:|:------------:|:------:|:-----------:|:-----------:|
| HU01 | Verificación de mayoría de edad | Must Have | 5 | 8 h/SP | 40 h | $45.000 | $1.800.000 | Media |
| HU02 | Catálogo de productos por categorías | Must Have | 5 | 8 h/SP | 40 h | $45.000 | $1.800.000 | Baja |
| HU03 | Registro e inicio de sesión | Must Have | 3 | 8 h/SP | 24 h | $45.000 | $1.080.000 | Baja |
| HU04 | Carrito de compras | Must Have | 5 | 8 h/SP | 40 h | $45.000 | $1.800.000 | Media |
| HU05 | Pago electrónico y contra entrega | Must Have | 8 | 8 h/SP | 64 h | $45.000 | $2.880.000 | Alta |
| HU06 | Gestión de inventario y stock | Must Have | 5 | 8 h/SP | 40 h | $45.000 | $1.800.000 | Media |
| HU07 | Asignación de pedidos a domiciliarios | Must Have | 8 | 8 h/SP | 64 h | $45.000 | $2.880.000 | Alta |
| HU08 | Seguimiento del pedido en tiempo real | Should Have | 8 | 8 h/SP | 64 h | $45.000 | $2.880.000 | Alta |
| HU09 | Verificación de edad en la entrega | Should Have | 5 | 8 h/SP | 40 h | $45.000 | $1.800.000 | Media |
| HU10 | Historial de pedidos del cliente | Could Have | 3 | 8 h/SP | 24 h | $45.000 | $1.080.000 | Baja |
| HU11 | Reportes de ventas y stock | Should Have | 5 | 8 h/SP | 40 h | $45.000 | $1.800.000 | Media |
| **TOTAL** | **Backlog completo** | — | **60** | — | **480 h** | — | **$21.600.000** | — |

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

### HU01 — Verificación de mayoría de edad
- **E =** 5 SP × 8 h/SP = **40 horas**
- **C =** 40 h × $45.000 COP/h = **$1.800.000 COP**

### HU02 — Catálogo de productos por categorías
- **E =** 5 SP × 8 h/SP = **40 horas**
- **C =** 40 h × $45.000 COP/h = **$1.800.000 COP**

### HU03 — Registro e inicio de sesión *(Pivote)*
- **E =** 3 SP × 8 h/SP = **24 horas**
- **C =** 24 h × $45.000 COP/h = **$1.080.000 COP**

### HU04 — Carrito de compras
- **E =** 5 SP × 8 h/SP = **40 horas**
- **C =** 40 h × $45.000 COP/h = **$1.800.000 COP**

### HU05 — Pago electrónico y contra entrega
- **E =** 8 SP × 8 h/SP = **64 horas**
- **C =** 64 h × $45.000 COP/h = **$2.880.000 COP**

### HU06 — Gestión de inventario y stock
- **E =** 5 SP × 8 h/SP = **40 horas**
- **C =** 40 h × $45.000 COP/h = **$1.800.000 COP**

### HU07 — Asignación de pedidos a domiciliarios
- **E =** 8 SP × 8 h/SP = **64 horas**
- **C =** 64 h × $45.000 COP/h = **$2.880.000 COP**

### HU08 — Seguimiento del pedido en tiempo real
- **E =** 8 SP × 8 h/SP = **64 horas**
- **C =** 64 h × $45.000 COP/h = **$2.880.000 COP**

### HU09 — Verificación de edad en la entrega
- **E =** 5 SP × 8 h/SP = **40 horas**
- **C =** 40 h × $45.000 COP/h = **$1.800.000 COP**

### HU10 — Historial de pedidos del cliente
- **E =** 3 SP × 8 h/SP = **24 horas**
- **C =** 24 h × $45.000 COP/h = **$1.080.000 COP**

### HU11 — Reportes de ventas y stock
- **E =** 5 SP × 8 h/SP = **40 horas**
- **C =** 40 h × $45.000 COP/h = **$1.800.000 COP**

---

## 7. Sumatorias Globales

| Concepto | Cálculo | Resultado |
|:---------|:--------|:----------|
| **Total SP** | 5+5+3+5+8+5+8+8+5+3+5 | **60 SP** |
| **E_total** | 60 × 8 | **480 horas** |
| **C_total** | 480 × $45.000 | **$21.600.000 COP** |

---

## 8. Producto Mínimo Viable (MVP)

### 8.1 Historias Must Have

HU01, HU02, HU03, HU04, HU05, HU06, HU07

### 8.2 Estimación del MVP

| Concepto | Cálculo | Resultado |
|:---------|:--------|:----------|
| **SP del MVP** | 5+5+3+5+8+5+8 | **39 SP** |
| **Esfuerzo** | 39 × 8 | **312 horas** |
| **Costo** | 312 × $45.000 | **$14.040.000 COP** |

### 8.3 Historias Postergadas

HU08, HU09, HU10, HU11 = 21 SP, 168 horas, $7.560.000 COP

---

## 9. Títulos para GitHub Issues

| Issue | Título |
|:-----:|:-------|
| HU01 | `[5 SP] HU01 - Verificación de mayoría de edad` |
| HU02 | `[5 SP] HU02 - Catálogo de productos por categorías` |
| HU03 | `[3 SP] HU03 - Registro e inicio de sesión` |
| HU04 | `[5 SP] HU04 - Carrito de compras` |
| HU05 | `[8 SP] HU05 - Pago electrónico y contra entrega` |
| HU06 | `[5 SP] HU06 - Gestión de inventario y stock` |
| HU07 | `[8 SP] HU07 - Asignación de pedidos a domiciliarios` |
| HU08 | `[8 SP] HU08 - Seguimiento del pedido en tiempo real` |
| HU09 | `[5 SP] HU09 - Verificación de edad en la entrega` |
| HU10 | `[3 SP] HU10 - Historial de pedidos del cliente` |
| HU11 | `[5 SP] HU11 - Reportes de ventas y stock` |

---
