---
title: Публикация и локальный запуск
description: Как собирать и публиковать Cursor AI Guide локально и на GitHub Pages.
---

# Публикация и локальный запуск

Документация публикуется на GitHub Pages при каждом push в `main` через GitHub Actions.

## GitHub Pages
1. Откройте Settings → Pages в репозитории.
2. Выберите источник:
   - Source: Deploy from branch → `gh-pages`, или
   - Source: GitHub Actions.
3. Сайт будет доступен по адресу `https://it1ro.github.io/cursor-guide`.

## Локальная разработка
```bash
pip install -r requirements.txt
mkdocs serve
```
