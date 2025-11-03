# Многослойный сервис «EnterpriseDataService» с использованием Spring Framework

Данный проект представляет собой многослойный сервис на основе Spring Framework, предназначенный для разработки надежных и масштабируемых корпоративных Java-приложений. Сервис реализует enterprise-уровень функциональности с акцентом на безопасность, управление транзакциями и отказоустойчивость.

## Установка 
1. Установить IntelliJ IDEA Ultimate с официального сайта: https://www.jetbrains.com/idea/download/
   В Community версии нет доступа к Framework Spring, поэтому надо установить Ultimate
2. Запустить файл .exe и следовать инструкциям мастера установки
3. Выбрать компоненты, жмем на все стрелочки 
4. Указать место установки
5. Создать ассоциации файлов 
6. Завершить установку — нажать «Install» и дождаться окончания процесса. По завершении можно выбрать опцию «Run IntelliJ IDEA» для немедленного запуска

## Запуск
1. Откройте проект в IntelliJ IDEA
2. Найдите файл DemoApplication.java
3. Нажмите зеленую кнопку "Run" рядом с методом main

## Примеры использования
1. Получение всех пользователей: curl -u user:password http://localhost:8080/api/users
2. Создание пользователя:

curl -u user:password -X POST http://localhost:8080/api/users \
  -H "Content-Type: application/json" \
  -d '{"name":"Иван Иванов", "email":"ivan@example.com"}'

3. Получение пользователя по ID: curl -u user:password http://localhost:8080/api/users/1
4. Удаление пользователя: curl -u user:password -X DELETE http://localhost:8080/api/users/1

## Структура репозитория 

enterprise-data-service/
│
├── src/
│   ├── main/
│   │   ├── java/com/example/demo/
│   │   │   ├── entity/           # Сущности базы данных (JPA entities)
│   │   │   │   └── User.java     # Модель пользователя
│   │   │   ├── repository/       # Слой доступа к данным (Spring Data JPA)
│   │   │   │   └── UserRepository.java # Репозиторий для работы с пользователями
│   │   │   ├── service/          # Бизнес-логика приложения
│   │   │   │   └── UserService.java # Сервис с транзакциями
│   │   │   ├── controller/       # REST API endpoints
│   │   │   │   └── UserController.java # Контроллер для управления пользователями
│   │   │   ├── config/           # Конфигурационные классы
│   │   │   │   └── SecurityConfig.java # Настройки безопасности Spring Security
│   │   │   └── DemoApplication.java # Главный класс приложения Spring Boot
│   │   └── resources/            # Ресурсы и конфигурации
│   │       ├── application.properties     # Основные настройки приложения
│   │       ├── application-dev.properties # Конфигурация для среды разработки
│   │       └── application-prod.properties # Конфигурация для продакшн среды
│   └── test/                     # Тесты приложения
│       └── java/com/example/demo/
│           ├── UserServiceTest.java    # Модульные тесты сервиса
│           └── UserControllerTest.java # Интеграционные тесты контроллера
│
├── data/                         # Директория для файлов базы данных H2
│   └── userdb.mv.db             # Файл базы данных H2 (создается автоматически)
│
├── target/                       # Собранные артефакты (генерируется при сборке)
├── .gitignore                    # Список файлов, игнорируемых Git
├── pom.xml                       # Конфигурация Maven и зависимости проекта
├── mvnw                          # Maven wrapper для Unix/Linux систем
├── mvnw.cmd                      # Maven wrapper для Windows систем
└── README.md                     # Документация проекта

## Технические требования

Язык программирования: Java 17

Фреймворки и библиотеки:
1. Spring Boot 3.0+
2. Spring Security
3. Spring Data JPA
4. H2 Database

Версии ПО:
1. Java: 17 или выше
2. Maven: 3.6+
3. Git: 2.20+

Операционные системы:
1. Windows 10/11
2. macOS 10.14+
3. Linux Ubuntu 18.04+

Минимальные системные требования:
1. Процессор: 2 ядра
2. Память: 2 GB RAM
3. Дисковое пространство: 100 MB

## Авторы, участники и их роли

Волохова Диана Андреевна - Full-stack Developer

1. Разработка архитектуры приложения
2. Реализация REST API и бизнес-логики
3. Настройка Spring Security и аутентификации
4. Конфигурация базы данных и транзакций
5. Написание тестов и документации
6. Настройка сборки Maven и развертывания

## Контактная информация

Email: volohovadiana685@gmail.com
