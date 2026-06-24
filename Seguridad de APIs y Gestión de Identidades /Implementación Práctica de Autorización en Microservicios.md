##  Autenticación en el Edge
El API Gateway verifica el token JWT (firma, expiración, issuer). Extrae claims de identidad (user_id, roles) y los adjunta como headers estandarizados antes de reenviar la solicitud al microservicio.

##  Passthrough de Contexto
El gateway añade headers como X-User-ID o X-Roles que el microservicio consume para decisiones de autorización. El microservicio NO revalida el token contra el IdP; confía en el gateway pero aplica sus propias reglas de negocio.

##  Autorización de Grano Grueso
En el gateway, valida scopes de OAuth y roles generales. Si la solicitud carece del scope invoices:read, recházala inmediatamente. Esto filtra tráfico no autorizado antes de que llegue a los servicios.

##  Autorización de Grano Fino
Dentro del microservicio, verifica BOLA: "¿El usuario 123 tiene permiso para ver la factura 456?" Comprueba propiedad del recurso en la base de datos. La combinación de ambas capas es defense in depth.

