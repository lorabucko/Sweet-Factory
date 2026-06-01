# Sweet workshop

Landing page / каталог для **Солодкої Майстерні**: адаптивний сайт магазину
десертів із динамічним завантаженням товарів, фільтрацією за категоріями,
відгуками клієнтів, FAQ, слайдерами та модальним вікном деталей десерту.

## Можливості

- Адаптивна верстка для mobile, tablet і desktop.
- Каталог десертів із завантаженням даних з API.
- Фільтрація за категоріями та пагінація через кнопку "Завантажити ще".
- Модальне вікно десерту із зображенням, ціною, описом, складом і рейтингом.
- Слайдер відгуків клієнтів.
- Слайдер зображень у секції "Про нас".
- FAQ-акордеон.
- Мобільне burger-меню з обробкою Escape і resize.
- Production-збірка налаштована для деплою під `/team-dev/`.

## Технології/Stack

- Vite
- Vanilla JavaScript modules
- HTML partials через `vite-plugin-html-inject`
- CSS-файли, зібрані через `src/css/styles.css`
- Axios
- Swiper
- Tom Select
- Accordion JS
- iziToast

## Запуск

Встановити залежності:

```bash
npm ci
```

Запустити dev-сервер:

```bash
npm run dev
```

Зібрати production-версію:

```bash
npm run build
```

Локально переглянути production-збірку:

```bash
npm run preview
```

## Структура проєкту

```text
src/
  index.html              Головна сторінка, зібрана з HTML partials
  main.js                 JavaScript entry point
  css/
    common/               Reset, base, container, animations, loader
    sections/             Стилі окремих секцій
    styles.css            Головний файл імпортів CSS
  js/
    exported/             Спільні constants, API та loader helpers
    partials/             Скрипти секцій і UI-поведінка
  partials/               HTML partials для секцій і модалок
  public/                 Статичні public assets
  img/                    Зображення та SVG sprite
```

## API

Застосунок використовує:

```js
https://deserts-store.b.goit.study/api
```

Основні endpoints:

- `GET /categories` - категорії десертів.
- `GET /desserts` - список десертів з пагінацією та опційною фільтрацією.
- `GET /desserts/:id` - деталі десерту для модального вікна.
- `GET /feedbacks` - відгуки клієнтів.
- `POST /orders` - відгуки клієнтів.

## Корисні скрипти

- `npm run dev` - запускає Vite у режимі розробки.
- `npm run build` - створює production-збірку в `dist/`.
- `npm run preview` - локально запускає production-збірку.

HEADER Main navigation section, provided by a nicely stylized mobile menu on
mobile devices and navigation links on desktops, also shows the main Logo.

image HERO Simple and light section. Background covered by an img that
dynamically changes on different devices for better UX and performance. The main
button is made as a link to the ABOUT US section.

image POPULAR Displaces dynamically loaded popular products. Equipped with a
nicely styled swiper and the ability to open a detailed menu about the product.

image DESSERT LIST Section with dynamically loaded products and categories from
the backend, which is also provided with a nicely stylized selection menu for
mobile users,the posibility to load more products, and filter by category. While
loading, it shows a loader for better UX.

image ABOUT US Section telling us about the company and what exactly it provides
for its customers, equiped with a swiper for desktop and tablet users.

image FEEDBACK The main element of that section is a swiper with dynamically
loaded feedback from users, telling us about users and customers stories of
relationships with the company.

image FAQ Displays frequently asked questions from users and customers and
provides the answers for them.

image DESSERT DETAIL MODAL Shows detailed information about the product and
provides the possibility to check the count of stars set by the users and
customers.

image ORDER MODAL Modal for ordering the product, where the user is supposed to
write down their name, phone number and an optional comment.

image FOOTER The last part of our website provides information about the policy,
logo, and links for social media, as well as sections for faster navigation on
the website.

image
