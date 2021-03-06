# css & html ПОДСКАЗКИ

## Базовые критерии верстки
- У всех изображений в теге **&lt;img&gt;** прописан размер.
- Использовано минимально возможное количество HTML-элементов (нет лишних элементов).
- Для стилизации не использованы #id.
- Нет вложенности селекторов больше двух.
- Отсутствует транслит в названиях классов, атрибутах и так далее.
- Явно указано подходящее vertical-align для потоковых блоков с display: inline-block.
- Вёрстка проходит тест на переполнение контентом.
- Явно указано подходящее vertical-align для потоковых блоков с display: inline-block.
- Для блока, у которого есть фоновое изображение, прописан фоновый цвет, который соответствует преобладающему цвету изображения (пока изображение не загружено, страница выглядит похоже на макет).
- В разметке есть правильный вьюпорт тег.

## Советы по верстке
- Старайтесь не использовать одновременно **width** и **height**, если это не декоративный элемент с фиксированными размерами.
- Старайтесь не задавать фиксированную
высоту.
- Если всё-таки нужна высота, то лучше
использовать min-height.
- Как бороться с **выпаданием**?
    - Родительскому блоку можно задать одно
из следующих свойств:
    - overflow : hidden; /* использовать осторожно */
    - padding-top : 1px; /* или */<br>
padding-bottom : 1px;
    - border-top : 1px solid transparent; /* или */<br>
border-bottom : 1px solid transparent;
- Как предотвратить **выпадение float** элементов?
    - Приём «распорка»: использовать свойство **clear: both** у элемента, расположенного после плавающих.
    - Приём «псевдораспорка»: контейнеру, содержащему флоаты, добавляются псевдоэлемент с clear: both.
      ```css
      .row::after {
        content: "";
        display: table;
        clear: both;
      }
      ```
- Построение сеток на флексбоксах (bas.lec.5)
    - Всегда явно задавайте размер колонок: width или flex-basis.
    - Расстояния между колонок можно задавать:
        - с помощью justufy-content, если отступы одинаковые;
        - с помощью margin, если отступы разные.
    - Если количество колонок может изменяться (карточный интерфейс), то margin предпочтительнее.
    - Следите за псевдоэлементами у флекс-контейнера.
    - flex-grow не подходит, если нужно добиться точного соответствия макету.
- Позиционирование
    - Гибкий механизм расположения элементов.
    - Не используется для создания сеток.
    - Используется для создания декоративных эффектов и многослойных элементов интерфейса.
- Нормализация стилей
    - Если хочется нормализовать стили, то можно использовать normalize.css.
    - http://necolas.github.io/normalize.css/
    - https://htmlacademy.ru/blog/64
- 

## Photoshop
- Все состояния элементов (styleguide.psd) прописаны в стилевом файле.

## Подборки
- Выбор брейкпоинтов: по макету (pro.lec.4.79)
- Вьюпорты (pro.lec.4.88)
