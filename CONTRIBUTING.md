# Руководство по внесению изменений

## Как предложить изменение

1. Обновите ветку `main` и создайте отдельную ветку для своей задачи.
2. Измените или добавьте Markdown-файлы в `docs/`. Для новой страницы обновите навигацию в `mkdocs.yml`.
3. Проверьте Markdown и сборку документации.
4. Создайте Pull Request в `main`, опишите изменения и дождитесь ревью.
5. Исправьте замечания. Сливайте Pull Request после одобрения и успешных проверок CI.

Для лабораторной работы оставьте не менее трёх содержательных комментариев к Pull Request партнёра.

## Имена веток и коммиты

Выбирайте короткие имена веток по задаче, например `docs/accessibility` или `fix/navigation`.

Используйте формат Conventional Commits: `<type>: <краткое описание>`.

```text
docs: add accessibility guidelines
fix: correct navigation links
ci: update documentation workflow
```

## Локальная проверка

```bash
npm ci
npm run lint:md
python -m pip install -r requirements.txt
mkdocs build --strict
mkdocs serve
```

## Как добавить раздел

1. Создайте файл `docs/<название-раздела>.md` с заголовком первого уровня.
2. Добавьте файл в навигацию `mkdocs.yml`.
3. Запустите проверки из раздела «Локальная проверка» и откройте Pull Request.
