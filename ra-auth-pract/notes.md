## Как создать серверную часть и клиентскую часть авторизации.

1.  Архитектура папок:
    ra-auth-pract/  
    ├── client/  
    │ ├── node_modules/  
    │ ├── public/  
    │ ├── src/  
    │ │ ├── components/  
    │ │ │ ├ LoginPage.jsx  
    │ │ │ ├ ProfilePage.jsx  
    │ │ │ └ ProtectedRoute.jsx  
    │ │ ├── App.css  
    │ │ ├── App.jsx  
    │ │ ├── index.css  
    │ │ └── main.jsx  
    │ └── (файлы рабочего окружения React)  
    │  
    └── server/  
    ├── package-lock.json  
    ├── package.json  
    └── server.js

2.  Что нужно установить через npm:  
    `npm install express bcrypt jsonwebtoken cors`

    ### express:

    Основа backend-сервера.

    Нужен для:
    - создания сервера,
    - маршрутов GET, POST,
    - req, res,
    - app.listen().

    ### bcrypt:

    Нужен для хеширования паролей.

    Используем для:
    - bcrypt.hash(password, 10) — создать хеш
    - bcrypt.compare(password, passwordHash) — проверить пароль

    ### jsonwebtoken:

    Нужен для работы с JWT.

    Используем для:
    - jwt.sign(...) — создать токен
    - jwt.verify(...) — проверить токен

    ### cors:

    Нужен, чтобы React frontend мог отправлять запросы на backend с другого порта.

    Например:
    - frontend: localhost:5173
    - backend: localhost:3000
    - Без cors браузер может блокировать запросы.
