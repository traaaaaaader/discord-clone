# Discord clone Next

<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=next,vite,ts,bun,tailwind,15min&perline=10" />
  </a>
</p>

---

## Содержание

1. [Внешний вид](#внешний-вид)
2. [Основной функционал](#основной-функционал)
3. [Конфигурация](#конфигурация)
4. [Установка и запуск](#установка-и-запуск)

## Внешний вид

<kbd>![Темная тема - текстовый канал](./images/auth.png)</kbd>
<kbd>![Темная тема - голосовой канал](./images/main_page.png)</kbd>
<kbd>![Светлая тема - модальное окно](./images/modal_window.png)</kbd>

## Основной функционал

| Функционал                     | Описание                                                                |
| ------------------------------ | ----------------------------------------------------------------------- |
| `Аутентификация`               | С помощью Clerk |
| `Личные сообщения`             | Сообщения между пользователями                                          |
| `Сообщения в тектовых каналах` | Сообщения в текстовом канале сервера между его участниками              |
| `Звонок на канале сервера`     | Создание/присоединение к комнате звонка через `livekit`        |
| `Звонок между пользователями`     | Создание/присоединение к звонку между 2 пользователями        |
| `Демонстрация экрана`          | Выбор окна для демонстрации изображения со своего компьютера            |
| `Включение веб-камеры`         | Выключение веб-камеры для демонстрации изображения с нее                |
| `Отправка файлов`              | Сообщение с файлом другому пользователю                                 |

## Конфигурация

В `.env` требуется указать переменные:

| Переменная                           | Описание                                                            | Значение по умолчанию                                      |
|--------------------------------------|---------------------------------------------------------------------|-------------------------------------------------------------|
| `NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY` | Публичный ключ для инициализации Clerk на клиенте                  | `pk_test_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx` |
| `CLERK_SECRET_KEY`                  | Секретный ключ для серверных запросов к Clerk                      | `sk_test_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx` |
| `NEXT_PUBLIC_CLERK_SIGN_IN_URL`     | URL для страницы входа                                              | `/sign-in`                                                  |
| `NEXT_PUBLIC_CLERK_SIGN_UP_URL`     | URL для страницы регистрации                                        | `/sign-up`                                                  |
| `NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL` | Редирект после входа                                              | `/`                                                         |
| `NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL` | Редирект после регистрации                                        | `/`                                                         |
| `DATABASE_URL`                      | Строка подключения к базе данных PostgreSQL                        | `postgresql://user:password@host/dbname?sslmode=require`    |
| `UPLOADTHING_TOKEN`                | Токен для взаимодействия с UploadThing                             | `uploadthing_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`   |
| `LIVEKIT_API_KEY`                  | Публичный API-ключ для LiveKit                                     | `livekit_api_key_xxxxxxxxxxxxx`                            |
| `LIVEKIT_API_SECRET`               | Секретный ключ для подписи JWT токенов LiveKit                     | `livekit_secret_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`            |
| `NEXT_PUBLIC_LIVEKIT_URL`          | URL WebSocket-сервера LiveKit для клиента                          | `wss://your-livekit-instance.livekit.cloud`                |



## Установка и запуск

Установить зависимости:

```
bun install
```

Запустить веб-приложение:

```
bun dev
```