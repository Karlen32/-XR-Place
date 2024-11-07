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
  
    
[Figma](https://clck.ru/3EQNom)

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

**1 месяц: реализация MVP, можно не полностью реализовать стили и эффекты и опустить второстепенный функционал.** 

## 1-я неделя:

**Задача 1**. Инициализация рабочего пространства
- создать репозиторий
- инициализировать структуру файлов и проект на nextjs
- настроить тесты (jest)
- установить и настроить инструментарий (eslint, prettier, stylelint, husky + lint-staged)
**Задача 2**. Подготовка базового кода (до получения макета, важно именование и расположение, содержание пока не важно)
- определить переменные окружения
- определить базовые константы в коде
- определить SCSS (и если надо CSS) переменные
- разметить структуру под будущий код, выделить фичи если работаем по FSD
  в ui-kit выделить как минимум типографику, формы, кнопки, базовые контейнеры
- в компоненты app, header, footer и layout
- в сервисы базовый API, если планируется работа с localStorage это тоже сюда, нельзя в компонентах напрямую работать с окружением для переиспользуемости кода
- если будем использовать глобальный менеджер состояний, то настраиваем и подключаем его, создаем в структуре требуемые под него файлы.
- 
💡 РЕВЬЮ: проверка базовой структуры проекта, тулсет настроен, сборка работает
  
**2-я и 3-я неделя, задачи выполняются параллельно по мере поступления требуемых вводных:**

**Задача 3**. Начинаем реализацию с UI-kit (уже должны быть вайрфреймы или черновик макета)
- создаем в структуре файлы под требуемые компоненты по макетам
- по мере готовности макета реализуем компоненты ui-kit, тестируем их и сверяемся с дизайнерами по реализации (могут быть правки)
- по готовности нужных компонентов в ui-kit начинаем накидывать компоненты (секции и блоки страниц), компонент начинаем только когда готовы все ui-kit элементы для него (не хардкодим! переиспользуем код)
- по готовности нужных компонент собираем страницы, данные мокаем через сервисы, где вместо запроса к API пока для отладки сразу возвращаем данные (Promise.resolve)
- Совет: Разделяйте отображение и бизнес логику (если проще: в одном компоненте верстка, в другом подключение к данным и обработчики событий, эффектов и т.д

**Задача 4**. Интеграция с сервером (требуется OpenAPI\Swagger контракт с бэкендом)

- начинать интеграцию нужно с авторизации если она есть
- обработку данных для соответствия требования фронтенда лучше проводить на уровне API-клиента, чтобы в компонент данные поступали уже в нужном виде.
- реализуем методы API по мере готовности на бекенде. Проверяем сначала в Postman и потом уже через код нашего API клиента. Можно автоматизировать через jest тестами.
  
💡 РЕВЬЮ: проверка базовой реализации, есть сторибук и в нем как минимум ui-kit, даже если еще нет интеграции, то данные не захардкожены, а вынесены в сервисы

## 4-я неделя:

**Задача 5**. Собираем все вместе
- Настраиваем сборку и деплой на сервер (деплоит бэк, мы даем исходные данные и по возможности создаем Dockerfile в своем репозитории)
- по мере говности API и страниц можно подключать данные к страницам. Подключение данных без глобального менеджера состояний делаем на уровне страницы,
  а с глобальным менеджером на уровне экшенов. Все методы работы с окружением также спускаем через пропсы.
- Финализируем внешний вид и функциональность приложения
- Пишем интеграционные тесты для проверки страниц в сборе (с моками)
- Фиксим ошибки по баг-репортам тестирования
  
💡 РЕВЬЮ: проверка опубликованного на сервере приложения

## 2-й месяц: Доработка, пред-релизная подготовка

**1-я и 2-я неделя:**

**Задача 6**. Доработка всей функциональности
- реализуем в том числе второстепенную функциональность не сделанную в первый месяц
- добиваем все стили и эффекты
- Производим локальный рефакторинг в требуемых компонентах и страницах если есть возможность уменьшить кодовую базу и более эффективно переиспользовать код
- оптимизируем производительность по необходимости, добавляем ленивую загрузку страниц, добавляем кэш на API запросы чтения, оптимизируем assets
- удаляем отладочный код и вывод в консоль (если нужно оставить в критических местах, можно скрыть через console.debug или обернуть в debug и выводить только при установленной в localStorage переменной)
- 
## 3-я и 4-я неделя: 

**Задача 7**. Тестируем, Фиксим, повторяем...

- Фиксим, доделываем
- Заполняем документацию: стэк, команда, инструкция по подготовке и запуску проекта, верхнеуровневая архитектура, ключевые компоненты,
  конфигурация (где лежат наши переменные, константы, как ключить логирование и т.д.), что сделано\что нет, известные проблемы или потенциальные места для рефакторинга и улучшения если известны.
- Тесты нужны хотя бы на уровне снэпшотов, чтобы понимать где что поменялось в случае изменения компонент.
- 
💡 РЕВЬЮ: финальное

# Финальное демо:

1. Собираемся, демонстрируем задеплоенное приложение, показываем работу основного функционала.
2. Объясняем какие решения применили (FSD, глобальный менеджер состояний, настройки тулсета, структура компонент) и почему
3. Рефлексия — что получилось, что не очень, какой опыт вынесли и насколько удалось освоиться с инструментарием и удержаться в рамках заданного процесса.
4. Что можно было бы улучшить, какие советы дали бы себе на старте с уже имеющимся опытом.

   
</details>

<details>
  <summary>Тест план</summary>
  
[Тест план](https://clck.ru/3EMcb9)

# Тест-план для UI/UX, кроссбраузерного и кроссплатформенного тестирования лендинга

## Цели тестирования
1. Проверить корректность отображения всех UI-элементов на разных браузерах (Chrome, Firefox, Safari) и разрешениях (Desktop 1920x1080, Tablet 768x1024, Mobile 360x640).
2. Убедиться в соответствии всех визуальных и интерактивных элементов макету, включая цвет, шрифты, расположение и стилизацию.
3. Проверить удобство использования (UX) на всех устройствах и браузерах, включая взаимодействие с кнопками и полями ввода.
4. Проверить адаптивность интерфейса и удобство взаимодействия с элементами на мобильных устройствах.

## Сценарии тестирования

### 1. Тестирование UI-элементов (вёрстка)
   - **Проверка фона**:
     - Градиент одинаково отображается на всех устройствах и браузерах.
   - **Проверка всех текстовых элементов**:
     - Заголовки, подзаголовки, обычные тексты имеют верный цвет, шрифт, и начертание.
     - Размер и расположение текста остаётся неизменным и адаптивным на всех устройствах.
   - **Проверка всех кнопок и полей ввода**:
     - Кнопки и поля отображаются корректно, соответствуют макету по цвету, размеру, тексту, и выравниванию.
     - На мобильных и планшетах кнопки адаптируются и остаются удобными для нажатия.
     - Проверка текста внутри полей ввода (плейсхолдеры) на правильность цвета и расположения.
   - **Проверка иконок социальных сетей и навигации**:
     - Кнопки для Instagram и LinkedIn имеют корректные иконки, отступы, и стиль (рамка и стрелка).
     - Пункты навигации отображаются в вертикальном порядке, с равномерными отступами, и легко кликабельны.

### 2. Проверка UX (удобства использования)
   - **Проверка кликабельности и доступности кнопок**:
     - Все кнопки и ссылки имеют корректные области нажатия, особенно на мобильных устройствах.
     - Кнопки социальных сетей и навигации легко нажимаются и открываются корректно.
   - **Адаптивность и визуальная иерархия**:
     - Проверка соответствия структуры и иерархии элементов на различных устройствах.
     - Заголовки и основные разделы видимы сразу и не перекрыты другими элементами.
   - **Проверка интерактивных элементов**:
     - При нажатии на кнопки и ссылки присутствует визуальная обратная связь, например, изменение цвета кнопок.
     - Взаимодействие с выпадающими элементами (например, вопросы в блоке FAQ и Преимущества) должно быть удобным на всех устройствах.

## Матрица тестирования

| Тест-кейс                        | Chrome (Desktop) | Firefox (Desktop) | Safari (Desktop) | iPad (Tablet) | Android (Tablet) | iOS (Mobile) | Android (Mobile) |
|----------------------------------|------------------|--------------------|------------------|---------------|------------------|--------------|------------------|
| Градиентный фон                  | ✅               | ✅                 | ✅               | ✅            | ✅               | ✅           | ✅               |
| Тексты и шрифты                  | ✅               | ✅                 | ✅               | ✅            | ✅               | ✅           | ✅               |
| Поля ввода и кнопки              | ✅               | ✅                 | ✅               | ✅            | ✅               | ✅           | ✅               |
| Иконки соцсетей                  | ✅               | ✅                 | ✅               | ✅            | ✅               | ✅           | ✅               |
| Удобство ввода и кликабельность  | ✅               | ✅                 | ✅               | ✅            | ✅               | ✅           | ✅               |
| Иерархия и видимость             | ✅               | ✅                 | ✅               | ✅            | ✅               | ✅           | ✅               |
| Визуальная обратная связь        | ✅               | ✅                 | ✅               | ✅            | ✅               | ✅           | ✅               |

> ✅ - Элемент отображается корректно  
> ❌ - Элемент отображается некорректно

## Критерии завершения тестирования
- Все элементы UI и UX на всех устройствах и браузерах соответствуют требованиям и макету.
- Любые визуальные отклонения исправлены, и элементы адаптированы под разные разрешения.
- UX элементов протестирован на удобство, и все интерактивные элементы работают корректно.

## Тестировщики
**Карлен Арабаджян**  
Telegram: [@Arabadzhyan](https://t.me/Arabadzhyan)

</details>

<details>
  <summary>Чек-лист десктоп</summary>

  [Десктоп](https://clck.ru/3EP3eB)

  # Чек-лист тестирования

| №   | Описание проверки                                                                 | Окружение 1 | Окружение 2 | Окружение 3 |
| --- | ---------------------------------------------------------------------------------- | ----------- | ----------- | ----------- |
| **Общие требования к блоку**                                                          | 1920x1080   | 1920x1080   | 1920x1080   |
| **Верхнее меню "Header" (логотип и навигация)**                                      | Firefox     | Chrome      | Safari      |
| t1  | Логотип расположен в левом верхнем углу и ведёт на главную страницу.              | Passed      | Passed      | Passed      |
| t2  | Цвет верхнего меню сливается с баннером. Цвет градиентный.                        | Passed      | Passed      | Passed      |
| t3  | При скролле фон верхнего меню (Header) черного цвета. Размер 48px/1690px           | Passed      | Passed      | Passed      |
| t4  | При скролле меню закреплено в верхней части экрана.                                | Passed      | Passed      | Passed      |
| t5  | Ссылки в верхнем меню, шрифт: Size 20px / Weight 400 / Color white                  | Passed      | Passed      | Passed      |
| t6  | Ссылки меню выровнены по центру верхней панели. По вертикали.                      | Passed      | Passed      | Passed      |
| t7  | При нажатии ссылки в меню, ведут к нужным секциям, соответствующим их названиям.   | Passed      | Passed      | Passed      |
| t8  | Шрифт текста в меню Size 20px / Weight 400 / Color White                           | Passed      | Passed      | Passed      |
| t9  | Кнопка смены языка выравнивание по правому краю меню                               | Passed      | Passed      | Passed      |
| t10 | Кнопка смены языка с острыми углами, выровнена по правой стороне. Цвет рамки и текста кнопки: "White" | Passed      | Passed      | Passed      |
| t11 | При нажатии на кнопку есть возможность выбрать язык "Ru" или "En"                  | Passed      | Passed      | Passed      |
| t12 | По умолчанию отображается язык "Ru"                                                | Passed      | Passed      | Passed      |
| t13 | После выбора языка "En" все детали отображаются корректно и не наезжают друг на друга | Skipped     | Skipped     | Skipped     |
| **Первый экран (баннер)**                                                           |             |             |             |
| t14 | Фон первого экрана — градиентный с плавным переходом из одного цвета в другой.    | Passed      | Passed      | Passed      |
| t15 | Заголовок "НОВЫЙ УРОВЕНЬ ВИЗУАЛИЗАЦИИ НЕДВИЖИМОСТИ" выровнен по левой стороне баннера. | Passed      | Passed      | Passed      |
| t16 | Шрифт заголовка Size 200px / Weight 700 / Color White                              | Passed      | Passed      | Passed      |
| t17 | Под заголовком текст "Увеличьте продажи, используя передовые 3D-технологии для сайтов строительных компаний". | Passed      | Passed      | Passed      |
| t18 | Шрифт текста : size 32px / Weight 400 / Color White                                | Passed      | Passed      | Passed      |
| t19 | Кнопка "Оставить заявку" расположена под текстом, выровнена по левому краю.       | Passed      | Passed      | Passed      |
| t20 | Кнопка прозрачная, текст на кнопке: size 32px / Weight 400 / Color White           | Passed      | Passed      | Passed      |
| t21 | При наведении на кнопку цвет кнопки получает оттенок white 10% .                   | Passed      | Passed      | Passed      |
| t22 | При нажатии на кнопку цвет кнопки получает оттенок white 20%                       | Passed      | Passed      | Passed      |
| t23 | Нажатие на кнопку "Оставить заявку" переводит на секцию «Обсудим?».               | Passed      | Passed      | Passed      |
| t24 | Справа от Заголовка отображается изображение смартфона с 3D-визуализацией.         | Passed      | Passed      | Passed      |
| t25 | Размер изображения смартфона 390px*799px                                           | Passed      | Passed      | Passed      |
| **Блок с процентами**                                                               |             |             |             |
| t26 | Блок с процентами состоит из трёх отдельных карточек, расположенных в ряд.        | Passed      | Passed      | Passed      |
| t27 | Карточки прозрачные с белой контурной линией, углы острые.                         | Passed      | Passed      | Passed      |
| t28 | Каждая карточка имеет отступы и равномерно распределена по горизонтали.          | Passed      | Passed      | Passed      |
| t29 | Карточка слева содержит текст "15%" - шрифт Size 200px / Weight 700 / Color White  | Passed      | Passed      | Passed      |
| t30 | Ниже на карточке расположен текст "Увеличение количества продаж квартир" шрифт: size 32px / Weight 400 / Color White | Passed      | Passed      | Passed      |
| t31 | Средняя карточка содержит текст "20%"- Size 200px / Weight 700 / Color White       | Failed      | Failed      | Failed      |
| t32 | Ниже на карточке текст "Увеличение количества целевых заявок" шрифт: size 32px / Weight 400 / Color White | Passed      | Passed      | Passed      |
| t33 | Правая карточка — "60%" - Size 200px / Weight 700 / Color White                    | Passed      | Passed      | Passed      |
| t34 | Ниже на карточке текст  "Увеличение проведения времени на сайте" шрифт size 32px / Weight 400 / Color White | Passed      | Passed      | Passed      |
| **Блок "3D-виджет"**                                                                |             |             |             |
| t35 | Заголовок "3D-виджет" расположен над изображениями. Выравнивание по левому краю, шрифт: Size 200px / Weight 700 / Color White | Passed      | Passed      | Passed      |
| t36 | Под заголовком три изображения, выстроенные в один ряд. Изображения расположены равномерно, между ними установлены одинаковые отступы. | Passed      | Passed      | Passed      |
| t37 | При наведении курсора на изображение изображение увеличивается появляется надпись | Passed      | Passed      | Passed      |
| t38 | При увеличении одного изображения два других уменьшаются в размере, сохраняя свое первоначальное расположение. | Passed      | Passed      | Passed      |
| t39 | Надпись первого изображения "Локация вокруг здания с любой стороны"              | Passed      | Passed      | Passed      |
| t40 | Надпись второго изображения "Наглядная планировка и интерьер"                     | Passed      | Passed      | Passed      |
| t41 | Надпись третьего изображения "Геймификация и свобода перемещения"                 | Passed      | Passed      | Passed      |
| t42 | Под изображениями большой "Iframe блок" 3D-моделью размер: Width 1599px / Height 872px | Passed      | Passed      | Passed      |
| t43 | На большом "Iframe блок" отображаются 4 кнопки на "3-D модели"                     | Failed      | Failed      | Failed      |
| t44 | Слева в нижней части горизонтально расположены три кнопки: Круглые, фон белый,иконки черные. | Passed      | Passed      | Passed      |
| t45 | Первая кнопка "Локация вокруг здания с любой стороны" выравнивание по левому краю | Passed      | Passed      | Passed      |
| t46 | Кнопка кликабельна и соответствует описанию. Она отображает локации вокруг здания с любой стороны. | Passed      | Passed      | Passed      |
| t47 | Вторая кнопка "Наглядная планировка и интерьер" выравнивание справа от кнопки "Локация вокруг здания с любой стороны" | Passed      | Passed      | Passed      |
| t48 | Кнопка кликабельна и соответствует описанию. Она отображает наглядную планировку и интерьер. | Passed      | Passed      | Passed      |
| t49 | Третья кнопка «Геймификация и свобода перемещения» выровнена справа от предыдущей кнопки. | Passed      | Passed      | Passed      |
| t50 | Кнопка кликабельна и соответствует описанию. Она позволяет Геймификацию и свободное перемещения по модулю | Passed      | Passed      | Passed      |
| t51 | С правом нижнем углу "Iframe блока" кнопка просмотра во весь экран. | Passed | Passed | Passed |
| t52 | Кнопка контрастная, не имеет формы. | Passed | Passed | Passed |
| t53 | Кнопка кликабельна, и при нажатии блок открывается на весь экран. | Passed | Passed | Passed |
| t54 | При повторном клике возврат просмотра блока на лендинге. | Passed | Passed | Passed |
| t55 | Из полноэкранного режима можно выйти по кнопке ESC. | Passed | Passed | Passed |
## Блок "Примеры работ"

| №   | Описание проверки | Общие требования к блоку | Окружение 1 (Firefox) | Окружение 2 (Chrome) | Окружение 3 (Safari) |
| --- | ----------------- | ------------------------ | --------------------- | -------------------- | -------------------- |
| t56  | Заголовок "Примеры работ" выровнен по левому краю. Шрифт: Size 200px / Weight 700 / Color White. | Passed | Passed | Passed |
| t57  | Справа от заголовка - стрелки прокрутки для перемещения между видеороликами. | Passed | Passed | Passed |
| t58  | Под заголовком расположены три видеоролика с примерами работ выстроенные в один ряд по горизонтали | Passed | Passed | Passed |
| t59  | Название видео ролика сверху видео выравнивание по левому краю | Passed | Passed | Passed |
| t60  | Название первого видеоролика "Дом в стиле минимализм" | Passed | Passed | Passed |
| t61  | Название второго видеоролика "Загородный лофт" | Passed | Passed | Passed |
| t62  | Название третьего видеоролика "Дом у моря" | Passed | Passed | Passed |
| t63  | Между видеороликами равномерные отступы: 40px | Passed | Passed | Passed |
| t64  | В центре каждого видеоролика расположена кнопка воспроизведения | Passed | Passed | Passed |
| t65  | При проигрывании в нижнем крае видеоролика отображается полоса прогресса и панель управления. Полосы работают корректно | Failed | Failed | Failed |

## Блок "Преимущества"

| №   | Описание проверки | Общие требования к блоку | Окружение 1 (Firefox) | Окружение 2 (Chrome) | Окружение 3 (Safari) |
| --- | ----------------- | ------------------------ | --------------------- | -------------------- | -------------------- |
| t66  | Заголовок "Преимущества" расположен над карточками, выровнен по левому краю. Size 200px / Weight 700 / Color White. | Passed | Passed | Passed |
| t67  | Под заголовком размещены четыре карточки преимуществ, выстроенные в два ряда и две колонки. | Passed | Passed | Passed |
| t68  | При наведении курсора карточки переворачиваются, и на обратной стороне отображается подробное описание данного преимущества. | Passed | Skipped | Passed |
| t69  | Первая карточка на лицевой стороне содержит текст "Повышение продаж на стадии строительство" и номер "01" | Passed | Passed | Passed |
| t70  | На обратной стороне текст: "Покупатели увидят полную копию объекта недвижимости, даже если он ещё на стадии строительства или расположен в другой стране, что увеличит конверсию продаж" | Failed | Failed | Failed |
| t71  | Вторая карточка на лицевой стороне содержит текст "Инвестиции в ваш цифровой бренд" и номер "02" | Passed | Passed | Passed |
| t72  | На обратной стороне текст: "Уникальный пользовательский опыт выделит вас среди конкурентов и улучшит ваш инновационный имидж, а интерактивная 3D-модель повысит доверие и вовлеченность клиентов" | Passed | Passed | Passed |
| t73  | Третья карточка на лицевой стороне содержит текст "Экономия на едином пакете визуализации" и номер "03" | Passed | Passed | Passed |
| t74  | На обратной стороне текст: "Единая 3D-модель позволяет нам создавать дополнительные виды 2D и 3D-визуализаций без двойной работы, а виджет легко встраивается в любое место на вашем сайте" | Failed | Failed | Failed |
| t75  | Четвертая карточка на лицевой стороне содержит текст "Доступность с любого устройства" и номер "04" | Passed | Passed | Passed |
| t76  | На обратной стороне текст: "Ваши клиенты смогут легко просматривать 3D-модели на компьютерах, планшетах, смартфонах в VR-очках, что обеспечит доступ к вашему продукту в любое время и из любого места" | Passed | Passed | Passed |
| t77  | На карточках с лицевой стороны шрифт текста : size 40px / Weight 400 / Color White. | Passed | Passed | Passed |
| t78  | В правом верхнем углу карточек есть значок в виде круговой стрелки | Passed | Passed | Passed |
| t79  | На обратной стороне карточки шрифт текста: size 24px / Weight 400 / Color White | Passed | Passed | Passed |
| t80  | Карточки имеют ровномерные отступы между собой. | Passed | Passed | Passed |

## Блок "Этапы работы"

| №   | Описание проверки | Общие требования к блоку | Окружение 1 (Firefox) | Окружение 2 (Chrome) | Окружение 3 (Safari) |
| --- | ----------------- | ------------------------ | --------------------- | -------------------- | -------------------- |
| t81  | Заголовок "Этапы работы" расположен по левой стороне блока. Size 200px / Weight 700 / Color White. | Passed | Passed | Passed |
| t82  | Блок градиентный с плавным переходом из одного цвета в другой. | Passed | Passed | Passed |
| t83  | Под заголовком три этапа работы, каждый из которых содержит номер, заголовок и описание. | Passed | Passed | Passed |
| t84  | Первый этап заголовок "Знакомство" — номер "01", шрифт:size 40px / Weight 400 / Color White. | Passed | Passed | Passed |
| t85  | Под заголовком описание с текстом: "Обсуждаем ваши цели и требования, анализируем аудиторию и архитектурные планы, чтобы лучше понять задачи." шрифт: size 24px / Weight 400 / Color White. | Passed | Passed | Passed |
| t86  | Второй этап заголовок "Старт работ" — номер "02", Size 40px / Weight 400 / Color White. | Passed | Passed | Passed |
| t87  | Под вторым заголовком описание с текстом: "Создаём концепцию 3D-виджета и интерактивный дизайн, согласуем все детали с вами и вносим необходимые правки." шрифт:size 24px / Weight 400 / Color White. | Passed | Passed | Passed |
| t88  | Третий этап "Процесс" — номер "03",шрифт: size 40px / Weight 400 / Color White | Passed | Passed | Passed |
| t89  | Под третьим заголовком описание с текстом: "Разрабатываем 3D-виджет с регулярными обновлениями для вас, проводим тестирование с учётом ваших пожеланий." шрифт:size 24px / Weight 400 / Color White | Passed | Passed | Passed |
| t90  | Блок "Этапы работы" можно двигать влево-вправо | Failed | Passed | Failed |

## Блок "FAQ"

| №   | Описание проверки | Общие требования к блоку | Окружение 1 (Firefox) | Окружение 2 (Chrome) | Окружение 3 (Safari) |
| --- | ----------------- | ------------------------ | --------------------- | -------------------- | -------------------- |
| t91  | Заголовок "FAQ" выровнен по левой стороне. Шрифт: Size 200px / Weight 700 / Color White. | Passed | Passed | Passed |
| t92  | Под заголовком по правой стороне текст: "Здесь вы сможете найти ответы на общие и часто задаваемые вопросы" шрифт: size 24px / Weight 400 / Color White | Failed | Failed | Failed |
| t93  | Блок под текстом содержит шесть карточек с вопросами, расположенных в три столбца по две карточки. | Passed | Passed | Passed |
| t94  | Карточки с вопросами прозрачные с белой контурной линией | Passed | Passed | Passed |
| t95  | Вопросы внутри карточек выравнивание по центру, шрифт: size 24px / Weight 400 / Color White. | Passed | Passed | Passed |
| t96  | По правому углу карточек «диагональная стрелка вниз влево» color white | Passed | Passed | Passed |
| t97  | При клике на карточку ответ отображается под вопросом, текст в ответе шрифт: size 24px / Weight 400 / Color White. | Passed | Passed | Passed |
| t98  | Расположение карточек остаётся двухрядным на больших экранах, с равномерными отступами между ними. | Passed | Passed |
  </details>

  <details>
  <summary>Чек-лист (планшет, мобилка)</summary>

  [Чек-лист (планшет, мобилка)](https://clck.ru/3EP3fu)
    </details>

  <details>
    <summary>Валидация полей</summary>

  [Валидация полей](https://clck.ru/3EPzYt)
    </details>

  <details>
  <summary>Особенности мобилки</summary>
  [Особенности мобилки](https://clck.ru/3EP3n8)
    </details>



  

  
