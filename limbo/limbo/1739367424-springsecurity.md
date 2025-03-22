---
id: 1739367424-springsecurity
aliases:
  - SpringSecurity
tags: []
---

# SpringSecurity

Es una framework de spring que permite autenticar y autorizar a ususarios y demas funcionalidades
relacionadas con sistemas de aplicaciones java

## Caracteristicas

- Autenticacion : Valida credenciales del usuario generalmente usuario y contrasena
- Autorizacion : Controla el acceso a los recursos en funcion de los roles o los usuarios autenticados en el sistema
- Proteccion contra ataques comunes :
- CSRF
- XXS
- Clickjaking
- Seguridad de cabeceras

- Soporte con varios sistemas de autenticacion basado en formularios
- HttpBasic
- Oauth2
- LDAP
- SAML
- JWT

## Como funciona Spring Security

- Configuracion : Este se configura mediante la clase de configuracion springSecurityFilterChain

## Filtro de seguridad

- Spring utiliza una cadena de filtros FilerChain para interceptar las solicitures http entrantes
  Estos filtros verifican y validan la request antes de que esta llegue al controller

## Filtros clave

- UsernamePasswordAuthenticationFilter :maneja la autenticacion basada en forlularios
- BasucAutenticationFilter: Procesa solicitudes HttpBasic
- SecurityCOntextPersistenceFFilter: administra el contexto de seguridad en toda al aplicacion
- CSRFFYLTER : protege contra ataques csrf

## Gestion de la autenticacion

- Spring security valida las credenciales de los usuarios mediante el autentication manager
  uqe puede utilizar implementaciones como :

- Dao AutenthicationProvider : valida las credenciale del usuario contra la base de datos usando userDetailService
- Una vez autenticado almacena las credenciales del usuario en el spring securioty context holder
