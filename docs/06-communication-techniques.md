# 6. Техники общения с Cursor

## 6.1. Техника «Роль + Контекст + Ограничения»

Cursor начинает работать идеально, когда ты задаёшь:

- **роль** (кто он сейчас),
- **контекст** (что за проект),
- **ограничения** (что нельзя делать).

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

Это превращает Cursor в инженера, который пишет код в твоём стиле.

---

## 6.2. Техника «Сначала предложи варианты»

Cursor по умолчанию даёт один ответ.  
Чтобы он стал полезным архитектором, ты всегда добавляешь:

```
Propose 3 variants.
Compare them.
Explain trade-offs.
Give a recommendation.
```

Это:

- расширяет пространство решений,
- помогает увидеть альтернативы,
- предотвращает “единственно правильный” ответ.

---

## 6.3. Техника «Сначала спроси, если не уверен»

Cursor иногда делает предположения, которые ломают архитектуру.  
Чтобы этого избежать:

```
If anything is unclear, ask before proceeding.
```

Cursor начинает уточнять:

- структуру,
- API,
- ограничения,
- naming.

---

## 6.4. Техника «Не делай»

Cursor любит “улучшать” код, но иногда делает хуже.  
Поэтому ты задаёшь **запреты**:

```
Do not:
- introduce new abstractions
- change the public API
- add dependencies
- modify unrelated files
- rewrite the architecture
```

Это удерживает Cursor в рамках.

---

## 6.5. Техника «Сначала план → потом код»

Cursor лучше работает, когда сначала делает план, а потом реализацию.

Пример:

```
First, create a step-by-step plan.
Wait for my confirmation.
Then implement.
```

Это:

- предотвращает ошибки,
- даёт тебе контроль,
- делает результат предсказуемым.

---

## 6.6. Техника «Формат ответа»

Cursor любит структурированные ответы.  
Ты задаёшь формат:

```
Output format:
1. Proposed API
2. Final TS implementation
3. Usage example
4. Integration notes
```

Cursor начинает выдавать:

- чистые,
- структурированные,
- предсказуемые ответы.

---

## 6.7. Техника «Ограничение области изменений»

Чтобы Cursor не трогал лишнее:

```
Only modify the code inside this module.
Do not touch other files.
Do not change imports unless necessary.
```

Это особенно важно для multi-file edits.

---

## 6.8. Техника «Проверка результата»

После выполнения задачи:

```
Check if the result:
- follows the architecture
- respects constraints
- keeps the API stable
- avoids unnecessary abstractions
```

Cursor сам проверяет свою работу.

---

## 6.9. Техника «Пошаговое улучшение»

Cursor лучше всего работает итеративно:

1. архитектура
2. API
3. реализация
4. тесты
5. документация
6. интеграция

Ты можешь прямо сказать:

```
We will work iteratively.
Step 1: propose architecture.
```

---

## 6.10. Техника «Минимальный контекст»

Cursor не любит перегрузку контекстом.  
Лучше давать:

- короткие описания,
- чёткие ограничения,
- конкретные задачи.

Пример:

```
Minimal context:
- TS-only
- pure functions
- deterministic
- modular
```

Этого достаточно.

---

Навигация: [← Предыдущий](05-ideation.md) | [Оглавление](index.md) | [Следующий →](07-workflows.md)