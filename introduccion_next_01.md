# Definición Next.js:
Next.js es un marco de desarrollo web de código abierto construido sobre Node.js y React que permite la creación de aplicaciones web de una sola página (SPA), aplicaciones web renderizadas en el servidor (SSR) y aplicaciones web estáticas (SSG). Fue desarrollado por Vercel (anteriormente conocido como Zeit) y se ha vuelto muy popular en la comunidad de desarrollo web debido a su enfoque en el rendimiento, la optimización y la facilidad de uso.

### Características principales de Next.js:

1. **Renderizado en el Servidor (SSR)**: Next.js permite el renderizado en el servidor de aplicaciones React, lo que mejora el rendimiento y la optimización para motores de búsqueda.

2. **Generación Estática de Sitios (SSG)**: También ofrece la capacidad de generar páginas estáticas en tiempo de compilación, lo que es útil para sitios que no necesitan actualizaciones en tiempo real.

3. **Desarrollo en Modo "Hot Reload"**: Next.js recarga automáticamente las páginas cuando se realizan cambios en el código, lo que facilita el desarrollo.

4. **Rutas Basadas en Archivos**: La estructura de rutas en Next.js se basa en el sistema de archivos, lo que hace que la configuración de rutas sea sencilla y fácil de entender.

5. **API Routes**: Next.js permite crear rutas API en el mismo proyecto, lo que facilita la construcción de aplicaciones full-stack.

6. **Optimización de Imágenes**: Viene con capacidades incorporadas para optimizar imágenes, lo que mejora el rendimiento de la página.

7. **Soporte para TypeScript**: Next.js tiene soporte nativo para TypeScript, lo que permite un desarrollo más robusto y seguro.

8. **División de Código Automática**: Next.js divide automáticamente el código para optimizar el rendimiento de la página, cargando solo los componentes necesarios para cada página.

9. **Amplia Comunidad y Ecosistema**: Dado que es una herramienta popular, hay una amplia gama de plugins, bibliotecas y recursos de la comunidad disponibles.

10. **Integración Fácil con Vercel**: Next.js se integra perfectamente con la plataforma de alojamiento Vercel, aunque también se puede alojar en otros servicios.

Es una herramienta muy versátil que se puede utilizar para una amplia variedad de proyectos web, desde blogs y portafolios hasta aplicaciones empresariales a gran escala.

---

# 4.1 ¿Qué es SSR?

El término "SSR" se refiere a "Server-Side Rendering" o "Renderizado en el Servidor" en español. Es una técnica utilizada en el desarrollo web para mejorar el rendimiento y la optimización para motores de búsqueda (SEO) de aplicaciones de una sola página (SPA).

### ¿Cómo funciona el SSR?

En una aplicación SPA típica, todo el código se ejecuta en el navegador del cliente. Esto significa que cuando un usuario visita la página, el servidor envía un archivo HTML vacío junto con los archivos JavaScript necesarios. El navegador ejecuta estos scripts para generar el contenido de la página. Aunque esto permite una experiencia de usuario muy interactiva, tiene algunas desventajas, como un tiempo de carga inicial más largo y problemas con el SEO.

En el SSR, el servidor genera el contenido HTML de la página en el servidor mismo antes de enviarlo al navegador. Esto significa que el navegador recibe una página completamente renderizada desde el servidor, lo que mejora el tiempo de carga inicial y facilita que los motores de búsqueda indexen la página.

### Ventajas del SSR:

1. **Mejor SEO**: Dado que el contenido se genera en el servidor, los motores de búsqueda pueden rastrear e indexar la página más fácilmente.

2. **Rendimiento Mejorado**: Al recibir una página completamente renderizada, el tiempo de carga inicial es generalmente más rápido.

3. **Contenido Dinámico**: El SSR permite generar contenido dinámico en el servidor, lo que es útil para mostrar información que cambia con frecuencia.

4. **Compatibilidad**: Algunos navegadores o configuraciones de red pueden tener limitaciones con JavaScript. El SSR garantiza que los usuarios vean el contenido incluso si JavaScript está deshabilitado en su navegador.

### Desventajas del SSR:

1. **Carga en el Servidor**: Dado que el servidor tiene que generar el contenido para cada solicitud, esto puede aumentar la carga en el servidor.

2. **Complejidad**: Implementar SSR puede ser más complejo que una SPA tradicional, especialmente cuando se trata de manejar estados, caché, etc.

En resumen, el SSR es una técnica que puede mejorar significativamente el rendimiento y la accesibilidad de una aplicación web, pero viene con su propio conjunto de desafíos y consideraciones.

# 4.2 ¿Como crear una aplicaicón de Next?
Crear una aplicación con Next.js es un proceso bastante sencillo y directo. A continuación se describen los pasos básicos para configurar una nueva aplicación Next.js desde cero:

### Requisitos previos:

- Node.js y npm instalados en tu máquina. Puedes descargarlos desde [el sitio web oficial de Node.js](https://nodejs.org/).

### Pasos para crear una aplicación Next.js:

1. **Instalar Create Next App**: Abre una terminal y ejecuta el siguiente comando para instalar el generador de aplicaciones Next.js, si aún no lo has hecho:

    ```bash
    npm install -g create-next-app
    ```

    O simplemente puedes usar `npx` que viene con npm 5.2.0 y versiones superiores.

2. **Crear una nueva aplicación**: Ejecuta el siguiente comando para crear una nueva aplicación Next.js. Reemplaza `mi-aplicacion-next` con el nombre que desees para tu proyecto.

    ```bash
    npx create-next-app mi-aplicacion-next
    ```

    Esto creará un nuevo directorio con el nombre `mi-aplicacion-next`, instalará todas las dependencias necesarias y configurará un proyecto Next.js básico para ti.

3. **Navegar al directorio del proyecto**: 

    ```bash
    cd mi-aplicacion-next
    ```

4. **Iniciar el servidor de desarrollo**: Ejecuta el siguiente comando para iniciar el servidor de desarrollo:

    ```bash
    npm run dev
    ```

    O si prefieres usar `yarn`:

    ```bash
    yarn dev
    ```

    Ahora deberías poder abrir tu navegador y navegar a `http://localhost:3000` para ver tu nueva aplicación Next.js en acción.

### Estructura básica del proyecto:

- `pages/`: Este directorio contiene todas las páginas de tu aplicación. Cada archivo de React en este directorio se convierte automáticamente en una ruta accesible.
  
- `public/`: Este directorio se utiliza para servir archivos estáticos como imágenes, archivos CSS, etc.

- `styles/`: Este directorio contiene archivos CSS globales.

- `package.json`: Este archivo contiene todas las dependencias y scripts para tu proyecto.

### Crear una página:

Para crear una nueva página, simplemente añade un nuevo archivo `.js` (o `.tsx` si estás usando TypeScript) en el directorio `pages/`. Por ejemplo, para crear una página llamada "acerca", añadirías un archivo llamado `acerca.js` en el directorio `pages/` y exportarías un componente React desde él.

```javascript
// pages/acerca.js

export default function Acerca() {
  return (
    <div>
      <h1>Acerca de nosotros</h1>
      <p>Esta es la página acerca de nuestra aplicación.</p>
    </div>
  );
}
```

### Estructura básica

- **`pages/`**: Este es quizás el directorio más importante en un proyecto Next.js. Cada archivo de React en este directorio se convierte automáticamente en una página web. Los nombres de los archivos se mapean a las rutas de la aplicación. Por ejemplo, `pages/index.js` se mapea a la ruta raíz (`/`), y `pages/about.js` se mapea a `/about`.

  - **`pages/api/`**: Este subdirectorio se utiliza para definir funciones de API. Cada archivo en este directorio se convierte en una ruta de API accesible.

- **`public/`**: Este directorio se utiliza para almacenar todos los archivos estáticos como imágenes, iconos, y cualquier otro recurso público. Los archivos aquí son accesibles desde la raíz del dominio. Por ejemplo, `public/logo.png` sería accesible como `<dominio>/logo.png`.

- **`styles/`**: Este directorio generalmente contiene tus archivos CSS globales. En un proyecto generado con `create-next-app`, encontrarás dos archivos CSS de ejemplo aquí.

- **`node_modules/`**: Este directorio contiene todas las bibliotecas y paquetes que se instalan a través de npm o yarn. No debes modificar nada aquí.

- **`package.json`**: Este archivo contiene metadatos sobre tu proyecto y las dependencias que utiliza. También define scripts que puedes ejecutar con `npm` o `yarn`.

- **`package-lock.json`** o **`yarn.lock`**: Estos archivos bloquean las versiones de las dependencias que tu proyecto utiliza. Se generan automáticamente cuando instalas paquetes con npm o yarn.

- **`.gitignore`**: Este archivo le dice a Git qué archivos o directorios ignorar en el repositorio.

- **`README.md`**: Este archivo generalmente contiene información sobre el proyecto, cómo ejecutarlo, etc.

### Estructura avanzada

Si bien los directorios y archivos anteriores son los más comunes, puedes encontrar o añadir otros según las necesidades de tu proyecto:

- **`components/`**: Este directorio no se crea automáticamente, pero es una práctica común almacenar aquí los componentes de React reutilizables.

- **`lib/`**: Este directorio se utiliza a menudo para almacenar código utilitario y funciones auxiliares.

- **`config/`**: Algunos proyectos pueden incluir un directorio de configuración para almacenar archivos de configuración, como configuraciones de Webpack personalizadas.

- **`tests/`**: Este directorio se utiliza para almacenar pruebas, aunque la ubicación y la estructura de los archivos de prueba pueden variar según la biblioteca de pruebas que estés utilizando.

- **`.env`**: Este archivo se utiliza para almacenar variables de entorno que tu aplicación necesita. Es importante no almacenar información sensible en este archivo si se va a subir al control de versiones.

- **`tsconfig.json`**: Si estás utilizando TypeScript, este archivo contiene las configuraciones específicas de TypeScript para tu proyecto.

Esta estructura de carpetas hace que sea fácil escalar tu proyecto a medida que crece, y la convención sobre configuración en Next.js facilita la adición de nuevas características y páginas.


