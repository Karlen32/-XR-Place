# Проект XR Place

Компания XR Place (https://xrplace.io/ru) создаёт real-time 3D модели квартир и домов для сайтов застройщиков,
позволяя пользователям свободно исследовать планировки и окружение недвижимости прямо в браузере.
Наш продукт увеличивает продажи и доверие покупателей, особенно для объектов, которые ещё не построены.


![image](https://github.com/user-attachments/assets/06d7202b-ca03-4f88-9740-06dd75e46b7c)

<details>
  <summary>Цель проекта</summary>

  Цель проекта — создать сайт, который демонстрирует возможности и преимущества 3D визуализации, 
  направленный на привлечение девелоперов и агентств недвижимости. Дизайн должен быть современным, 
  с акцентом на интерактивность и SEO-оптимизацию. Важно также включить видео и интерактивные 
  демо для полного погружения пользователей.
</details>

<details>
  <summary>Макеты</summary>
  
    
https://clck.ru/3EQNom

![image](https://github.com/user-attachments/assets/c5ee2153-3d43-4654-8259-8a8c5a96f140)

</details>

<details>
  <summary>ТЕХНИЧЕСКОЕ ЗАДАНИЕ</summary>

  # Описание проекта
  
Мы создаём real-time 3D квартиры и дома для сайтов застройщиков - это похоже на web игру, где мы показываем планировку и локацию вокруг будущей недвижимости. 
Это особенно актуально для покупателей из других городов, а также для объектов недвижимости, которые ещё не построены.
Создать сайт, где будет понятно, что за продукт мы делаем, и показать его преимущества. В первую очередь сайт нужен, чтобы направить туда партнеров, 
с кем мы ведем переговоры напрямую. Трафик лить пока не планируем, но это тоже в будущем возможно.
Работающий сайт https://xrplace.io/ 

# Стек 

NextJS: Основной фреймворк для создания интерфейса. 
TypeScript: Статически типизированный язык программирования
SASS (SCSS): Препроцессор CSS для создания модульных, многоразовых стилей, облегчая поддержку и структурирование стилей приложения.
Можно использовать  Tailwind.
 TanStack Query или встроенные механизмы nextjs для отправки запросов.

# Результат

Репозиторий на гитхабе должен содержать:
воспроизводимый код проекта
описание и инструкция по запуску в файле README.md

# Требования к окружению

Node.js (рекомендуется v18.x.x и выше)
npm (рекомендуется v7.x.x и выше)

# Требования к инфраструктуре

Инфраструктура nextjs.
Настроенный линтинг eslint, prettier, editorconfig
Автоформатирование и проверка линтера при коммите с помощью husky
Commitizen для структурированных коммитов

# Организация работы в репозитории:

— ветка main главная, в нее нельзя напрямую коммитить, только через пулл-реквест после проверки наставником
— ветка develop, основная рабочая где собираете код, сюда сливаются через пулл-реквесты выполненные фиксы и фичи, проверяется тимлидами или другими участниками команды на кросс-ревью
— ветки fix/* feat/* chore/* для работы над задачами, соответственно исправления, новые фичи, задачи не связанные с изменением основного кода (сборка, тулсет, документация, тесты и т.д.).



# Функциональные требования 

Сайт во многом визиточный, но точно нужно оставить место под call to action - заполнить форму на демо.
Кроме этого должно быть место под i-frame с нашим виджетом и его видео вариантом (как мне сейчас представляется)

По разделам можно отталкиваться от текущей версии сайта, сейчас у нас так:
Слоган - главное преимущество - видео версия нашего продукта
Ключевые фичи (вид из окна, интерактивность, свобода перемещения)
Сам 3D виджет в работе

Преимущества
Доступность с любого устройства
Форма заявки на демо, чтобы узнать стоимость
Контакты
Подвал
Политика обработки данных и cookies

## Поддержка мультиязычности  

Нужна поддержка переключения языка для контента (в nextjs есть механизмы)

## Анимации и интерактивность

Для анимаций и интерактивности использовать библиотеки GSAP (для скрола и появления) или Three.js для создания вау эффекта, но при этом сильно не перегружать сайт анимациями.

# План работ:

1 месяц: реализация MVP, можно не полностью реализовать стили и эффекты и опустить второстепенный функционал.

## 1-я неделя:

Задача 1. Инициализация рабочего пространства
создать репозиторий
инициализировать структуру файлов и проект на nextjs
настроить тесты (jest)
установить и настроить инструментарий (eslint, prettier, stylelint, husky + lint-staged)
Задача 2. Подготовка базового кода (до получения макета, важно именование и расположение, содержание пока не важно)
определить переменные окружения
определить базовые константы в коде
определить SCSS (и если надо CSS) переменные
разметить структуру под будущий код, выделить фичи если работаем по FSD
в ui-kit выделить как минимум типографику, формы, кнопки, базовые контейнеры
в компоненты app, header, footer и layout
в сервисы базовый API, если планируется работа с localStorage это тоже сюда, нельзя в компонентах напрямую работать с окружением для переиспользуемости кода
если будем использовать глобальный менеджер состояний, то настраиваем и подключаем его, создаем в структуре требуемые под него файлы.
💡 РЕВЬЮ: проверка базовой структуры проекта, тулсет настроен, сборка работает
2-я и 3-я неделя, задачи выполняются параллельно по мере поступления требуемых вводных:
Задача 3. Начинаем реализацию с UI-kit (уже должны быть вайрфреймы или черновик макета)
создаем в структуре файлы под требуемые компоненты по макетам
по мере готовности макета реализуем компоненты ui-kit, тестируем их и сверяемся с дизайнерами по реализации (могут быть правки)
по готовности нужных компонентов в ui-kit начинаем накидывать компоненты (секции и блоки страниц), компонент начинаем только когда готовы все ui-kit элементы для него (не хардкодим! переиспользуем код)
по готовности нужных компонент собираем страницы, данные мокаем через сервисы, где вместо запроса к API пока для отладки сразу возвращаем данные (Promise.resolve)
Совет: Разделяйте отображение и бизнес логику (если проще: в одном компоненте верстка, в другом подключение к данным и обработчики событий, эффектов и т.д.)
Задача 4. Интеграция с сервером (требуется OpenAPI\Swagger контракт с бэкендом)
начинать интеграцию нужно с авторизации если она есть
обработку данных для соответствия требования фронтенда лучше проводить на уровне API-клиента, чтобы в компонент данные поступали уже в нужном виде.
реализуем методы API по мере готовности на бекенде. Проверяем сначала в Postman и потом уже через код нашего API клиента. Можно автоматизировать через jest тестами.
💡 РЕВЬЮ: проверка базовой реализации, есть сторибук и в нем как минимум ui-kit, даже если еще нет интеграции, то данные не захардкожены, а вынесены в сервисы

4-я неделя:
Задача 5. Собираем все вместе
Настраиваем сборку и деплой на сервер (деплоит бэк, мы даем исходные данные и по возможности создаем Dockerfile в своем репозитории)
по мере готовности API и страниц можно подключать данные к страницам. Подключение данных без глобального менеджера состояний делаем на уровне страницы, а с глобальным менеджером на уровне экшенов. Все методы работы с окружением также спускаем через пропсы.
Финализируем внешний вид и функциональность приложения
Пишем интеграционные тесты для проверки страниц в сборе (с моками)
Фиксим ошибки по баг-репортам тестирования
💡 РЕВЬЮ: проверка опубликованного на сервере приложения
2-й месяц: Доработка, пред-релизная подготовка
1-я и 2-я неделя:
Задача 6. Доработка всей функциональности
реализуем в том числе второстепенную функциональность не сделанную в первый месяц
добиваем все стили и эффекты
Производим локальный рефакторинг в требуемых компонентах и страницах если есть возможность уменьшить кодовую базу и более эффективно переиспользовать код
оптимизируем производительность по необходимости, добавляем ленивую загрузку страниц, добавляем кэш на API запросы чтения, оптимизируем assets
удаляем отладочный код и вывод в консоль (если нужно оставить в критических местах, можно скрыть через console.debug или обернуть в debug и выводить только при установленной в localStorage переменной)
3-я и 4-я неделя:
Задача 7. Тестируем, Фиксим, повторяем...
Фиксим, доделываем
Заполняем документацию: стэк, команда, инструкция по подготовке и запуску проекта, верхнеуровневая архитектура, ключевые компоненты, конфигурация (где лежат наши переменные, константы, как ключить логирование и т.д.), что сделано\что нет, известные проблемы или потенциальные места для рефакторинга и улучшения если известны.
Тесты нужны хотя бы на уровне снэпшотов, чтобы понимать где что поменялось в случае изменения компонент.
💡 РЕВЬЮ: финальное
Финальное демо:
Собираемся, демонстрируем задеплоенное приложение, показываем работу основного функционала.
Объясняем какие решения применили (FSD, глобальный менеджер состояний, настройки тулсета, структура компонент) и почему
Рефлексия — что получилось, что не очень, какой опыт вынесли и насколько удалось освоиться с инструментарием и удержаться в рамках заданного процесса.
Что можно было бы улучшить, какие советы дали бы себе на старте с уже имеющимся опытом.
</details>
