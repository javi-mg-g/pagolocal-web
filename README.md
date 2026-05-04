# pagolocal-web

Web pública de PagoLocal — landing y página de restablecimiento de contraseña.

Servida con Cloudflare Pages → `pagolocal.xyz`

## Páginas

- `/` — Landing principal
- `/reset` — Restablecimiento de contraseña (recibe `?token=...` por URL)

## Despliegue

Cualquier push a `main` se despliega automáticamente vía Cloudflare Pages.
