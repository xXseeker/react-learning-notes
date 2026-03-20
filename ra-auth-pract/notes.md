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

    **express:**
    Основа backend-сервера.

        Нужен для:
         - создания сервера,
         - маршрутов GET, POST,
         - req, res,
         - app.listen().
