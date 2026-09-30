# Documento de Especificación de Requisitos - LicorExpress

**Universidad Mariana**
**Ingeniería de Software I**
**Proyecto Transversal - Unidad 2**

**Equipo:**
- [uis felipe paredes riascos— Desarrollador / Equipo de Desarrollo
- [Santiago chamorro marinez] — Scrum Master
- [Pujimuy yeferson — Desarrollador / Equipo de Desarrollo
**Fecha:** 30 de septiembre de 2026

---

## 1. Contextualización del Proyecto

LicorExpress es una plataforma web para la comercialización y domicilio de bebidas alcohólicas en ciudades de alta demanda. El sistema busca resolver problemas de control de inventario, verificación de edad para la venta de licor, gestión de pedidos a domicilio, y falta de información para los dueños sobre ventas y productos más solicitados.

### Problemas reales que resuelve:
- Venta de licor a menores de edad sin verificación adecuada.
- Pérdida de inventario por falta de control de stock en tiempo real.
- Pedidos mal gestionados y sin seguimiento ni coordinación con repartidores.
- Falta de reportes para tomar decisiones de compra y ventas.
- Domiciliarios entregan licor sin verificar edad en la puerta.

---

## 2. Actores Principales del Sistema

| # | Actor | Descripción |
|:-:|:------|:------------|
| **1** | **Cliente / Comprador** | Usuario final que explora el catálogo, verifica su edad, agrega productos al carrito, paga y recibe su pedido a domicilio. |
| **2** | **Administrador / Dueño de Licorería** | Gestiona el inventario, precios, promociones, pedidos y consulta reportes de ventas y stock. |
| **3** | **Domiciliario / Repartidor** | Recibe pedidos asignados, actualiza el estado de entrega, confirma ubicación y entrega el pedido verificando edad en la puerta. |

---

## 3. Matriz de Transformación: Problemas, Necesidades y Requisitos Funcionales

| # | Problema Identificado | Necesidad de Software | Requisito Funcional |
|:-:|:----------------------|:----------------------|:--------------------|
| **1** | Venta de licor a menores de edad sin verificación adecuada. | Validar la mayoría de edad del comprador antes de la venta. | El sistema debe solicitar y validar documento de identidad o selfie con cédula antes de confirmar la compra. |
| **2** | Pérdida de inventario por falta de control de stock en tiempo real. | Registrar y actualizar automáticamente el stock de cada producto. | El sistema debe descontar del inventario cada producto vendido y alertar cuando el stock esté por debajo del mínimo. |
| **3** | Pedidos a domicilio sin seguimiento ni coordinación con repartidores. | Asignar pedidos a repartidores y rastrear el estado en tiempo real. | El sistema debe asignar el pedido al repartidor disponible más cercano y mostrar el estado (preparando, en camino, entregado). |
| **4** | Falta de reportes para decisiones de compra y ventas. | Generar indicadores de ventas, productos más vendidos y stock. | El sistema debe mostrar reportes de ventas por día, semana y mes, con los productos más y menos vendidos. |
| **5** | Domiciliarios entregan licor sin verificar edad en la puerta. | Verificar edad al momento de la entrega. | El sistema debe permitir al repartidor escanear el documento del cliente o registrar la verificación antes de completar la entrega. |
| **6** | Clientes no saben si su pedido está en camino. | Notificar al cliente cada cambio de estado. | El sistema debe enviar notificaciones push y por WhatsApp en cada cambio de estado del pedido. |
| **7** | Proceso de pago lento y sin opciones. | Ofrecer múltiples métodos de pago electrónico. | El sistema debe permitir pago con tarjeta, PSE, Nequi y contra entrega. |
| **8** | Falta de catálogo organizado por categorías. | Publicar catálogo digital con búsqueda y filtros. | El sistema debe mostrar productos organizados por categoría (cervezas, vinos, licores, mixers) con búsqueda y filtros. |

---

## 4. Historias de Usuario (Backlog)

> **Nota:** El backlog completo con las 11 Historias de Usuario, su priorización MoSCoW y estimación se encuentra en los archivos:
> - `DOCS/02_priorizacion.md`
> - `DOCS/03_estimacion_y_costos.md`

### Resumen del Backlog

| ID | Historia de Usuario | MoSCoW | SP |
|:--:|:--------------------|:------:|:--:|
| HU01 | Verificación de mayoría de edad | Must Have | 5 |
| HU02 | Catálogo de productos por categorías | Must Have | 5 |
| HU03 | Registro e inicio de sesión | Must Have | 3 |
| HU04 | Carrito de compras | Must Have | 5 |
| HU05 | Pago electrónico y contra entrega | Must Have | 8 |
| HU06 | Gestión de inventario y stock | Must Have | 5 |
| HU07 | Asignación de pedidos a domiciliarios | Must Have | 8 |
| HU08 | Seguimiento del pedido en tiempo real | Should Have | 8 |
| HU09 | Verificación de edad en la entrega | Should Have | 5 |
| HU10 | Historial de pedidos del cliente | Could Have | 3 |
| HU11 | Reportes de ventas y stock | Should Have | 5 |
| | **TOTAL** | | **60 SP** |

---

## 5. Criterios de Aceptación (INVEST)

Cada Historia de Usuario cuenta con mínimo 3 criterios de aceptación verificables mediante casillas de verificación (`- [ ]`), los cuales se encuentran documentados en cada Issue de GitHub.

### Ejemplo — HU01: Verificación de mayoría de edad

**Como** cliente
**Quiero** verificar mi mayoría de edad antes de comprar
**Para** cumplir con la normativa legal de venta de licor

**Criterios de Aceptación:**
- [ ] El sistema solicita fecha de nacimiento al registrarse
- [ ] Se valida que el usuario sea mayor de 18 años
- [ ] Se solicita foto del documento de identidad para validación
- [ ] Si el usuario es menor, se bloquea el acceso a la compra
- [ ] La verificación se guarda en el perfil del usuario

---

## 6. Roles del Equipo

| Integrante | Rol | Responsabilidades |
|:-----------|:----|:------------------|
| **[Nombre 1]** | Product Owner | Gestionar y priorizar el Product Backlog, representar el valor del producto y definir prioridades. |
| **[Nombre 2]** | Scrum Master | Facilitar Scrum, apoyar al equipo, eliminar impedimentos y promover el cumplimiento del proceso. |
| **[Nombre 3]** | Desarrollador / Equipo de Desarrollo | Diseñar, construir, probar e integrar las funcionalidades del producto. |

---

## 7. Modelo de Proceso

Se selecciona **Scrum** porque LicorExpress es una plataforma comercial que puede desarrollarse de forma iterativa, entregando primero las funcionalidades críticas (MVP) y posteriormente las funcionalidades de experiencia y administración.

- **Velocidad del equipo:** 12 SP por Sprint
- **Duración de cada Sprint:** 2 semanas
- **Duración estimada:** 5 Sprints / 10 semanas

---

## 8. Estimación Global

| Concepto | Valor |
|:---------|:------|
| **Total Story Points** | 60 SP |
| **Factor de conversión** | 8 horas / SP |
| **Esfuerzo total** | 480 horas |
| **Tarifa profesional** | $45.000 COP / hora |
| **Costo estimado total** | $21.600.000 COP |

---

