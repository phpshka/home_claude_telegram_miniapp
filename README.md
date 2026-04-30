# home_claude_telegram_miniapp

Mini App (Telegram WebApp) для бота `home_claude_telegram` — POC дашборд группы ЗОЖ.

## Назначение

Telegram WebApp (HTML/CSS/JS), открывается из бота `@HomeAssistentPlushkinBot` по команде `/dashboard` в группе ЗОЖ. Показывает визуальный дашборд: цифры за день, графики недельных трендов, цели, напоминания.

## Статус

🟡 **POC** (proof-of-concept). Mock-данные, без backend, без аутентификации. Цель — оценить UX в реальном Telegram на iPhone до того, как инвестировать недели в полноценный backend.

## Хостинг

GitHub Pages (бесплатно, HTTPS из коробки): https://phpshka.github.io/home_claude_telegram_miniapp/

## Связь с ботом

- `bot.py` команда `/dashboard` (admin + группа ЗОЖ only) → отвечает inline-кнопкой `WebApp(url=...)`
- На твоём iPhone Telegram открывает страницу в WebView
- Telegram WebApp SDK даёт доступ к `initData.user`, теме, языку

## Структура

```
home_claude_telegram_miniapp/
├── README.md
├── VERSION
├── .gitignore
└── index.html        ← single-page POC (Tailwind CDN + Chart.js + mock data)
```

## Версия

0.0.0.1 — pre-alpha POC.
