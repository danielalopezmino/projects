# Portafolio para GitHub Pages

Plantilla de portafolio creada con **Jekyll**, el generador integrado en GitHub Pages. Cada proyecto se publica como una entrada Markdown, sin editar las páginas HTML.

## 1. Personaliza tus datos

Edita `_config.yml` y reemplaza:

- `title`
- `description`
- `author.name`
- `author.role`
- `author.email`
- `author.location`
- enlaces de LinkedIn e Instagram

## 2. Publica un proyecto nuevo

1. Duplica `_drafts/plantilla-proyecto.md` y mueve la copia a `_posts`.
2. Renómbralo con este formato:

   `AAAA-MM-DD-nombre-del-proyecto.md`

3. Edita el bloque inicial entre `---`.
4. Escribe el contenido usando Markdown.
5. Guarda la imagen de portada en `assets/images/`.

Ejemplo:

```md
---
layout: post
title: "Nombre del proyecto"
description: "Resumen corto para la tarjeta del proyecto."
date: 2026-07-28
category: ui-ux
category_label: "UI/UX"
category_url: /ui-ux/
cover: /assets/images/mi-proyecto.jpg
cover_alt: "Descripción accesible de la imagen"
featured: true
year: 2026
client: "Nombre del cliente"
role: "Mi rol"
tools: "Figma, Photoshop"
---

## El reto

Explica aquí el contexto del proyecto.

## Mi proceso

Añade texto, listas e imágenes.

![Descripción de la imagen](/assets/images/otra-imagen.jpg)
```

## Categorías disponibles

Usa exactamente uno de estos valores en `category`:

- `ui-ux`
- `diseno-grafico`
- `fotografia`
- `escritura-creativa`

Pon `featured: true` para mostrar el proyecto en la página de inicio. Usa `false` para mostrarlo únicamente en su categoría.

## 3. Publicar en GitHub Pages

1. Crea preferiblemente un repositorio llamado exactamente `TU-USUARIO.github.io`. Así el sitio quedará publicado en la raíz y no tendrás que configurar rutas adicionales.
2. Sube todos los archivos de esta carpeta a la raíz del repositorio.
3. En GitHub abre **Settings → Pages**.
4. En **Build and deployment**, selecciona **Deploy from a branch**.
5. Selecciona la rama `main` y la carpeta `/ (root)`.
6. Guarda. GitHub publicará el sitio automáticamente.

La URL normalmente será:

`https://TU-USUARIO.github.io/NOMBRE-DEL-REPOSITORIO/`

Las secciones independientes quedarán disponibles en:

- `/ui-ux/`
- `/diseno-grafico/`
- `/fotografia/`
- `/escritura-creativa/`

## 4. Repositorio con nombre de usuario

Si el repositorio se llama exactamente `TU-USUARIO.github.io`, el sitio estará en la raíz y no debes cambiar nada.

Para un repositorio con otro nombre, edita `_config.yml` y cambia `baseurl` por el nombre del repositorio. Ejemplo: `baseurl: "/mi-portafolio"`. La plantilla usa `relative_url`, por lo que los menús y recursos tomarán ese prefijo automáticamente. En las imágenes añadidas dentro de Markdown, usa `{{ site.baseurl }}/assets/images/archivo.jpg` para que también funcionen en un repositorio de proyecto.

## 5. Probar localmente (opcional)

Con Ruby instalado:

```bash
bundle install
bundle exec jekyll serve
```

Después abre `http://localhost:4000`.
