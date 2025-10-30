# Modelo de datos y almacenamiento

## Persistencia
- **Room Database** con tres tablas principales:
  - `tasks`
  - `gym_entries`
  - `radar_metrics`
- **DataStore Preferences** para ajustes como modo oscuro, idioma y recordatorios.

## Esquema Room
```sql
CREATE TABLE tasks (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    title TEXT NOT NULL,
    description TEXT,
    is_completed INTEGER NOT NULL DEFAULT 0,
    due_date INTEGER,
    category TEXT,
    created_at INTEGER NOT NULL,
    updated_at INTEGER NOT NULL
);

CREATE TABLE gym_entries (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    week_start INTEGER NOT NULL,
    weight REAL NOT NULL,
    workouts_done INTEGER NOT NULL,
    notes TEXT,
    created_at INTEGER NOT NULL,
    updated_at INTEGER NOT NULL
);

CREATE TABLE radar_metrics (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    period_start INTEGER NOT NULL,
    period_type TEXT NOT NULL,
    habits REAL NOT NULL,
    energy REAL NOT NULL,
    mindset REAL NOT NULL,
    learning REAL NOT NULL,
    relationships REAL NOT NULL,
    created_at INTEGER NOT NULL,
    updated_at INTEGER NOT NULL
);
```

## Sincronización futura
- API REST opcional con endpoints `/tasks`, `/gym`, `/radar`.
- Uso de `WorkManager` para sincronización en segundo plano.

## Backups
- Exportar a CSV/JSON desde la app.
- Integración con Google Drive opcional.
