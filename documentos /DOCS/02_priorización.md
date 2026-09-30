# Priorización MoSCoW y Estimación Empírica - LicorExpress

**Universidad Mariana**
**Ingeniería de Software I**
**Proyecto Transversal - Unidad 2**

**Equipo:**
- [Santiago chamorro] — Product Owner
- [Pujimuy yeferson ] — Desarrollador / Equipo de Desarrollo
- [luis felipe paredes] — Desarrollador / Equipo de Desarrollo

**Fecha:** 30 de septiembre de 2026

---

## 1. Marco Teórico

### 1.1 Valor de Negocio y Criterios de Impacto

El Valor de Negocio determina el beneficio estratégico, operativo o financiero que aporta una funcionalidad al sistema. Se analiza mediante tres criterios de impacto:

- **Impacto Operativo:** Garantiza la estabilidad, disponibilidad y funcionamiento continuo del servicio.
- **Impacto Financiero / Monetario:** Permite el recaudo, la transacción económica y la generación directa de ingresos.
- **Impacto en Experiencia de Usuario (UX):** Optimiza la usabilidad y la interacción visual.

### 1.2 Método MoSCoW

| Categoría | Significado |
|:---------:|:------------|
| **M — Must Have** | Imprescindible. Sin ellas el sistema no puede funcionar en producción. |
| **S — Should Have** | De alto valor, pero postergables para el lanzamiento inicial. |
| **C — Could Have** | Deseables o secundarias; solo si hay tiempo sobrante. |
| **W — Won't Have** | Fuera del alcance para la iteración actual. |

---

## 2. Matriz de Priorización

| ID | Historia de Usuario | MoSCoW | Impacto (Valor de Negocio) | Justificación Estratégica | Complejidad Empírica | SP |
|:--:|:--------------------|:------:|:--------------------------:|:--------------------------|:--------------------:|:--:|
| HU01 | Verificación de mayoría de edad | **Must Have** | Operativo / Legal | Necesaria para cumplir la normativa legal de venta de licor. Sin esto, el negocio es ilegal. | Media | 5 |
| HU02 | Catálogo de productos por categorías | **Must Have** | UX / Financiero | Necesaria para la operación básica. Sin catálogo no hay venta posible. | Baja | 5 |
| HU03 | Registro e inicio de sesión | **Must Have** | Operativo | Necesaria para la operación básica. Sin identidad no hay control de pedidos. | Baja | 3 |
| HU04 | Carrito de compras | **Must Have** | Financiero | Necesaria para la operación básica. Sin carrito no hay pedido. | Media | 5 |
| HU05 | Pago electrónico y contra entrega | **Must Have** | Financiero | Necesaria para la operación básica. Sin pago no hay recaudo. | Alta | 8 |
| HU06 | Gestión de inventario y stock | **Must Have** | Operativo | Necesaria para evitar pérdidas y controlar disponibilidad en tiempo real. | Media | 5 |
| HU07 | Asignación de pedidos a domiciliarios | **Must Have** | Operativo | Necesaria para gestionar los domicilios y coordinar entregas. | Alta | 8 |
| HU08 | Seguimiento del pedido en tiempo real | **Should Have** | UX | Aporta valor al cliente, pero puede postergarse usando notificaciones simples. | Alta | 8 |
| HU09 | Verificación de edad en la entrega | **Should Have** | Operativo / Legal | Refuerza la verificación legal en puerta, pero puede validarse con el perfil registrado. | Media | 5 |
| HU10 | Historial de pedidos del cliente | **Could Have** | UX | Aporta valor de recompra, pero puede postergarse. | Baja | 3 |
| HU11 | Reportes de ventas y stock | **Should Have** | Financiero | Aporta valor para decisiones gerenciales, pero puede postergarse. | Media | 5 |

**Total Backlog:** 60 SP

---

## 3. Producto Mínimo Viable (MVP)

### 3.1 Historias Must Have

| ID | Historia | SP |
|:--:|:---------|:--:|
| HU01 | Verificación de mayoría de edad | 5 |
| HU02 | Catálogo de productos por categorías | 5 |
| HU03 | Registro e inicio de sesión | 3 |
| HU04 | Carrito de compras | 5 |
| HU05 | Pago electrónico y contra entrega | 8 |
| HU06 | Gestión de inventario y stock | 5 |
| HU07 | Asignación de pedidos a domiciliarios | 8 |
| | **TOTAL MVP** | **39 SP** |

### 3.2 Justificación del MVP

El MVP cubre las **tres dimensiones críticas del negocio**:

- **Legalidad:** HU01 (verificación de edad) cumple la normativa legal de venta de licor.
- **Recaudo financiero:** HU02 (catálogo), HU04 (carrito) y HU05 (pago) habilitan la transacción.
- **Operatividad:** HU03 (registro), HU06 (inventario) y HU07 (asignación) permiten gestionar pedidos y stock.

### 3.3 Estimación del MVP

| Concepto | Valor |
|:---------|:------|
| **SP del MVP** | 39 SP |
| **Esfuerzo** | 39 × 8 = 312 horas |
| **Costo** | 312 × $45.000 = **$14.040.000 COP** |

### 3.4 Funcionalidades Postergadas

| ID | Historia | MoSCoW | SP | Costo |
|:--:|:---------|:------:|:--:|:------|
| HU08 | Seguimiento en tiempo real | Should Have | 8 | $2.880.000 |
| HU09 | Verificación edad en entrega | Should Have | 5 | $1.800.000 |
| HU10 | Historial de pedidos | Could Have | 3 | $1.080.000 |
| HU11 | Reportes de ventas y stock | Should Have | 5 | $1.800.000 |
| | **TOTAL POSTERGADO** | | **21 SP** | **$7.560.000 COP** |

> **Nota:** El seguimiento en tiempo real (HU08) se pospone para el siguiente ciclo, sustituyéndolo temporalmente por notificaciones push y por WhatsApp en cada cambio de estado.

---

## 4. Labels de GitHub

| Label | Color sugerido | Issues |
|:------|:---------------|:-------|
| `must-have` | Rojo | HU01, HU02, HU03, HU04, HU05, HU06, HU07 |
| `should-have` | Naranja | HU08, HU09, HU11 |
| `could-have` | Amarillo | HU10 |
| `wont-have` | Gris | Ninguna en la iteración actual |

---

## 5. Resumen de Priorización

| Categoría MoSCoW | Historias | Total SP |
|:----------------:|:----------|:--------:|
| Must Have | 7 | 39 |
| Should Have | 3 | 18 |
| Could Have | 1 | 3 |
| Won't Have | 0 | 0 |
| **TOTAL** | **11** | **60** |

---
