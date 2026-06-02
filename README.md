# CourseHub - Plataforma de Cursos en Línea (Versión 2)

¡Bienvenido a **CourseHub**! Una plataforma web interactiva y moderna para la gestión y aprendizaje de cursos en línea, construida con tecnologías web estándar (HTML5, CSS3, JavaScript) y persistencia del lado del cliente.

Este proyecto simula el comportamiento de una aplicación web completa, incluyendo registro de usuarios, inicio de sesión, perfiles personalizados, un catálogo de cursos y la posibilidad de cambiar de tema (claro/oscuro) de manera global.

---

## 📁 Estructura del Proyecto

A continuación se detalla la organización de los archivos en el proyecto:

```bash
CourseHub2/
├── presentacion.html         # Página de aterrizaje (Landing Page) interactiva y principal
├── presentacion.css          # Estilos generales y animaciones de la landing page
├── presentacion.js           # Lógica interactiva para la landing page
├── cursos.html               # Catálogo de cursos disponibles y buscador interactivo
├── ini_sesion.html           # Interfaz de inicio de sesión de usuarios
├── registro.html             # Interfaz de registro para nuevos usuarios
├── usuario.html              # Perfil de usuario y visualización de progreso/sesión
├── nosotros.html             # Información sobre la misión, visión y el equipo de CourseHub
├── auth.js                   # Controlador del sistema de autenticación (LocalStorage)
├── tema.js                   # Gestor para alternar y guardar el estado del Tema Oscuro/Claro
└── usuarios_registrados.txt  # Estructura del backup local generado para los usuarios
```

---

## 🚀 Características Principales

1. **Autenticación en el Cliente (Sin Servidor Backend):**
   * Controlado a través de [auth.js](file:///e:/Trabajos%20chidos/CourseHub2/auth.js).
   * Almacenamiento seguro de usuarios registrados y sesiones activas en el navegador mediante `localStorage` (`coursehub_db_v2` y `coursehub_session_v2`).
   * Validación avanzada para prevenir correos electrónicos o nombres de usuario duplicados.
   * Exportación de la base de datos de usuarios en formato de texto legible (`usuarios_registrados.txt`).

2. **Diseño Adaptativo y Moderno (Responsive Design):**
   * Interfaces construidas pensando en la experiencia del usuario (UX) en dispositivos móviles y de escritorio.
   * Transiciones y animaciones suaves para guiar la atención del usuario.

3. **Tema Oscuro Persistente:**
   * Controlado a través de [tema.js](file:///e:/Trabajos%20chidos/CourseHub2/tema.js).
   * Detecta automáticamente las preferencias de tema del sistema operativo del usuario.
   * Guarda de forma permanente la preferencia elegida mediante `localStorage`.

4. **Panel de Usuario y Cursos:**
   * Gestión dinámica de vistas en base a si el usuario tiene una sesión activa o no (redirecciones automáticas si intenta entrar sin estar autenticado).
   * Filtrado y navegación intuitiva dentro del catálogo de cursos.

---

## 🛠️ Tecnologías Utilizadas

* **HTML5:** Estructura semántica para mejorar la accesibilidad y el posicionamiento SEO local.
* **CSS3:** Estilos responsivos utilizando Flexbox, Grid y variables CSS avanzadas para el soporte de temas.
* **JavaScript (Vanilla ES6+):** Lógica orientada a objetos y programación modular sin dependencias externas pesadas, asegurando tiempos de carga rápidos.
* **LocalStorage API:** Persistencia y almacenamiento de datos local en el navegador web del cliente.

---

## 💻 Instrucciones de Uso

Para ejecutar el proyecto localmente, sigue estos sencillos pasos:

1. **Clona o descarga** este repositorio en tu máquina local.
2. Abre el archivo principal [presentacion.html](file:///e:/Trabajos%20chidos/CourseHub2/presentacion.html) en tu navegador web preferido (Google Chrome, Firefox, Edge, Safari).
3. Para una experiencia óptima de desarrollo y simulación de redirecciones, se recomienda abrir el proyecto utilizando un servidor local como la extensión **Live Server** en VS Code, o ejecutando en terminal:
   ```bash
   python -m http.server 8000
   ```
   Luego ingresa a `http://localhost:8000/presentacion.html` en tu navegador.
