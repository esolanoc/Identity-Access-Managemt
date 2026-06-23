Cuando un usuario decide autenticarse sobre una app protegida por LDAP, ocurre una secuencia precisa llamada Operación Bind (enlace).

### El DSA Directory System Agent es el servidor LDAP - el cliente envía una solicitud de bind que contiene tres elementos, la versión del protocolo LDAP, el DN Distinguished Name y las credenciales del usuario

## 🔑 Existen dos tipos de Bind

Bind simple: Envía el DN y los credenciales, debe de usarse TLS por seguridad 
SASL Simple Authentication and Security layer: usa un marco extensible que permite integrar mecanismos como Kerberos o certificados digitales ofreciendo autenticación más robusta para la empresa
