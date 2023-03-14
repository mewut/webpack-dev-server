# Webpack

Устанавливаем webpack:
```
npm install webpack webpack-cli --save-dev
```

Для css устанавливаем загрузчики:
```
npm i style-loader css-loader --save-dev
npm install  mini-css-extract-plugin  --save-dev
```

Далее для DevServer cтавим шаблонизатор:
```
npm i html-webpack-plugin --save-dev
```

И шаблонизатор pug: 
```
npm i pug pug-loader --save-dev
```

И не забываем всю красоту добавить в webpack.config.js.

# DevServer

Устанавливаем:
```
npm install webpack-dev-server --save-dev
```

В packade.json добавляем скрипт для запуска ```npm run start:dev```:
"start:dev": "webpack serve --config config/webpack.dev.js"

# Минификация 

Устанавливаем плагины:
```
npm i terser-webpack-plugin  --save-dev
npm i css-minimizer-webpack-plugin --save-dev
```

# Json-server

Устанавливаем json-server:
```
npm i -g json-server
```

Создаем в корне файл database.json
Добавляем в него информацию:
```
{
    "games": [
        { "id": 1, "name": "GTA", "year": "2010", "price": "999" },
        { "id": 2, "name": "Mass Effect", "year": "2015", "price": "9999" },
        { "id": 3, "name": "Atomic Heart", "year": "2023", "price": "99999" }
    ]    
  }
  ```
Запускаем: 
```
json-server --watch database.json
```

# Линтер

Устанавливаем линтер:
```
npm i eslint --save-dev
```

И файл конфигурации: 
```
npx eslint --init
```

После запускаем линтер, отвечаем на его вопросы. Он создаст файл .eslintrc.js.

После ставим для СSS:
```
npm i stylelint stylelint-webpack-plugin --save-dev
npm i stylelint --save-dev
npm i stylelint-config-standard
```

# Git-хуки

Устанавливаем: 
```
npm i husky --save-dev
npm set-script prepare "husky install"
```

После запускаем компонент: ```npm run prepare```. А потом добавляем хук: npx husky add .husky/pre-commit "npm run lint"
