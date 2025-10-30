# PersonalRadarScreen

## Objetivo
Representar el estado integral del desarrollo personal mediante un gráfico de radar y acciones concretas.

## Componentes clave
- Encabezado con puntuación promedio y mensaje motivacional.
- Selector de período (semana, mes, trimestre).
- Gráfico radar con métricas: Hábitos, Energía, Mentalidad, Aprendizaje, Relaciones.
- Controles tipo slider o stepper para actualizar los valores actuales.
- Lista de recomendaciones personalizadas según métricas bajas.
- Botón "Generar plan de acción" que abre diálogo con sugerencias.

## Interacciones
- Sliders actualizan el gráfico en tiempo real.
- Guardado automático al cambiar valores (debounce).
- Permitir comparar con promedio histórico (toggle).

## Dark/Light Mode
- Fondo degradado sutil en modo claro; fondo sólido en modo oscuro.
- Radar relleno con transparencia y borde visible.
- Tipografías con contraste suficiente.
