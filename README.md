# IronCore — лендинг (демо)

Демо: **https://d1trepes.github.io/ironcore-landing/**
Переключение вариантов первого экрана: панель внизу слева, или ссылки `?hero=a`, `?hero=b`, `?hero=c`. Без подписей: `&labels=0`. Без панели (чистый вид для заказчика): `&demo=0`.

## Как устроено
- `docs/STATUS.md` — что сделано и какой шаг следующий.
- `docs/roadmap.md` — план по чатам и спеки.
- `docs/content.md` — все тексты из ТЗ.
- `docs/design-rules.md`, `docs/brand.md` — правила дизайна, цвета, логотип.
- `docs/image-prompts.md` — промпты картинок для Gemini и имена файлов.
- `docs/tz/` — скриншоты исходного ТЗ.

## Как загрузить картинку
GitHub → папка `assets/img` → **Add file → Upload files** → перетащить файл с именем из `image-prompts.md` → **Commit changes**. Через 1–2 минуты появится в демо.

## Настройка проекта в Claude
Создайте Project «IronCore» и вставьте в его инструкции:
```
Работаем над лендингом IronCore в репозитории GitHub d1trepes/ironcore-landing.
В начале каждого чата подключи этот репозиторий, прочитай CLAUDE.md и docs/STATUS.md и делай шаг, который я назову (или текущий из STATUS.md).
Отвечай по-русски, коротко. Я не программист.
В конце: обнови docs/STATUS.md, commit + push в main, дай ссылку на демо и стартовое сообщение для следующего чата.
```
