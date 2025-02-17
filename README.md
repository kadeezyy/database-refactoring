# Рефакторинг баз данных и приложений
Студент: Тороев Канатбек P34131

# Проект: OpenBook

# Описание проекта
Проект представляет собой сервис бронирования книг в городских библиотеках, которые находятся в базе данных.
Администраторы могут добавлять библиотеки, новые книги в каталог. 

## Сценарии использования:
- Регистрация и авторизация пользователей
- Добавление, изменение и удаление библиотеки из базы
- Поиск, бронирование и оформление книг в библиотеках пользователями

## Компоненты системы
* Backend-приложение на Kotlin с использованием Spring Boot, отвечающее за работу с каталогом книг (core-catalog)
  * Работает со связанной базой данных PostgreSQL
* Backend-приложение на Kotlin с использованием Spring Boot, отвечающее за авторизацию и регистрацию пользователей (gateway)
  * Работает со связанной базой данных PostgreSQL
* Backend-приложение на Kotlin с использованием Spring Boot, отвечающее за работу с бронированием книг в библиотеках (core-booking)
    * Работает со связанной базой данных PostgreSQL

# Этапы разработки проекта

## Этап 1: Анализ и планирование
На данном этапе фокусируемся на сборе и анализе требований, проектировании архитектуры системы и подготовке плана разработки.

План: 
1. Изучить сценарии использования, чтобы понять все необходимые функции и их взаимосвязи
2. Определить, как компоненты системы будут взаимодействовать друг с другом. Спроектировать REST API, описывающее основные взаимодействия
3. Подготовить окружение для разработки, выбрать необходимые библиотеки для Spring. Настроить PostgreSQL и средство осуществления миграций БД для использования в системе

## Этап 2: Разработка MVP
Создать минимальную рабочую версию системы, которая будет включать основные функции для проверки концепции. Сбор первоначальной обратной связи.
План:
1. Реализовать регистрацию и авторизацию пользователей
2. Реализовать функции добавления библиотек и книг в базу
3. Реализовать функции поиска и бронирования книг пользователями
4. Протестировать и отладить работу MVP. Провести тестирование всех функций и устраните обнаруженные баги.


## Этап 3: Сбор отзывов и улучшение MVP
На этом этапе улучшаем платформу на основании обратной связи пользователей и собранных данных.

План: 
1. Собрать обратную связь пользователей нашего проекта
2. Реализовать функционал просмотра истории бронирований пользователя
3. Повысить удобство использования сервиса посредством внедрения списков избранного


# Общая информация о процессе и технологиях
1. Контроль версий и совместная разработка будет вестись через текущий git-репозиторий
2. Миграции БД будем осуществлять с использованием Liquibase
3. Реализация UI в рамках выполнения проекта не предусмотрена, демо-записи и финальная демонстрация будет проводиться через платформу тестирования API (Bruno/Postman)


## План рефакторинга базы данных:
- Интеграция Liquibase плагина для миграций в проекте
- Внедрение liquibase-миграций sql-скриптов в приложение