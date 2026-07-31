# genai-portfolio

Portfolio estático de **product imaging con IA** (Agustín Expósito).

**URL:** https://aguexposito.github.io/genai-portfolio/

## Contenido

- Serie A — Sofá terciopelo esmeralda: base + living diurno / noche / loft.
- Serie B — Silla cáscara beige: base + mesa redonda / comedor / viñeta editorial.
- Trabajos previos con IA (assets / CGs).

## Actualizar escenas

Copiar los archivos generados con estos nombres exactos:

```
images/serie-a/01_living_dia.png
images/serie-a/02_living_noche.png
images/serie-a/03_loft.png
images/serie-b/01_mesa_redonda.png
images/serie-b/02_comedor.png
images/serie-b/03_vineta.png
```

No hace falta editar el HTML: el script carga cada `data-src` y, si existe, reemplaza el placeholder.

Luego:

```bash
git add images/
git commit -m "Add generated product scene images"
git push
```

## Preview local

Abrir `index.html` en el navegador, o:

```bash
npx --yes serve .
```
