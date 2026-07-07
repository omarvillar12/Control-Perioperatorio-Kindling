# Monitor peri-operatorio · Rata (modelo Kindling)

Aplicación web (**PWA**) para el registro peri-operatorio durante la cirugía
estereotáxica de implantación de electrodos en la rata: cotejo de sedación,
control de frecuencia respiratoria cada 15 min, conversor de dosis por UI,
escala de dolor (RGS), cotejo de alta y registro quirúrgico. Funciona **sin
conexión** tras la primera carga.

> Aviso médico: herramienta de **apoyo al registro**. No sustituye el juicio
> profesional, la prescripción del Médico Veterinario responsable ni la
> aprobación del comité de ética/IACUC. Dosis y concentraciones de referencia:
> valídalas institucionalmente.

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

## Cómo usarla

1. Abre la URL de GitHub Pages en el teléfono, tableta o computadora.
2. Instálala como app: **iPhone/iPad** (Safari): Compartir → *Añadir a inicio*;
   **Android** (Chrome): menú ⋮ → *Instalar app*.
3. Tras abrirla una vez con conexión, **funciona offline**.
4. Guía de uso dentro de la app: pestaña **ℹ️ Guía**.

> Actualizar la app: sube los archivos nuevos y **cambia la versión del caché** en
> `sw.js` (por ejemplo `periop-rata-v1` → `v2`) para que los dispositivos
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
