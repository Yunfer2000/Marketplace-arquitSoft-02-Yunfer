# Estilo arquitectónico

## Estilo seleccionado

El sistema utilizará un **Monolito Modular**.

El sistema se implementará como una única aplicación desplegable, organizada internamente en módulos independientes según las responsabilidades del negocio.

## Justificación

Se selecciona el estilo de Monolito Modular porque permite mantener una estructura organizada y modular, facilitando la evolución del sistema sin introducir inicialmente la complejidad de múltiples servicios desplegables.

Además, permite responder a los controladores de escalabilidad y mantenibilidad mediante una adecuada separación de módulos.

## Módulos principales

- Usuarios
- Catálogo
- Carrito
- Pedidos
- Pagos
- Envíos

## Características

- Una aplicación desplegable.
- Módulos separados por responsabilidad.
- Comunicación interna entre módulos.
- Posibilidad de evolución y escalamiento posterior.
- Separación de responsabilidades.
- Integración con servicios externos mediante adaptadores.

## Diagrama del estilo arquitectónico

```mermaid
graph TD

    APP["Marketplace - Monolito Modular"]

    APP --> USU["Módulo de Usuarios"]
    APP --> CAT["Módulo de Catálogo"]
    APP --> CAR["Módulo de Carrito"]
    APP --> PED["Módulo de Pedidos"]
    APP --> PAG["Módulo de Pagos"]
    APP --> ENV["Módulo de Envíos"]

    PAG --> EXT1["Pasarela de pago"]
    ENV --> EXT2["Servicio de envío"]