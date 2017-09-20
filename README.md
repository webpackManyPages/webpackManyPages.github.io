# Webpack для сайта с несколькими страницами (точками входа).

npm i :Импортировать необходимые модули.Зависимости указаны в файле package.json

set NODE_ENV=development&webpack
или
set NODE_ENV=production&webpack

**set NODE_ENV=development&webpack - ВЕБПАК СОБИРЕТ ОБЫЧНЫЙ ФАЙЛЫ .js**<br />
**set NODE_ENV=production&webpack - ВЕБПАК СОБИРЕТ МИНИМИЗИРОВАННЫЕ UglifyJsPlugin ПЛАГИНОМ ФАЙЛЫ .js**

Плагин NoErrorsPlugin – не добавляет в сборку файлы с ошибками
Плагин CommonsChunkPlugin – убирает ИЗ РАЗНЫХ ТОЧЕК ВХОДА (файлов) одинаковый код и помещает его в один общий файл
В файл commons.js можно добавлять и СВОЙ код, к которому добавится общий код

Файл package.json содержит следующие зависимости:
npm i webpack@1 -S
npm i babel-loader@5 -S
npm i babel-runtime@5 -S

set NODE_ENV=production  **СОЗДАЕТСЯ ГЛОБАЛЬНАЯ ПЕРЕМЕННАЯ ДЛЯ WINDOWS**<br />
webpack **ВЕБПАК СОБИРАЕТ С УЧЕТОМ УКАЗАННОЙ ГЛОБАЛЬНОЙ ПЕРЕМЕННОЙ WINDOWS**

set NODE_ENV=development  **СОЗДАЕТСЯ ГЛОБАЛЬНАЯ ПЕРЕМЕННАЯ ДЛЯ WINDOWS**<br />
webpack **ВЕБПАК СОБИРАЕТ С УЧЕТОМ УКАЗАННОЙ ГЛОБАЛЬНОЙ ПЕРЕМЕННОЙ WINDOWS**

Добавить к основному адресу home.html или about.html- повится функционал