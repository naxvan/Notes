---
id: 1741654100-cursoquarkus
aliases:
  - CursoQuarkus
tags: []
---

# CursoQuarkus

## Que es quarkus

quarkus es un framework de desarrollo de aplicaciones java, orientadas a la nube, que permite desarrollar aplicaciones de forma rápida y eficiente, con un bajo consumo de recursos y un rápido tiempo de arranque.

## Como se crea un proyecto en quarkus

quarkus tiene dos herramientas principales para crear inicialmente los proyectos

- terminal de comandos podemos generar un proyecto con dependencias adicionales para que el proyecto trabaje
- tambien podemos genrear un proyecto por medio de un initializer queda en <https://code.quarkus.io/> y alli podemos
  genera nuevos proyectos con dependencias adicionales.

## Como definir un ednpint en quearkus

para definir un endpint en quearjus debemos tener en cuenta las siguientes notaciones como

@Path Puede ir a nivel de clase o metodo de controller  
@GET
@Produces va a nivel de clase o metodo este define que es lo que devilvera la api puede ser xml,json,html,etc

## Como puedo enviar paramentros por url y tambien enviar parametros en cuerpo de la peticion

Cuando navegamos a nuestros endpoints lo que hacemos es enviar cierta informacion para que nos retorne una respuesta frente a esto podemos enviar parametros por url y tambien enviar parametros en el cuerpo de la peticion

inicial mente para metodos de tipo get podemos hacerlo de dos maneras

- QueryParam: son parametros que se envian por medio de la url por ejemplo ?name=carlos
- Path Param: esto se hace enviando parametros por medio de las rutas url por ejemplo /saludo/name/gritar

## Como retorno objetos json en quarkus
