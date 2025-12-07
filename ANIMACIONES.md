# 🎬 Animaciones - Guía de Uso

Este proyecto incluye un sistema completo de animaciones CSS creadas con Sass.

## 📁 Archivo Principal
`scss/_animations.scss`

## 🎨 Animaciones Disponibles

### Animaciones de Entrada
- **fadeIn**: Aparece gradualmente
- **slideInUp**: Desliza desde abajo
- **slideInDown**: Desliza desde arriba
- **slideInLeft**: Desliza desde la izquierda
- **slideInRight**: Desliza desde la derecha
- **scaleUp**: Escala desde pequeño (zoom in)

### Animaciones de Movimiento
- **bounce**: Rebote suave
- **pulse**: Pulso/latido
- **float**: Flotación continua
- **shake**: Sacudida horizontal
- **rotate**: Rotación 360°

### Animaciones de Carga
- **shimmer**: Efecto skeleton/placeholder

## 💻 Cómo Usar

### 1. Con clases de utilidad (HTML)
```html
<div class="partido-card fade-in">...</div>
<div class="jugador-card slide-in-up delay-2">...</div>
<button class="btn pulse">Click aquí</button>
```

### 2. Con el mixin en SCSS
```scss
.mi-elemento {
    @include animate(fadeIn, 0.5s, ease-out, 0.2s);
    // nombre, duración, timing, delay
}
```

### 3. Animación manual en SCSS
```scss
.mi-card {
    animation: slideInUp 0.5s ease-out backwards;
    
    &:hover {
        animation: pulse 1s ease-in-out infinite;
    }
}
```

## ⏱️ Clases de Delay

Usa estas clases para crear efectos escalonados:
```html
<div class="partido-card slide-in-up delay-1">Card 1</div>
<div class="partido-card slide-in-up delay-2">Card 2</div>
<div class="partido-card slide-in-up delay-3">Card 3</div>
```

Delays disponibles: `.delay-1` a `.delay-5` (0.1s - 0.5s)

## 🎯 Animaciones Ya Aplicadas en el Proyecto

### Página de Partidos (`_partidos.scss`)
- Cards aparecen con `slideInUp`
- Delays escalonados para cada card
- Hover: elevación suave

### Página de Jugadores (`_jugadores.scss`)
- Cards aparecen con `scaleUp`
- Delays escalonados hasta 9 cards
- Hover: elevación suave

### Página de Clases (`_clases.scss`)
- Description box con `fadeIn`
- Hover: escala ligera (1.02)

### Header (`_header.scss`)
- Título con `slideInLeft`
- Links del nav con elevación en hover

### Botones (`_buttons.scss`)
- Hover: elevación con sombra
- Active: presionado (translateY)

## 🔧 Personalización

### Cambiar duración
```scss
.mi-elemento {
    animation-duration: 1s; // más lento
}
```

### Repetir infinitamente
```scss
.mi-icono {
    animation: float 3s ease-in-out infinite;
}
```

### Crear delay personalizado
```scss
.mi-card {
    animation-delay: 0.7s;
}
```

## 📝 Ejemplo Completo

```html
<!-- HTML -->
<div class="partidos-grid">
    <div class="partido-card">Partido 1</div>
    <div class="partido-card">Partido 2</div>
    <div class="partido-card">Partido 3</div>
</div>
```

```scss
// SCSS
.partidos-grid {
    display: grid;
    
    .partido-card {
        animation: slideInUp 0.5s ease-out backwards;
        
        @for $i from 1 through 6 {
            &:nth-child(#{$i}) {
                animation-delay: #{$i * 0.1}s;
            }
        }
        
        &:hover {
            transform: translateY(-5px);
            transition: all 0.3s ease;
        }
    }
}
```

## 🎨 Consejos de Diseño

1. **No abuses**: Menos es más con las animaciones
2. **Coherencia**: Usa los mismos tipos de animación en elementos similares
3. **Timing**: 0.3s - 0.5s es ideal para interacciones
4. **Performance**: Usa `transform` y `opacity` (más rápidas que otras propiedades)
5. **Accesibilidad**: Respeta `prefers-reduced-motion` para usuarios sensibles al movimiento

## 🚀 Próximos Pasos

Puedes crear tus propias animaciones en `_animations.scss`:

```scss
@keyframes miAnimacion {
    from { /* estado inicial */ }
    to { /* estado final */ }
}

// Luego úsala
.mi-elemento {
    animation: miAnimacion 0.5s ease-out;
}
```
