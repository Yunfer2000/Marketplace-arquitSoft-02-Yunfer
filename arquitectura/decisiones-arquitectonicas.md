# Decisiones arquitectónicas

## ADR-001 — Monolito modular

| Elemento | Descripción |
|---|---|
| ID | ADR-001 |
| Decisión arquitectónica | Monolito modular |
| Driver relacionado | DA01 - Escalabilidad; DA06 - Mantenibilidad |
| Justificación | Organizar las funcionalidades en módulos independientes dentro de una misma aplicación desplegable. |
| Resultado | Módulos de Catálogo, Carrito, Pedidos, Pagos y Usuarios. |

---

## ADR-002 — Clean Architecture

| Elemento | Descripción |
|---|---|
| ID | ADR-002 |
| Decisión arquitectónica | Clean Architecture |
| Driver relacionado | DA06 - Mantenibilidad |
| Justificación | Separar las reglas del negocio de los detalles tecnológicos. |
| Resultado | Capas de Dominio, Aplicación, Infraestructura y Presentación. |

---

## ADR-003 — Estrategia de caché

| Elemento | Descripción |
|---|---|
| ID | ADR-003 |
| Decisión arquitectónica | Estrategia de caché |
| Driver relacionado | DA02 - Rendimiento |
| Justificación | Reducir consultas repetitivas a la fuente de datos y mejorar los tiempos de respuesta. |
| Resultado | Caché para información de consulta frecuente. |

---

## ADR-004 — Integración de pagos mediante interfaces y adaptadores

| Elemento | Descripción |
|---|---|
| ID | ADR-004 |
| Decisión arquitectónica | Integración de pagos mediante interfaces y adaptadores |
| Driver relacionado | DA04 - Integración con pagos |
| Justificación | Desacoplar los casos de uso del proveedor de pagos. |
| Resultado | Contrato de pagos y adaptador para la pasarela externa. |

---

## ADR-005 — API REST

| Elemento | Descripción |
|---|---|
| ID | ADR-005 |
| Decisión arquitectónica | Comunicación mediante API REST |
| Driver relacionado | DA05 - API REST |
| Justificación | Separar la interfaz de usuario de los servicios del sistema mediante una interfaz de comunicación estándar. |
| Resultado | Comunicación entre frontend y backend mediante API REST. |