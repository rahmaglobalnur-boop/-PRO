# -PRO — база дизайн-наработок RAHMAGLOBAL

Этот репозиторий — память по дизайну. Перед любой вёрсткой, макетом, лендингом или визуалом
прочитай нужный файл отсюда.

## Что где лежит
| Файл | Откуда | Для чего |
|---|---|---|
| `docs/NUR_DESIGN_SYSTEM.md` | `Minimalizm` | Apple Monochrome × Laguta. Токены, шрифты, компоненты, Manhaj-фильтр, UX-паттерны. Стандарт для FURSAN·FURKAN, TASLIM, NUR Mediaholding |
| `docs/RAHMAGLOBAL_UZ_DESIGN_PRINCIPLES.md` | `claude-dizayn-Rahmaglobal.1` | Система сайта rahmaglobal.uz: Ammar + Interphases, cream/ink, Apple-нейтрали для SEO-страниц, правила Impeccable |
| `docs/LAGUTA_REFERENCES.md` | `A.LAGUTA` | Разбор референсов Лагуты (GRID, OPERA AUSTRALIA, скриншоты) |
| `.claude/skills/apple-design` | роадмап владельца | Apple Design Skills: 9 разделов от HIG до реальных проектов |
| `.claude/skills/nur-design-standard` | `Minimalizm` | Автоприменение NUR-стандарта |
| `.claude/skills/cheap-generation` | `Minimalizm` | Генерация картинок/видео через Artlist вместо Higgsfield |
| `.claude/skills/brief-interview` | `COMANDOS` | Бриф кнопками → мега-ТЗ перед стройкой |
| `.claude/skills/design-jury` | `COMANDOS` | Слепая оценка сайта по 8 критериям Awwwards |
| `.claude/skills/verify-site` | `COMANDOS` | Проверка сайта через Playwright, 3 круга |

## Какую систему брать
- FURSAN·FURKAN, TASLIM, NUR Mediaholding → `NUR_DESIGN_SYSTEM.md` целиком, токены без изменений.
- rahmaglobal.uz → `RAHMAGLOBAL_UZ_DESIGN_PRINCIPLES.md`. От NUR-системы берутся только принципы, не цвета и шрифты.
- Новый проект без своей системы → принципы Лагуты + Apple, спросить владельца про палитру.

## Общие правила (во всех проектах)
- Radius 0. Сетка 4 колонки, выравнивание по левому краю.
- Один акцентный цвет максимум, один primary CTA на экран.
- Анимации ≤500ms, `cubic-bezier(.16,1,.3,1)`, hover едва заметен.
- Manhaj-фильтр блокирующий: без людей и животных с лицами, без женских образов, без инструментальной музыки.
- Без AI-слопа: никаких eyebrow-надписей над заголовками, эмодзи вместо иконок, фиолетовых градиентов, скруглённых шаблонных карточек.
- Факты не выдумывать. Для еды: «продукт питания, не лекарство».

## Порядок работы
1. Короткий запрос на сайт → `brief-interview`.
2. Стройка по нужной системе.
3. `verify-site` → `design-jury` (цель 9/10).

Живой источник NUR-стандарта — Notion, ссылки в `docs/NUR_DESIGN_SYSTEM.md`.
