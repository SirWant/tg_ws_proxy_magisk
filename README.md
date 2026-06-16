# TG-WS Proxy Magisk
Magisk-реализация MTProto-прокси через WebSocket для Android (Magisk/KernelSU/APatch). Предназначено для обхода ограничений, когда стандартный TCP трафик Telegram блокируется или замедляется.
## Особенности
* Rust-core: Высокая производительность и низкое потребление ресурсов.
* WebSocket: Маскировка трафика под стандартный HTTPS.
* Action Button: Запуск и мгновенное получение ссылки кнопкой в менеджере модулей. 
* Config-driven: Гибкая настройка через WEBUI
* Auto-connect: Автоматическое открытие Telegram с готовой кнопкой подключения.
* CD_BYPASS: Система автоматического подбора оптимального домена Cloudflare.

| Параметр | Описание |
| :--- | :--- |
| PORT | Локальный порт (по умолчанию 1443) |
| HOST | Адрес (по умолчанию 127.0.0.1) |
| SECRET | 32 hex символа. Если пусто - генерируется автоматически. |
| CF_DOMAIN | Домен Cloudflare. Если пусто и CD_BYPASS включен - выберет сам. |
| CF_WORKER_DOMAIN | Домен [Cloudflare Worker](https://github.com/Flowseal/tg-ws-proxy/blob/main/docs/CfWorker.md). |
| FAKE_TLS | Домен для маскировки TLS трафика. (по умолчанию: www.mozilla.org) |
| AUTOSTART | Авто-запуск при загрузке системы. |
| CD_BYPASS | Автоматический выбор лучшего домена из списка. |

## Использование
Настройка и управление через WEBUI, и/или запуск/остановка уже настроенного (через WEBUI или файлом /data/adb/modules/tg_ws_proxy_f1ndle/config.conf) в менеджере модулей.

# Поддержать автора ([F1NDLE](https://github.com/F1NDLE/tg_ws_proxy_magisk))

ЮMoney - 4100119389701453

T-Банк - 2200701799637712 (Маис. М)
---
Binary: [tg-ws-proxy-rs](https://github.com/valnesfjord/tg-ws-proxy-rs)  
Original Project: [FLOWSEAL](https://github.com/Flowseal/tg-ws-proxy)  
Module by: [F1NDLE](https://github.com/F1NDLE/tg_ws_proxy_magisk)
