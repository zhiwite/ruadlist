Использование TortoiseHg и её аналогов в Linix.

Cначала нужно сделать clone в эту папку. Команда на вкладке Source.

После clone сделай следующее:
1. Зайди в папку .hg
2. Открой hgrc в N++.
3. Замени содержимое на:

```
[paths]
default = https://code.google.com/p/ruadlist/

[auth]
gcode.prefix = https://code.google.com/
gcode.username = имя гуглопрофиля
gcode.password = пароль гуглокода

[ui]
username = имя гуглопрофиля
```

Это избавит от ввода пароля при пушах. В виндовой версии с TortoiseHg тоже работает.

Кстати, при желании можешь поставить TortoiseHg и в Linux - у него есть версия для Linux.