# 7. Production — SEO, скорость, тесты

## Скорость (Core Web Vitals, порог «хорошо»)
| Метрика | Цель |
|---|---|
| LCP | ≤ 2.5 s |
| INP | ≤ 200 ms |
| CLS | ≤ 0.1 |

Что это значит для Apple-подобных страниц с большими визуалами:
- Hero-картинка: `fetchpriority="high"`, AVIF/WebP, `width`/`height` заданы (иначе CLS).
- Остальные картинки: `loading="lazy"`, `srcset` + `sizes`.
- Видео: `preload="none"` или `metadata`, постер, для iPhone обязательны `muted playsinline autoplay`
  как атрибуты (урок rahmaglobal.uz, см. его CHECKPOINT).
- Шрифты: `woff2`, `font-display: swap`, preload только для шрифта hero.
- Анимации — `transform` и `opacity`, не `top/left/height`.
- `backdrop-filter` на больших площадях дорогой — проверять на среднем Android.

## SEO
- Один `<h1>` на страницу, заголовки по порядку.
- `<title>` до ~60 символов, description до ~155.
- Open Graph и превью-картинка 1200×630.
- `hreflang` для языковых версий (ru / uz / en / ar).
- JSON-LD: `Organization`, `Product`, `FAQPage` — только с правдивыми данными.
- Текст — HTML, не картинка. Заголовок, «нарисованный» в PNG, поисковик не прочитает.

## Тесты перед релизом
1. `verify-site` — прохождение как пользователь, 1440 и 390 px, консоль чистая.
2. Lighthouse / PageSpeed — Performance, Accessibility, SEO.
3. Клавиатура: пройти страницу только Tab/Enter/Esc.
4. VoiceOver (или NVDA): заголовки и кнопки читаются осмысленно.
5. Тёмная тема, увеличенный шрифт 200%, `prefers-reduced-motion`.
6. `design-jury` — цель 9/10.
