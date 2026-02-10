# 🚀 Guía Rápida: Publicar en GitHub Pages

## ⚠️ SOBRE EL ERROR QUE VES AHORA

El error que aparece en la consola:
```
Error al registrar Service Worker: TypeError: Failed to register...
```

**ES NORMAL** - Aparece porque estás viendo la app desde claudeusercontent.com (el preview de Claude). 

**Cuando la subas a GitHub, el error desaparecerá** porque GitHub Pages tiene HTTPS y todos los archivos estarán en el mismo servidor. ✅

---

## 📦 ARCHIVOS A SUBIR A GITHUB

Tienes **2 opciones** de nombre:

### OPCIÓN 1: Con nombre personalizado (tareas-pablo.html)
✅ `tareas-pablo.html`
✅ `manifest.json`
✅ `service-worker.js`

**URL final:** `https://tu-usuario.github.io/nombre-repo/tareas-pablo.html`

### OPCIÓN 2: Con index.html (más simple)
✅ `index.html` (renombra tareas-pablo.html)
✅ `manifest.json` (necesita cambio - ver abajo)
✅ `service-worker.js`

**URL final:** `https://tu-usuario.github.io/nombre-repo/`

---

## 🔧 SI USAS index.html (RECOMENDADO)

Cambia en `manifest.json`:

**De:**
```json
"start_url": "tareas-pablo.html",
```

**A:**
```json
"start_url": "./",
```

**Ventaja:** URL más corta y limpia.

---

## 📝 PASOS PARA GITHUB PAGES

### 1. Crear Repositorio
- Ve a GitHub.com
- Click en "+" → "New repository"
- Nombre: `tareas-pablo` (o el que quieras)
- Público ✅
- Create repository

### 2. Subir Archivos
- Click en "Add file" → "Upload files"
- Arrastra los 3 archivos:
  - `tareas-pablo.html` (o `index.html`)
  - `manifest.json`
  - `service-worker.js`
- Click "Commit changes"

### 3. Activar Pages
- Settings → Pages (en el menú lateral)
- Source: **main** branch
- Folder: **/ (root)**
- Save

### 4. Esperar
- ⏰ 1-2 minutos
- Verás: "Your site is published at..."
- Copia esa URL

### 5. Abrir en el Celular
- Abre la URL en Safari (iOS) o Chrome (Android)
- Agregar a pantalla de inicio
- **¡Ya no habrá error de Service Worker!** ✅

---

## 🎯 URLS FINALES

Si usas `index.html`:
```
https://TU-USUARIO.github.io/tareas-pablo/
```

Si usas `tareas-pablo.html`:
```
https://TU-USUARIO.github.io/tareas-pablo/tareas-pablo.html
```

---

## ✅ CHECKLIST SUPER RÁPIDO

□ Tener cuenta de GitHub
□ Crear nuevo repositorio
□ Subir 3 archivos (arrastar y soltar)
□ Ir a Settings → Pages
□ Activar Pages (branch: main)
□ Esperar 2 minutos
□ Copiar URL
□ Abrir en celular
□ Instalar como app
□ **¡El Service Worker funcionará!** ✅

---

## 💡 RECOMENDACIÓN

**USA `index.html`** porque:
- URL más corta
- Más fácil de recordar
- Es el estándar web
- Pablo solo necesita `tu-usuario.github.io/tareas-pablo/`

---

## 🆘 ¿POR QUÉ NO FUNCIONA AQUÍ?

Cuando ves la app en claudeusercontent.com:
- ❌ Los archivos están separados
- ❌ Service worker busca en claudeusercontent.com
- ❌ No encuentra manifest.json ni service-worker.js
- ❌ Por eso el error 404

Cuando la subes a GitHub:
- ✅ Todos los archivos están juntos
- ✅ Service worker encuentra todo
- ✅ HTTPS activado
- ✅ ¡Funciona como app real!

---

## 🚀 ¡LISTO!

**No te preocupes por el error actual.** Es temporal. Una vez en GitHub Pages, todo funcionará perfecto y Pablo tendrá su app instalable. 📱✨

**Tiempo total: 10 minutos**
**Costo: $0**
