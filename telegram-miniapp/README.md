# ElfBull — Telegram Mini App

Telegram Mini App с тем же интерфейсом, что и основной сайт ElfBull.

## Структура

```
telegram-miniapp/
├── index.html              # Главная страница (каталог)
├── vaporesso-xros3.html    # Страница товара Vaporesso XROS 3
├── geekvape-aegis-legend-2.html
├── smok-nord-5.html
├── assets/                 # Изображения
│   ├── elfbull-logo-full.png
│   ├── vaporesso-xros3.png
│   ├── geekvape-aegis-legend-2.png
│   └── smok-nord-5.png
└── README.md
```

## Как подключить к боту Telegram

1. **Создайте бота** (если ещё нет): напишите [@BotFather](https://t.me/BotFather), отправьте `/newbot` и следуйте инструкциям.

2. **Опубликуйте Mini App** — загрузите папку `telegram-miniapp` на хостинг (GitHub Pages, Vercel, Netlify или свой сервер). URL должен быть HTTPS, например:
   - `https://ваш-сайт.com/telegram-miniapp/`
   - `https://ваш-сайт.com/elfbull-miniapp/`

3. **Привяжите Mini App к боту**:
   - Напишите [@BotFather](https://t.me/BotFather)
   - Отправьте `/newapp` или `/mybots` → выберите бота → Bot Settings → Menu Button
   - Выберите "Configure menu button"
   - Укажите URL вашего Mini App, например: `https://ваш-сайт.com/telegram-miniapp/index.html`

4. **Готово.** При открытии бота пользователи увидят кнопку меню, ведущую в Mini App.

## Локальный тест

Mini App корректно работает только внутри Telegram (нужен `tgWebAppData` и др.). Для проверки интерфейса можно открыть `index.html` в браузере — интерфейс будет таким же, но без Telegram-событий.

## Используемые API Telegram Web App

- `Telegram.WebApp.ready()` — сообщение о готовности
- `Telegram.WebApp.expand()` — на весь экран
- `Telegram.WebApp.setHeaderColor()` / `setBackgroundColor()` — цвет шапки и фона
- `Telegram.WebApp.showAlert()` — всплывающее уведомление при оформлении заказа
