## Favicon ##  
updated 20240716  

**Favicon** (сокр. от англ. Favorite icon — «значок для избранного») — значок веб-сайта или веб-страницы. Отображается браузером во вкладке перед названием страницы, и в качестве картинки рядом с закладкой, а также в адресной строке в некоторых браузерах.  

Минимальный вариант - поместить `favicon.ico` в корень сайта, браузер сам подключит иконку, но все-равно лучше вписать `<link>` в `<head>`:  

`<link rel="icon" type="image/x-icon" href="/favicon.ico" sizes="32x32">`  

Как вариант, можно использовать вместо ico иконку формата png:  

`<link rel="icon" type="image/png" href="../../assets/images/favicon-32x32.png" sizes="32x32">`  

Еще лучше использовать векторную иконку svg, которая отлично масштабируется и может содержать светлую и темную темы и медиа-запросы для их переключения:  

`<link rel="icon" type="image/svg+xml" href="../../assets/images/icon.svg">`  

Наиболее универсальный способ подключения favicon с учетом всех размеров и применений - создать пять иконок и один файл `.webmanifest` формата JSON с иконками png для android (можно создать в генераторе иконок):  

```
<link rel="icon" type="image/x-icon" href="/favicon.ico" sizes="32x32">
<link rel="icon" type="image/svg+xml" href="../../assets/images/icon.svg">
<link rel="apple-touch-icon" type="image/png" href="../../assets/images/apple-touch-icon.png" sizes="180x180">
<link rel="manifest" href="../../assets/images/site.webmanifest">
```

```
// manifest.webmanifest
{
  "icons": [
    { "src": "../../assets/images/icon-192.png", "type": "image/png", "sizes": "192x192" },
    { "src": "../../assets/images/icon-512.png", "type": "image/png", "sizes": "512x512" }
  ]
}
```

**Генераторы иконок**:  
https://realfavicongenerator.net/  
https://favicon.io/  



