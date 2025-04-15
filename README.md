# Kiosk Design System Tokens

Este repositorio contiene los tokens de diseño extraídos desde Figma, disponibles en formatos JSON y SCSS.
Es la base para maquetar las interfaces de los kioscos de TPC

## 📁 Archivos Generados

Los tokens están organizados por tipo y modo (tema). Cada archivo contiene los tokens por modo (como `core`, `light`, `dark`, etc.).

### 🟡 _colors.json / _colors.scss
Contiene los tokens de color.

```json
{
  "core": {
    "colorbackgroundprimary": "#ffffff",
    "colortextprimary": "#000000"
  }
}
```

```scss
$core-colorbackgroundprimary: #ffffff;
$core-colortextprimary: #000000;
```

---

### 🔠 _typography.json / _typography.scss
Contiene tokens tipográficos como `font-size`, `line-height`, `font-weight`, etc.

```json
{"display-l": {
      "font-family": "$font-familybasemedium--sweet-coffee",
      "font-weight": "Medium",
      "font-size-default": 104,
      "line-height-default": 160
    }
}
```

```scss
$sweet-coffee-display-l-font-family: $font-familybasemedium--sweet-coffee;
$sweet-coffee-display-l-font-weight: Medium;
$sweet-coffee-display-l-font-size-default: 104;
$sweet-coffee-display-l-line-height-default: 160;
```

*NOTA: Si el letter spacing es cero, no aparece en el estilo de texto.
---

### 📏 _foundation-dimensions.json / _foundation-dimensions.scss
Incluye radius, stroke y componentes.

```json
{
  "core": {
    "radius": {
      "full": 9999,
      "medium": 8
    }
  }
}
```

```scss
$core-radius-full: 9999;
$core-radius-medium: 8;
```

---

## 🚀 ¿Cómo usar los tokens?

### 📦 Como archivos SCSS
1. Copia los archivos `.scss` a tu proyecto.
2. Importa el modo que quieras usar:

```scss
@import 'tokens/_colors.scss';
@import 'tokens/_typography.scss';
@import 'tokens/_foundation-dimensions.scss';
```

### 🧩 Como archivos JSON
1. Puedes consumirlos en cualquier entorno JS/TS y procesarlos como desees:

```ts
import tokens from './tokens/_colors.json';
console.log(tokens.core.colorbackgroundprimary);
```

---

## 🛠️ ¿Cómo actualizar los tokens?

Pide al administrador del sistema de diseño que ejecute el siguiente comando:

```bash
npm run update-tokens
```

Esto descargará los tokens desde la API de Figma y generará nuevamente los JSON y SCSS.


## 🧾 Licencia
Este repositorio está disponible bajo la licencia MIT.

---

¿Dudas? Abre un issue o contáctame.

---

✨ ¡Feliz diseño y desarrollo!
