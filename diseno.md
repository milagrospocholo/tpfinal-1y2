# Trabajo Práctico: Patitas con Ayuda

---

## Etapa 1 — Investigación y análisis

### 1.1 Elección del caso
- **Nombre:** Patitas con Ayuda
- **Descripción:** Organización sin fines de lucro dedicada al rescate, atención veterinaria, rehabilitación y búsqueda de hogares responsables para perros y gatos en situación de calle o maltrato.
- **Público al que se dirige:**
  1. Familias y personas individuales interesadas en adoptar una mascota de manera responsable.
  2. Personas que desean colaborar como voluntarios, ofreciendo hogares de tránsito, o donando alimento, insumos médicos y dinero.
- **Objetivo principal de la presencia web:**
  Vincular (conectar animales rescatados con adoptantes) y convocar (sumar voluntarios y colaboradores a la causa).
- **Contenidos mínimos del sitio:**
  1. Presentación (misión y llamada a la acción).
  2. Catálogo de animales en adopción (tarjetas con foto y datos).
  3. Formas de ayudar (adopción, voluntariado, donaciones).
  4. Canales de contacto.

---

## Etapa 2 — Diseño del sistema

### 2.1 Definición de variables de diseño

#### Paleta de colores (nombres semánticos)
- `--color-primario: #5C3D2E;` (Marrón café profundo para títulos y marca)
- `--color-accion: #C47B36;` (Caramelo cálido para botones y llamadas a la acción)
- `--color-fondo-principal: #F3ECE4;` (Crema / arena suave para el fondo general)
- `--color-fondo-tarjeta: #FFFFFF;` (Blanco puro para las tarjetas y contenedores)
- `--color-texto-principal: #2B1E16;` (Café muy oscuro para lectura accesible)
- `--color-texto-secundario: #7A685D;` (Tono tierra medio para datos secundarios)
- `--color-borde: #DECFC0;` (Beige claro para bordes y separadores)

#### Escala tipográfica (tamaños nominados)
- `--tipo-pequeno: 0.875rem;` (14px - detalles y etiquetas)
- `--tipo-base: 1rem;` (16px - párrafos y texto general)
- `--tipo-grande: 1.5rem;` (24px - títulos de sección y tarjetas)
- `--tipo-display: 2.25rem;` (36px - título principal hero)
- `--fuente-principal: system-ui, -apple-system, 'Segoe UI', Roboto, sans-serif;`

#### Escala de espaciado (valores nominados y semánticos)
- `--espacio-xs: 0.5rem;` (8px - espaciado mínimo / interno de etiquetas)
- `--espacio-sm: 1rem;` (16px - espaciado de elementos / botones)
- `--espacio-md: 1.5rem;` (24px - espaciado de contenedor / tarjetas y grilla)
- `--espacio-lg: 3rem;` (48px - espaciado entre secciones)

---

### 2.2 Inventario de componentes

#### Átomos
- Botón principal: `.boton`, `.boton--accion`
- Etiqueta informativa: `.etiqueta`
- Imagen de animal: `.imagen-animal`
- Campo de texto: `.campo-texto`
- Logo: `.logo`

#### Moléculas
- Tarjeta de animal: `.tarjeta-animal`
- Formulario de contacto: `.formulario-contacto`
- Menú de navegación: `.nav-menu`

#### Organismos
- Encabezado: `.encabezado`
- Hero / Portada: `.seccion-hero`
- Catálogo de adopciones: `.seccion-adopciones`
- Formas de ayudar: `.seccion-ayuda`
- Pie de página: `.pie-pagina`

---

### 2.3 Estructura de layout (CSS Grid)
- **Grilla base:** Sistema de 12 columnas para el contenedor principal.
- **Comportamiento responsive:**
  - *Mobile (< 768px):* 1 sola columna (`1fr`). Flujo vertical apilado.
  - *Tablet (768px - 1024px):* Grilla a 2 columnas para contenidos y tarjetas.
  - *Desktop (> 1024px):* Grilla a 3 columnas para tarjetas y distribución horizontal de bloques.
- **Posiciones de organismos:**
  - `.encabezado`: ancho completo (`1 / -1`).
  - `.seccion-hero`: ancho completo (`1 / -1`).
  - `.seccion-adopciones`: ancho completo con grilla interna adaptable de tarjetas.
  - `.seccion-ayuda`: ancho completo con columnas internas en desktop.
  - `.pie-pagina`: ancho completo (`1 / -1`).