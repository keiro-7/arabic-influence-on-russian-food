# Как опубликовать презентацию на GitHub Pages

## Вариант 1: Через сайт GitHub (без командной строки)

1. Зайди на [github.com](https://github.com) → войди в аккаунт
2. Нажми зелёную кнопку **New** (или `+` справа сверху → **New repository**)
3. Заполни:
   - **Repository name:** `arabic-cuisine-presentation`
   - **Public** (обязательно для бесплатного GitHub Pages)
   - НЕ ставь галки на README/gitignore (они уже есть)
4. **Create repository**
5. На странице нового репозитория → **uploading an existing file**
6. Перетащи в окно содержимое папки `arabic-cuisine-presentation`:
   - `index.html`
   - `README.md`
   - `.gitignore`
   - `DEPLOY.md`
7. Внизу нажми **Commit changes**

### Включить GitHub Pages

8. В репозитории → вкладка **Settings** (вверху справа)
9. Слева в меню → **Pages**
10. Source → **Deploy from a branch**
11. Branch → **main** + **/ (root)** → **Save**
12. Подожди 1–2 минуты. Обнови страницу.
13. Сверху появится зелёная плашка с ссылкой:

    `https://<твой-логин>.github.io/arabic-cuisine-presentation/`

Эта ссылка — её можно отправить кому угодно.

---

## Вариант 2: Через командную строку (если установлен Git)

```bash
cd "c:/VS Cod/arabic-cuisine-presentation"
git init
git add .
git commit -m "initial: presentation"
git branch -M main
git remote add origin https://github.com/<твой-логин>/arabic-cuisine-presentation.git
git push -u origin main
```

Затем включи Pages так же, как в шагах 8–13 выше.

---

## Если что-то пошло не так

- **Страница пустая / 404** — подожди 2–3 минуты после включения Pages, GitHub медленно деплоит первый раз
- **Не отображаются картинки** — нужен интернет (фото с Unsplash подгружаются по сети)
- **Не отображаются диаграммы** — то же самое: Chart.js загружается с CDN
- **Шрифты не те** — нужен интернет для Google Fonts

Если хочешь сделать презентацию полностью автономной (без интернета) — нужно скачать шрифты, картинки и Chart.js локально. Скажи, и я переделаю.
