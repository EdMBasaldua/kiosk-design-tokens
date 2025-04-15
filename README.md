# Design System Tokens

Este repositorio contiene los tokens de diseño para nuestro sistema modular. Los tokens se dividen en tres categorías principales: **Colores**, **Tipografía** y **Dimensiones de Fundación**. Además, están organizados en diferentes **modos (THEMES)**, lo que permite la personalización según el contexto o tema de la interfaz.

## Archivos de Tokens

Los tokens se encuentran en el directorio `/tokens` y se dividen en los siguientes archivos:

- **_colors.json**: Contiene los valores de colores (por colección y tema).
- **_typography.json**: Contiene los valores de tipografía (por colección y tema).
- **_foundation-dimensions.json**: Contiene las dimensiones de fondo (Radio, Componentes y Stroke, por colección y tema).

### Usar los Tokens en JSON

Los archivos JSON contienen los valores de cada token, organizados por colecciones y por tema (modo). Ejemplo de un archivo de color:

```json
{
  "Theme-Mama Shawarma": {
    "light": {
      "color-backgroundpositiveweak": "#A1C4FD",
      "color-backgroundneutral": "#E0E0E0"
    },
    "dark": {
      "color-backgroundpositiveweak": "#3F6B9C",
      "color-backgroundneutral": "#4A4A4A"
    }
  }
}

Cada token está organizado por modo (como light o dark), y dentro de cada modo, los tokens de color tienen un nombre basado en la convención de nombres de Figma. Puedes usar estos tokens en tu aplicación de la siguiente forma:

import tokens from 'path-to-tokens/_colors.json';
console.log(tokens['Theme-Mama Shawarma']['light']['color-backgroundpositiveweak']);

Usar los Tokens en SCSS
Los tokens también están disponibles como variables SCSS, que puedes importar en tu hoja de estilo. Ejemplo de un archivo SCSS generado a partir de los tokens:
$Theme-Mama-Shawarma--light--color-backgroundpositiveweak: #A1C4FD;
$Theme-Mama-Shawarma--dark--color-backgroundpositiveweak: #3F6B9C;

body {
  background-color: $Theme-Mama-Shawarma--light--color-backgroundpositiveweak;
}

Para usar los tokens en SCSS, importa el archivo SCSS generado en tu proyecto:
@import 'path-to-tokens/_colors';
