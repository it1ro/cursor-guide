# 5. Cursor в развитии идеи

## 5.1. Генерация концептов: как заставить Cursor думать вместе с тобой

Cursor может генерировать:

- варианты моделей,
- подходы к симуляции,
- способы упрощения физики,
- архитектурные схемы,
- идеи для API,
- способы оптимизации.

Пример промпта:

```
We are exploring aerodynamic modeling for telnik-flight-engine.

Task:
Propose 3 conceptual approaches to modeling lift and drag for low-speed arcade-style flight.

Constraints:
- must be simple enough for real-time browser simulation
- must be deterministic
- must be modular and composable
- must avoid complex CFD

Compare approaches by:
- realism,
- performance,
- implementation complexity,
- suitability for arcade physics.
```

Cursor выдаёт варианты → ты выбираешь → уточняешь.

---

## 5.2. Проверка физических моделей

Cursor отлично умеет:

- объяснять формулы,
- находить ошибки,
- сравнивать модели,
- предлагать упрощения,
- проверять корректность.

Пример:

```
Check this lift formula for correctness and potential issues:

L = 0.5 * rho * v^2 * S * Cl

Focus on:
- edge cases,
- numerical stability,
- typical ranges,
- potential simplifications for arcade physics.
```

Cursor найдёт:

- проблемы с нулевой скоростью,
- проблемы с отрицательными значениями,
- проблемы с масштабированием,
- возможные оптимизации.

---

## 5.3. Проектирование структур данных

flight-engine — модульный, декларативный проект.  
Cursor может помочь проектировать структуры:

- состояния,
- параметров,
- конфигураций,
- результатов симуляции.

Пример:

```
Design a minimal state structure for a flight simulation step.

Constraints:
- explicit fields
- no hidden state
- no classes
- deterministic
- minimal but extensible
```

Cursor предложит:

```ts
interface FlightState {
  position: Vector3;
  velocity: Vector3;
  orientation: Quaternion;
  angularVelocity: Vector3;
}
```

Ты можешь уточнить:

- убрать лишнее,
- добавить параметры,
- сделать структуру более декларативной.

---

## 5.4. Создание usage examples

Cursor может генерировать usage examples, которые:

- понятны,
- минималистичны,
- демонстрируют API,
- помогают пользователям.

Пример:

```
Write a minimal usage example for the calculateDrag module.
Include:
- state setup
- function call
- logging result
```

Cursor создаёт идеальный пример.

---

## 5.5. Обсуждение компромиссов

Cursor может объяснить:

- почему модель A проще,
- почему модель B реалистичнее,
- что стоит производительности,
- что стоит ясности.

Пример:

```
Compare the trade-offs between:
1. simple linear drag model
2. quadratic drag model

Focus on:
- realism,
- performance,
- stability,
- suitability for arcade physics.
```

---

## 5.6. Уточнение формул и моделей

Cursor может:

- выводить формулы,
- объяснять коэффициенты,
- проверять размерности,
- находить ошибки в единицах.

---

Навигация: [← Предыдущий](04-implementation.md) | [Оглавление](index.md) | [Следующий →](06-communication-techniques.md)

Пример:

```
Check dimensional consistency of this thrust formula:

T = k * rpm^2 * D^4

Explain:
- what each term represents
- whether the dimensions match
- potential issues
```

---

## 5.7. Быстрое прототипирование идей

Ты можешь использовать Cursor для:

- создания черновых модулей,
- проверки гипотез,
- генерации альтернативных API,
- создания mock-версий модулей.

Пример:

```
Create a simplified mock version of the lift module for prototyping.
Requirements:
- deterministic
- pure function
- minimal inputs
- stable API
```

