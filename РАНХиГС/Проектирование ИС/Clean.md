### Рекомендованный план:

1. Обновляйте систему раз в несколько дней:
    
    bash
    
    
    `sudo pacman -Syu`
    
2. Чистите кэш и удаляйте ненужные пакеты раз в месяц:
    
    
    `sudo paccache -r sudo pacman -Rns $(pacman -Qdtq)`
    
3. Раз в несколько месяцев проверяйте состояние системы:
    
    
    `sudo pacman -Dk sudo fsck /dev/sdX`