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

1.2 HPP

- Previene los denominados ataques HTTP Parameter Pollution
- Formato middleware
- ```GET /search?name=Foo&name=Bar```

2. Express Mongo Sanitize

- Previene inyecciones NoSQL en Mongo

explicación de los campos en el cuerpo de la solicitud:

"email": {"gt": ""}: Esta estructura parece estar utilizando un operador de consulta de MongoDB llamado "gt" (greater than, mayor que) dentro del campo "email". Sin embargo, hay un error de sintaxis en la estructura del JSON, ya que los corchetes de cierre están escritos incorrectamente (deberían ser corchetes rectos "]" en lugar de corchetes curvos "}").

"password": "123456": Este campo representa la contraseña proporcionada por el usuario para autenticarse en la API.

```
POST /api/login
    {
        "email": {"gt": ""},
        "password": "123456"
    }
``` 

2.1 Express Rate Limit

- Puede prevenir ataques DDoS y ataques de fuerza bruta
- Soporte para: Redis,Memcached,MongoDB y en memoria
- Formato middleware

Alternativas:

- Express Brute: Redis, Memcached, MongoDB, Mongoose, Sequelize, Knex, RethinkDB y Loki.js Implementación en paquetes separados

3. AUTENTICACION JWT

- JSON Web Token: estándar que define una forma segura de transmitir información
- Header: Contiene codificado el algoritmo de firma y el tipo de token
- Payload: contenido codificado en forma de clave-valor
- Signature: texto codificado que verifica la autenticidad del token

Algoritmos

HMAC: usando un secret
RSA: usando un par de claves pública/privada
ECDSA: usando un par de claves pública/privada

¿Como viaja el JWT?

- Cabecera de Authorization
- Autenticación Bearer, autenticacion por token
Creada como parte del protocolo OAuth 2.0

![image](https://github.com/Juandieruiz/Angular-NodeJS/assets/77864382/b76923ba-82d7-4339-9e32-6eb360754cfa)

JWT Payload

- Se compone de Claims, elementos de KV(Key-Value)
- Principales Claims:
    - iss: identifica al creador del token
    - iat: timestamp en formato unix de la fecha de creación
    - exp: timestamp en formato unix de la fecha de expiración
    - sub: identifica a quien ha pidio el token(normalmente mail)
    - aud: identifica al receptor, normalmente dirección web


- Podemos definir las nuestras para almacenar información
![image](https://github.com/Juandieruiz/Angular-NodeJS/assets/77864382/97a423b0-7574-4168-b6f3-e733e5edc807)

Debugger Web -> https://jwt.io/




