<div align="center">

# AniMori — Toolkit for AniList

**Перевод интерфейса, русские названия, плеер, рейтинги, дерево франшиз, экспорт и сравнение списков с Shikimori.**

[![Greasy Fork](https://img.shields.io/badge/Greasy%20Fork-%D1%83%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%B8%D1%82%D1%8C-02A9FF?style=flat-square&logo=javascript&logoColor=white&labelColor=0B1622)](https://greasyfork.org/ru/scripts/572948-animori-anilist-toolkit)
[![Релиз](https://img.shields.io/github/v/release/foulnike/Animori-Script?style=flat-square&logo=github&logoColor=white&label=%D1%80%D0%B5%D0%BB%D0%B8%D0%B7&labelColor=0B1622&color=02A9FF)](https://github.com/foulnike/Animori-Script/releases/latest)
[![Лицензия](https://img.shields.io/badge/%D0%BB%D0%B8%D1%86%D0%B5%D0%BD%D0%B7%D0%B8%D1%8F-MIT-02A9FF?style=flat-square&labelColor=0B1622)](LICENSE)

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Vue 3](https://img.shields.io/badge/Vue%203-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Sass](https://img.shields.io/badge/Sass-CC6699?style=flat-square&logo=sass&logoColor=white)
![Tampermonkey](https://img.shields.io/badge/Tampermonkey-00485B?style=flat-square&logo=tampermonkey&logoColor=white)

[Возможности](#возможности) · [Установка](#установка) · [Авторизация](#авторизация) · [Сборка](#сборка)

</div>

---

Пользовательский скрипт для [anilist.co](https://anilist.co). Работает в браузере поверх сайта, ничего кроме менеджера скриптов не требует.

Проект неофициальный и с командой AniList не связан.

> [!NOTE]
> У проекта три продукта, у каждого свой репозиторий: юзерскрипт — здесь,
> приложение для Windows — `foulnike/AniMori-AniList-Toolkit`, версия для
> приставки — `foulnike/Animori-TV`.

## Как выглядит

<div align="center">

<img src="https://raw.githubusercontent.com/foulnike/Animori-Script/main/assets/screenshots/home.webp" width="900" alt="Каталог AniList с переведённым интерфейсом и русскими названиями">

</div>

<details>
<summary><b>Страница аниме</b> — русское описание с указанием источника, рейтинги, музыкальные темы, дерево франшизы, внешние ссылки</summary>
<br>
<div align="center">
<img src="https://raw.githubusercontent.com/foulnike/Animori-Script/main/assets/screenshots/media.webp" width="900" alt="Страница аниме с блоками AniMori">
</div>
</details>

<details>
<summary><b>Плеер</b> — выбор озвучки с избранным и переключение серий без перезагрузки страницы</summary>
<br>
<div align="center">
<img src="https://raw.githubusercontent.com/foulnike/Animori-Script/main/assets/screenshots/player.webp" width="900" alt="Встроенный плеер с панелями озвучек и эпизодов">
</div>
</details>

## Возможности

- **Перевод интерфейса** — строки сайта по словарю `dictionary.json`.
- **Русские тайтлы и описания** — с Shikimori или anime365, с указанием источника. Основной источник и запасной выбираются в настройках.
- **Перевод персонажей и персонала** — имена с Shikimori.
- **Плеер** — выбор озвучки и серий (Kodik).
- **Рейтинги MAL и Shikimori** — рядом с оценкой AniList.
- **Дерево франшизы** — хронология связанных тайтлов, включая записи, которых нет на AniList.
- **Музыкальные темы** — опенинги и эндинги, поиск в VK Музыке, YouTube Music, Spotify и SoundCloud.
- **Русский поиск** — аниме, манга, персонажи, персонал.
- **Внешние ссылки** — RuTracker, YummyAnime, AnimeGO, MangaLib, домены настраиваются. Свои ссылки задаются шаблонами с `{ru}`, `{romaji}`, `{query}`.
- **Сравнение списков Shikimori ⇄ AniList** — расхождения по статусу, оценке, прогрессу, пересмотрам и заметкам, сравнение избранного, связанные сезоны, игнор-лист.
- **Импорт Shikimori → AniList** — аниме, манга, избранное, даты просмотров. Нужен токен AniList.
- **Локальный словарь** — свои переводы поверх общей базы: вручную или выделением текста на странице. Редактор с поиском, импортом, экспортом и отправкой в общую базу.
- **Цветовые темы** — акцентный цвет AniMori.
- **Кэш** — данные Shikimori и MAL в IndexedDB на 90 дней.
- **Настройки** — модули включаются в панели «⚙» в левом нижнем углу.
- **Логгер** — по желанию.

Блокировщика рекламы нет: в браузере с этим справится профильное расширение.

## Установка

1. Установите менеджер пользовательских скриптов — [Tampermonkey](https://www.tampermonkey.net/).
2. Установите скрипт со страницы **[Greasy Fork](https://greasyfork.org/ru/scripts/572948-animori-anilist-toolkit)** — оттуда же приходят обновления.
3. Откройте [anilist.co](https://anilist.co) — внизу слева появится кнопка **⚙**.

Файл `animori.user.js` из [релизов](https://github.com/foulnike/Animori-Script/releases) — для ручной установки.

## Авторизация

Перевод, плеер и рейтинги работают без входа. Импорт списка из Shikimori и изменение списка на AniList требуют токен:

1. Панель **⚙** → «Авторизация AniList».
2. Создайте API-клиент на [anilist.co/settings/developer](https://anilist.co/settings/developer), в поле redirect укажите `https://anilist.co/api/v2/oauth/pin`.
3. Вставьте Client ID, сгенерируйте ссылку, получите токен и вставьте его в поле.

Токен хранится в хранилище менеджера скриптов.

## Источники данных

| Источник                              | Назначение                                                                  |
| :------------------------------------ | :-------------------------------------------------------------------------- |
| `raw.githubusercontent.com`           | словарь перевода интерфейса (этот репозиторий)                              |
| `graphql.anilist.co`                  | данные и списки AniList                                                     |
| `shikimori.io`, `shikimori.rip`       | русские названия, описания, персонажи, франшизы (`.rip` — запасное зеркало) |
| `smotret-anime.online`, `anime365.ru` | тайтлы и описания                                                           |
| `api.animethemes.moe`                 | музыка                                                                      |
| `kodik-api.com`                       | видеоплеер                                                                  |

Запросы идут из браузера через `GM_xmlhttpRequest`. Токен и настройки остаются на вашей машине, кэш — в локальной IndexedDB.

## Словарь перевода

`dictionary.json` — пары `оригинал → перевод` для строк интерфейса AniList:

```json
{
  "Home": "Главная",
  "Browse": "Просмотр",
  "Settings": "Настройки"
}
```

Словарь подгружается из репозитория, поэтому правки применяются у всех без обновления скрипта. Непереведённую или неточную строку присылайте формой «Ошибка перевода».

## Сборка

Нужен Node.js.

```bash
npm install
npm run build       # → dist/animori.user.js и dist/animori.meta.js
npm run typecheck
npm run format
```

Выпуск делает тег вида `script-2.2.0`: прогон сверяет номер в теге с `package.json`, собирает скрипт и создаёт релиз с описанием из верхнего раздела `CHANGELOG.md`. На Greasy Fork версия выкладывается отдельно — оттуда людям приходят обновления.

Исходный код: `src/`, входная точка — `src/main.ts`.

## Лицензия

[MIT](LICENSE) © foulnike

Лицензия покрывает код проекта и переводы участников. Данные сторонних сервисов ею не покрываются: оригинальные строки интерфейса в ключах `dictionary.json` принадлежат AniList, русские названия, описания и имена — Shikimori и anime365, музыкальные метаданные — AnimeThemes. Всё это показывается со ссылкой на источник и не хранится в репозитории.

Сторонние сервисы принадлежат их владельцам и используются через их публичные API. Видео отдаёт сторонний плеер: проект не хранит и не раздаёт видео.
