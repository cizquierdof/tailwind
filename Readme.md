# Instalación

Instalación básica para web con CLI.

1. Instalar vía npm
```shell
npm install -D tailwindcss
npx tailwindcss init
```

2. configurar tailwind.config.js
```javascript
/** @type {import('tailwindcss').Config} */ 
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

3. añadir directivas en css de entrada src/input.css

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

4. Arrancar CLI
```shell
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
```

5. Añadir el css de salida al head

```html
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="/dist/output.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```

El CLI va actualizando los cambios