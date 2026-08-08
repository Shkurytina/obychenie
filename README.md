# RESCUE OPS — обучающие игры о спасателях

Сборник из трёх мини-игр на тему спасательных служб:

- **`games/quiz.html`** — экзамен по первой помощи (10 вопросов, таймер обратной связи)
- **`games/memory.html`** — игра на память со спасательным снаряжением
- **`games/backpack.html`** — сборы тревожного рюкзака за 30 секунд с лимитом по весу

Чистый HTML/CSS/JS, без сборки и зависимостей — работает как статический сайт.

## Структура

```
rescue-games/
├── index.html          # главная страница ("доска нарядов")
├── assets/
│   └── style.css        # общая тема оформления
└── games/
    ├── quiz.html
    ├── memory.html
    └── backpack.html
```

## Как запустить локально

Просто открой `index.html` в браузере — никаких серверов и установок не требуется.

Либо запусти локальный сервер (удобнее для проверки ссылок):

```bash
python3 -m http.server 8000
```

и открой `http://localhost:8000`.

## Как выложить на GitHub Pages

1. Создай новый репозиторий на GitHub (например, `rescue-games`).
2. Залей туда содержимое этой папки:

   ```bash
   git init
   git add .
   git commit -m "Initial commit: rescue ops educational games"
   git branch -M main
   git remote add origin https://github.com/<твой-логин>/rescue-games.git
   git push -u origin main
   ```

3. В репозитории зайди в **Settings → Pages**.
4. В разделе **Build and deployment** выбери:
   - Source: `Deploy from a branch`
   - Branch: `main`, папка `/ (root)`
5. Сохрани — через 1-2 минуты сайт будет доступен по адресу:

   ```
   https://<твой-логин>.github.io/rescue-games/
   ```

Никаких дополнительных настроек (Jekyll, workflow-файлов) не требуется — GitHub Pages отдаёт статические файлы как есть.

## Возможные доработки

- Добавить сохранение рекордов через `localStorage`
- Добавить новые вопросы в квиз или новые предметы в игру на память
- Сделать общий экран статистики по всем трём играм
