# Заполнитель Google-формы для заданий ЕГЭ

Скрипт был написан для занятий в Лицее №7 г. Казани для выполнения весьма нишевой задачи:
заполнения нудной формы для отправки решений заданий при подготовке к ЕГЭ.

Видео с демонстрацией: https://youtu.be/SD40Mkiu0-E

## Предзапуск

Как минимум, у вас должен быть python3, его установку читайте в любом другом месте.

Установите вебдрайвер для своего браузера (поддерживаются примерно все раздутые браузеры
(т.е. твой, username, поддерживается)).
Ссылки ищите тут: https://www.seleniumhq.org/about/platforms.jsp

Установите библиотеку selenium для python: `python3 -m pip install selenium`

В коде в строках после "Edit lines bellow" исправьте `webdriver.WebKitGTK()` на то,
что у вас.
Вероятно, потребуется ввести путь (`executable_path`) до вебдрайвера,
поэтому вот пример для нубов:

```
driver = webdriver.Chrome(executable_path='C:\Documents\')
```

## Запуск

`python3 main.py`

Если вылетит сразу после запуска, значит неправильно установили вебдрайвер.
Читайте ошибку сами.

## Использование

Залогиньтесь в Google-аккаунт, иначе заполнитель умрет от неизвестности места нажатия.

Заполните поля:
 * Задание: это номер задания из ЕГЭ
 * Начинать с номера: номер, с которого заполнитель начнет работу
 * Вы залогинились в Google?: наберите 'y' или 'yes', если да, иначе никак невозможно

Во время ввода ответа пишите его ПОЛНОСТЬЮ, как вы бы сами писали бы в форму.
Бот не магический, он просто возьмет ваше сообщение и отправит.

Хотите вернуться назад или пропустить задание? Используйте стрелочки несколько раз (`<`
или `>`).  Так же можно использовать `@` с номером задания, чтобы перейти конкретно к нему. Например:

```
№10: <<
№8: >>>>
№12: КОЧЕВНИК
№13: 2
№14: @25
№25: ОТВЕТ
№26: @1
№1:
...
```
## Лицензия

Подробности в файле LICENSE.
