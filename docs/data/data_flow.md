# Flujo de datos y casos de uso

## Casos de uso principales
1. **Crear tarea**
   - Validar campos obligatorios.
   - Insertar en `tasks`.
   - Mostrar snackbar de confirmación.

2. **Completar tarea**
   - Actualizar `is_completed` y `updated_at`.
   - Registrar evento para estadísticas semanales.

3. **Registrar semana de gym**
   - Verificar que `week_start` no exista.
   - Calcular diferencia de peso vs semana anterior.
   - Actualizar gráfico inmediatamente.

4. **Actualizar radar personal**
   - Recoger valores de sliders.
   - Normalizar (0-10) y guardar en `radar_metrics`.
   - Recomendar acciones basadas en valores < 6.

## Integraciones
- **Notificaciones locales**: recordatorios diarios para completar tareas y formulario semanal.
- **Widgets**: versión simplificada del checklist y gráfico de peso.
- **Uso offline**: toda la funcionalidad debe operar sin conexión, sincronizando cuando sea posible.
