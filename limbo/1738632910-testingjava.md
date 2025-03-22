---
id: 1738632910-testingjava
aliases:
  - TestingJava
tags: []
---

# Testing Java

## Primer paso

Debemos modificar el `pom.xml` para agregar las dependencias con las que haremos el testing. En este caso, sería con JUnit -Jupiter-Api.

```xml
<!-- https://mvnrepository.com/artifact/org.junit.jupiter/junit-jupiter-api -->
<dependency>
    <groupId>org.junit.jupiter</groupId>
    <artifactId>junit-jupiter-api</artifactId>
    <version>5.12.0-M1</version>
    <scope>test</scope>
</dependency>
```

## Segundo paso

Después de recargar la dependencia en nuestro proyecto, identificamos que en nuestra estructura de proyecto tenemos dos carpetas:

- `src`
- `test` -> Aquí debemos crear los archivos que tenemos en `main`, dejando por fuera la clase `main` ya que en los tests estos se ejecutan en clases especiales.

### Carpetas a duplicar

- `org`
- `example`
- `resources`

## Tercer paso

Después de haber configurado la dependencia y haber configurado el repositorio con las carpetas respectivas, lo que tenemos que hacer es:

```java
// creamos una clase copia de la clase con el código que irá a producción, esta irá nombrada con la palabra Test al final

public class ExampleTest {

    // creamos un método que no devuelve valor y que se llama igual al de la clase
    // pero este sí con la palabra test antes del inicio

    void testSuma() {
        // Dentro del método instancio la clase real
        Example example = new Example();

        // defino el resultado utilizando la función de mi clase
        int result = example.suma(4, 4);
        int expectedResult = 8;

        // utilizo assertions para validar si es válido el método
        Assertions.assertEquals(expectedResult, result);
    }
}
```

### Principales Assertions de JUnit

- `assertEquals(expected, actual)` --> sirve para evaluar un valor esperado
- `assertTrue(condition)` --> siempre espera true
- `assertFalse(condition)` --> Siempre espera falso
- `assertNull(object)` -->  valida que el objeto sea null
- `assertNotNull(object)` --> valida que el objeto de respuesta no sea configurado
- `assertThrows(expectedType, executable)` --> Me sirve para testear errores
- `assertInstanceOf(Integer.class,result)` --> para validar si un objeto es valido

---
