![TechCoders](logo.png)
# Guia de Codificación JS

Para el uso de javascript podemos hacer uso de la guia de [google](https://google.github.io/styleguide/jsguide.html)

## Archivos

1. Deben de tener la codificación UTF-8
2. Los nombres deben de ser con **guiones bajos**

## Identación

1.- Debe de ser de 2 espacios **NO tabulaciones**

## Punto y Coma

1.- Todas las sentencias deben de terminar con su respectivo punto y coma

## Variables

1. Se deben declarar usando **camelCase**
2. Se debe hacer uso de const y let
3. Las constantes deben ser en mayúsculas y con guiones bajos si el nombre es largo

## Clases

1. Se deben de declarar usando **StudlyCase** o como lo menciona el documento del link **UpperCamelCase**
2. La llave de apertura debe estar en la misma linea de la declaración de la clase y la de cierre en su propia linea

```javascript
class MiClase {
  
}
```

## Métodos y Funciones

1. Se deben declarar usando **camelCase**
2. Se deben documentar
3. La llave de apertura debe estar en la misma linea de la declaración de la clase y la de cierre en su propia linea

```javascript
/**
* Descripción
*
* @param {string} primerParametro
* @param {number} segundoParametro
* @return {void}
*/
function miFuncion(primerParametro, segundoParametro) {
  //hacer algo
}
```
