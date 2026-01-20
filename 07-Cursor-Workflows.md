_(готовые шаблоны для работы с Cursor в telnik-flight-engine)_

---

# 7.1. Workflow: Архитектурный анализ модуля

Используй, когда начинаешь новый модуль или хочешь пересмотреть существующий.

```
You are an architect working on telnik-flight-engine.

Context:
- TS-only
- pure functions
- deterministic
- modular and composable
- no classes
- no hidden state
- minimal abstractions

Task:
Analyze the architecture of the [MODULE NAME] module.

Steps:
1. Propose 3 architectural variants.
2. Compare them by clarity, composability, performance, and integration.
3. Explain trade-offs.
4. Give a recommendation.

Output format:
- Variants
- Comparison table
- Trade-offs
- Recommendation
```

---

# 7.2. Workflow: Проектирование API

Используй, когда нужно создать или уточнить API модуля.

```
You are designing the API for the [MODULE NAME] module.

Requirements:
- minimal and explicit API
- pure functions only
- no classes
- no new abstractions
- stable naming conventions
- deterministic behavior

Steps:
1. Propose 2–3 API variants.
2. Explain pros/cons.
3. Recommend the minimal variant.

Output:
- API signatures
- Explanation
- Recommendation
```

---

# 7.3. Workflow: Реализация модуля

Используй, когда нужно написать модуль с нуля.

```
You are implementing the [MODULE NAME] module for telnik-flight-engine.

Constraints:
- TS-only
- pure functions
- deterministic
- no classes
- no hidden state
- no new abstractions

Steps:
1. Propose a minimal implementation plan.
2. Wait for confirmation.
3. Implement the module.
4. Provide usage example.
5. Add integration notes.

Output:
- Plan
- TS implementation
- Usage example
- Integration notes
```

---

# 7.4. Workflow: Multi-file refactor

Используй, когда нужно изменить API, переименовать функцию, перенести модуль.

```
You are performing a multi-file refactor in telnik-flight-engine.

Task:
[Describe the change]

Constraints:
- do not change logic
- do not modify unrelated files
- do not introduce new abstractions
- keep API stable unless explicitly stated

Steps:
1. Show the list of files you plan to modify.
2. Show the planned changes.
3. Wait for confirmation.
4. Apply changes.

Output:
- File list
- Change plan
```

---

# 7.5. Workflow: Генерация тестов

Используй, когда нужно покрыть модуль тестами.

```
Write unit tests for the [MODULE NAME] module.

Requirements:
- pure function tests
- deterministic inputs
- no mocks
- test edge cases
- follow existing test style

Output:
- Test file
- Explanation of edge cases
```

---

# 7.6. Workflow: Документация (TS-only)

Используй, когда нужно создать документацию для модуля.

```
Write TS-only documentation for the [MODULE NAME] module.

Include:
- purpose
- formula (if applicable)
- parameters
- return value
- usage example
- no narrative text
- no external dependencies
```

---

# 7.7. Workflow: Debug / поиск ошибок

Используй, когда что-то ведёт себя странно.

```
Analyze this module for potential issues.

Focus on:
- edge cases
- floating point stability
- hidden state
- non-deterministic behavior
- naming inconsistencies
- incorrect formulas

Output:
- Issues found
- Explanation
- Suggested fixes
```

---

# 7.8. Workflow: Быстрое прототипирование

Используй, когда хочешь быстро проверить идею.

```
Create a simplified prototype of the [MODULE NAME] module.

Requirements:
- pure function
- minimal inputs
- deterministic
- stable API
- suitable for experimentation

Output:
- Prototype implementation
- Usage example
- Notes on limitations
```

