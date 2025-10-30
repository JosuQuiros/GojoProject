# Especificación general de la app

## Arquitectura propuesta
- **Lenguaje**: Kotlin con Jetpack Compose.
- **Patrón**: Clean Architecture + MVVM.
- **Capas**:
  - **UI**: pantallas Compose, navegación `Navigation Compose`, estados inmutables gestionados con ViewModels.
  - **Dominio**: casos de uso para tareas, progreso físico y desarrollo personal.
  - **Datos**: repositorios que combinan Room (persistencia) y DataStore (preferencias).
- **Inyección de dependencias**: Hilt.

## Navegación
Tres tabs principales con barra inferior:
1. **Tareas** (`TasksScreen`)
2. **Progreso Gym** (`GymProgressScreen`)
3. **Radar Personal** (`PersonalRadarScreen`)

Cada tab tendrá subtareas específicas:
- `TasksScreen`: lista de tareas, botón flotante para agregar, filtros y estadísticas rápidas.
- `GymProgressScreen`: formulario semanal (fecha, peso, métricas opcionales), historial, gráfico de línea.
- `PersonalRadarScreen`: sliders o inputs para valores (hábitos, energía, mentalidad, aprendizaje, relaciones), gráfico radar y recomendaciones.

## Estado y datos
- **Tareas**
  - Entidad: `Task(id, title, description, isCompleted, dueDate, category)`.
  - Acciones: crear, editar, completar, archivar.
  - Vista: checklist con opción de agrupar por categoría o fecha.

- **GymProgress**
  - Entidad: `GymEntry(id, weekStart, weight, workoutsDone, notes)`.
  - Datos para gráfico: pares `(fecha, peso)`. Se usará `MPAndroidChart` o Compose Charts.

- **PersonalRadar**
  - Entidad: `RadarMetric(name, score)` con rangos 0-10.
  - Se almacenan los últimos valores y un historial mensual.

## UI y estilo
- Temas claro y oscuro con color primario inspirado en azules/teal y secundarios neutros.
- Tipografía `Inter` o `Roboto`.
- Componentes reutilizables: tarjetas (`Surface`), botones rellenos y outlined, chips para filtros.
- Animaciones sutiles: transiciones en tabs, animación al completar tareas.

## Plan de desarrollo
1. **Iteración 1**: configurar proyecto, navegación y pantallas base con datos mock.
2. **Iteración 2**: persistencia local (Room + DataStore), formularios y validaciones.
3. **Iteración 3**: gráficos dinámicos y estadísticas, exportación de datos.
4. **Iteración 4**: sincronización en la nube opcional y notificaciones inteligentes.

## Métricas de éxito
- Tiempo medio para registrar tarea < 10s.
- Registro semanal constante (al menos 1 vez por semana).
- Visualización clara del progreso con gráficos responsivos.
