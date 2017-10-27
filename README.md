# Автотесты для раздела "Edit Issue" GutHub API.

Структура проекта:
-   Файл ```users_imfromation.py``` содержит имя владельца и название репозитория,
    а также данные для входа в аккаунты GitHub
-   Файл ```json_editor.py``` предназначен для кодирования контента задачи в формат
    JSON, а также для быстрого доступа к значениям полей JSON
-   Файл ```issue_editor.py``` содержит реализация POST, PUT, DELETE запросов к GutHub API
-   Файл ```github-api-tests.py``` содержит описание и реализацию автотестов

От каких тестов пришлось отказаться:
-   От тестов, проверяющих правильность заполнения различных текстовых полей задачи 
    (так как они все относятся к одному классу эквивалентности - редактирование задачи корректными данными)
-   От детализации тестов, проверяющих возникновение ошибки при редактировании задачи JSON-ом, 
    у которого одно или несколько полей имеют некорректный тип (один класс эквивалентности - 
    редактирование задачи с сипользованием некорректных данных)
-   От тестов на проверку граничных значений, так как такого рода тесты, по моему мнению,
    ближе к модулю создания задачи, а не редактирования.