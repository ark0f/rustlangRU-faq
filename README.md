# faq

## IDE && Tools

### Чем RLS плох?

@vlad20012:
```
Во-первых, там используется save-analysis, т.е. сначала проект компилится полностью, часть внутренних структур данных компилятора дампается, и по ним уже RLS лазит. Что тут плохого - проект нужно полностью перекомпилировать при любом изменении, чтоб RLS'ом получить актуальные данные, и это охренеть как долго. Мб инкрементальная компиляция поможет, но это и есть одно из тех самых "изменений архитектуры", что необходимы RLS. И пилят это довольно долго. И все равно это будет медленно, пока save-analysis не отпилят полностью.

Во-вторых, компилятор очень плохо работает с кодом, который не компилится. Если поломан синтакисис - то вообще giving up. Это причина, почему в RLS комплишен до сих пор через racer, ибо комплишн - это почти всегда "поломанный синтаксис".
```

### В чём преимущества Rust-плагина для Intellij IDEA?

@vlad20012:
```
У нас с самого начала все пилится с учетом IDE'шных требований. Парсер умеет восстанавливаться на поломанном синтаксисе, типы нормально выводятся на незавершенных выражениях, и т.п. Ну и перфоманс - компилится только открытая в IDE вкладка. Зачем весь проект компилить? Ну и подобным подходам уже с десяток лет, в остальных JetBrains IDE примерно так же все работает. И практически для всех языков мы заново компилятор писали. Исключения я пока 2 знаю - это, во-первых, kotlin (для которого мы сами компилятор и писали, лол), во-вторых C#. С C# близко не знаком, хз как так вышло
``
