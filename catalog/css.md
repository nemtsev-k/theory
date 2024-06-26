# CSS

**CSS** (Cascading Style Sheets — Каскадные таблицы стилей) — это язык таблиц стилей для описания представления документов, написанных на языке разметки, таком как HTML или XML (включая диалекты XML, такие как SVG, MathML или XHTML).

CSS является краеугольной технологией Всемирной паутины, наряду с HTML и JavaScript. Первая окончательная спецификация CSS была опубликована в 1996 году Хоконом Виум Ли и Бертом Босом.

Типичный стилевой файл состоит из списка CSS-правил, идущих друг за другом. CSS-правило состоит из селектора и перечня свойств и значений.

## Селекторы

**Селектор** - первая часть CSS-правила. Он определяет, к какому HTML-тегу или к какому множеству HTML-тегов применится набор свойств этого CSS-правила.

**Типы селекторов:**

* Селектор по имени тега: main { }
* Селектор по классу: .main { }
* Селектор по идентификатору: #main { }
* Комбинированные селекторы
  * Группировка: .element1, .element2 { }
  * Объединение: .class1.class2 { }
  * Потомки .element1 .element2 { }
  * Непосредственно вложенные: .element1 > .element2 { }
  * Смежные: .element1 + .element2 { }
  * Последующие: .element1 ~ .element2 { }

## Псевдоклассы

**Псевдоклассы** — необходимы для усиления селекторов.

Есть псевдоклассы, которые помогают выбирать элементы с учётом их расположения относительно других элементов. Например, можно выбрать последний или первый элемент, каждый второй или каждый третий элемент и так далее.

Ещё есть псевдоклассы, которые добавляют возможность реагировать на состояния элементов. Например, было обычное поле ввода, потом на него навели мышкой и оно изменилось, затем в него поставили курсор, и это поле ещё как-то изменилось.

И ещё есть специальные псевдоклассы, которые добавляют возможность реагировать на состояние элементов форм. Например, можно выбрать все обязательные или, наоборот, необязательные поля формы.

ПРИВЕСТИ примеры...

## Псевдоэлементы

**Псевдоэлементы** — это элементы, которых не существует в HTML-разметке. Они создаются и позиционируются исключительно при помощи CSS. Чаще всего используются для создания различных декоративных элементов (которые не несут содержательного смысла). Примеры 
* ::before — располагается перед содержимым элемента.
* ::after — располагается после содержимым элемента.
* ::first-letter — выбор первой буквы в строке или абзаце текста (буквица).
* ::first-line — выбор первой строки текста.
* ::selection — управление стиля текста, который пользователь выделяет при помощи мыши.
* ::placeholder — стилизация подсказки, которая выводится в поле ввода текста
* ::marker — псевдоэлемент, отвечающий за маркерное поле.

**Свойства**
Вторая часть CSS-правила — это перечень свойств и их значений внутри фигурных скобок. Свойство и значение разделяются двоеточием, а пары свойств-значений разделяются точкой с запятой.

**Каскадность** — позволяет разбивать код стилей на маленькие кусочки, а потом комбинировать их. Причем комбинирование делают намеренно, специально задавая тегу несколько классов. В простейшем случае, когда у конфликтующих CSS-правил однотипные селекторы, выигрывает то правило, которое находится ниже в коде.

**Специфичность** — определяет, какое количество элементов потенциально может выбрать селектор. Чем больше элементов может выбрать селектор, тем меньше специфичность. Чем меньше элементов может выбрать селектор, тем специфичность выше. Браузер определяет, у какого CSS-правила селектор специфичнее и это CSS-правило побеждает.

**Кастомные свойства** — ...

вложенные запросы

## CSS-in-JS

## CSS Modules

## Анимация

## Адаптивность

**Медиазапросы** — позволяют назначать страницам стили на основе размера окна браузера.

**Подходы:**

* Desktop first – предпочтение компьютерам.
* Mobile first – предпочтение смартфонам.

##Сетка

**Сетка** (раскладка) — это взаимное расположение крупных визуальных блоков на странице. Фактически вёрстка сетки сайта подразумевает выстраивание порядка и расположения этих прямоугольников друг относительно друга, а также относительно границ экрана. К сетке относят самые крупные области макета, примерно до 3 уровня вложенности.

**Микросетки** — это сетки, к которым относят более мелкие блоки, такие как карточки товаров, номера страниц в переключателе, пункты меню, ссылки на страницы социальных сетей и так далее.

**Признаки, по которым можно отличить сетки от микросеток**

* **Постоянное или переменное количество элементов.** В крупной сетке количество элементов не меняется. Например, если в шапке предусмотрено две колонки, то это количество не изменится никогда. В микросетке же, наоборот, количество элементов может легко меняться. К примеру, пунктов меню может стать как больше, так и меньше. Эти изменения делаются за пару минут любым контент-менеджером в админке сайта.
* **Независимость или зависимость размера элементов от содержания.** Размер элементов в крупной сетке не зависит от содержания, а задаётся согласно макету. Например, ширина колонок всегда берётся из макета и принимается как данность. Дизайнер подбирает эту ширину так, чтобы в колонку помещалось, к примеру, три товара. Но вне зависимости от того, сколько в итоге товаров будет на странице, один или десять, ширина колонки останется постоянной. Размер элементов в микросетке наоборот, чаще всего, зависит от содержания. Например, ширина пунктов меню зависит от конкретного текста каждого пункта. Но при этом иногда ширина может быть фиксированной, например, у карточек товаров.

**Поток документа** — определяет, как именно элементы отрисовываются на веб-странице и как этот порядок отрисовки соотносится с HTML-кодом. Все элементы расположены ровно в том же порядке, в котором они были в коде.

**Для управления потоком в нашем распоряжении есть две группы CSS-свойств:**

1. группа, изменяющая поведение элементов в потоке: display, float.
2. группа, изменяющая размеры самих элементов: width, height, margin, padding, border, box-sizing.

### Flex

**CSS Flex Layout** — это технология для раскладки элементов на веб-страницах. Основная идея флексов — гибкое распределение места между элементами, гибкая расстановка, выравнивание, гибкое управление. Flex — англ. гибко.

Флексами удобно делать или колонки, или ряды элементов. При этом флексбокс позволяет управлять шириной каждой колонки и отступами между ними. Но одновременно двумя направлениями во флексбоксе управлять сложно.

[Подробнее](https://doka.guide/css/flexbox-guide/)

### Grid

**CSS Grid Layout** — это технология для раскладки элементов на веб-страницах. Гриды дают возможность работать одновременно с двумя измерениями: горизонталью и вертикалью. Grid — англ. сетка.

Принцип работы гридов чем-то похож на таблицы. Вместо работы только с рядами или только с колонками с помощью гридов можно работать с так называемыми грид-ячейками, позиционируя элементы по вертикали и горизонтали одновременно.

[Подробнее](https://doka.guide/css/grid-guide/)

#### auto-fill и auto-fit

В тех случаях, когда количество колонок или строк не известно для свойств **grid-template-columns** и **grid-template-rows** можно установить значения auto-fill или auto-fit. Оба эти параметра автоматически добавляют в грид-сетку из примера выше колонки. Но эти колонки ведут себя немного по-разному.

**auto-fill** - позволяет контенту растягиваться для заполнения всей ширины строки.

**auto-fit** - позволяет пустым колонкам занимать место в строке наравне со своими непустыми соседями. Для них будет отведено место даже, если внутри них нет грид элементов, что влияет на размер/ширину.

[Подробнее](https://webformyself.com/avtomaticheskoe-izmenenie-razmera-stolbcov-v-css-grid-auto-fill-protiv-auto-fit/)

## БЭМ

**БЭМ** — это система «Блок — Элемент — Модификатор». Это один из подходов к компонентной вёрстке и одна из самых распространённых в мире методологий вёрстки.

**Компонентная вёрстка** — это такой подход к вёрстке, когда отдельные компоненты сайта создаются изолированно и могут использоваться в любом месте, вне зависимости от окружения и содержания.

**Блок** - функционально независимый компонент страницы, который может быть повторно использован.

**Элемент** - это часть, деталь блока, то, что вообще не может использоваться вне своего блока.

**Модификатор** - это вариативность блока или элемента. Всегда только внешняя.

**БЭМ-дерево** - абстрактная структура страницы в блоках, элементах и модификаторах. Показывает вложенность блоков друг в друга, подчинение элементов блокам, наличие модификаторов.

имя-блока__имя-элемента--модификатор

### Правила БЭМ

1. Не использовать селектор по идентификатору
2. Не использовать селектор по тегу
3. Не использовать универсальный селектор (*)
4. Не использовать CSS-сброс
5. Не использовать вложенные селекторы
6. Не использовать комбинацию селекторов
7. Не использовать селектор по атрибуту
8. Не задавать внешнюю геометрию блокам
9. Не стараться определить все стили в одном CSS правиле (шрифты, сетка, декор, отступы)

**Композиция** — это процесс сборки проекта из отдельных компонентов. Компоненты собираются вместе, вкладываются один в другой.

**Декомпозиция** — это обратный процесс, деление макета на множество кусочков, каждый такой кусочек макета это компонент или БЭМ-блок.

**Тема** — это общий дизайн и оформление вашего сайта. Темы определяют, где и как на сайте будут отображаться кнопки, меню и другие виджеты. Тема определяет цветовую схему, шрифты, размеры, отступы и другие характеристики дизайна.

## Препроцессоры CSS

**Препроцессоры CSS** — это программа, которая генерирует CSS на основе собственного уникального синтаксиса препроцессора. Существует множество препроцессоров CSS на выбор, однако большинство препроцессоров CSS добавляют функции, которых нет в чистом CSS, такие как миксины, вложенность селекторов или селекторы наследования. Эти функции делают структуру CSS более читаемой и простой в обслуживании.

### Примеры

**Sass** (Syntactically Awesome Style Sheets — синтаксически привлекательные таблицы стилей) — язык сценариев с препроцессором, который интерпретируется или компилируется в каскадные таблицы стилей (CSS). SassScript - это сам язык сценариев.

Sass состоит из двух синтаксисов. Исходный синтаксис, называемый синтаксисом с отступом, использует синтаксис, аналогичный HAML. Он использует отступ для разделения блоков кода и символы новой строки для разделения правил. Более новый синтаксис, SCSS (Sassy CSS — Дерзкий CSS), использует форматирование блоков, подобное CSS, с фигурными скобками для обозначения блоков кода и точкой с запятой для разделения строк внутри блока. Синтаксису с отступом и файлам SCSS традиционно присваиваются расширения .sass и .scss соответственно. Sass был разработан в 2006 году Хэмптоном Кэтлином и Натали Вайценбаум.

**Less** (Leaner Style Sheets - компактная таблица стилей) - Язык динамических таблиц стилей препроцессора, который может быть скомпилирован в каскадные таблицы стилей (CSS) и запущен на стороне клиента или сервера. Синтаксис Less с отступами является вложенным метаязыком, поскольку допустимый CSS - это допустимый код Less с той же семантикой. Less предоставляет переменные, вложенность, миксины, операторы и функции. Основное отличие Less от других прекомпиляторов CSS заключается в том, что Less позволяет выполнять компиляцию в реальном времени через less.js браузер. Less был впервые выпущен в 2009 году.

**Stylus** –

Краткая характеристика
переменные, миксины,Вложенные селекторы

**Миксины** (примеси) – это ссылки на группу CSS-правил, которые можно использовать многогратно. Также миксины могут принимать данные и использовать для управление стилей. Например,

```
@mixin rotate($deg) { 
  transform: rotate($deg) 
}
```

@import vs @use
