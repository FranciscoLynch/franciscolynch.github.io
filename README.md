# franciscolynch.github.io

Portfolio personal construido con [Hugo](https://gohugo.io/) y el tema [PaperMod](https://github.com/adityatelange/hugo-PaperMod).

## Qué es

Mi sitio web personal donde muestro proyectos, escribo posts sobre SysAdmin & DevOps, y comparto información de contacto. Disponible en español e inglés.

## Cómo funciona

- **Hugo** genera el sitio estático a partir de archivos Markdown en `content/`.
- **PaperMod** es el tema, incluido como git submodule en `themes/PaperMod/`.
- La configuración del sitio está en `hugo.yml`.
- Los layouts custom están en `layouts/` y los estilos en `assets/css/`.

### Estructura

```
content/          → Contenido del sitio (posts, proyectos, contacto)
layouts/          → Templates custom
assets/css/       → Estilos custom
themes/PaperMod/  → Tema (submodule)
hugo.yml          → Configuración de Hugo
.github/workflows → CI/CD para deploy automático
```

## Desarrollo local

Requisitos: [Hugo Extended](https://gohugo.io/installation/) (v0.112+)

```bash
# Clonar con submodules
git clone --recurse-submodules https://github.com/FranciscoLynch/franciscolynch.github.io.git
cd franciscolynch.github.io

# Levantar servidor local
hugo server -D
```

El sitio queda disponible en `http://localhost:1313/`.
