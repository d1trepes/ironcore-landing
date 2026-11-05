# Бренд IronCore: логотип, цвета, картинки

## Цвета (из эскиза заказчика)
| Роль | HEX | Где |
|---|---|---|
| Синий (основной) | `#1E3A8A` | «IRON», кнопки, ссылки, линии схем |
| Красный (акцент) | `#D62839` | «CORE», ядро знака, главная CTA, активные состояния |
| Графит | `#141821` | текст, тёмные фоны |
| Серый текст | `#5B6475` | второстепенный текст |
| Светлый фон | `#F4F6FA` | фоны секций |
Точные оттенки фона и нейтралей подбирает каждый вариант hero; синий и красный общие.

## Логотип
Эскиз заказчика: надпись IRONCORE, синий и красный цвета, буква O с «ядром»-точкой. Нужно добавить значок.
Варианты знака (Ядро, Щит, Слои ЦОД, Гайка, Над и под землёй, Монограмма IC) — на холсте https://claude.ai/artifact/2YTvUwpTLDRfi2W4fS1b6W. Рекомендуем «Ядро» или «Щит».

Как делать:
1. Значок генерируем в Gemini **без текста** (нейросети портят буквы).
2. Надпись IRONCORE набираем шрифтом в коде (IRON синим, CORE красным).
3. Выбранный значок перерисовываем в SVG (вектор, чёткий на любом размере) — делает Claude по картинке, кладём в `assets/img/logo.svg` и `assets/img/favicon.svg`.
4. До готового логотипа на сайте стоит временный SVG «Ядро».

### Промпт для Gemini (значок)
```
Minimal geometric logo mark for "IronCore", a company that designs secure data centers. Concept: a protected core — a solid red circle (#D62839) at the center, enclosed by a thick deep-blue (#1E3A8A) shape that suggests armor or a shield. Flat vector style, 2 colors only, no gradients, no shadows, no 3D, no text, no letters. Bold strokes with consistent width, perfectly symmetric, works at 16px favicon size. Centered on a pure white background, lots of empty space around it. Style of a Swiss engineering firm identity, like Pentagram or Wolff Olins.
```
Вариации (меняйте только вторую фразу):
- щит: `…enclosed by a deep-blue shield outline with rounded joins.`
- слои: `…the red element is the top layer of three stacked isometric server layers drawn in deep blue.`
- гайка: `…enclosed by a deep-blue hexagon, like an engineering nut seen from above.`

Просите 4 варианта, выбирайте самый простой. Если Gemini добавил текст или тени — допишите в начало `Strictly no text.`

## Картинки для сайта (Gemini)
Общий стиль, добавлять в конец каждого промпта:
```
Photorealistic architectural visualization, realistic materials (concrete, steel, glass), believable scale and human-height details, natural soft daylight or blue-hour light, muted cool color grading with deep blues, a single small red accent element, no text, no logos, no people close-up, no sci-fi, no neon glow, 16:9, high detail.
```
Правила:
- Разрезы ЦОД (вид в разрезе, cutaway) — главный повторяющийся приём: так видно и здание, и подземный уровень, и инженерку.
- Один ракурс и свет на весь набор, иначе сайт выглядит лоскутным.
- Конкретные промпты для каждого блока пишутся в `docs/image-prompts.md` в тот момент, когда блок делается.
- Готовые картинки: формат `.webp` или `.jpg`, ширина 1920px для hero и 1200px для карточек, имена — как указано в `image-prompts.md`, папка `assets/img/`.
