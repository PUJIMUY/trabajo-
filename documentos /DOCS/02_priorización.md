# Priorización MoSCoW y Estimación Empírica - TicketPass

**Universidad Mariana**
**Ingeniería de Software I**
**Proyecto Transversal - Unidad 2**

**Equipo:**
- Luis Felipe Paredes — Product Owner
- Yeferson Pujimuy — Scrum Master
- Santiago Chamorro — Desarrollador / Equipo de Desarrollo

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
| HU01 | Fila virtual para compra de boletos | **Must Have** | Operativo | Necesaria para la operación básica del MVP. Evita el colapso del servidor en picos de demanda. | Alta | 13 |
| HU02 | Generación de código QR dinámico | **Must Have** | Financiero y Seguridad | Necesaria para la operación básica del MVP. Protege el recaudo impidiendo falsificación. | Media | 5 |
| HU03 | Parametrización de zonas y precios | **Must Have** | Financiero | Necesaria para la operación básica del MVP. Habilita la configuración comercial del evento. | Baja | 2 |
| HU04 | Selección de boletos mediante mapa interactivo | **Should Have** | UX | Aporta valor visual, pero puede postergarse y sustituirse por un menú desplegable. | Alta | 8 |
| HU05 | Validación de boletos en punto de acceso | **Must Have** | Operativo | Necesaria para la operación básica del MVP. Permite el control de ingreso en puerta. | Baja-Media | 3 |
| HU06 | Registro de usuarios | **Must Have** | Operativo | Necesaria para la operación básica del MVP. Sin identidad no hay control de compras. | Baja-Media | 3 |
| HU07 | Catálogo de eventos | **Should Have** | UX | Aporta valor de descubrimiento, pero puede postergarse a una segunda iteración. | Media | 5 |
| HU08 | Pago de boletería | **Must Have** | Financiero | Necesaria para la operación básica del MVP. Sin pago no hay recaudo. | Media | 5 |
| HU09 | Historial de compras | **Could Have** | UX | Aporta valor de consulta posterior, pero puede postergarse. | Baja-Media | 3 |
| HU10 | Monitoreo de ventas y recaudo | **Should Have** | Financiero | Aporta valor para el organizador, pero puede postergarse a una segunda iteración. | Media | 5 |
| HU11 | Notificaciones de compra | **Could Have** | UX | Aporta valor de evidencia, pero puede postergarse. | Baja-Media | 3 |

**Total Backlog:** 55 SP

---

## 3. Producto Mínimo Viable (MVP)

### 3.1 Historias Must Have

| ID | Historia | SP |
|:--:|:---------|:--:|
| HU01 | Fila virtual para compra de boletos | 13 |
| HU02 | Generación de código QR dinámico | 5 |
| HU03 | Parametrización de zonas y precios | 2 |
| HU05 | Validación de boletos en punto de acceso | 3 |
| HU06 | Registro de usuarios | 3 |
| HU08 | Pago de boletería | 5 |
| | **TOTAL MVP** | **31 SP** |

### 3.2 Justificación del MVP

El MVP cubre las **tres dimensiones críticas del negocio**:

- **Operatividad:** HU01 (fila virtual) evita el colapso, HU05 (validación) controla el ingreso.
- **Recaudo financiero:** HU03 (parametrización) habilita la venta, HU08 (pago) concreta la transacción.
- **Identidad y seguridad:** HU02 (QR dinámico) protege la autenticidad, HU06 (registro) gestiona cuentas.

### 3.3 Estimación del MVP

| Concepto | Valor |
|:---------|:------|
| **SP del MVP** | 31 SP |
| **Esfuerzo** | 31 × 8 = 248 horas |
| **Costo** | 248 × $45.000 = **$11.160.000 COP** |

### 3.4 Funcionalidades Postergadas

| ID | Historia | MoSCoW | SP | Costo |
|:--:|:---------|:------:|:--:|:------|
| HU04 | Mapa interactivo | Should Have | 8 | $2.880.000 |
| HU07 | Catálogo de eventos | Should Have | 5 | $1.800.000 |
| HU09 | Historial de compras | Could Have | 3 | $1.080.000 |
| HU10 | Monitoreo de ventas | Should Have | 5 | $1.800.000 |
| HU11 | Notificaciones de compra | Could Have | 3 | $1.080.000 |
| | **TOTAL POSTERGADO** | | **24 SP** | **$8.640.000 COP** |

> **Nota:** La historia HU04 (Mapa Interactivo) se pospone para el siguiente ciclo de desarrollo, sustituyéndola temporalmente por una selección de zona mediante menú desplegable convencional.

---

## 4. Labels de GitHub

| Label | Color sugerido | Issues |
|:------|:---------------|:-------|
| `must-have` | Rojo | HU01, HU02, HU03, HU05, HU06, HU08 |
| `should-have` | Naranja | HU04, HU07, HU10 |
| `could-have` | Amarillo | HU09, HU11 |
| `wont-have` | Gris | Ninguna en la iteración actual |

---

## 5. Resumen de Priorización

| Categoría MoSCoW | Historias | Total SP |
|:----------------:|:----------|:--------:|
| Must Have | 6 | 31 |
| Should Have | 3 | 18 |
| Could Have | 2 | 6 |
| Won't Have | 0 | 0 |
| **TOTAL** | **11** | **55** |

---

**Fin del documento.**
