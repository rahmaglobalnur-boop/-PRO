---
name: apple-design
description: Apple Design Skills — HIG-принципы, типографика, цвет, компоненты, паттерны, доступность, перенос iOS-приёмов на веб, токены и Figma, продакшн (SEO, скорость, тесты) и разбор реальных типов проектов (дашборд, CMS, SaaS). Используй, когда просят «в стиле Apple», «как на apple.com», «по HIG», «Apple-минимализм», делают iOS/macOS-подобный интерфейс, или когда задача по NUR/Rahma-проектам упирается в вопрос «как это сделал бы Apple». Работает вместе с nur-design-standard: если проект NUR/Rahma, токены и radius 0 берутся из его системы, а отсюда — принципы и паттерны.
---

# Apple Design Skills

Скил устроен как роадмап. Читай только тот файл, который нужен задаче.

```
1. Foundations      → references/01-foundations.md    HIG, типографика, цвет, сетка
2. Components       → references/02-components.md     кнопки, поля, навигация
3. Patterns         → references/03-patterns.md       формы, списки, модалки, состояния
4. Accessibility    → references/04-accessibility.md  контраст, клавиатура, скринридеры
5. Web vs iOS       → references/05-web-vs-ios.md     что переносится на веб, что нет
6. Design Systems   → references/06-design-systems.md токены, переменные, Figma
7. Production       → references/07-production.md     SEO, скорость, тесты
8. Real Projects    → references/08-real-projects.md  дашборд, CMS, SaaS
9. Resources        → references/09-resources.md      ссылки, репозитории
```

## Главное правило приоритета
Apple — это источник принципов, а не палитры. Если проект уже имеет систему, она главнее:
- FURSAN·FURKAN / TASLIM / NUR Mediaholding → `docs/NUR_DESIGN_SYSTEM.md` (radius 0, монохром, teal-акцент).
- rahmaglobal.uz → `docs/RAHMAGLOBAL_UZ_DESIGN_PRINCIPLES.md`.

Apple скругляет углы. В NUR-проектах углы остаются острыми (radius 0), это решение владельца.

## Быстрый чек-лист «это выглядит как Apple?»
- [ ] Один главный CTA, остальные — вторичные.
- [ ] Контент важнее хрома: интерфейс не спорит с содержимым.
- [ ] Иерархия читается по размеру и весу шрифта, а не по цвету.
- [ ] Много воздуха, короткие строки текста.
- [ ] Анимации короткие и объясняют переход, а не украшают.
- [ ] Работает в тёмной теме, с увеличенным шрифтом и без мыши.
