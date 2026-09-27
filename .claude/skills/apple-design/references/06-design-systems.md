# 6. Design Systems — токены, переменные, Figma

## Три слоя токенов
1. **Примитивы** — сырые значения: `--gray-900: #1D1D1F`, `--space-4: 16px`.
2. **Семантика** — роли: `--color-text`, `--color-bg-alt`, `--color-accent`. Тёмная тема меняет только этот слой.
3. **Компоненты** — `--button-primary-bg: var(--color-text)`. Только при необходимости.

```css
:root {
  --gray-900:#1D1D1F; --gray-500:#6E6E73; --gray-100:#F5F5F7; --line:#D2D2D7;
  --color-text:var(--gray-900); --color-text-2:var(--gray-500);
  --color-bg:#FFFFFF; --color-bg-alt:var(--gray-100); --color-line:var(--line);
  --ease:cubic-bezier(.16,1,.3,1); --dur:400ms;
}
@media (prefers-color-scheme: dark) {
  :root { --color-text:#F5F5F7; --color-text-2:#A1A1A6; --color-bg:#000; --color-bg-alt:#1D1D1F; --color-line:#424245; }
}
```
Для NUR-проектов примитивы берутся из `docs/NUR_DESIGN_SYSTEM.md` без изменений значений.

## Figma
- Variables: коллекции `Primitives` и `Semantic`, режимы `Light` / `Dark`.
- Имена переменных в Figma совпадают с CSS (`color/text` ↔ `--color-text`), иначе хендоф ломается.
- Text styles — по ролям (Title 1, Body, Caption), не по размерам («24 bold»).
- Компоненты с вариантами: `state=default|pressed|disabled`, `size=s|m|l`.
- Официальные iOS/macOS UI-киты Apple лежат в Apple Design Resources (см. 09-resources).
- Если в сессии есть Figma MCP — токены можно тянуть через `get_variable_defs`.

## Правила
- Новое значение появляется в коде только через токен.
- Нельзя «почти такой же серый». Если его нет в системе — либо добавить в систему, либо взять существующий.
- Документация токена: имя, значение, где применять, где нельзя.
