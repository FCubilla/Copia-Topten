# 🎾 Topten - Plataforma de Pádel

Plataforma web para reservar canchas de pádel, encontrar jugadores y unirse a clases.

## 📋 Descripción

Topten es un sitio web que facilita la gestión de partidos de pádel, permitiendo a los usuarios:
- Reservar canchas y horarios
- Buscar jugadores disponibles
- Inscribirse en clases
- Consultar información sobre las instalaciones

## 🚀 Tecnologías Utilizadas

- **HTML5**: Estructura semántica
- **CSS3**: Estilos y animaciones
- **Sass/SCSS**: Preprocesador CSS con arquitectura modular
- **Bootstrap 5**: Framework CSS (via CDN)
- **Git**: Control de versiones

## 🎨 Características del Proyecto

### Arquitectura Sass
- Variables centralizadas para colores, espaciado y tipografía
- Mixins reutilizables para responsive, flexbox, grid
- Extends con placeholders para componentes comunes
- Separación por páginas y componentes
- Sistema de animaciones CSS

### Animaciones
- Animaciones de entrada (fadeIn, slideIn, scaleUp)
- Efectos hover en cards y botones
- Delays escalonados para elementos múltiples
- Transiciones suaves en navegación

### Páginas
- **Inicio**: Bienvenida y galería
- **Partidos**: Listado de partidos y reservas de canchas
- **Jugadores**: Perfiles de jugadores disponibles
- **Clases**: Información sobre clases y entrenamientos
- **Sobre Nosotros**: Información de contacto

## 🛠️ Instalación y Uso

### Prerrequisitos
- [Sass](https://sass-lang.com/install) instalado

### Compilar Sass

```bash
# Compilación única
sass scss/style.scss:assets/css/style.css

# Modo watch (compilación automática)
sass --watch scss/style.scss:assets/css/style.css
```

### Ver el proyecto
Abre `index.html` en tu navegador o usa un servidor local.

## 📖 Documentación Adicional

- **[ANIMACIONES.md](ANIMACIONES.md)**: Guía completa del sistema de animaciones

## 👤 Autor

**FCubilla**

## 📄 Licencia

Este proyecto es de código abierto.
