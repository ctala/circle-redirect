# Preview del Landing

## Ver Localmente (Opción 1 - Más Rápido)

Abrir directamente en navegador:

```bash
firefox /home/moltbot/clawd/projects/circle-redirect/index.html
# o
google-chrome /home/moltbot/clawd/projects/circle-redirect/index.html
```

## Ver con Servidor Local (Opción 2)

```bash
cd /home/moltbot/clawd/projects/circle-redirect
python3 -m http.server 8000
```

Luego visitar: http://localhost:8000

## Checklist de Revisión

Antes de aprobar, revisar:

### Copy
- [ ] **Headline** — ¿Comunica claramente el cambio?
- [ ] **Historia** — ¿Es honesta y conecta emocionalmente?
- [ ] **Beneficios** — ¿Son concretos y relevantes?
- [ ] **CTA** — ¿Es claro y sin fricción?

### Diseño
- [ ] **Colores** — ¿Verde #39ff14 + Cyan #00d4ff se ven bien?
- [ ] **Tipografía** — ¿Tamaños y jerarquía correctos?
- [ ] **Responsive** — Probar en mobile (F12 → Toggle device toolbar)
- [ ] **Animaciones** — ¿Fade-in se siente natural?

### Técnico
- [ ] **Meta tags** — `noindex, follow` para evitar competir con Skool
- [ ] **Canonical** — Apunta a Skool
- [ ] **Email contacto** — cristian@cristiantala.com correcto

## Cambios que puedo hacer

Si necesitas ajustes:

1. **Copy diferente** — Cambiar headline, historia, beneficios
2. **Colores** — Probar otras combinaciones de la marca
3. **Estructura** — Agregar/quitar secciones
4. **CTA** — Cambiar texto del botón
5. **Footer** — Links adicionales, disclaimer legal

Solo dime qué modificar.

## Next Steps (Después de Aprobar)

1. Crear repo GitHub `circle-redirect`
2. Push del código
3. Conectar a Cloudflare Pages
4. Configurar custom domain `comunidad.ecosistemastartup.com`
5. Verificar wildcard routing
6. Eliminar cuenta Circle

Tiempo estimado deployment: **5-10 minutos**
