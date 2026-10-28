# Когнитивные искажения

[![hexlet-check](https://github.com/kicha3007-boop/layout-designer-project-58/actions/workflows/hexlet-check.yml/badge.svg)](https://github.com/kicha3007-boop/layout-designer-project-58/actions)
[![ci](https://github.com/kicha3007-boop/layout-designer-project-58/actions/workflows/ci.yml/badge.svg)](https://github.com/kicha3007-boop/layout-designer-project-58/actions/workflows/ci.yml)

Лендинг о пяти распространённых когнитивных искажениях в программировании: эффект ИКЕА,
преждевременная оптимизация, искажение новизны, гиперболическое обесценивание и ошибка планирования.
Первый проект профессии «Верстальщик» на Хекслете: семантическая разметка, Flexbox, позиционирование,
переиспользуемые классы в духе OOCSS и Atomic CSS.

- Учебный проект Хекслета: https://ru.hexlet.io/programs/layout-designer
- Как это должно выглядеть: https://files.hexlet.app/a/t4iwus
- Опубликованная версия (Surge): _ссылка появится после `make deploy`_

## Стек

- HTML5 и CSS3 (Flexbox), без сборки и фреймворков
- Шрифты Neucha и Open Sans лежат локально в `src/fonts` (копии из Google Fonts)
- Линтеры: [HTMLHint](https://htmlhint.com/) и [Stylelint](https://stylelint.io/) с `stylelint-config-standard`

## Структура

```
src/
  index.html   — вся вёрстка
  style.css    — все стили
  images/      — иллюстрации, фон и иконка отправки
  fonts/       — шрифты woff2
```

## Как открыть локально

Нужен Node.js 18+.

```bash
git clone https://github.com/kicha3007-boop/layout-designer-project-58.git
cd layout-designer-project-58
make install   # npm ci
make start     # локальный сервер vite: http://localhost:3000
```

Страницу лучше смотреть через сервер: при открытии `src/index.html` как файла Chrome может не подгрузить локальные шрифты.

## Линтеры

```bash
make lint      # htmlhint + stylelint
```

Те же проверки запускаются в GitHub Actions (`.github/workflows/ci.yml`) на каждый push.

## Публикация на Surge

```bash
make deploy    # npx surge ./src — при первом запуске попросит войти или зарегистрироваться
```

После публикации впишите полученный адрес в раздел выше.

---

<details>
<summary>Автоматические тесты Хекслета</summary>

Тесты запускаются на каждый коммит. За запуск отвечает файл `.github/workflows/hexlet-check.yml` — не удаляйте и не переименовывайте ни его, ни репозиторий.

Проверка сравнивает скриншоты секций при ширине окна 1440px с эталонными: `header`, `#preview-image`,
`#navigation`, `#ikea-effect`, `#premature-optimization`, `#distortion-of-novelty`,
`#hyperbolic-depreciation`, `#errors-in-planning`, `footer` и всю страницу целиком.

</details>

## О Хекслете

[Хекслет](https://ru.hexlet.io/) — школа программирования: авторские программы обучения с практикой, поддержкой наставников и реальными проектами, которые остаются в резюме. Этот репозиторий — один из таких проектов.
