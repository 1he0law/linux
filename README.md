В терминале вводим команду
'nano /etc/ufw/before.rules'

Находим строчку
ok icmp codes for INPUT

и в конце этого блока добавляем

-A ufw-before-input -p icmp --icmp-type source-quench -j DROP

в этом же блоке меняет ACCEPT на DROP
