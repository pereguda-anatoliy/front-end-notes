## Web-Fonts ##  
updated 20240715  

### Web-Fonts Сheat sheet ##  

```
@font-face {  
  font-display: swap;  
  font-family: 'Roboto';  
  font-style: normal;  
  font-weight: 400;  
  src: url('../fonts/roboto-v30-latin-regular.woff2') format('woff2');  
}  
```

```
body {
    font-family: Roboto, Arial, sans-serif;
    font-weight: 400;
    font-style: normal;
    font-size: 16px;
    line-height: 1.5;
}
```

### Google Fonts ###  

Бибилиотека бесплатных web-fonts для скачивания и онлайн использования:  
[Google Fonts](https://fonts.google.com/)  

Конвертеры форматов шрифтов:  
https://www.fontconverter.io/en  
https://transfonter.org/  

Утилита для удобного скачивания и подключения шрифтов с google fonts  
[Google Webfonts Helper](https://gwfh.mranftl.com/fonts/roboto?subsets=latin)  

### Подключение шрифтов через CSS директиву `@font-face` ###  

- Используется для подключения файлов из локальной папки  
Каждая вариация шрифта подключается своим `@font-face`  

- директива `@font-face` должна стоять в CSS сразу за директивами @import  

- Можно использовать свое название `font-family` для каждого варианта, например, `font-family: 'Roboto-Regular';` и `font-family: 'Roboto-Bold';` и спользовать эти названия `font-family` в CSS:  
```
body {  
  font-family: "Roboto-Regular", sans-serif;  
}  
```

- Либо использовать одно `font-family` во всех вариациях шрифта в `@font-face`, а в CSS использовать конкретные параметры:  
```
body {  
  font-family: "Roboto", sans-serif;  
  font-weight: normal;  
}  
```

- Существует компактная форма описания `font-family` (применяется редко, порядок важен) и развернутая:
```
body {
    font: 700 italic normal normal 16px/1.5 Roboto, Arial, sans-serif;
/*
font-weight: 700;
font-style: italic;
font-stretch: normal;
font-variant: normal;
font-size: 16px;
line-height: 1.5;
font-family: Roboto, Arial, sans-serif;
*/
}
```

- Содержание `@font-face` в случае использования с **Modern Browsers**:  
```
@font-face {  
  font-display: swap;  
  font-family: 'Roboto';  
  font-style: normal;  
  font-weight: 400;  
  src: url('../fonts/roboto-v30-latin-regular.woff2') format('woff2');  
}  
```

- Содержание `@font-face` в случае использования с **Legacy Support**:  
```
/* roboto-regular - latin */
@font-face {  
  font-display: swap;  
  font-family: 'Roboto';  
  font-style: normal;  
  font-weight: 400;  
  src: url('../fonts/roboto-v30-latin-regular.eot');  
  src: url('../fonts/roboto-v30-latin-regular.eot?#iefix') format('embedded-opentype'),  
       url('../fonts/roboto-v30-latin-regular.woff2') format('woff2'),  
       url('../fonts/roboto-v30-latin-regular.woff') format('woff'),  
       url('../fonts/roboto-v30-latin-regular.ttf') format('truetype')  
       url('../fonts/roboto-v30-latin-regular.svg#Roboto') format('svg');  
}  
```

- Ссылки на локально установленные шрифты в настоящее время не применяются:  
```
src: local("Roboto-Regular"),  
    local("Roboto Regular");  
```

- В случае использования вариативного шрифта в CSS применяются дополнительные параметры:
```
font-family: "Open Sans", sans-serif;  
font-optical-sizing: auto;  
font-weight: 400;  
font-style: normal;  
font-variation-settings: "wdth" 75;  
```
где свойство `font-variation-settings` контролирует характеристики вариативных шрифтов с помощью четырёхбуквенных имён осей: стандартных или специфичных для шрифта. Эти имена зашиты прямо в шрифте.  

Названия стандартных осей:  
`"wght" 675` — weight  
`"wdth" 75` — stretch (condensed)  
`"slnt" 6` — style (range is from 0 to 12)  
`"ital" 0.5` — style (0 - not italic, 0.5 - halfway italic, 1 - fully italic)  
`"opsz" none ` — optical sizing ( auto, none)  

- Важно в `font-family` в CSS указывать после основного шрифта веб-безопасный шрифт, а потом, на крайний случай, тип шрифта `serif`, `sans-serif`, `monospace`, `cursive`, `fantasy`, `system-ui`. В случае, если первый шрифт не загрузится, браузер воспользуется альтернативными вариантами.  

Примеры:  
font-family: Roboto, Arial, Tahoma, sans-serif;  
font-family: "Roboto Slab", Georgia, "Times New Roman" serif;  
font-family: "Roboto Mono", "Courier New", "Lucida Console", monospace;  

### Подключение шрифтов через CSS директиву `@import` ###  

- Используется для подключения шрифтов из удаленного хранилища (Google Fonts) в `css` файле (например вариативный шрифт `Open Sans`, `Roman`, `Regular 400`, `Condensed 75`):  
```
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wdth@75&display=swap');  
```  

- директива `@import` должна стоять первой в CSS  

### Подключение шрифтов через разметку тегом `<link>` в теге `<head>` ###  

Подключение шрифта с удаленного хранилища Google Fonts через `<link>` в `<head>`:  
- для не вариативных шрифтов в Google Fonts можно выбрать только нужные font-weight и font-style (например шрифт `Poppins` начертаний `Regular 400`, `Regular 400 Italic`, `Bold 700` и `Bold 700 Italic`):  
```
<link rel="preconnect" href="https://fonts.googleapis.com">  
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>  
<link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,400;0,700;1,400;1,700&display=swap" rel="stylesheet">  
```

- для вариативных можно либо выбрать шрифт со всеми существующими начертаниями (включая новый параметр - ширину): 
```
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Open+Sans:ital,wdth,wght@0,75..100,300..800;1,75..100,300..800&display=swap" rel="stylesheet">
```
- либо выбрать один вариант шрифта с конкретными параметрами для подключения (например шрифт `Open Sans`, `Roman`, `Regular 400`, `Condensed 75`):
```
<link rel="preconnect" href="https://fonts.googleapis.com">  
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>  
<link href="https://fonts.googleapis.com/css2?family=Open+Sans:wdth@75&display=swap" rel="stylesheet">  
```

### Параметры шрифтов ###

**Font Weights:**  
Thin 100  
ExtraLight 200  
Light 300  
Regular 400  
Medium 500  
SemiBold 600  
Bold 700  
ExtraBold 800  
Black 900  

**Font Style:**  
normal  
italic  




