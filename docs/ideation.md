# Развитие идеи с Cursor

## Генерация концептов

Cursor может генерировать:
- варианты моделей
- подходы к симуляции
- способы упрощения физики
- архитектурные схемы
- идеи для API
- способы оптимизации

Пример:

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
- realism
- performance
- implementation complexity
- suitability for arcade physics
```

Cursor выдаст варианты → ты выбираешь → уточняешь.

## Проверка физических моделей

Cursor умеет:
- объяснять формулы
- находить ошибки
- сравнивать модели
- предлагать упрощения
- проверять корректность

Пример:

```
Check this lift formula for correctness and potential issues:

L = 0.5 * rho * v^2 * S * Cl

Focus on:
- edge cases
- numerical stability
- typical ranges
- potential simplifications for arcade physics
```

Cursor найдёт:
- проблемы с нулевой скоростью
- проблемы с отрицательными значениями
- проблемы с масштабированием
- возможные оптимизации

## Проектирование структур данных

```
Design a minimal state structure for a flight simulation step.

Constraints:
- explicit fields
- no hidden state
- no classes
- deterministic
- minimal but extensible
```

Cursor предложит структуру. Можешь уточнить:
- убрать лишнее
- добавить параметры
- сделать структуру более декларативной

## Usage examples

```
Write a minimal usage example for the calculateDrag module.
Include:
- state setup
- function call
- logging result
```

Cursor создаст пример.

## Обсуждение компромиссов

```
Compare the trade-offs between:
1. simple linear drag model
2. quadratic drag model

Focus on:
- realism
- performance
- stability
- suitability for arcade physics
```

## Уточнение формул

Cursor может:
- выводить формулы
- объяснять коэффициенты
- проверять размерности
- находить ошибки в единицах

Пример:

```
Check dimensional consistency of this thrust formula:

T = k * rpm^2 * D^4

Explain:
- what each term represents
- whether the dimensions match
- potential issues
```

## Прототипирование

```
Create a simplified mock version of the lift module for prototyping.
Requirements:
- deterministic
- pure function
- minimal inputs
- stable API
```