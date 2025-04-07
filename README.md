# Проект SWAPI
![SWAPI](png/Image.jpg)
В одной далёкой-далёкой галактике бушевали звёздные API... Стоп! Что-то тут не так, какие ещё такие API? 
API — это сокращение от Application Programming Interface, а если по-русски, то программный интерфейс приложения. 
Обычно под API инженеры данных подразумевают сайт, к которому можно обращаться по определённым правилам и который будет возвращать заранее оговорённый стандартный ответ.
SWAPI, или Star Wars API — как раз такой пример. Он хранит информацию о персонажах, космических кораблях, планетах и других объектах, которые связаны со вселенной «Звёздных войн».

---
Описание проекта
--
  
* **Импорт requests:** библиотека для отправки HTTP-запросов.
Path из модуля pathlib: используется для работы с файлами и директориями.  
* **Класс APIRequester:**
Инициализирует объект с базовым URL-адресом (base_url), чтобы все запросы выполнялись относительно этого адреса.
Метод get() отправляет GET-запросы к указанному пути (tail_url) и возвращает ответ сервера. Если возникает ошибка, она обрабатывается через блок try/except.
* **Подкласс SWRequester:**
Этот класс наследуется от APIRequester. В нем реализованы дополнительные методы для работы со Star Wars API.
Метод get_sw_categories() запрашивает корневой путь API и извлекает доступные категории (например, "films", "people", "planets").
Метод get_sw_info() запрашивает конкретную категорию и возвращает её содержимое.  
* **Функция save_sw_data():**
Создается папка data для хранения файлов.
Для каждой категории выполняется запрос к API, результат сохраняется в отдельный текстовый файл в этой папке.
Таким образом, этот скрипт позволяет взаимодействовать с API Star Wars, получать информацию по категориям и сохранять эти данные в файлы.
