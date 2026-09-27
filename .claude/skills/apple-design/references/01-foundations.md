# 1. Foundations — HIG, типографика, цвет

## Принципы HIG
Актуальная формулировка (HIG после WWDC25, Liquid Glass): **Hierarchy, Harmony, Consistency**.
- Hierarchy — элементы управления отступают, контент впереди.
- Harmony — интерфейс повторяет геометрию устройства и системы.
- Consistency — одинаковые вещи выглядят и ведут себя одинаково на всех платформах.

Старая тройка **Clarity, Deference, Depth** по смыслу та же и хорошо объясняет apple.com:
ясность текста, интерфейс уступает контенту, глубина через слои и движение.

## Типографика
- Системный шрифт — SF Pro. На iOS/macOS он подключается сам через `system-ui` / `-apple-system`.
- Файлы SF Pro нельзя встраивать в веб-сайт (лицензия Apple разрешает их только для Apple-платформ).
  На вебе — стек `system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif`
  или свой шрифт проекта (в NUR это Space Grotesk / Barlow Condensed).
- Dynamic Type, iOS, размер по умолчанию (Large), в pt:

| Стиль | Размер | Вес |
|---|---|---|
| Large Title | 34 | Regular |
| Title 1 | 28 | Regular |
| Title 2 | 22 | Regular |
| Title 3 | 20 | Regular |
| Headline | 17 | Semibold |
| Body | 17 | Regular |
| Callout | 16 | Regular |
| Subheadline | 15 | Regular |
| Footnote | 13 | Regular |
| Caption 1 | 12 | Regular |
| Caption 2 | 11 | Regular |

- Иерархия строится весом и размером. Цвет — только вторичный/третичный серый для подписей.
- Крупные заголовки — отрицательный трекинг, мелкий текст — нулевой или положительный.

## Цвет
Apple.com (веб):
| Роль | Цвет |
|---|---|
| Текст | `#1D1D1F` |
| Вторичный текст | `#6E6E73` |
| Светлый фон секций | `#F5F5F7` |
| Линии | `#D2D2D7` |
| Ссылка / акцент | `#0071E3` |

iOS системные (light / dark):
| Токен | Light | Dark |
|---|---|---|
| systemBlue | `#007AFF` | `#0A84FF` |
| systemRed | `#FF3B30` | `#FF453A` |
| systemGreen | `#34C759` | `#30D158` |
| systemGroupedBackground | `#F2F2F7` | `#000000` |

- Цвет несёт смысл: синий — действие, красный — разрушительное действие, зелёный — успех.
- Один акцент на интерфейс. В NUR его место занимает teal `#00B4A6`.

## Сетка и отступы
- База 8pt (мелкие шаги по 4). В NUR база 4px — совместимо.
- Боковые поля iOS: 16pt на компактной ширине, 20pt на широкой.
- Безопасные зоны (safe area) — контент не под вырезом и не под home-индикатором.
  На вебе: `padding: env(safe-area-inset-*)` + `viewport-fit=cover`.
