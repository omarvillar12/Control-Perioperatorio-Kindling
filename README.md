# Monitor peri-operatorio · Rata (modelo Kindling)

Aplicación web (**PWA**) para el registro peri-operatorio durante la cirugía
estereotáxica de implantación de electrodos en la rata: cotejo de sedación,
control de signos vitales cada 5 min, conversor de dosis por UI, balance hídrico
(ingresos/egresos, volumen sanguíneo y goteo), esquemas anestésicos
(ketamina/pentobarbital + xilazina con inducción y mantenimiento), ficha
farmacológica de referencia (dosis por peso + monografías), escala de dolor
(RGS), cotejo de alta y registro quirúrgico. Funciona **sin conexión** tras la
primera carga.

> Aviso médico: herramienta de **apoyo al registro**. No sustituye el juicio
> profesional, la prescripción del Médico Veterinario responsable ni la
> aprobación del comité de ética/IACUC. Dosis y concentraciones de referencia:
> valídalas institucionalmente.

---

## Varias cirugías a la vez (multi-caso)

En la barra superior **«🐀 Casos activos»** puedes registrar **varios animales en
el mismo dispositivo**, cada uno con su propio registro aislado:

- **＋ Nuevo caso** agrega un animal.
- El **desplegable** cambia entre casos.
- **🗑** elimina el caso activo.

Los casos se guardan **solo en ese dispositivo** (`localStorage`); **no** se
comparten en vivo con otros equipos. Modelo recomendado: **un dispositivo por
persona/estación**; cada estación lleva sus propios casos y al final se combinan
los reportes/CSV. Usa **«Respaldo (JSON, todos los casos)»** para respaldar todo.

---

## Tipo de licencia

**Software propietario — «Todos los derechos reservados» (All Rights Reserved).**

- **NO** es software libre ni de código abierto (no es MIT, GPL, Apache, etc.).
- **NO** es una licencia Creative Commons.
- Identificador SPDX: `LicenseRef-Proprietary` (licencia personalizada, no estándar;
  por eso GitHub la mostrará como “Other/No license detected”, lo cual es normal
  y esperado en una licencia propietaria).
- Términos completos en [`LICENSE.txt`](LICENSE.txt): prohibida la copia,
  redistribución, modificación, obras derivadas, reutilización del código o del
  diseño y el uso comercial **sin autorización escrita del autor**. Publicarla en
  un repositorio público **no** renuncia a ningún derecho.

**Copyright © 2026 Dr. Omar Villa-Robledo. Todos los derechos reservados.**
Contacto para permisos: **villa.omar@uabc.edu.mx**

---

## Cómo subirla a GitHub y publicarla con GitHub Pages

### Opción A — Interfaz web de GitHub (sin instalar nada)

1. Entra a <https://github.com> → **New repository**.
2. Nombre del repo, por ejemplo `monitor-rata-kindling`.
   - Para máxima protección contra copia, elige **Private**. *(Nota: GitHub Pages
     solo publica desde repos privados en cuentas de pago; en cuenta gratuita, para
     usar Pages el repo debe ser **Public**. Si es Public, tu respaldo es la
     licencia + la autoría fechada de los commits.)*
3. Crea el repo → en la página del repo pulsa **“uploading an existing file”**.
4. Arrastra **el contenido de esta carpeta** (`index.html`, `manifest.json`,
   `sw.js`, los `icon-*.png`, `LICENSE.txt`, `README.md`, `.gitignore`,
   `.nojekyll`) y pulsa **Commit changes**.
   - El archivo `.nojekyll` a veces no se arrastra desde el Finder por empezar con
     punto; si falta, créalo en GitHub con **Add file → Create new file**, nómbralo
     `.nojekyll` y déjalo vacío.
5. Ve a **Settings → Pages**:
   - **Source:** *Deploy from a branch*.
   - **Branch:** `main` y carpeta **/(root)** → **Save**.
6. Espera 1–2 min. Tu app quedará en:
   `https://TU-USUARIO.github.io/monitor-rata-kindling/`

### Opción B — Línea de comandos (git)

```bash
cd github_pages          # carpeta con estos archivos
git init
git add .
git commit -m "PWA Monitor peri-operatorio rata (Kindling) — v2 multi-caso"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/monitor-rata-kindling.git
git push -u origin main
```

Luego activa **Settings → Pages → Deploy from a branch → main / (root)**.

---

## Cómo usarla

1. Abre la URL de GitHub Pages en el teléfono, tableta o computadora.
2. Instálala como app: **iPhone/iPad** (Safari): Compartir → *Añadir a inicio*;
   **Android** (Chrome): menú ⋮ → *Instalar app*.
3. Tras abrirla una vez con conexión, **funciona offline**.
4. Guía de uso dentro de la app: pestaña **ℹ️ Guía**.

> Actualizar la app: sube los archivos nuevos y **cambia la versión del caché** en
> `sw.js` (por ejemplo `periop-rata-v2` → `v3`) para que los dispositivos
> descarguen la versión nueva.

---

## Archivos de este paquete

| Archivo | Descripción |
|---|---|
| `index.html` | Aplicación (JavaScript **ofuscado**). |
| `manifest.json` | Manifiesto PWA. |
| `sw.js` | Service worker (offline, cache-first). |
| `icon-192.png`, `icon-512.png`, `icon-180.png` | Íconos. |
| `LICENSE.txt` | Licencia propietaria — Todos los derechos reservados. |
| `.nojekyll` | Evita el procesamiento Jekyll en GitHub Pages. |
| `.gitignore` | Excluye artefactos y el código fuente sin ofuscar. |

---

Elaborado por **Dr. Omar Villa-Robledo** · © 2026 · Todos los derechos reservados
