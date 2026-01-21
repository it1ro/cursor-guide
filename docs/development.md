# Разработка

Документация публикуется на GitHub Pages при каждом push в `main` через GitHub Actions.

## GitHub Pages

1. Открой Settings → Pages в репозитории
2. Выбери источник:
   - Source: Deploy from branch → `gh-pages`, или
   - Source: GitHub Actions
3. Сайт будет доступен по адресу `https://it1ro.github.io/cursor-guide`

## Локальная разработка

```bash
pip install -r requirements.txt
mkdocs serve
```