# 🔗 Prophet Code Link Tree

Una página link-in-bio moderna, performante y visualmente impactante construida con Astro. Este proyecto sirve como un hub centralizado para todas las redes sociales, cursos, portafolio y enlaces de contacto de Prophet Code.

## ✨ Características

- 🎨 **UI/UX Moderna** - Diseño glassmorphism elegante con animaciones suaves y efectos hover
- 🚀 **Ultra Rápido** - Construido con Astro para rendimiento óptimo y cero JavaScript por defecto
- 📱 **Totalmente Responsivo** - Diseño adaptativo que funciona perfectamente en móvil, tablet y desktop
- 🖼️ **Imágenes Optimizadas** - Imágenes responsivas con art direction usando elementos `<picture>` nativos
- 🎯 **Type-Safe** - TypeScript en todo el proyecto para mejor experiencia de desarrollo
- 🎭 **Iconos Personalizados** - Iconos SVG hechos a mano como componentes Astro reutilizables
- 🧩 **Componentes Modulares** - Componentes de botones y enlaces reutilizables con arquitectura basada en slots
- 🎨 **SCSS con Mixins** - Sistema de breakpoints responsivos con utilidades SCSS personalizadas
- ♿ **Accesible** - HTML semántico y atributos ARIA apropiados


## ���️ Stack Tecnológico

- **Framework:** [Astro](https://astro.build)
- **Estilos:** SCSS con mixins personalizados
- **Lenguaje:** TypeScript
- **Iconos:** Componentes SVG personalizados
- **Optimización de Imágenes:** Astro Assets con imágenes responsivas

## ��� Estructura del Proyecto

Dentro del proyecto de Astro, verás las siguientes carpetas y archivos:

```text
/
├── public/
│   └── favicon.svg
├── src/
│   ├── assets/              # Imágenes y recursos estáticos
│   │   ├── me.webp
│   │   ├── heroe-mobile.webp
│   │   └── heroe-desktop.webp
│   ├── components/          # Componentes UI reutilizables
│   │   ├── HubLinkComponent.astro
│   │   ├── HubComponent.astro
│   │   └── SocialNetworksComponent.astro
│   ├── constants/           # Constantes y configuración global
│   │   └── prophet-code-links.ts
│   ├── icons/               # Componentes de iconos SVG
│   │   ├── TikTokIcon.astro
│   │   ├── YouTubeIcon.astro
│   │   ├── InstagramIcon.astro
│   │   └── TwitchIcon.astro
│   ├── layouts/             # Layouts de página
│   │   └── Layout.astro
│   ├── pages/               # Enrutamiento basado en archivos
│   │   └── index.astro
│   └── styles/              # Estilos globales y utilidades SCSS
│       ├── index.scss
│       └── _tools.scss      # Mixins responsivos
├── astro.config.mjs         # Configuración de Astro con alias de rutas
└── tsconfig.json            # Configuración de TypeScript
```

## 🧞 Comandos

Todos los comandos se ejecutan desde la raíz del proyecto:

| Comando                   | Acción                                                |
| :------------------------ | :---------------------------------------------------- |
| `npm install`             | Instala las dependencias                              |
| `npm run dev`             | Inicia servidor de desarrollo en `localhost:4321`     |
| `npm run dev -- --host`   | Inicia servidor accesible en la red local             |
| `npm run build`           | Construye el sitio de producción en `./dist/`         |
| `npm run preview`         | Previsualiza la build localmente antes de desplegar   |
| `npm run astro ...`       | Ejecuta comandos CLI como `astro add`, `astro check`  |

## 🎨 Características Clave Explicadas

### Sistema de Breakpoints Responsivos

Sistema de mixins SCSS personalizado para diseño responsivo consistente:

```scss
@use '../styles/tools' as tools;

.component {
  font-size: 1rem;
  
  @include tools.respond-to('md') {
    font-size: 1.25rem;
  }
}
```

### Path Aliases

El proyecto usa el alias `@/` para imports más limpios:

```ts
import Layout from '@/layouts/Layout.astro';
import { YOUTUBE_URL } from '@/constants/prophet-code-links';
```

### Componentes de Iconos

Los iconos están implementados como componentes Astro reutilizables con props personalizables:

```astro
<TikTokIcon width={32} fill="#fff" />
```

### Imágenes Responsivas con Art Direction

Diferentes imágenes para móvil y desktop usando `<picture>` HTML nativo:

```astro
<picture>
  <source media="(min-width: 768px)" srcset={heroeDesktopImg.src} />
  <img src={heroeMobileImg.src} alt="..." />
</picture>
```

## 📝 Configuración

### Agregar Nuevos Enlaces

Edita `src/constants/prophet-code-links.ts` para agregar o modificar enlaces:

```ts
export const YOUTUBE_URL = 'https://youtube.com/@prophetcode';
export const NEW_LINK_URL = 'https://your-link.com';
```

### Personalizar Colores

Actualiza las custom properties CSS en `src/styles/index.scss`:

```scss
:root {
  --primary-color: #AA0C18;
  --accent-color: #FFC360;
  --neutral-black-color: #1C1C1C;
}
```

### Breakpoints Responsivos

Modifica los breakpoints en `src/styles/_tools.scss`:

```scss
$sm-breakpoint: 576px;
$md-breakpoint: 768px;
$lg-breakpoint: 992px;
```

## 🚢 Despliegue

Este proyecto puede ser desplegado en cualquier servicio de hosting estático:

- [Vercel](https://vercel.com)
- [Netlify](https://netlify.com)
- [Cloudflare Pages](https://pages.cloudflare.com)
- [GitHub Pages](https://pages.github.com)

Construye el proyecto con `npm run build` y despliega la carpeta `dist/`.

## 👨‍💻 Autor

**Alexander Avila** - Prophet Code
- YouTube: [@prophetcode](https://youtube.com/@prophetcode)
- Twitch: [@prophetcode](https://twitch.tv/prophetcode)

---

Construido con ❤️ usando [Astro](https://astro.build)
