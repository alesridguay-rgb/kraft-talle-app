# Kraft Talle · cámara

App estática: detecta el A4 solo (jscanify + OpenCV.js), cámara en vivo, mide con truco de pared.
Sin backend, sin Supabase. Solo `index.html`.

## Deploy a Vercel (elegí una)

**A) Web (lo más rápido)**
1. Entrá a vercel.com → Add New → Project.
2. Arrastrá la carpeta `kraft-talle-app` (o subila a un repo de GitHub e importala).
3. Framework Preset: **Other**. Build/Output: dejar vacío. Deploy.
4. Te da una URL HTTPS. Abrila en el celular.

**B) CLI**
```
cd kraft-talle-app
npx vercel        # primera vez te pide login
npx vercel --prod # para la URL definitiva
```

## Probar desde el celular
- Abrí la URL HTTPS (la cámara SOLO funciona en HTTPS).
- "Encender cámara" → permití el acceso.
- Apuntá al folio desde arriba; cuando el borde se pinta de amarillo → "Capturar y medir".
- Ajustá el umbral y calibrá con tu medida real.

## Notas
- La carga de OpenCV.js tarda unos segundos la primera vez (el botón se habilita solo cuando está listo).
- El pie se detecta por contraste sobre el folio blanco: aproximado. La detección fina (modelo entrenado) es el siguiente paso.
