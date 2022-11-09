# evernote-example
Упражнение на чтение кода. Взаимодействие с API Evernote.

Перед запуском этих программ, необходимо создать учетную запись Evernote на странице https://sandbox.evernote.com/Registration.action. Кроме того, следует создать блокноты и заметки в них. 

# config.py
Применяется для настройки параметров подключения к Evernote, включая ключ пользователя, а также идентификаторы блокнотов и шаблона заметки. 
Для работы с программами потребуется указать следующие параметры: 
* `EVERNOTE_PERSONAL_TOKEN` - ключ пользователя, который можно получить на странице https://sandbox.evernote.com/api/DeveloperToken.action
* `INBOX_NOTEBOOK_GUID` - один из идентификаторов блокнотов, выдаваемых программой list_notebooks.py 
* `JOURNAL_NOTEBOOK_GUID` - один из идентификаторов блокнотов, выдаваемых программой list_notebooks.py 
* `JOURNAL_TEMPLATE_NOTE_GUID` - можно найти в строке адреса заметки. Это значение между строкой `Home.action#n=` и первым за ней символом `&`.

# list_notebooks.py
Выдает список блокнотов, в котором перечислены значения параметров Notebook GUID и имена блокнотов. Notebook GUID потребуется в дальнейшем для работы других файлов. Вывод этой программы выглядит следующим образом: 

![list_notebooks.py](https://github.com/eug11ne/evernote-example/blob/main/1.jpg?raw=true)

# dump_inbox.py
В качестве аргумента принимает число заметок. Выдает содержимое заданного числа заметок из блокнота, который указан в файле `config.py` с помощью параметра `INBOX_NOTEBOOK_GUID`. Вывод этой программы выглядит следующим образом: 

![dump_inbox.py](https://github.com/eug11ne/evernote-example/blob/main/2.jpg?raw=true)

# add_note2journal.py
Принимает дату в формате ГГГГ-ММ-ДД и создает заметку в блокноте, который указан в файле `config.py` с помощью параметра `JOURNAL_NOTEBOOK_GUID`. Заметка создается на основе заголовка заметки, указанной с помощью параметра `JOURNAL_TEMPLATE_NOTE_GUID`, а также даты и дня недели. 



