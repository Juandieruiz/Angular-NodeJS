# Angular-NodeJS
Babel University Formation

Introducción

- NVM
- Helmet
    - Diseñado para Express
    - Configura las cabeceras de respuesta HTTP
    - Previene por defecto multitud de ataques
    - Formato MiddleWare

1. Helmet se encarga de recibir respuestas y añadir o eliminar cabeceras en la peticion HTTPS que esten deprecadas o sean necesarias.
- Content-Security-Policy
- X-Content-Type-Options
- X-Frame-Options
- Content-Security-Policy

1.1. Configuración de Helmet

- Uso de configuración por defecto
- Configuracion especifica por encabezado

Example: https://securityheaders.com/

- Prueba de sitios web y análisis de cualquier página web, respecto a terminos en el Header y posibles Cabeceras que tengan vulnerabilidades

1.2. Express Content Length Validator

- Impide los denominados ataques "Large Payload"
- Puede replicarse sin mucha dificultad, pero... no reinventes la rueda


