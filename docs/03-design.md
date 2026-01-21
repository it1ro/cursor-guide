# 3. Cursor в проектировании

Cursor — это не просто исполнитель кода.  
В проектировании он работает как **архитектурный собеседник**, который:

- генерирует варианты,
- сравнивает подходы,
- выявляет компромиссы,
- помогает формировать структуру модулей,
- проверяет архитектурные решения на согласованность,
- предлагает улучшения без ломки API.

Ты остаёшься архитектором.  
Cursor — генератор вариантов и аналитик.

---

## 3.1. Как обсуждать архитектуру модуля с Cursor

Перед реализацией любого модуля flight-engine ты начинаешь с **архитектурного диалога**.

Пример промпта:

```
You are an architect working on telnik-flight-engine — a modular TS flight physics engine.

Task:
Propose 3 architectural variants for the [MODULE NAME] module.

Constraints:
- TS-only.
- Pure functions.
- No classes.
- No hidden state.
- Deterministic.
- Minimal abstractions.
- API must be explicit and stable.

Compare variants by:
- clarity,
- composability,
- performance,
- integration with existing modules.

Output:
1. Three variants.
2. Comparison table.
3. Recommendation.
```

Cursor выдаёт варианты → ты выбираешь → уточняешь.

---

## 3.2. Как заставить Cursor предлагать варианты, а не "единственно верный" подход

Cursor по умолчанию любит давать один ответ.  
Чтобы он стал полезным архитектором, ты всегда добавляешь:

- “Propose 3 variants”
- “Compare them”
- “Explain trade-offs”
- “Give a recommendation”

Это превращает Cursor в **генератор архитектурных решений**, а не в “орекла”.

---

## 3.3. Как проектировать API через Cursor

После выбора архитектурного варианта — уточняешь API.

Пример:

```
Based on Variant 2, propose a minimal API for the module.

Requirements:
- Single pure function (or small set of pure functions).
- No new abstractions.
- No classes.
- Explicit inputs and outputs.
- Follow existing naming conventions.

Output:
1. API signature.
2. Short explanation.
```

Cursor предложит API, а ты можешь уточнить:

- убрать лишнее,
- сделать параметры явными,
- убрать implicit state,
- сделать API более декларативным.

---

## 3.4. Как использовать Cursor для проверки архитектурных решений

После проектирования API можно попросить Cursor проверить:

```
Check if this API aligns with the architecture of telnik-flight-engine.
List:
- matches,
- mismatches,
- potential improvements.
```

Cursor найдёт:

- несогласованности,
- нарушения принципов,
- потенциальные проблемы,
- naming issues.

Это особенно полезно, когда проект растёт.

---

## 3.5. Как использовать Cursor для проектирования модульных связей

flight-engine — модульный, композиционный проект.  
Cursor может помочь проектировать связи:

```
Explain how this module should integrate with:
- state update pipeline,
- integrator,
- atmosphere model,
- other force modules.

Propose minimal integration points.
```

Cursor предложит:

- где вызывать модуль,
- какие данные передавать,
- как избежать дублирования,
- как сохранить чистоту архитектуры.

---

## 3.6. Как использовать Cursor для roadmap и декомпозиции

Cursor отлично умеет превращать архитектурную идею в **план разработки**.

Пример:

```
Create a roadmap for implementing the [MODULE NAME] module.

Include:
- steps,
- dependencies,
- risks,
- testing strategy,
- documentation tasks.
```

Ты получаешь:

- чёткий план,
- порядок задач,
- список рисков,
- что тестировать,
- что документировать.

---

## 3.7. Как использовать Cursor для анализа компромиссов

Cursor может объяснить:

- почему вариант A лучше B,
- какие trade-offs,
- что будет стоить производительности,
- что будет стоить простоты.

Пример:

```
Explain trade-offs between Variant 1 and Variant 2.
Focus on:
- performance,
- clarity,
- maintainability,
- composability.
```

Это помогает принимать архитектурные решения осознанно.