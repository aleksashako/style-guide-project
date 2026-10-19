# Руководство по стилю контента сайта «Победа»

Учебный проект по методологии **Docs as Code**. В репозитории разрабатывается стайлгайд для авторов пользовательской и справочной документации сайта авиакомпании «Победа».

Руководство помогает писать понятные инструкции, единообразно использовать авиационные термины и точно описывать услуги, ограничения и действия на сайте.

**Открыть руководство:** [GitHub Pages](https://aleksashako.github.io/style-guide-project/)

## Разделы руководства

- [Тон коммуникации](docs/tone-of-voice.md)
- [Терминология и форматы](docs/glossary-and-formats.md)
- [Веб-интерфейс](docs/web-interface.md)
- [Инструкции](docs/instructions.md)
- [Системные сообщения](docs/system-messages.md)
- [Предупреждения](docs/warnings.md)
- [Доступность текста](docs/accessibility.md)

Полная навигация по руководству находится на [главной странице](docs/index.md).

## Локальный просмотр

Нужны Python и Node.js. Установите зависимости и запустите MkDocs:

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
npm ci
mkdocs serve
```

Для Windows PowerShell активация окружения выглядит так:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
npm ci
mkdocs serve
```

Откройте адрес, который покажет MkDocs, обычно `http://127.0.0.1:8000/`.

## Проверки

Проверить формат Markdown и сборку сайта:

```bash
npm run lint:md
mkdocs build --strict
```

## Публикация

При изменениях в `main` GitHub Actions запускает проверки Markdown, а затем публикует сайт командой `mkdocs gh-deploy --force`. MkDocs собирает HTML-файлы и отправляет их в ветку `gh-pages`.


## Структура репозитория

- `docs/` — исходные страницы стайлгайда;
- `mkdocs.yml` — настройки MkDocs и навигация сайта;
- `.github/workflows/` — проверки и публикация через GitHub Actions;
- `.markdownlint-cli2.jsonc` — настройки Markdown-lint;
- `requirements.txt` — зависимости Python;
- `package.json` — команда линтинга Markdown;
- `CONTRIBUTING.md` — порядок внесения изменений и требования к коммитам.

## Внесение изменений

Создавайте отдельную ветку, вносите правки и открывайте Pull Request в `main`. Для новой страницы добавьте Markdown-файл в `docs/` и включите его в навигацию в `mkdocs.yml`.

Подробнее — в [руководстве для участников](CONTRIBUTING.md).
