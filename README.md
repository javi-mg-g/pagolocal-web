# pagolocal-web

Web pública de PagoLocal — landing, política de privacidad, términos y restablecimiento de contraseña.

Servida con **GitHub Pages** → `https://pagolocal.xyz`

## Estructura

```
.
├── index.html              # Landing principal
├── privacy.html            # Política de Privacidad (RGPD)
├── terms.html              # Términos y Condiciones
├── reset.html              # Restablecimiento de contraseña (recibe ?token=...&tipo=usuario|comercio)
├── styles.css              # Estilos compartidos (paleta, header, footer, modal, botones)
├── CNAME                   # Dominio personalizado (pagolocal.xyz)
├── .nojekyll               # Desactiva Jekyll en GitHub Pages
├── .well-known/
│   └── assetlinks.json     # Verificación de Universal Links para Android
└── README.md
```

## Despliegue

Cualquier push a la rama `main` se despliega automáticamente en GitHub Pages.

## Cómo cambiar cosas

| Quiero cambiar… | Edito… |
|---|---|
| Colores de la web | Variables CSS al principio de `styles.css` (`--primary`, `--accent`, `--bg`, …) |
| Textos de la landing | Objeto `I18N.es` dentro de `<script>` al final de `index.html` |
| Enlaces de las apps | `APP_LINKS` al inicio del `<script>` de `index.html` (sustituir las cadenas vacías) |
| Contenido legal | Directamente el HTML de `privacy.html` o `terms.html` |
| Endpoint del backend en reset | `API_BASE` en el `<script>` de `reset.html` |

## Idiomas

La landing (`index.html`) está preparada para Español, Valencià e Inglés. Por ahora solo Español está rellenado. Para activar Valencià o Inglés:

1. Copia el bloque `es: { … }` dentro de `I18N`.
2. Pégalo bajo `val: {}` o `en: {}` y traduce los valores.
3. Quita el atributo `disabled` del botón correspondiente en el selector `.lang-switch` del HTML.
