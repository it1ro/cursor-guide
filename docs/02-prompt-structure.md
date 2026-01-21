# 2. Структура эффективного промпта

## 2.1. Контекст (минимальный, но достаточный)

Cursor не должен “угадывать”, что такое flight-engine.  
Ему нужно короткое, но точное описание:

```
You are working on telnik-flight-engine — a modular TypeScript flight physics engine for browser games.
Architecture principles:
- TS-only, no external dependencies unless absolutely necessary.
- Modular, composable, declarative.
- No hidden state, no side effects.
- Deterministic, reproducible simulation.
- Minimal abstractions, no overengineering.
- API must stay stable and predictable.
```

Это **жёстко ограничивает** его поведение и предотвращает:

- лишние классы,
- новые слои,
- “умные” абстракции,
- магию,
- сторонние библиотеки.

---

## 2.2. Текущая задача (чётко и узко)

Пример:

```
Task: design a minimal module for aerodynamic drag.
Goal: provide a pure function that computes drag force based on velocity, area, density, and drag coefficient.
```

Cursor любит узкие задачи.  
Чем меньше — тем лучше результат.

---

## 2.3. Критерии качества (это твой стиль)

```
Quality criteria:
- Pure function.
- No classes.
- No side effects.
- No new abstractions.
- Follow existing naming conventions.
- Keep the API minimal and explicit.
- Provide usage example.
```

Это превращает Cursor в **инженера, который пишет код в твоём стиле**, а не в своём.

---

## 2.4. Формат ответа

```
Output format:
1. Proposed API (short).
2. Final TypeScript implementation.
3. Usage example.
4. Notes on integration with existing modules.
```

Cursor начинает выдавать структурированные, предсказуемые ответы.

---

## 2.5. Пример полного промпта для flight-engine

```
You are a senior TypeScript engineer working on telnik-flight-engine — a modular TS flight physics engine for browser games.

Architecture principles:
- TS-only, no external deps.
- Modular, composable, declarative.
- Pure functions, no side effects.
- Deterministic simulation.
- Minimal abstractions, stable API.

Task:
Design a minimal aerodynamic drag module.

Quality criteria:
- Pure function.
- No classes.
- No new abstractions.
- Follow existing naming conventions.
- Provide usage example.

Output format:
1. Proposed API.
2. Final TS implementation.
3. Usage example.
4. Integration notes.
```

Это — **идеальный промпт**, который даёт идеальный результат.

---

Навигация: [← Предыдущий](01-principles.md) | [Оглавление](index.md) | [Следующий →](03-design.md)
