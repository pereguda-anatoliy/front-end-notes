## VS Code ##  
updated 20240703  

### Полное удаление VS Code ###  
- удалить программу из панели управления;  
- удалить папку c:\Users\UserName\\.vscode  
- удалить папку c:\Users\UserName\AppData\Roaming\Code  

### Установка VS Code ###  
- https://code.visualstudio.com/  
- в ходе установки добавляем галочки "открыть с помощью Code"  

### Запуск на слабом ПК ###  
- вписать в ярлыке на запуск в пути к файлу флаг --disable-gpu  

### Установка Git ###   
- https://git-scm.com/downloads
- значения установки оставляем по умолчанию, кроме:
    - Choosing the default editor used by Git
    выбираем Use Visual Studio Code as Git's default editor
    - Adjusting the name of the initial branch in new repositories
    выбираем Override the default branch name for new repositiries (main)
- проверка установки Git  
    - Windows+X - Windows PowerShell - Набрать команду git --version 
    - Если Git установлен (пример) git version 2.45.2.windows.1 

### Установка Node.js ###  
- https://nodejs.org/en/
- не ставим Automatically install the necessory tools
- проверяем установку Node.js в консоли, выводим версию node -v
- проверяем установку NPM в консоли, выводим версию npm -v

### Установка расширений для VS Code ###  
- сайт по выбору расшений https://marketplace.visualstudio.com/vscode  
- Russian Language Pack for Visual Studio Code (русский языковый пакет, если нужно)
- Brackets Light Pro (светлая тема)  
- Material Icon Theme (иконки типов файлов)  
- Live Server (просмотр в браузере, перезагрузка страницы после внесения измений)
- Auto Complete Tag (закрытие и переименование тэгов)
- Indent-Rainbow (расскрашивание отступов, настройка цветов для светлой темы в setting.json)
- Better Comments (расскрасить комментарии по типам ! ? // TODO * настройка цветов для светлой темы в setting.json)
- eCSStractor for VSCode (генератор CSS по классам из HTML)
- CSS Navigation (быстрое перемещение из HTML в нужный класс CSS по F12 и Alt+F12 с медиа-запросами)
- Image Preview (иконка с изображением на полях)
- Project Manager (переключение между проектами)

### Настройка VS Code ###  
- открыть панель терминалов CTRL+`  
в панели управления справа открыть Select Default Profile  
выбрать Git Bash  
- открыть панель настроек CTRL+, найти параметры и изменить  
    - Files: Auto Save - afterDelay (включить автосохранение с определенной задержкой)  
    - Editor: Font Size - 16 (установить размер шрифта)   
    - Editor: Line Height - 1.8 (установить межстрочный интервал)  
    - Editor: Detect Identation - True (разрешить замену табуляции заданным количеством пробелов, см. два пункта ниже)  
    - Editor: Tab Size - 4 (установить количество пробелов в табуляции)  
    - Editor: Insert Spaces - True (заменить табуляцию пробелами)  
    - Editor: Hover Enabled - False (убрать всплывающую подсказку, но и убрать произвольную настройку цвета в CSS)
    - Editor: Close Empty Groups - False (не закрывать вкладку без файлов)
    - Editor: Format On Paste - True (отформатировать код при вставке)  
    - Editor: Format On Save - True (отформатировать код при сохранении)
    - Editor: Bracket Pair Colorization - Enabled (расскрасить парные скобки)
    - Editor: Guides Bracket Pairs - active (соединить линией парные скобки)   
    - Editor: Match Brackets - never (не подсвечивать парные скобки)
    - Editor: Render Whitespace - all (показать все пробелы)
    - Workbench: Color Customizations - edit in settings.json (цвет индикации пробелов)
    - Emmet: Trigger Expansion On Tab (при перемещении от и потом возвращении тэгу, TAB его раскроет)
  
### Конфигурационный файл VS Code ###  
- для контроля, редактирования, переноса настроек  
- открыть панель команд CTRL+SHIFT+P
- найти open user settigs json
- выбрать Preferences: Open User Settigs (JSON)
- откроется setting.json

### Экспорт/Импорт профиля ###
для переноса всех настроек и расширений  
Manage (шестеренка слева) - Profile - Export (Import) Profile

### Settings Sync ###
для хранения/переноса всех настроек и расширений через GitHub
Manage - Backup and Sync Settings...
https://code.visualstudio.com/docs/editor/settings-sync

### Полезные материалы ###
- Видео "VS Code настройка установка плагины" 2020.02.28    
https://www.youtube.com/watch?v=nxCLXMBl4e4  
от https://www.youtube.com/@FreelancerLifeStyle  
текстовая версия https://habr.com/ru/articles/490754/  
посмотреть позже про снипеты, расширения для SCSS  
- Видео "GIT: установка на Windows" 2023.08.21  
https://www.youtube.com/watch?v=cfookORo0M4  
от https://www.youtube.com/@stepdev24  
обзор параметров при установке  
