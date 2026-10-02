# Drivers arquitectónicos

| ID | Driver arquitectónico | Origen | ¿Por qué influye en la arquitectura? |
|---|---|---|---|
| DA01 | Escalabilidad | AC03 - Escalabilidad | El sistema debe soportar un incremento importante de usuarios durante campañas comerciales. |
| DA02 | Rendimiento | AC01 - Rendimiento | El sistema debe mantener tiempos de respuesta adecuados durante alta concurrencia. |
| DA03 | Seguridad | AC02 - Seguridad | El sistema debe proteger los datos de usuarios y las operaciones de compra. |
| DA04 | Integración con pagos | RF06 - Pago externo | El sistema debe integrarse con una pasarela de pago externa. |
| DA05 | API REST | RNF05 - API REST | La comunicación entre frontend y backend debe realizarse mediante una API REST. |
| DA06 | Mantenibilidad | AC04 - Mantenibilidad | La arquitectura debe facilitar el mantenimiento y evolución del sistema. |