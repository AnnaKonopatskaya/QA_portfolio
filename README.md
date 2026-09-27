# Баг-репорт: тестирование stavkinasport.com

**Тип работы:** тестовое задание на позицию Manual QA Engineer
**Время выполнения:** 2 ч 49 мин
**Объект тестирования:** сайт [stavkinasport.com](https://stavkinasport.com/) — новостной/аналитический ресурс о ставках на спорт
**Окружения:** Desktop / Chrome, iPhone / iOS 26.3.1 / Safari

## Задача

Провести исследовательское тестирование сайта на desktop и мобильном устройстве, найти и оформить дефекты в формате баг-репорта: с шагами воспроизведения, ожидаемым/фактическим результатом, приоритетом и подтверждением в виде скриншотов/видео.

## Итоги

Найдено **26 дефектов**: 17 — на desktop, 16 — на мобильной версии (часть багов пересекается на обеих платформах).

Распределение по приоритету:

| Приоритет | Кол-во |
|---|---|
| Критический | 2 |
| Высокий | 9 |
| Средний | 19 |
| Низкий | 3 |

Основные категории найденных проблем:
- **Некликабельные/нерабочие элементы** — кнопка входа, поиск, фильтры и сортировка не реагируют на действия пользователя (в т.ч. критичные баги, блокирующие вход и поиск).
- **Необработанные шорткоды** — на множестве страниц вместо баннеров/виджетов отображается технический текст вида `[ap-quiz id="..."]`, `[wp_revive_banner zone_id="..."]`.
- **Битые изображения** — отсутствуют иллюстрации в нескольких разделах (битые ссылки).
- **Вёрстка** — смещение блоков, нарушенное выравнивание элементов.
- **Неполная функциональность соцсетей** — в футере и блоке соцсетей активна только одна из заявленных кнопок.
- **Нерабочая форма подписки** на странице бонусов.

## Полная таблица дефектов (desktop)

Полное описание, шаги воспроизведения и ссылки на скриншоты — в оригинальном файле [`bug-report-stavkinasport.xlsx`](./bug-report-stavkinasport.xlsx).

[dt]: ./desktop_table.md
<!-- таблица ниже сгенерирована из xlsx для удобного просмотра прямо в GitHub -->

| № | Дата | Устройство/браузер | Страница | Описание бага | Приоритет |
|---|------|---------------------|----------|----------------|-----------|
| 1 | 19.09.2026<br>18:22 | Desktop / Chrome | Главная / stavkinasport.com | Кнопка "Вход" <br>в хедере не <br>реагирует на клик | Критический |
| 2 | 19.09.2026<br>18:24 | Desktop / Chrome | Главная / stavkinasport.com | Поиск не выдаёт <br>результатов ни на <br>один запрос | Высокий |
| 3 | 19.09.2026<br>18:27 | Desktop / Chrome | https://stavkinasport.com/cybersport-prognozy/ | На странице https://stavkinasport.com/cybersport-prognozy/ отображается непереведённый шорткод [wp_revive_banner zone_id="predicts"] | Высокий |
| 4 | 19.09.2026<br>18:30 | Desktop / Chrome | https://stavkinasport.com/bk-pari/ | Непоследовательное поведение <br>иконок платёжных систем на <br>странице обзора БК Пари | Высокий |
| 5 | 19.09.2026<br>18:32 | Desktop / Chrome | https://stavkinasport.com/prognozy/ | Не работают фильтры и сортировка на странице прогнозов | Высокий |
| 6 | 19.09.2026<br>18:45 | Desktop / Chrome | https://stavkinasport.com/prognozy/ | На странице "Прогнозы" вместо изображения\блока отображается необработанный шорткод | Высокий |
| 7 | 19.09.2026<br>18:47 | Desktop / Chrome | https://stavkinasport.com/skaner-bukmekerskih-vilok/ | На странице сканера вилок отображается непереведённый шорткод [ap-quiz id="90412"] | Высокий |
| 8 | 19.09.2026<br>18:48 | Desktop / Chrome | https://stavkinasport.com/rating-bookmakers/ | На странице рейтинга букмекеров отображается непереведённый шорткод [ap-quiz id="82915"] | Высокий |
| 9 | 19.09.2026<br>18:50 | Desktop / Chrome | https://stavkinasport.com/novosti/ | На странице новостей отображается непереведённый шорткод [wp_revive_banner zone_id="news"] | Средний |
| 10 | 19.09.2026<br>18:53 | Desktop / Chrome | https://stavkinasport.com/video/ | На странице "Видео" вместо рекламного баннера отображается необработанный шорткод | Средний |
| 11 | 19.09.2026<br>18:55 | Desktop / Chrome | https://stavkinasport.com/vse-bonusy-bukmekerov/ | Съехавшая вёрстка блока "Материал подготовлен" на страницах раздела бонусов | Средний |
| 12 | 19.09.2026<br>18:58 | Desktop / Chrome | https://stavkinasport.com/vernyak/ | На странице "Верняк Дня" некорректно отображается изображение | Средний |
| 13 | 19.09.2026<br>19:01 | Desktop / Chrome | https://stavkinasport.com/ | В блоке "Наши соцсети" активна только кнопка Telegram | Средний |
| 14 | 19.09.2026<br>19:05 | Desktop / Chrome | https://stavkinasport.com/ | В футере в разделе "Соцсети" указан только Telegram | Средний |
| 15 | 16.09.2026<br>19:07 | Desktop / Chrome | https://stavkinasport.com/vse-bonusy-bukmekerov/ | Форма подписки на бонусы не работает | Средний |
| 16 | 19.09.2026<br>19:10 | Desktop / Chrome | https://stavkinasport.com/rating-bookmakers/<br>https://stavkinasport.com/prognozy/ | Кривое выравнивание элементов в блоке "Лучшие букмекеры для ставок" | Низкий |
| 17 | 19.09.2026<br>19:21 | Desktop / Chrome | https://stavkinasport.com/express/ | Множественные отсутствующие изображения на странице https://stavkinasport.com/express/ | Низкий |

## Полная таблица дефектов (мобильное тестирование, iOS/Safari)

| № | Дата | Устройство/браузер | Страница | Описание бага | Приоритет |
|---|------|---------------------|----------|----------------|-----------|
| 18 | 19.09.2026<br>19:32 | iPhone / iOS 26.3.1 / Safari | Главная / stavkinasport.com | Кнопка "Вход" <br>в хедере не <br>реагирует на клик | Критический |
| 19 | 19.09.2026<br>19:35 | iPhone / iOS 26.3.1 / Safari | Главная / stavkinasport.com | Поиск не выдаёт <br>результатов ни на <br>один запрос | Высокий |
| 20 | 19.09.2026<br>19:42 | iPhone / iOS 26.3.1 / Safari | https://stavkinasport.com/cybersport-prognozy/ | На странице https://stavkinasport.com/cybersport-prognozy/ отображается непереведённый шорткод [ap-quiz id = "90413"] | Средний |
| 21 | 19.09.2026<br>19:48 | iPhone / iOS 26.3.1 / Safari | https://stavkinasport.com/fribet-v-bk-pari/ | На странице https://stavkinasport.com/fribet-v-bk-pari/ отображается непереведённый шорткод [ap-quiz id = "90412"] | Средний |
| 22 | 19.09.2026<br>20:04 | iPhone / iOS 26.3.1 / Safari | https://stavkinasport.com/prognozy/ | Не работает поле "Поиск прогнозов" на странице прогнозов | Высокий |
| 23 | 19.09.2026<br>20:07 | iPhone / iOS 26.3.1 / Safari | https://stavkinasport.com/prognozy-na-futbol/ | На странице https://stavkinasport.com/prognozy-na-futbol/ отображается непереведённый шорткод [ap-quiz id = "69988"] | Средний |
| 24 | 19.09.2026<br>20:15 | iPhone / iOS 26.3.1 / Safari | https://stavkinasport.com/prognozy-na-tennis/ | На странице https://stavkinasport.com/prognozy-na-tennis/ отображается непереведённый шорткод [ap-quiz id = "80337"] | Средний |
| 25 | 19.09.2026<br>20:20 | iPhone / iOS 26.3.1 / Safari | https://stavkinasport.com/prognozy-na-mma/ | На странице https://stavkinasport.com/prognozy-na-mma/ отображается непереведённый шорткод [ap-quiz id = "80311"] | Средний |
| 26 | 19.09.2026<br>20:23 | iPhone / iOS 26.3.1 / Safari | https://stavkinasport.com/prognozy-na-basketbol/ | На странице https://stavkinasport.com/prognozy-na-basketbol/ отображается непереведённый шорткод [ap-quiz id = "91355"] | Средний |
| 27 | 19.09.2026<br>20:26 | iPhone / iOS 26.3.1 / Safari | https://stavkinasport.com/cybersport-prognozy/ | На странице https://stavkinasport.com/cybersport-prognozy/ отображается непереведённый шорткод [ap-quiz id = "91379"] | Средний |
| 28 | 19.09.2026<br>20:41 | iPhone / iOS 26.3.1 / Safari | https://stavkinasport.com/vernyak/ | На странице https://stavkinasport.com/vernyak/ отображается непереведённый шорткод [wp_revieve_banner zone_id="articles_1"] | Средний |
| 29 | 19.09.2026<br>20:44 | iPhone / iOS 26.3.1 / Safari | https://stavkinasport.com/vernyak/ | На странице https://stavkinasport.com/vernyak/ в статье "Верняк для 13 марта! Динамо Махачкала" отсутствует заглавное изображение | Низкий |
| 30 | 19.09.2026<br>20:49 | iPhone / iOS 26.3.1 / Safari | https://stavkinasport.com/o-nas/ | Ошибка 404 при переходе на вкладку "Редакция " | Средний |
| 31 | 19.09.2026<br>20:54 | iPhone / iOS 26.3.1 / Safari | https://stavkinasport.com/novosti/ | На странице https://stavkinasport.com/novosti/ отображается непереведённый шорткод [wp_revieve_banner zone_id="news"] | Средний |
| 32 | 19.09.2026<br>21:00 | iPhone / iOS 26.3.1 / Safari | Главная / stavkinasport.com | В блоке "Наши соцсети" активна только кнопка Telegram | Средний |
| 33 | 19.09.2026<br>21:11 | iPhone / iOS 26.3.1 / Safari | Главная / stavkinasport.com | В футере в разделе "Соцсети" указан только Telegram | Средний |

## Инструменты

- Ручное исследовательское тестирование
- DevTools (Chrome)
- Google Photos для хранения скриншотов/видео подтверждений
