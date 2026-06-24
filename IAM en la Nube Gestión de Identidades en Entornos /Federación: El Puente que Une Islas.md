## La federación de identidades:
Es el mecanismo que permite crear confianza entre proveedores de identidad (IdP) separados. En un mundo multi-cloud, significa que un empleado puede autenticarse una sola vez en el sistema corporativo (Azure AD, Okta, Ping Identity) y obtener acceso automatizado a recursos en AWS, GCP o Azure sin necesidad de credenciales adicionales.

El proceso funciona mediante protocolos estándar como SAML 2.0 o OpenID Connect (OIDC). Cuando un usuario solicita acceso a un recurso cloud, el Service Provider (la nube destino) redirige al IdP corporativo. Tras la autenticación exitosa, el IdP emite un token firmado que contiene claims sobre la identidad del usuario, grupos a los que pertenece y atributos relevantes.
El Service Provider evalúa estas claims contra roles predefinidos y otorga acceso conforme a las políticas mapeadas.

AWS IAM Identity Center (anteriormente AWS SSO), Azure AD single sign-on y Google Cloud Workload Identity Federation son los servicios SSO nativos que cada proveedor ofrece para facilitar esta integración.
