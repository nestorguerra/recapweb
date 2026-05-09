# Playbook · IA en Oncología · RECAP NOW · Ipsen

Web del taller de Inteligencia Artificial impartido en el congreso **RECAP NOW** de Ipsen (Mallorca, 9 de mayo de 2026). Contiene los prompts copiables del Taller 1 (Investigar) y Taller 2 (Crear), más los tres documentos clínicos de referencia para cargar en NotebookLM.

**Autor:** Néstor Guerra · NCompany
**Código de aprobación:** CBZ-ES-002105

---

## 📂 Estructura del repositorio

```
playbook-recap-now-ipsen/
├── index.html          ← La web (un solo archivo, sin dependencias)
├── .nojekyll           ← Le dice a GitHub Pages que NO procese con Jekyll
├── README.md           ← Este archivo
└── pdfs/               ← Carpeta donde van los 3 PDFs de referencia
    ├── checkmate-9er.pdf
    ├── cabopoint.pdf
    └── eau-rcc-2026.pdf
```

---

## 🚀 Cómo subirlo a GitHub Pages — paso a paso

### 1. Crear el repositorio

1. Entra en GitHub → botón verde **New repository**.
2. Nombre sugerido: `playbook-recap-now-ipsen` (o el que quieras).
3. Marca **Public** (Pages gratis solo funciona en repos públicos en cuentas free).
4. NO marques "Initialize with README" (ya tenemos uno).
5. Crea el repo.

### 2. Subir los archivos

**Opción A · Drag & drop (la más rápida):**
1. En el repo recién creado, pulsa **uploading an existing file**.
2. Arrastra los archivos descomprimidos del zip:
   - `index.html`
   - `.nojekyll`
   - `README.md`
   - La carpeta `pdfs/` completa
3. Pulsa **Commit changes**.

**Opción B · Línea de comandos:**
```bash
git clone https://github.com/TUUSUARIO/playbook-recap-now-ipsen.git
cd playbook-recap-now-ipsen
# Copiar aquí todos los archivos del zip
git add .
git commit -m "Initial commit"
git push origin main
```

### 3. Activar GitHub Pages

1. En el repo, ve a **Settings** (engranaje arriba a la derecha).
2. Menú izquierdo → **Pages**.
3. En **Source**, elige:
   - Branch: `main`
   - Folder: `/ (root)`
4. Pulsa **Save**.
5. Espera 1-2 minutos. GitHub te dará la URL pública (ej. `https://tuusuario.github.io/playbook-recap-now-ipsen/`).

### 4. Subir los PDFs

Los tres botones "Abrir PDF" de la web esperan estos archivos exactos en la carpeta `pdfs/`:

| Documento | Nombre del archivo (obligatorio) |
|---|---|
| CheckMate 9ER (Motzer 2026) | `checkmate-9er.pdf` |
| CaboPoint (Albiges 2026) | `cabopoint.pdf` |
| EAU Guidelines RCC 2026 | `eau-rcc-2026.pdf` |

Si quieres usar otros nombres, cambia los `href` en `index.html` (busca `pdfs/`).

---

## 🔧 Personalización

Todo el contenido (textos, prompts, paleta) está dentro de `index.html`:

- **Colores y tipografía:** bloque `:root` al principio del `<style>`, variables CSS.
- **Prompts:** dentro de los `<div class="prompt-body">`.
- **Datos del estudio (cards de NotebookLM):** dentro de cada `<div class="material-card">`.
- **Footer:** al final del `<body>`.

---

## 🌐 Dominio personalizado (opcional)

Si quieres un dominio tipo `playbook.ncompany.es`:

1. Crea un fichero `CNAME` en la raíz con una sola línea: `playbook.ncompany.es`.
2. En tu proveedor de DNS, crea un registro `CNAME` apuntando a `tuusuario.github.io`.
3. En **Settings → Pages → Custom domain** mete el dominio y marca **Enforce HTTPS**.

---

## 📝 Licencia y uso

Material de soporte del taller RECAP NOW · Ipsen. Para uso interno educativo.
Código de aprobación: CBZ-ES-002105 (mayo 2026).

Para preguntas, formación in-company o consultoría aplicada de IA en oncología:
**Néstor Guerra — NCompany (Madrid).**
