<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Название вашего блога</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<header>
<h1>Название вашего блога</h1>
<nav>
<ul>
<li><a href="#">Главная</a></li>
<li><a href="#">О блоге</a></li>
<li><a href="#">Контакты</a></li>
</ul>
</nav>
</header>
<main>
<article>
<h2>Заголовок статьи</h2>
<p>Текст статьи...</p>
<!-- Дополнительный контент -->
</article>

<aside>
<h3>Боковая панель</h3>
<ul>
<li>Ссылка 1</li>
<li>Ссылка 2</li>
<li>Ссылка 3</li>
</ul>
</aside>
</main>

<footer>
<p>Авторское право &copy; 2023 Ваше имя</p>
</footer>
</body>
</html>
# BLOG
// Объект для хранения пользователей
constusers = [];

// Функция регистрации пользователя
functionregisterUser(username, password) {
  // Проверяем, есть ли уже пользователь с таким именем
const existingUser = users.find(user => user.username === username);
  if (existingUser) {
    return "Username is already taken. Pleasechooseanotherusername";
  }

  // Создаем нового пользователя и добавляем в список
const newUser = {
    username: username,
    password: password
};
  users.push(newUser);

  return "Registration successful! You can now log in";
}

// Функция входа пользователя
function loginUser(username, password) {
// Проверяем, существует ли пользователь с заданными именем и паролем
const user = users.find(user => user.username === username && user.password === password);
  if (user) {
    return "Login successful! Welcome back!";
  }

  return "Invalid username or password. Pleasetryagain";
}

// Пример использования функций
console.log(registerUser("alice", "pa$$w0rd")); // Регистрация пользователя "alice"
console.log(registerUser("bob", "123456")); // Регистрация пользователя "bob"
console.log(loginUser("alice", "pa$$w0rd")); // Вход пользователя "alice", успешный
console.log(loginUser("eve", "password123")); // Вход пользователя "eve", неуспешный
