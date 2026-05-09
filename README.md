# Playbook · IA en Oncología · RECAP NOW · Ipsen

Web del taller de Inteligencia Artificial impartido en el congreso **RECAP NOW** de Ipsen (Mallorca, 9 de mayo de 2026). Contiene los prompts copiables del Taller 1 (Investigar) y Taller 2 (Crear), más los tres documentos clínicos de referencia descargables.

**Autor:** Néstor Guerra · NCompany
**Código de aprobación:** CBZ-ES-002105

---

## 📂 Estructura del repositorio

```
playbook-recap-now-ipsen/
├── index.html          ← La web (un solo archivo, sin dependencias)
├── .nojekyll           ← Para que GitHub no procese con Jekyll
├── README.md           ← Este archivo
└── pdfs/               ← Los 3 PDFs de referencia van aquí
    ├── checkmate-9er.pdf
    ├── cabopoint.pdf
    └── eau-rcc-2026.pdf
```

---

## 📎 Nombres EXACTOS de los PDFs (esto es lo que más falla)

Los tres botones "Descargar PDF" buscan estos nombres **literalmente**. GitHub Pages distingue mayúsculas, minúsculas, guiones y espacios. Si no coincide al 100%, da 404.

| Documento | Nombre del archivo (obligatorio) |
|---|---|
| CheckMate 9ER (Motzer 2026) | `checkmate-9er.pdf` |
| CaboPoint (Albiges 2026) | `cabopoint.pdf` |
| EAU Guidelines RCC 2026 | `eau-rcc-2026.pdf` |

✅ Todo en **minúsculas**.
✅ Guiones simples (`-`), nunca espacios ni guiones bajos (`_`).
✅ Extensión `.pdf` en minúsculas.

> Si tus PDFs tienen otros nombres, tienes dos opciones:
> 1. Renómbralos a los de la tabla (lo más rápido).
> 2. Edita los `href` correspondientes en `index.html` (busca `pdfs/` y cambia el nombre).

---

## 🚀 Subir a GitHub Pages — paso a paso

### 1. Crear el repositorio
1. GitHub → botón verde **New repository**.
2. Nombre: `playbook-recap-now-ipsen` (o el que quieras).
3. **Public** (Pages gratis solo funciona en repos públicos).
4. NO marques "Initialize with README".
5. **Create repository**.

### 2. Subir los archivos

**Opción A · Drag & drop (más fácil):**
1. En el repo recién creado, pulsa **uploading an existing file**.
2. Arrastra TODOS los archivos descomprimidos: `index.html`, `.nojekyll`, `README.md`, y la carpeta `pdfs/` con los 3 PDFs dentro.
3. **Commit changes**.

**Opción B · Línea de comandos:**
```bash
git clone https://github.com/TUUSUARIO/playbook-recap-now-ipsen.git
cd playbook-recap-now-ipsen
# Copia aquí los archivos descomprimidos
git add .
git commit -m "Initial commit"
git push origin main
```

### 3. Activar GitHub Pages
1. **Settings** → menú izquierdo → **Pages**.
2. Source:
   - Branch: `main`
   - Folder: `/ (root)`
3. **Save**.
4. En 1-2 min tendrás la URL pública (`https://tuusuario.github.io/playbook-recap-now-ipsen/`).

---

## 🧰 Troubleshooting — si los PDFs dan error

Si al pulsar "Descargar PDF" sale un mensaje de "No se encuentra el archivo" o un 404, repasa este checklist:

### ✅ Checklist
- [ ] Los PDFs están **dentro de la carpeta `pdfs/`** del repo (no en la raíz).
- [ ] Los nombres son **exactamente** los de la tabla de arriba (incluida la extensión `.pdf`).
- [ ] Los nombres están en **minúsculas** y con **guiones simples**.
- [ ] **Han pasado 2-3 minutos** desde que subiste los PDFs (GitHub Pages tarda en propagar).
- [ ] Has **vaciado la caché** del navegador o probado en ventana de incógnito.
- [ ] El repo es **público**.

### Comprobación manual
Abre directamente en el navegador:
```
https://TUUSUARIO.github.io/playbook-recap-now-ipsen/pdfs/checkmate-9er.pdf
```
- Si descarga el PDF → todo bien, era caché.
- Si da 404 → el archivo no está donde toca, o el nombre no coincide.

### Errores típicos y su causa
| Síntoma | Causa más probable |
|---|---|
| "No se encuentra el archivo" al pulsar | El PDF no está subido aún, o su nombre no coincide |
| Da 404 desde móvil pero funciona en escritorio | Caché del navegador móvil — fuerza recarga |
| El botón parece no hacer nada | Bloqueador de descargas del navegador — comprueba la barra de URL |
| Funciona en local pero no en GitHub Pages | Mayúsculas/minúsculas distintas (Windows/Mac no distinguen, GitHub sí) |

---

## 🌐 Dominio personalizado (opcional)

Para usar `playbook.ncompany.es` en lugar de la URL de GitHub:
1. Crea un fichero `CNAME` en la raíz con una sola línea: `playbook.ncompany.es`.
2. En tu DNS, registro `CNAME` apuntando a `tuusuario.github.io`.
3. **Settings → Pages → Custom domain** → mete el dominio → marca **Enforce HTTPS**.

---

## 🔧 Personalización rápida

Todo el contenido vive dentro de `index.html`:
- **Colores y tipografía:** bloque `:root` al principio del `<style>`, variables CSS.
- **Prompts:** dentro de los `<div class="prompt-body">`.
- **Datos de los estudios:** dentro de cada `<div class="material-card">`.
- **Footer:** al final del `<body>`.

---

## 📝 Licencia y uso

Material de soporte del taller RECAP NOW · Ipsen. Para uso interno educativo.
Código de aprobación: CBZ-ES-002105 (mayo 2026).

Para preguntas, formación in-company o consultoría aplicada de IA en oncología:
**Néstor Guerra — NCompany (Madrid).**
