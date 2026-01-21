# Проектирование с Cursor

Cursor работает как архитектурный собеседник:
- генерирует варианты
- сравнивает подходы
- выявляет компромиссы
- помогает формировать структуру модулей
- проверяет согласованность решений
- предлагает улучшения без ломки API

Ты остаёшься архитектором. Cursor — генератор вариантов.

## Обсуждение архитектуры модуля

Пример промпта:

```
You are an architect working on telnik-flight-engine — a modular TS flight physics engine.

Task:
Propose 3 architectural variants for the [MODULE NAME] module.

Constraints:
- TS-only
- Pure functions
- No classes
- No hidden state
- Deterministic
- Minimal abstractions
- API must be explicit and stable

Compare variants by:
- clarity
- composability
- performance
- integration with existing modules

Output:
1. Three variants
2. Comparison table
3. Recommendation
```

Cursor выдаст варианты → ты выбираешь → уточняешь.

## Заставить предлагать варианты

Cursor по умолчанию даёт один ответ. Добавляй:
- "Propose 3 variants"
- "Compare them"
- "Explain trade-offs"
- "Give a recommendation"

Cursor станет генератором решений, а не оракулом.

## Проектирование API

После выбора архитектуры — уточняй API.

Пример:

```
Based on Variant 2, propose a minimal API for the module.

Requirements:
- Single pure function (or small set of pure functions)
- No new abstractions
- No classes
- Explicit inputs and outputs
- Follow existing naming conventions

Output:
1. API signature
2. Short explanation
```

Можешь уточнить:
- убрать лишнее
- сделать параметры явными
- убрать implicit state
- сделать API более декларативным

## Проверка архитектурных решений

```
Check if this API aligns with the architecture of telnik-flight-engine.
List:
- matches
- mismatches
- potential improvements
```

Cursor найдёт:
- несогласованности
- нарушения принципов
- потенциальные проблемы
- naming issues

## Проектирование связей модулей

```
Explain how this module should integrate with:
- state update pipeline
- integrator
- atmosphere model
- other force modules

Propose minimal integration points.
```

Cursor предложит:
- где вызывать модуль
- какие данные передавать
- как избежать дублирования
- как сохранить чистоту архитектуры

## Roadmap и декомпозиция

```
Create a roadmap for implementing the [MODULE NAME] module.

Include:
- steps
- dependencies
- risks
- testing strategy
- documentation tasks
```

Получишь:
- чёткий план
- порядок задач
- список рисков
- что тестировать
- что документировать

## Анализ компромиссов

```
Explain trade-offs between Variant 1 and Variant 2.
Focus on:
- performance
- clarity
- maintainability
- composability
```

Помогает принимать решения осознанно.