# Circle → Skool Migration Landing

Landing page profesional para redirigir tráfico de `comunidad.ecosistemastartup.com` (Circle) a la nueva comunidad en Skool.

**Versión:** V2 (2026-02-16)  
**Copy:** Tono personal Cristian, roadmap 2026, visión automatización para emprendedores sin equipo

## Features

✅ **Wildcard routing** — Captura todos los paths sin errores 404  
✅ **Copy personal Cristian** — Voz directa, honesta, sin marketing corporativo  
✅ **Roadmap 2026** — 11 cursos publicados + 8 en roadmap (Feb-Ago)  
✅ **Visión clara** — Automatización como primer empleado para emprendedores sin equipo  
✅ **Números reales** — ~100 miembros, $600/mes Circle, exit US$23M  
✅ **SEO-friendly** — Meta tags, canonical, noindex (no competir con Skool)  
✅ **Responsive** — Mobile-first, funciona perfecto en cualquier dispositivo  
✅ **Brand personal** — Colores Synthwave (verde #39ff14 + cyan #00d4ff)  
✅ **Zero-friction CTA** — Botón directo a Skool + "Plan gratuito disponible"

## V2 Changes (2026-02-16)

- **$300 → $600/mes** (costo real Circle)
- **Stats aclaradas:** "Miembros en Skool", "ya publicados", "+ roadmap 2026"
- **Roadmap section:** 8 cursos Feb-Ago 2026, visión automatización
- **Reframing números:** No suena "poco" — suena curado y con plan potente
- **Copy más directo:** "Circle Ya No Existe" (no "nos mudamos")
- **Enfoque:** Ayudar emprendedores que aún no pueden tener equipo  

## Deployment a Cloudflare Pages

### 1. Crear repo en GitHub

```bash
cd /home/moltbot/clawd/projects/circle-redirect
git init
git add .
git commit -m "Initial commit: Circle migration landing"
git remote add origin https://github.com/ctala/circle-redirect.git
git branch -M main
git push -u origin main
```

### 2. Conectar a Cloudflare Pages

1. Dashboard Cloudflare → **Pages** → **Create a project**
2. **Connect to Git** → Seleccionar repo `circle-redirect`
3. **Build settings:**
   - Framework preset: **None** (HTML estático)
   - Build command: (dejar vacío)
   - Build output directory: `/`
4. **Deploy**

### 3. Configurar custom domain

1. Pages → **Custom domains** → **Set up a custom domain**
2. Agregar: `comunidad.ecosistemastartup.com`
3. Cloudflare manejará automáticamente:
   - SSL/TLS
   - Wildcard routing (todos los paths)
   - CDN global

### 4. DNS (si es necesario)

Si el dominio está en Cloudflare:
- Crear CNAME: `comunidad` → `circle-redirect.pages.dev`
- Proxy activado (nube naranja)

## Testing Local

Abrir `index.html` directamente en navegador o:

```bash
python3 -m http.server 8000
# Visitar http://localhost:8000
```

## Wildcard Paths

La landing responde igual en:
- `comunidad.ecosistemastartup.com/`
- `comunidad.ecosistemastartup.com/home`
- `comunidad.ecosistemastartup.com/cualquier/path/aqui`

Todos redirigen a Skool con mismo mensaje.

## Analytics (Opcional)

Para trackear origen del tráfico, agregar en `<script>`:

```javascript
// Google Analytics, Plausible, etc.
gtag('event', 'circle_migration_view', {
  'original_path': currentPath
});
```

## Stack

- **HTML puro** — Sin dependencias, carga instantánea
- **CSS Grid + Flexbox** — Responsive nativo
- **JavaScript vanilla** — Path tracking, CTA analytics

## License

Uso interno Ecosistema Startup / Cristian Tala

---

**Última actualización:** 2026-02-16  
**Deploy:** Cloudflare Pages  
**Redirect:** Circle → Skool
