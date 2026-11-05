# Промпты для картинок (Gemini)

Просто прикрепите готовую картинку в чат — Claude сам сохранит её с нужным именем.
Статус: ⬜ нужно · ✅ готово.

## Первый экран (hero)

✅ `hero-a-model` — вариант A, 4:3 (1600×1200)
```
Photograph of a white architectural scale model of a secure data center, cut in vertical cross-section, standing on a light grey studio table. Above the ground line: a two-storey rectangular concrete building with rooftop cooling units. Below the ground line: a reinforced underground hall with rows of tiny server racks; only the racks in the underground hall are deep red (#D62839), everything else is matte white and pale grey. Soil layers shown as stacked light grey cardboard sheets. On the right: two small shipping-container data center modules on the surface. Soft diffused studio light from the upper left, gentle natural shadows, medium-format camera, 50mm lens, viewed slightly from above at three-quarter angle. Plain light grey background (#E9ECF1). No text, no labels, no people, no glow, no HDR, no lens flare.
```

✅ `hero-b-night` — вариант B. Gemini сделал кадр с пустой левой половиной; в файле оставлена только правая половина (вертикальная), фон слева на сайте — цвет `#1D283A`, переход градиентом.
```
Photorealistic architectural visualization at blue hour, cross-section cutaway of a secure data center campus. The left 45% of the frame is empty dark sky and dark ground (space for text). On the right half: a modern two-storey dark concrete data center building with softly lit windows and rooftop cooling units; the ground in front of it is cut open, revealing a reinforced underground server hall lit in cool white, rows of black server racks, with exactly one rack row softly glowing red; next to the building, three dark grey container data center modules on a concrete pad. Visible soil and rock layers in the cut. Wet asphalt, perimeter fence, overcast dark blue sky. Camera: wide shot, eye level, 35mm, realistic proportions. Muted cool color grading, deep navy and graphite tones. No text, no logos, no people, no neon, no lens flare, no sci-fi.
```

✅ `hero-c-ground`, `hero-c-underground`, `hero-c-container` — вариант C, три вертикальные 4:5 (1200×1500). Генерировать по очереди в одном чате Gemini, чтобы стиль совпал; в конце каждого промпта: «Same photographic style, light and color grading as the previous image.»
```
1) Architectural photograph of a modern minimalist data center building made of grey concrete and dark perforated metal panels, flat landscape, overcast soft daylight, muted natural colors, vertical composition, shot on a medium-format camera, 35mm, eye level. No text, no logos, no people.

2) Architectural photograph inside an underground data center hall: reinforced concrete vaulted ceiling, rows of black server racks with cold aisle containment, cool white linear lighting, clean polished concrete floor, one small red accent light at the far end, vertical composition, symmetrical one-point perspective, medium-format camera. No text, no logos, no people.

3) Architectural photograph of three dark grey container data center modules standing on a concrete pad, cooling units on top, cable trays, gravel and a fence around, overcast soft daylight, muted natural colors, vertical composition, medium-format camera, 35mm. No text, no logos, no people.
```
