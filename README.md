<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>МойБлог</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<header>
<h1>МойБлог</h1>
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
functionsubscribeToUserProfile(userId) {
  // Отправка запроса на сервер для подписки на профиль пользователя
$.ajax({
    url: '/subscribe',
    method: 'POST',
    data: { userId: userId },
    success: function(response) {
// В случае успешной подписки обновляем интерфейс или выполняем другие действия
console.log('Подписка выполнена успешно!');
    },
error: function(error) {
      // Обрабатываем ошибку подписки
console.error('Произошла ошибка при подписке', error);
    }
  });
}

// Пример использования функции
varuserId = 123; // Здесь указывается ID пользователя, на которого нужно подписаться
subscribeToUserProfile(userId);
constsubscribes = [
  {'user1', ['пост1', 'пост2', 'пост3'] },
  {'user2', ['пост4', 'пост5', 'пост6'] },
  {'user3', ['пост7', 'пост8', 'пост9'] }
];

// Функция для генерации списка публикаций на основе подписок
function generateList(subscription) {
  let listPost = [];

  // Обход массива подписок
  subscription.forEach(subscription => {
    const {subscribes } = subscription;

    // Добавление публикаций в общий список публикаций
ListPost = listPost.concat(post);
  });

  Return listPost;
}

// Вызов функции генерации списка публикаций
const list = generateListPost(subscription);

// Вывод списка публикаций на консоль
console.log(list);
function viewPublicPosts() {

  fetch('https://127.0.0.1/api/posts/public')
    .then(response => response.json())
    .then(posts => {
// Пример обработки и отображения постов
posts.forEach(post => {
console.log(`Заголовок: ${post.title}`);
console.log(`Автор: ${post.author}`);
        console.log(`Содержимое: ${post.content}`);
        console.log('-------------------------');
      });
    })
    .catch(error => {
      console.error('Ошибка при загрузке публичных постов:', error);
    });
}

// Вызов функции просмотра публичных постов
viewPublicPosts();
functionshowHiddenPost() {
  // Получить элемент, представляющий скрытый пост
var hiddenPost = document.getElementById('hidden-post');

// Проверить, скрыт ли уже пост
if (hiddenPost.style.display === 'none') {
    // Если да, показать пост
hiddenPost.style.display = 'block';
console.log('Показан скрытый пост');
  } else {
    // Если нет, скрыть пост
hiddenPost.style.display = 'none';
console.log('Скрыт пост');
  }
}
// Симулируем базу данных с постами
letposts = [
  { id: 1, title: 'Заголовок поста 1', content: 'Содержимое поста 1' },
  { id: 2, title: 'Заголовок поста 2', content: 'Содержимое поста 2' },
  { id: 3, title: 'Заголовок поста 3', content: 'Содержимое поста 3' }
];

// Поиск поста по его идентификатору
functionfindPostById(id) {
return posts.find(post => post.id === id);
}

// Редактирование поста
function editPost(id, newTitle, newContent) {
  const post = findPostById(id);
  if (post) {
    post.title = newTitle;
    post.content = newContent;
    console.log('Пост успешно отредактирован');
  } else {
console.log('Пост не найден');
}
}

// Удаление поста
function deletePost(id) {
  const postIndex = posts.findIndex(post => post.id === id);
  if (postIndex !== -1) {
    posts.splice(postIndex, 1);
    console.log('Пост успешно удален');
  } else {
console.log('Пост не найден');
  }
}

// Пример использования
editPost(2, 'Новый заголовок', 'Новое содержимое');
deletePost(3);
console.log(posts);
// Создаем объект, представляющий пост блога
functionBlogPost(title, content, tags) {
this.title = title;
  this.content = content;
  this.tags = tags;
}

// Создаем объект, представляющий блог
functionBlog() {
this.posts = [];

  // Функция для добавления нового поста
this.addPost = function(title, content, tags) {
    var post = new BlogPost(title, content, tags);
    this.posts.push(post);
  };

  // Функция для сортировки постов по тегам
this.sortByTag = function(tag) {
    var filteredPosts = this.posts.filter(function(post) {
      return post.tags.includes(tag);
    });

    return filteredPosts;
  };
}

// Создаем экземпляр блога
var myBlog = new Blog();

// Добавляем посты с тегами
myBlog.addPost("Заголовок 1", "Содержимое 1", ["тег1", "тег2"]);
myBlog.addPost("Заголовок 2", "Содержимое 2", ["тег2", "тег3"]);
myBlog.addPost("Заголовок 3", "Содержимое 3", ["тег1", "тег3"]);
myBlog.addPost("Заголовок 4", "Содержимое 4", ["тег2"]);

// Сортируем посты по тегам
varpostsWithTag1 = myBlog.sortByTag("тег1");
console.log(postsWithTag1); // Выводим посты с тегом "тег1"
<div id="comments">
<h2>Комментарии</h2>

<form id="comment-form">
<textarea id="comment-text" placeholder="Введите комментарий"></textarea>
<input type="text" id="comment-author" placeholder="Имя автора" />
<button type="submit">Отправить</button>
</form>

<ul id="comment-list"></ul>
</div>
// Функция для добавления комментария в список комментариев
function addComment() {
  const commentText = document.getElementById('comment-text').value;
  const commentAuthor = document.getElementById('comment-author').value;

  // Создание нового элемента комментария
  const commentItem = document.createElement('li');
  commentItem.textContent = `${commentAuthor}: ${commentText}`;

  // Добавление комментария в список комментариев
  const commentList = document.getElementById('comment-list');
  commentList.appendChild(commentItem);

  // Очистка полей формы после добавления комментария
document.getElementById('comment-text').value = '';
  document.getElementById('comment-author').value = '';
}

// Обработчик отправки формы комментария
document.getElementById('comment-form').addEventListener('submit', function(event) {
  event.preventDefault(); // Предотвращение отправки формы
addComment(); // Добавление комментария
});
