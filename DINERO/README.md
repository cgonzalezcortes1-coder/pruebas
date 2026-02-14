# 🎯 Liberador de Deudas - PWA

App de control de deudas usando el método Snowball. Instalable en Android/iOS.

## 📱 Instalación

### Opción 1: Usar iconos pre-generados (Más fácil)

1. Abre el archivo `create_simple_icons.html` en tu navegador Chrome/Firefox
2. Haz click en los enlaces "Descargar icon-192.png" y "Descargar icon-512.png"
3. Guarda los archivos en la misma carpeta que los demás archivos

### Opción 2: Generar iconos con Python (Opcional)

```bash
pip install cairosvg pillow
python convert_icons.py
```

## 🌐 Publicar la App

Tienes varias opciones para que tu amigo pueda instalarla:

### A) GitHub Pages (GRATIS - Recomendado)

1. Crea un repositorio en GitHub
2. Sube todos los archivos:
   - deudas-snowball.html
   - manifest.json
   - sw.js
   - icon-192.png
   - icon-512.png
3. Ve a Settings → Pages → Source: main branch
4. Tu app estará en: `https://tu-usuario.github.io/nombre-repo/deudas-snowball.html`

### B) Netlify Drop (GRATIS - Más fácil)

1. Ve a https://app.netlify.com/drop
2. Arrastra todos los archivos a la página
3. Te da una URL instantánea

### C) Servidor web propio

Sube todos los archivos a tu hosting y accede por HTTPS (obligatorio para PWA).

## 📲 Instalar en el celular

### Android (Chrome):

1. Abre la URL de la app en Chrome
2. Ve al menú (⋮) → "Agregar a pantalla de inicio"
3. Dale un nombre y confirma
4. ¡Listo! Aparecerá como una app en tu celular

### iPhone (Safari):

1. Abre la URL de la app en Safari
2. Toca el botón de compartir (□ con flecha)
3. Selecciona "Agregar a pantalla de inicio"
4. Dale un nombre y confirma

## ✨ Características PWA

- ✅ Funciona offline (después de la primera carga)
- ✅ Se instala como app nativa
- ✅ Icono en la pantalla de inicio
- ✅ Pantalla completa (sin barra de navegador)
- ✅ Datos guardados localmente en el dispositivo

## 🗂️ Archivos incluidos

```
├── deudas-snowball.html      # App principal
├── manifest.json              # Configuración PWA
├── sw.js                      # Service Worker (offline)
├── icon-192.png              # Icono pequeño
├── icon-512.png              # Icono grande
├── create_simple_icons.html  # Generador de iconos
└── README.md                 # Este archivo
```

## 🔧 Notas técnicas

- La app guarda datos en `localStorage` del navegador
- NO requiere conexión después de la primera carga
- Los datos NO se sincronizan entre dispositivos
- Para hacer backup: exportar/importar datos (pendiente implementar)

## 🎨 Personalización

Para cambiar colores, edita las variables CSS en `deudas-snowball.html`:

```css
:root {
    --bg-main: #f8f4ed;
    --primary: #2d5016;
    --accent-green: #7fb069;
    --accent-red: #d94e4e;
    --accent-yellow: #f2cc8f;
}
```

## 📝 Uso

1. **Agregar deudas**: Click en "➕ Agregar Nueva Deuda"
2. **Registrar pagos regulares**: Click en "⚡ Pago Rápido"
3. **Pagos adelantados**: Click en "💰 Pago Adelantado" y escribe el nuevo saldo
4. **Seguimiento visual**: Barras de progreso muestran avance
5. **Método Snowball**: La deuda más pequeña siempre es prioridad

---

Creado con ❤️ para ayudar a eliminar deudas
