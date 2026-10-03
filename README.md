# Journal Trace — сайт на GitHub Pages

Готовый статический сайт. Сборка, Node.js и серверная часть для публикации не нужны.

## Публикация

1. Загрузите содержимое этой папки в корень репозитория `JournalTrace-Analyzer/JournalTrace-Analyzer.github.io`, в ветку `main`. Загружайте файлы, а не папку целиком. Не забудьте скрытый файл `.nojekyll`.
2. Откройте **Settings → Pages → Build and deployment**.
3. В **Source** выберите **Deploy from a branch**, затем **main** и **/(root)**, нажмите **Save**.
4. Дождитесь успешного задания Pages в **Actions**. Адрес сайта: https://journaltrace-analyzer.github.io/ . Настройки HTTPS доступны в Settings → Pages.
5. Откройте сайт и проверьте скачивание EXE, меню, фильтры, экспорт CSV и мобильную версию.

Инструкция GitHub: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Ссылки

- Все кнопки скачивания: https://github.com/JournalTrace-Analyzer/JournalTrace-Analyzer.github.io/releases/download/JournalTrace/JournalTrace.exe
- Кнопка GitHub: https://github.com/JournalTrace-Analyzer/JournalTrace-Analyzer.github.io/releases/tag/JournalTrace
- В конце имени EXE нет дополнительной точки. Файл подтверждён через GitHub API 4 октября 2026 года. При переименовании или удалении ресурса релиза ссылка перестанет работать.

## Файлы

`index.html`, `style.css`, `script.js` — страница, стили и интерактивный пример.
`scene.js` и `drive.glb` — 3D-модель, загружаемая отдельно после готовности элементов страницы.
`manrope-*.woff2` — локальные шрифты.
`favicon.svg`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png`, `manifest.webmanifest` — иконки и манифест.
`og.png` — превью для соцсетей. `robots.txt`, `sitemap.xml` — индексация.
`404.html` — страница ошибки. `.nojekyll` — отключение Jekyll.

Все эти файлы нужно загрузить вместе. README не требуется браузеру, его можно оставить в репозитории как инструкцию.
Локальный просмотр: запустите обычный HTTP-сервер в папке сайта, например `python -m http.server 8000`, и откройте http://localhost:8000/ . Для модулей и загрузки модели двойной щелчок по HTML не подходит.

## Индексация и продвижение после публикации

- Подтвердите владение сайтом в [Google Search Console](https://search.google.com/search-console) и [Яндекс Вебмастере](https://webmaster.yandex.ru/). Коды подтверждения можно добавить только после получения их в ваших аккаунтах.
- Передайте `https://journaltrace-analyzer.github.io/sitemap.xml`, проверьте URL главной страницы и запросите индексацию.
- Проверьте PageSpeed Insights и реальные показатели загрузки после публикации.
- Дополняйте сайт полезными материалами: примерами работы с USN Journal, реальными снимками приложения, инструкциями и описаниями новых версий. Получайте релевантные ссылки на сайт.
- При смене домена обновите canonical, Open Graph и JSON-LD в `index.html`, а также `robots.txt` и `sitemap.xml`.

Title, description, canonical, социальные метаданные и SoftwareApplication настроены. Страница доступна для индексации без JavaScript. Микроразметка не гарантирует расширенный сниппет; фиктивные отзывы и рейтинги не добавлены.
SEO не гарантирует первое место или включение в индекс: https://developers.google.com/search/docs/fundamentals/seo-starter-guide

Встроенный журнал использует демонстрационные данные. Сайт не читает файлы компьютера. Приложение Windows распространяется отдельным ресурсом релиза; лицензия приложения должна быть подтверждена его владельцем. Уведомления о лицензии Three.js сохранены в `scene.js`.
