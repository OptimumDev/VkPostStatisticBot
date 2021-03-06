# VkPostStatisticBot

## Перед Запуском
Установите переменные окружения:
 - `VK_STATISTICS_APP_ID` - ID приложения VK - `ulong` число
 - `VK_STATISTICS_USER_LOGIN` - логин пользователя VK, от имени которого будут создаваться посты со статистикой
 - `VK_STATISTICS_USER_PASSWORD` - пароль пользователя VK, от имени которого будут создаваться посты со статистикой
 - `VK_STATISTICS_WALL_ID` - ID страницы VK, в которую будет поститься статистика (если это группа, то посты будут создаваться от имени группы, а пользователь должен быть ее администратором) - `long` число. __Важно:__ 
    - Это именно ID, а не ссылка. Например для пользователя `vk.com/id123` ID будет являться число `123`
    - ID группы должно начинаться со знака минус. Например для группы `vk.com/club123` ID будет являться число `-123`

## ТЗ
Бот для [VK](vk.com)

Оформление:
 - Программа представляет собой консольное приложение на языке C#.
 - Программа должна корректно обрабатывать вероятные ошибки и исключения.
 - Использование сторонних библиотек - допускается для работы с API vkontakte и сериализацией.

Задача:
 - Получить статистику с последних 5 постов какого-то аккаунта в vk.
 - Запостить сообщение от собственного аккаунта с этой статистикой.
 - Статистика – [частотность букв](https://ru.wikipedia.org/wiki/%D0%A7%D0%B0%D1%81%D1%82%D0%BE%D1%82%D0%BD%D0%BE%D1%81%D1%82%D1%8C), составляется по данным из постов.

Пример сообщения от собственного аккаунта:
`{username}, статистика для последних 5 постов: {статистика}`  
`{статистика}` представить в виде JSON объекта `{"a": 0.01, "b": 0.003}`

Пожелания:
 - Программа запрашивает id очередного аккаунта до ввода пустой строки.
 - Программа распознаёт id пользователей и групп, цифровые и человекочитаемые.
    - id1
    - durov
    - public147415323
    - tech
 - Вывести статистику в консоль.

Возможные проблемы/вопросы
 - Если не хочется работать с vk или нет там учетки, можно сделать то же самое с другой соцсетью, например twitter или facebook. Однако twitter в последнее время очень долго выдает ключи для api.
 - Если не хочется создавать посты от своего имени во время отладки, можно создать группу и постить в ней.

P.S. Основная цель разработчика – делать что-то прикольное, поэтому не возбраняется:
 1. Писать красивый код.
 2. Закладываться на масштабируемость.
 3. Применение навыков работы со стандартными классами .net и сторонними библиотеками.
 4. Проявление понимания ООП и SOLID.
