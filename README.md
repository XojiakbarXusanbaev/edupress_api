# EduPress API

EduPress API — это мощный инструмент для управления образовательным контентом и пользователями в онлайн-обучении.

## Возможности
- Управление пользователями (регистрация, аутентификация, роли)
- Работа с курсами (создание, редактирование, удаление)
- Управление уроками и материалами
- Отслеживание прогресса студентов
- API для интеграции с другими сервисами

## Установка

1. Клонируйте репозиторий:
   ```sh
   git clone https://github.com/xusanbaevxojiakbar/edupress-api.git
   cd edupress-api
   ```
2. Установите зависимости:
   ```sh
   pip install -r requirements.txt
   ```
3. Настройте переменные окружения в `.env`:
   ```ini
   DATABASE_URL=postgres://user:password@localhost:5432/edupress
   SECRET_KEY=your_secret_key
   ```
4. Выполните миграции:
   ```sh
   python manage.py migrate
   ```
5. Запустите сервер:
   ```sh
   python manage.py runserver
   ```

## Использование API
API предоставляет эндпоинты для работы с пользователями, курсами, уроками и другими сущностями. Подробная документация доступна по `/docs`.

Пример запроса для получения списка курсов:
```sh
curl -X GET "http://localhost:8000/api/courses/" -H "Authorization: Bearer your_token"
```

## Авторизация
Используется JWT-аутентификация. Для получения токена:
```sh
curl -X POST "http://localhost:8000/api/token/" -d "username=your_username&password=your_password"
```

## Лицензия
Проект распространяется под лицензией MIT.

## Контакты
Если у вас есть вопросы или предложения, обращайтесь: your.email@example.com

