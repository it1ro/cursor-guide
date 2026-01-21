# Настройки Cursor

## Критичные настройки

### Model

**Где:** верхняя панель → Model

**Что:** выбрать максимальную доступную модель

**Зачем:** влияет на качество архитектурных решений, рефакторинга и понимания контекста

### Codebase Indexing

**Где:** Settings → Codebase

**Что:** включить индексацию проекта

**Зачем:** Cursor видит структуру, типы, функции, naming conventions

### Multi-file Edits

**Где:** Settings → AI Editing

**Что:** включить multi-file edits + включить "Show plan before applying changes"

**Зачем:** безопасные массовые изменения, контроль перед применением

### Git Integration

**Где:** Sidebar → Git

**Что:** включить Git, разрешить диффы, автокоммиты

**Зачем:** контроль изменений, откаты, прозрачность

### Inline Suggestions

**Где:** Settings → Editor → Inline AI

**Что:** включить AI-подсказки в редакторе

**Зачем:** ускоряет рутину, автодополнение в твоём стиле

## Удобные настройки

### Custom Instructions

**Где:** Settings → AI Behavior → Custom Rules

**Что:** добавить правила проекта:
- TS-only
- pure functions
- deterministic
- no classes
- no hidden state
- minimal abstractions

**Зачем:** Cursor пишет код в твоём стиле автоматически

### Prompt Templates

**Где:** Settings → Templates

**Что:** создать шаблоны:
- архитектура
- API
- тесты
- документация
- рефакторинг

**Зачем:** ускоряет повторяющиеся задачи

### File Exclusions

**Где:** Settings → Codebase → Ignore Patterns

**Что:** исключить:
- `dist/`
- `node_modules/`
- большие JSON
- build-артефакты

**Зачем:** Cursor не тратит контекст на мусор

### Auto-formatting

**Где:** Settings → Editor → Formatting

**Что:** включить Prettier, ESLint, автофикс

**Зачем:** чистый, единообразный код

### Terminal Integration

**Где:** Bottom panel → Terminal

**Что:** использовать встроенный терминал

**Зачем:** запуск тестов/линтеров без переключений

## Дополнительные настройки

### UI Preferences

**Где:** Settings → Appearance

**Что:** тёмная тема, компактный интерфейс, скрытие панелей

**Зачем:** меньше визуального шума

### Cloud Sync

**Где:** Settings → Account → Sync

**Что:** синхронизация настроек и шаблонов

**Зачем:** удобно при работе на нескольких устройствах

### Experimental Features

**Где:** Settings → Experiments

**Что:** включить экспериментальные улучшения (если доступны)

**Зачем:** более умный рефакторинг и контекст

### Cursor Agents

**Где:** если доступны

**Что:** автоматизация рутинных задач

**Зачем:** ускоряет миграции, boilerplate, массовые изменения