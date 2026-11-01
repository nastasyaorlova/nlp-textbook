# NLP в рекламе и PR — учебник курса

Онлайн-учебник на [Jupyter Book](https://jupyterbook.org). Каждая глава — тетрадка Jupyter (`.ipynb`) из папки `lectures/`. Сайт собирается автоматически и публикуется на GitHub Pages при каждом изменении в ветке `main`.

## Первая публикация

1. Создайте на GitHub новый **публичный** репозиторий `nlp-textbook` (без README).
2. Загрузите в него все файлы из этой папки, включая скрытую папку `.github`.
3. В файле `_config.yml` замените `GITHUB_USERNAME` на ваш логин GitHub.
4. В репозитории откройте **Settings → Pages** и в поле **Source** выберите **GitHub Actions**.
5. Через 2–3 минуты учебник будет доступен по адресу `https://<логин>.github.io/nlp-textbook/`. Ход сборки виден во вкладке **Actions**.

## Как добавить новую лекцию

1. Положите тетрадку в папку `lectures/`, например `lectures/lecture02.ipynb`. Сохраняйте её **с выполненными ячейками**: при сборке код не запускается, на сайте показываются сохранённые результаты.
2. Добавьте строку в `_toc.yml` в нужный раздел:

   ```yaml
   parts:
     - caption: Основы
       chapters:
         - file: lectures/lecture01
         - file: lectures/lecture02
     - caption: Сбор данных
       chapters:
         - file: lectures/lecture03
   ```

3. Сохраните изменения (commit) в ветку `main` — сайт обновится сам.

## Сборка на своём компьютере (по желанию)

```bash
pip install -r requirements.txt
jupyter-book build .
```

Готовый сайт появится в `_build/html/index.html`.
