# sufa-genai-portfolio

Portfolio estático de **product imaging con IA** (Agustín Expósito).

**URL objetivo:** https://aguexposito.github.io/sufa-genai-portfolio/

## Contenido

- Serie A / B: foto base real + slots de escenas (img2img + ControlNet + IP-Adapter).
- Las escenas pendientes se muestran como placeholder hasta que existan los JPG.

## Actualizar escenas (Fase 3b)

Copiar los JPG generados con estos nombres exactos:

```
images/serie-a/01_living_dia.jpg
images/serie-a/02_living_noche.jpg
images/serie-a/03_loft.jpg
images/serie-b/01_lectura.jpg
images/serie-b/02_dormitorio.jpg
images/serie-b/03_showroom.jpg
```

No hace falta editar el HTML: el script carga cada `data-src` y, si existe, reemplaza el placeholder.

Luego:

```bash
git add images/
git commit -m "Add generated product scene images"
git push
```

## Deploy a GitHub Pages

Esta carpeta ya tiene git local (`main`) con el commit inicial.

**Opción A — GitHub CLI** (si tenés `gh` instalado y autenticado):

```bash
cd 0-OfertasTrabajo/sufa-genai-portfolio
gh repo create AguExposito/sufa-genai-portfolio --public --source=. --remote=origin --push
# Luego: Settings → Pages → Branch main / root /
```

**Opción B — manual (recomendada si no hay `gh`):**

1. En GitHub.com crear repo público vacío `AguExposito/sufa-genai-portfolio` (sin README).
2. En esta carpeta:

```bash
cd 0-OfertasTrabajo/sufa-genai-portfolio
git remote add origin https://github.com/AguExposito/sufa-genai-portfolio.git
git push -u origin main
```

3. Repo → **Settings → Pages** → Source: Deploy from branch → `main` / `/` (root) → Save.
4. Abrir https://aguexposito.github.io/sufa-genai-portfolio/ (puede tardar 1–2 min).

## Preview local

Abrir `index.html` en el navegador, o:

```bash
npx --yes serve .
```

## Nota

Docs internos (BRIEF, PROMPTS, checklist) viven en `../sufa-portfolio/` y no se publican aquí.
