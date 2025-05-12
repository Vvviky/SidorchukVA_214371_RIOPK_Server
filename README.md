# Серверная часть приложения управления задачами

Этот репозиторий содержит серверную реализацию приложения для управления задачами.

## Структура проекта

```
server/
├── src/
│   ├── controllers/     # Обработчики запросов и бизнес-логика
│   ├── models/         # Модели базы данных и схемы
│   ├── routes/         # Определения API маршрутов
│   ├── middleware/     # Пользовательские промежуточные функции
│   ├── config/         # Конфигурационные файлы
│   └── utils/          # Вспомогательные функции и утилиты
├── tests/              # Файлы тестов
├── .env               # Переменные окружения (не отслеживаются в git)
├── .gitignore        # Файл игнорирования Git
├── package.json      # Зависимости проекта и скрипты
└── README.md         # Документация проекта
```

## Технологический стек

- Node.js
- Express.js
- MongoDB
- Mongoose ODM
- JSON Web Tokens (JWT) для аутентификации
- bcrypt для хеширования паролей
- cors для Cross-Origin Resource Sharing

## Предварительные требования

- Node.js (версия 14 или выше)
- MongoDB (версия 4.4 или выше)
- npm (Менеджер пакетов Node)

## Установка

1. Клонируйте репозиторий:
```bash
git clone https://github.com/Vvviky/SidorchukVA_214371_RIOPK_Server.git
cd SidorchukVA_214371_RIOPK_Server
```

2. Установите зависимости:
```bash
npm install
```

3. Создайте файл `.env` в корневой директории со следующими переменными:
```env
PORT=3000
MONGODB_URI=mongodb://localhost:27017/task-manager
JWT_SECRET=your_jwt_secret_key
```

4. Запустите сервер разработки:
```bash
npm run dev
```

## Конечные точки API

### Аутентификация
- `POST /api/auth/register` - Регистрация нового пользователя
- `POST /api/auth/login` - Вход пользователя

### Задачи
- `GET /api/tasks` - Получить все задачи
- `POST /api/tasks` - Создать новую задачу
- `GET /api/tasks/:id` - Получить задачу по ID
- `PUT /api/tasks/:id` - Обновить задачу
- `DELETE /api/tasks/:id` - Удалить задачу

## Конфигурация

Сервер можно настроить с помощью переменных окружения в файле `.env`:

- `PORT`: Номер порта для сервера (по умолчанию: 3000)
- `MONGODB_URI`: Строка подключения к MongoDB
- `JWT_SECRET`: Секретный ключ для генерации JWT токенов

## Документация

Полная документация проекта находится в репозитории [SidorchukVA_214371_RIOPK_Spec](https://github.com/Vvviky/SidorchukVA_214371_RIOPK_Spec ) 
