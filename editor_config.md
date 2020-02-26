![TechCoders](logo.png)
# Configuracion del IDE

Ya sea el IDE que utilices verifica que pueda leer el archivo **.editorconfig** ya que este archivo contiene la configuración
base de las guías de estilos para la codificación.

Este [archivo](.editorconfig) debe ser descargado y agregado en todos los proyectos.

```editorconfig
root = true

[*]
charset = utf-8
end_of_line = lf
insert_final_newline = true
indent_style = space
indent_size = 4
trim_trailing_whitespace = true

[*.{html,twig,blade.php,js,vue}]
indent_size = 2

[*.md]
trim_trailing_whitespace = false

[*.{yml,yaml}]
indent_size = 2

```
