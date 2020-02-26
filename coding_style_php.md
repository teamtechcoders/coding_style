![TechCoders](logo.png)
# Guia de Codificación PHP

En este documento se define el estándar de código PHP que se usará para el desarrollo de los sistemas en TechCoders, los cuales se basan en el [PSR 12](https://www.php-fig.org/psr/psr-12/),  [PSR 2](https://www.php-fig.org/psr/psr-2/) y [PSR1](https://www.php-fig.org/psr/psr-1/).

A Continuación solo se describirán los más usados, para familiarizarte favor de ir a la página oficial.

## Archivos

1. Deben tener la codificación UTF-8 sin BOM
2. Deben usar Unix LF para el terminado de las líneas
3. Los archivos que solo contengan código PHP solo deben tener la etiqueta de apertura **<?php**
4. Los archivos que combinen código PHP y HTML deben cerrar el código PHP entre sus respectivas etiquetas así como hacer uso de la sintaxis alternativa de las estructuras de control, esto siempre y cuando no se esté usando un Framework y que no tenga la posibilidad de procesar vistas

## Líneas

1. Pueden tener entre 80 y 120 caracteres, si excede este limite se deben separar en múltiples lineas

## Identación

1. El código se debe identar con **4 espacios NO tabulaciones**

## Variables

1. Se deben declarar usando **camelCase**

## Namespace

1. Debe ir después de dejar una linea en blanco después de la etiqueta de apertura **<?php**

```php
<?php
 
namespace Foo\Bar;
```

## Imports

1. Los imports **use** deben de ir después de dejar una linea en blando después del namespace

```php
<?php
namespace Foo\Bar;

use Vendor\Package\FooClass;
use Vendor\Package\BarClass;
```

## Clases

1. La declaración de la clase debe ir después de dejar una linea en blanco después de los imports
1. Se deben declarar usando **StudlyCaps**
2. Las llaves de apertura y cierre deben de ir en su **propia linea**

```php
<?php

namespace Foo\Bar;

use Vendor\Package\FooClass;
use Vendor\Package\BarClass;

class MyClassName
{

}
```

## Traits

1. Se deben de declarar después de la llave de apertura de la clase

```php
<?php

namespace Foo\Bar;

use Vendor\Package\FooClass;
use Vendor\Package\BarClass;
use Vendor\Package\FirstTrait;

class MyClassName
{
    use FirstTrait;
}
```

## Constantes y Propiedades de Clase

1. Deben declararse después de los traits en caso de existir
1. Las constantes se deben declarar usando **const** y el nombre en mayúsculas y separadas por guiones bajos
2. Las propiedades deben declarar usando public, protected o private y el nombre debe ser en **camelCase**
3. Siempre deben de ir separadas por una linea en blanco
4. Se debe documentar cada una

```php
<?php

namespace Foo\Bar;

use Vendor\Package\FooClass;
use Vendor\Package\BarClass;
use Vendor\Package\FirstTrait;

class MyClassName
{
    use FirstTrait;

    /**
     * Descripción
     *
     * @var string
     */
    const STATUS_ACTIVE = 'A';

    /**
     * Descripción
     *
     * @var bool
     */  
    public $fooBar = true;
}
```

## Métodos y Funciones

1. Se deben declarar usando public, protected o private y el nombre debe ser en **camelCase**
2. Las llaves de apertura y cierre deben ir en su **propia línea**
3. Se deben de documentar indicando el tipo de dato que regresa

```php
<?php

namespace Foo\Bar;

use Vendor\Package\FooClass;
use Vendor\Package\BarClass;
use Vendor\Package\FirstTrait;

class MyClassName
{
    use FirstTrait;

    /**
     * Descripción
     *
     * @var string
     */
    const STATUS_ACTIVE = 'A';

    /**
     * Descripción
     *
     * @var bool
     */  
    public $fooBar = true;

    /**
     * Descripción
     *
     * @return void
     */
    public function customMethod()
    {
    
    }
}
```

## Estructuras de control

1. Debe haber un espacio después de la palabra reservada
2. No deben haber espacios después del paréntesis de apertura
3. No deben haber espacios después del paréntesis de cierre
4. La llave de apertura debe ir en la misma linea de la declaración y no debe de haber ningún espacio después de ella
6. La llave de cierre debe ir en su propia linea y no debe de haber ningún espacio después de ella
7. El código dentro de la estructura debe estar identado

```php
if ($expr1) {
    // if body
}

if ($expr1) {
    // if body
} elseif ($expr2) {
    // elseif body
}

if ($expr1) {
    // if body
} elseif ($expr2) {
    // elseif body
} else {
    // else body;
}

switch ($expr) {
    case 0:
        echo 'First case, with a break';
        break;
}

while ($expr) {
    // structure body
}

do {
    // structure body;
} while ($expr);

for ($i = 0; $i < 10; $i++) {
    // for body
}

foreach ($iterable as $key => $value) {
    // foreach body
}

try {
    // try body
} catch (FirstThrowableType $e) {
    // catch body
} catch (OtherThrowableType | AnotherThrowableType $e) {
    // catch body
} finally {
    // finally body
}
```
