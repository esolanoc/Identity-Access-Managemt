Mientras SAML dominaba la era de las aplicaciones web monolíticas empresariales, la revolución móvil y las APIs demandaban algo más ligero. 

## 🚀 OAuth 2.0:
Publicado en 2012, nació como un framework de autorización, no de autenticación. Su propósito original era permitir que aplicaciones de terceros actuaran en nombre de usuarios sin obtener sus contraseñas.
Imagina una aplicación de fitness que necesita acceder a tus fotos de Google Photos para crear un collage de tu progreso. OAuth 2.0 permite que Google emita un Access Token con alcance limitado (solo fotos, solo lectura) sin revelar tu contraseña. La app nunca ve tu credencial, solo el token temporal. Este es el flujo que usas cada vez que una aplicación pide "Iniciar sesión con Google" o "Continuar con Facebook".
Pero OAuth 2.0 no define quién eres, solo qué puedes hacer.

## 🛡️ OpenID Connect (OIDC), una capa de identidad construida sobre OAuth 2.0: 
Publicada en 2014. OIDC introduce el ID Token: un JWT (JSON Web Token) que contiene claims sobre tu identidad (sub, name, email, picture). Mientras SAML usa SOAP y XML, OIDC usa REST y JSON, haciéndolo ideal para aplicaciones móviles, SPAs (Single Page Applications) y APIs.
La diferencia de implementación es profunda: SAML requiere intercambio manual de metadatos XML y certificados X.509. OIDC usa Discovery dinámico: conoces la URL del IdP (como https://accounts.google.com) y la aplicación descubre automáticamente los endpoints disponibles consultando /.well-known/openid-configuration. Las claves para verificar tokens se obtienen dinámicamente como JSON Web Keys (JWK), permitiendo rotación sin intervención manual.
