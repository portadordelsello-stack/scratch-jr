# ScratchJr Web (1.3.2)

Adaptación web de **ScratchJr 1.3.2** para funcionar en cualquier navegador moderno sin requerir emuladores ni tabletas.

## 🚀 Despliegue en Vercel (Zero Configuration)

Este repositorio está 100% optimizado para Vercel:

1. Conecta tu repositorio en [Vercel](https://vercel.com/new).
2. Haz clic en **Deploy** (no necesitas configurar variables ni cambiar directorios).
3. Vercel ejecutará automáticamente la compilación (`npm run build`) y publicará los estáticos optimizados desde `web/dist`.

### Optimizaciones incluidas para Vercel:
- **`vercel.json` en raíz y subcarpeta:** Soporte tanto si se importa en raíz (`./`) como si se selecciona `web/` como Root Directory.
- **Cabeceras WASM:** Soporte MIME (`application/wasm`) y caché inmutable para `sql.js` WebAssembly.
- **Caché CDN agresiva:** Caché inmutable de 1 año para activos estáticos (`/assets/*`, `/sounds/*`, `/pnglibrary/*`, `/svglibrary/*`).
- **Seguridad:** Cabeceras `X-Content-Type-Options: nosniff` y `Referrer-Policy: strict-origin-when-cross-origin`.
- **Rutas directas:** `cleanUrls: false` para navegación nativa entre `index.html`, `home.html`, `editor.html` y `gettingstarted.html`.

---

## 💻 Desarrollo Local

```bash
# Instalar dependencias
npm install

# Iniciar servidor de desarrollo
npm run dev

# Compilar para producción
npm run build

# Previsualizar build de producción
npm run preview
```
