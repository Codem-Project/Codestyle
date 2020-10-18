 🧿 Code Style Guide (CODEM)
 ========================
***

📍 **Codem Code Style** включает в себя обширную сборку JavaScript и TypeScript ESLint правил для написания понятного и чистого кода для проекта.

### 💻 Установка ###
***

***1. Установите npm зависимости***

```js
npm install --save-dev eslint eslint-plugin-no-loops @typescript-eslint/parser @typescript-eslint/eslint-plugin
```

***2. Добавьте lint script***

Необходимо добавить скрипт в файл ```package.json ```

```js 
{
  "scripts": {
    ...
    "lint": "eslint . --ext .ts",
  }
}
```
### ⚙️ Текущая конфигурация ###
***

Название правила  | Состояние | Рекомендации 
----------------|----------------------|----------------------
no-loops/no-loops | error | Использование ```.map```, ```.forEach```, ```.filter```, ```.reduce``` 
no-await-in-loop | warn | -
no-compare-neg-zero | warn | Не использовать сравнение с -0
no-cond-assign | error | Не использовать операции присваивания в условных выражениях
no-dupe-args | error | Не использовать повторяющиеся аргументы в функции
no-dupe-else-if | error | Не использовать повторяющиеся выражения в конструкции if...else
no-dupe-keys | error | Не использовать повторяющиеся ключи в объектах
no-duplicate-case | error | Не использовать повторяющиеся case
no-empty | warn | Описывать тело любых блочных выражений
no-unreachable | error | Удалить код после ```return```, ```throw```, ```break```, и ```continue```
use-isnan | error | Использовать isNan() вместо прямого сравнения с NaN
complexity | error, 4 | Не использовать выражения больше 4 уровня цикломатической сложности
default-case | error | Использовать default case в switch
default-case-last | error | Обязательно использовать default case в switch в конце конструкции 
no-alert | error | Не использовать ```alert```, ```promt```
no-redeclare | error | Не использовать передекларирование переменных
no-return-assign | error | Не использовать присваивание в ```return```
no-unmodified-loop-condition | error | Не использовать неизмененные условия циклов
camelcase | warn | Верблюжий case для именования
max-nested-callbacks | error, 3 | Не использовать больше 3 уровней callback вложенности
no-unneeded-ternary | warn | Не использовать тернарные операторы, когда существуют более простые альтернативы
prefer-exponentiation-operator | warn | Использовать ```**```, вместо ````Math.pow()````
arrow-parens | warn | Использовать круглые скобки для аргументов стрелочных функций
arrow-spacing | error | Использовать пробел до / после стрелки функции стрелки
no-const-assign | warn | Не изменять переменные, объявленные с использованием ```const```
no-var | error | Использовать ```let, const``` вместо ```var```
prefer-arrow-callback | error | Использовать стрелочные функции для callback 
prefer-const | error | Использовать ```const``` для неизменяемых переменных
indent | error | Использовать табуляцию для отступов
prefer-destructuring | error | Использовать деструктуризацию
@typescript-eslint/no-for-in-array | error | Не использовать for-in для перебора массива
@typescript-eslint/no-misused-promises | error | Избегайте использования обещаний в местах, не предназначенных для их обработки
@typescript-eslint/no-non-null-asserted-optional-chain | warn | Не использовать ненулевое утверждение после необязательного цепного выражения
@typescript-eslint/no-unnecessary-condition | error | Предотвращает условные выражения, где тип всегда правдивый или всегда ложный
@typescript-eslint/no-unnecessary-type-assertion | warn | Предупреждает, если утверждение типа не изменяет тип выражения
@typescript-eslint/brace-style | warn | Обеспечить согласованный стиль скобок для блоков
@typescript-eslint/no-empty-function | error | Не использовать пустые функции
@typescript-eslint/no-extra-parens | error | Удалите ненужные скобки
@typescript-eslint/no-extra-semi | error | Удалите ненужные точки с запятой
@typescript-eslint/no-unused-expressions | error | Удалите неиспользуемые выражения
@typescript-eslint/no-unused-vars | error | Удалите неиспользуемые переменные
@typescript-eslint/no-use-before-define | error | Не использовать переменные до объявления
@typescript-eslint/quotes | error, single | Использовать одинарные ```(''```) кавычки
@typescript-eslint/require-await | error | Не использовать асинхронные функции без ```await``` выражения
