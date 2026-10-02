# Enfoque arquitectónico

## Clean Architecture

El sistema utilizará el enfoque de **Clean Architecture** para organizar las responsabilidades y controlar las dependencias entre las diferentes partes de la aplicación.

El objetivo principal es mantener las reglas del negocio independientes de los detalles tecnológicos, como frameworks, bases de datos, interfaces de usuario y servicios externos.

## Capas

### 1. Dominio

Contiene las entidades, modelos y reglas principales del negocio.

Ejemplos:

- Producto
- Carrito
- Pedido
- Reglas de negocio
- Contratos necesarios para interactuar con elementos externos

El dominio debe ser independiente de frameworks y tecnologías externas.

### 2. Aplicación

Contiene los casos de uso que representan las operaciones que el sistema debe realizar.

Ejemplos:

- Consultar catálogo
- Agregar producto al carrito
- Registrar compra

Los casos de uso utilizan las reglas y contratos definidos por el dominio.

### 3. Infraestructura

Contiene las implementaciones concretas de los contratos definidos por el dominio.

Ejemplos:

- Repositorios de productos
- Repositorios de pedidos
- Procesadores de pagos
- Servicios de notificación
- Conexiones con servicios externos

### 4. Presentación

Contiene los componentes mediante los cuales el usuario interactúa con el sistema.

Ejemplos:

- Catálogo
- Carrito
- Formularios
- Interfaces de usuario

## Regla de dependencias

Las dependencias deben apuntar hacia las capas internas.

```text
PRESENTACIÓN
      │
      ▼
APLICACIÓN
      │
      ▼
DOMINIO
      ▲
      │
INFRAESTRUCTURA