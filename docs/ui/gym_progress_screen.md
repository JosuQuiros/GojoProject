# GymProgressScreen

## Objetivo
Registrar el progreso semanal del gimnasio y visualizar la evolución del peso corporal.

## Componentes clave
- Cabecera con progreso semanal (porcentaje de workouts completados).
- Formulario con campos:
  - Fecha (selector de semana).
  - Peso corporal (kg).
  - Entrenamientos completados (0-7).
  - Notas opcionales.
- Botón primario "Guardar semana" con estado de carga.
- Sección "Historial" con tarjetas resumidas.
- Gráfico de línea con los últimos 12 registros (deslizables).

## Interacciones
- Validaciones en vivo: peso > 0, semana no duplicada.
- Al guardar, mostrar snack bar de confirmación.
- Permitir editar registros desde el historial.

## Visualización del gráfico
- Eje X: semanas (formato `dd MMM`).
- Eje Y: peso en kg.
- Líneas suaves (`cubic Bézier`).
- Punto resaltado para la última medición.
- Soporte de gestos (zoom/pan) opcional.

## Dark/Light Mode
- Líneas con colores adaptados (azul brillante en oscuro, teal en claro).
- Fondo del gráfico transparente sobre `Surface`.
