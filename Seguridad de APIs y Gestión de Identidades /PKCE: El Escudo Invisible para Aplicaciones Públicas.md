## Proof Key for Code Exchange (PKCE):
Las aplicaciones móviles o single-page-application SPA's, carecen de seguridad, el código JavaScript es visible
 
PKCE es una extensión de OAUTH 2.0 que resuelve esa vulnerabilidad. 
 
### ¿Como funciona? Este genera un secreto aleatorio, lo trasforma a SHA 256 y lo envía al server con la solicitud de autorización.
 
PKCE es obligatorio 
RFC 9700 establece que clientes públicos DEBEN usar PKCE. Si tu SPA o app móvil autentica sin PKCE, estás expuesto
