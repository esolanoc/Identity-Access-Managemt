Cuando un usaurio decide autenticarse sobre una app protegida por LDAP, ocurre una secuencia precisa llamada Operacion Bind (enlace). 

### El DSA Directory System Agent es el servidor LDAP - el cliente envia una solictiud de bine que contiene tres elementos, la version del protocolo LDAP,  el DN Distinguished Name y las credenciales del usuario

## 🔑 Existen dos tipos de Bind

Bind simple: Envia el DN y los credenciales, debe de usarse TLS por seguridad
SASL Simple Authentication and Security layer: usa un marco extensible que permite integrar mecanismos como Kerberos o certificados digitales ofrecendp authenticacion mas robusta para la empresa
