# genai-portfolio

Portfolio estático de **product imaging con IA** (Agustín Expósito).

**URL:** https://aguexposito.github.io/genai-portfolio/

## Contenido

- Serie A / B: foto base real + slots de escenas (img2img + ControlNet + IP-Adapter).
- Las escenas pendientes se muestran como placeholder hasta que existan los JPG.

## Actualizar escenas (Fase 3b)

Copiar los JPG generados con estos nombres exactos:

```
images/serie-a/01_living_dia.jpg
images/serie-a/02_living_noche.jpg
images/serie-a/03_loft.jpg
images/serie-b/00_base.jpg
images/serie-b/01_mesa_redonda.png
images/serie-b/02_comedor.png
images/serie-b/03_editorial.png
```

Serie A: el script carga cada `data-src` y, si existe, reemplaza el placeholder. Serie B ya incluye las escenas en el HTML.

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

## Nota

Docs internos de la postulación viven en `../sufa-portfolio/` y no se publican aquí.
