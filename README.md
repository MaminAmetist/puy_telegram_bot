---

# 🧾 puy\_telegram\_bot

Telegram-бот для оформления платной подписки с использованием Telegram Payments.

## 🚀 Возможности

* Команда `/buy` запускает оформление подписки на 1 месяц;
* Поддержка Telegram Payments (включая тестовый режим);
* Обработка этапов оплаты: выставление счета, подтверждение, успешный платеж.

## ⚙️ Установка и запуск

### 1. Клонировать репозиторий

```bash
git clone https://github.com/MaminAmetist/puy_telegram_bot.git
cd puy_telegram_bot
```

### 2. Установить зависимости

```bash
pip install -r requirements.txt
```

> **Примечание:** Убедитесь, что у вас установлен Python 3.7+

### 3. Создать файл `config.py`

Создайте файл `config.py` в корне проекта со следующим содержимым:

```python
TOKEN = "ВАШ_TELEGRAM_BOT_TOKEN"
PAYMENTS_TOKEN = "ВАШ_PROVIDER_PAYMENT_TOKEN"
```

* `TOKEN` — токен Telegram-бота;
* `PAYMENTS_TOKEN` — платежный токен от [@BotFather](https://t.me/botfather) или [@PaymentBot](https://t.me/PaymentBot). Используйте `TEST:` токен для тестирования.

### 4. Запуск

```bash
python bot.py
```

Бот начнет работать в режиме long polling.

## 💡 Пример использования

Пользователь пишет `/buy`, бот предлагает оформить подписку. После успешной оплаты бот уведомляет пользователя о результате.

## 🧾 Зависимости

* [aiogram](https://github.com/aiogram/aiogram) — асинхронная библиотека для Telegram Bot API
