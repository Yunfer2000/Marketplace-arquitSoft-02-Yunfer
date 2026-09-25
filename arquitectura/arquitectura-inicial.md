# Arquitectura inicial del sistema

## Diagrama de arquitectura

```mermaid
flowchart TD

subgraph ACTORES["ACTORES"]
Cliente["Cliente"]
Seller["Seller"]
Admin["Administrador"]
end

subgraph PRESENTACION["PRESENTACIÓN"]
Web["Aplicación Web → API REST"]
end

subgraph NEGOCIO["LÓGICA DE NEGOCIO"]
Usuarios["Usuarios"]
Sellers["Sellers"]
Catalogo["Catálogo"]
Carrito["Carrito"]
Pedidos["Pedidos"]
end

subgraph DATOS["DATOS"]
BD["Base de datos"]
end

subgraph EXTERNOS["SISTEMAS EXTERNOS"]
Pago["Pasarela de pago"]
ERP["ERP"]
Envio["Servicio de envío"]
end

ACTORES --> PRESENTACION
PRESENTACION --> NEGOCIO
NEGOCIO --> DATOS

DATOS -->|"integraciones"| EXTERNOS

Cliente ~~~ Seller
Seller ~~~ Admin
Usuarios ~~~ Sellers
Sellers ~~~ Catalogo
Catalogo ~~~ Carrito
Carrito ~~~ Pedidos
Pago ~~~ ERP
ERP ~~~ Envio