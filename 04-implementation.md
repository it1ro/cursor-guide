# 4. Cursor в реализации

## 4.1. Multi-file edits: как заставить Cursor менять код безопасно

Cursor умеет редактировать несколько файлов одновременно — это его суперсила.  
Но чтобы он не сломал архитектуру, ты задаёшь **жёсткие рамки**.

Пример промпта:

```
You are modifying telnik-flight-engine.

Task:
Apply the following change across the project:
- rename `computeDrag` to `calculateDrag`
- update all imports and usage
- do not change logic
- do not introduce new abstractions
- do not modify unrelated code

Constraints:
- TS-only
- pure functions
- deterministic
- stable API

Before applying changes:
- show the list of files you plan to modify
```

Почему это важно:

- Cursor сначала покажет список файлов → ты проверяешь → он вносит изменения.
- Это предотвращает случайные изменения в чужих модулях.

---

## 4.2. Рефакторинг: как заставить Cursor улучшать код, не ломая архитектуру

Cursor любит “улучшать” код, но иногда делает хуже.  
Чтобы этого избежать, ты задаёшь **рамки рефакторинга**.

Пример:

```
Refactor this module to improve clarity and remove duplication.

Constraints:
- do not change the public API
- do not introduce new abstractions
- do not change naming conventions
- keep all functions pure
- keep the module deterministic
- do not add dependencies
```

Cursor делает:

- упрощение логики,
- удаление дублирования,
- улучшение читаемости,
- но **не ломает API**.

---

## 4.3. Миграции: как безопасно менять архитектуру

Когда flight-engine растёт, тебе нужно:

- менять API,
- переносить функции,
- объединять модули,
- менять структуру директорий.

Cursor может сделать это идеально, если задать правильный промпт:

```
We are migrating the aerodynamic modules into a new structure.

Task:
Move all aerodynamic force modules into `/modules/aero/`.
Update imports across the project.
Do not change logic.
Do not rename anything.
Do not modify unrelated files.

Before applying changes:
- show the migration plan
- list affected files
```

Cursor:

- строит план,
- показывает список файлов,
- делает миграцию.

---

## 4.4. Тестирование: как заставить Cursor писать тесты в твоём стиле

Ты можешь заставить Cursor писать тесты, которые:

- минималистичны,
- проверяют edge cases,
- не зависят от внешнего состояния.

Пример:

```
Write unit tests for the `calculateDrag` function.

Requirements:
- pure function tests
- no mocks
- test edge cases (zero velocity, negative values, extremely high values)
- follow existing test style
- use deterministic inputs
```

Cursor создаёт:

- тесты на корректность,
- тесты на крайние случаи,
- тесты на стабильность.

---

## 4.5. Документация: TS-only, без лишних слов

Ты можешь заставить Cursor писать документацию, которая:

- минималистична,
- точна,
- не содержит воды,
- соответствует твоему стилю.

Пример:

```
Write TS-only documentation for this module.

Include:
- purpose
- formula
- parameters
- return value
- usage example
- no external dependencies
- no narrative text
```

Cursor выдаёт идеальный JSDoc.

---

## 4.6. Генерация boilerplate: как ускорить создание новых модулей

Ты можешь создать шаблон:

```
Generate a new module template for telnik-flight-engine.

Requirements:
- pure function
- deterministic
- minimal API
- TS-only
- include usage example
- include documentation block
```

Cursor создаёт:

- файл модуля,
- тесты,
- документацию,
- usage example.

---

## 4.7. Debug workflow: как использовать Cursor для поиска ошибок

Cursor отлично умеет:

- объяснять ошибки,
- находить несогласованности,
- анализировать edge cases.

Пример:

```
Analyze this module for potential bugs.

Focus on:
- edge cases
- floating point issues
- hidden state
- non-deterministic behavior
- naming inconsistencies
```

Cursor найдёт:

- ошибки округления,
- неправильные формулы,
- потенциальные nondeterministic patterns.