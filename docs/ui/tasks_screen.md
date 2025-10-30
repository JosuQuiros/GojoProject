# TasksScreen

## Objetivo
Permitir al usuario gestionar sus tareas pendientes mediante un checklist intuitivo.

## Componentes clave
- Barra superior con fecha, saludo y botón de configuración.
- Lista vertical con elementos `TaskItem`:
  - Checkbox animado.
  - Título y descripción opcional.
  - Chips para categoría/prioridad.
  - Indicador de fecha límite.
- FAB (Floating Action Button) para agregar una nueva tarea.
- Bottom sheet para filtros (categoría, estado, orden).

## Interacciones
- Tocar el checkbox cambia `isCompleted` con animación de rebote.
- Deslizar a la izquierda muestra acciones "Editar" y "Archivar".
- FAB abre formulario modal.

## Estados vacíos
- Ilustración minimalista y CTA "Crea tu primera tarea".
- Sugerencia para importar hábitos recurrentes.

## Dark/Light Mode
- Usa `MaterialTheme.colorScheme`.
- Superficies con contraste adecuado y tarjetas con bordes suaves.
