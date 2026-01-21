# Реализация с Cursor

## Multi-file edits

Cursor умеет редактировать несколько файлов одновременно. Задавай жёсткие рамки.

Пример:

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
- Cursor сначала покажет список файлов → ты проверяешь → он вносит изменения
- Это предотвращает случайные изменения в чужих модулях

## Рефакторинг

Задавай рамки рефакторинга.

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

Cursor сделает:
- упрощение логики
- удаление дублирования
- улучшение читаемости

Но не сломает API.

## Миграции

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
- строит план
- показывает список файлов
- делает миграцию

## Тестирование

```
Write unit tests for the `calculateDrag` function.

Requirements:
- pure function tests
- no mocks
- test edge cases (zero velocity, negative values, extremely high values)
- follow existing test style
- use deterministic inputs
```

Cursor создаст:
- тесты на корректность
- тесты на крайние случаи
- тесты на стабильность

## Документация

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

Cursor выдаст JSDoc.

## Генерация boilerplate

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

Cursor создаст:
- файл модуля
- тесты
- документацию
- usage example

## Debug

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
- ошибки округления
- неправильные формулы
- потенциальные nondeterministic patterns