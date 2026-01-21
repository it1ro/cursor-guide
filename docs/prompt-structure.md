# Структура промпта

## Контекст

Коротко и точно. Cursor не должен угадывать.

Пример:

```
You are working on telnik-flight-engine — a modular TypeScript flight physics engine for browser games.

Architecture principles:
- TS-only, no external dependencies unless absolutely necessary
- Modular, composable, declarative
- No hidden state, no side effects
- Deterministic, reproducible simulation
- Minimal abstractions, no overengineering
- API must stay stable and predictable
```

Это ограничивает поведение и предотвращает:
- лишние классы
- новые слои
- "умные" абстракции
- магию
- сторонние библиотеки

## Задача

Чётко и узко.

Пример:

```
Task: design a minimal module for aerodynamic drag
Goal: provide a pure function that computes drag force based on velocity, area, density, and drag coefficient
```

Чем меньше задача — тем лучше результат.

## Критерии качества

Это твой стиль.

```
Quality criteria:
- Pure function
- No classes
- No side effects
- No new abstractions
- Follow existing naming conventions
- Keep the API minimal and explicit
- Provide usage example
```

Cursor начнёт писать код в твоём стиле, а не в своём.

## Формат ответа

```
Output format:
1. Proposed API (short)
2. Final TypeScript implementation
3. Usage example
4. Notes on integration with existing modules
```

Cursor выдаст структурированный ответ.

## Полный пример

```
You are a senior TypeScript engineer working on telnik-flight-engine — a modular TS flight physics engine for browser games.

Architecture principles:
- TS-only, no external deps
- Modular, composable, declarative
- Pure functions, no side effects
- Deterministic simulation
- Minimal abstractions, stable API

Task:
Design a minimal aerodynamic drag module

Quality criteria:
- Pure function
- No classes
- No new abstractions
- Follow existing naming conventions
- Provide usage example

Output format:
1. Proposed API
2. Final TS implementation
3. Usage example
4. Integration notes
```

Это даёт предсказуемый результат.