# Техники общения с Cursor

## Роль + Контекст + Ограничения

Cursor начинает работать идеально, когда задаёшь:
- роль (кто он сейчас)
- контекст (что за проект)
- ограничения (что нельзя делать)

Пример:

```
You are a senior TypeScript engineer working on telnik-flight-engine.

Context:
- TS-only
- pure functions
- deterministic
- modular and composable
- no classes
- no hidden state

Constraints:
- do not introduce new abstractions
- do not change naming conventions
- do not modify unrelated code
```

Cursor начнёт писать код в твоём стиле.

## Сначала предложи варианты

Cursor по умолчанию даёт один ответ. Добавляй:

```
Propose 3 variants.
Compare them.
Explain trade-offs.
Give a recommendation.
```

Это:
- расширяет пространство решений
- помогает увидеть альтернативы
- предотвращает "единственно правильный" ответ

## Сначала спроси, если не уверен

```
If anything is unclear, ask before proceeding.
```

Cursor начнёт уточнять:
- структуру
- API
- ограничения
- naming

## Не делай

Задавай запреты:

```
Do not:
- introduce new abstractions
- change the public API
- add dependencies
- modify unrelated files
- rewrite the architecture
```

Это удерживает Cursor в рамках.

## Сначала план → потом код

```
First, create a step-by-step plan.
Wait for my confirmation.
Then implement.
```

Это:
- предотвращает ошибки
- даёт тебе контроль
- делает результат предсказуемым

## Формат ответа

```
Output format:
1. Proposed API
2. Final TS implementation
3. Usage example
4. Integration notes
```

Cursor выдаст структурированный ответ.

## Ограничение области изменений

```
Only modify the code inside this module.
Do not touch other files.
Do not change imports unless necessary.
```

Важно для multi-file edits.

## Проверка результата

После выполнения:

```
Check if the result:
- follows the architecture
- respects constraints
- keeps the API stable
- avoids unnecessary abstractions
```

Cursor сам проверит свою работу.

## Пошаговое улучшение

Работай итеративно:
1. архитектура
2. API
3. реализация
4. тесты
5. документация
6. интеграция

```
We will work iteratively.
Step 1: propose architecture.
```

## Минимальный контекст

Cursor не любит перегрузку контекстом. Давай:
- короткие описания
- чёткие ограничения
- конкретные задачи

Пример:

```
Minimal context:
- TS-only
- pure functions
- deterministic
- modular
```

Этого достаточно.