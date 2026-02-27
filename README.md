<p aling="center"><a href="https://github.com/distillium/soxks5-proxy-manager">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="./media/logo.png" />
   <source media="(prefers-color-scheme: light)" srcset="./media/logo-black.png" />
   <img alt="socks5" src="./media/logo.png" />
 </picture>
</a></p>

Скрипт представляет собой установку и управление SOCKS5-прокси на базе **Dante** с поддержкой нескольких профилей.

⚠️ Поддерживаются только системы на базе **Debian/Ubuntu**.  
ℹ️ Требуется наличие **UFW (Uncomplicated Firewall)**

## Возможности:
- Установка и настройка `dante-server` за один шаг
- Создание неограниченного числа SOCKS5 профилей (порт, логин, пароль)
- Автогенерация или ручной ввод учетных данных и порта
- Просмотр списка подключений
- Удаление отдельных профилей или полное удаление менеджера
- Быстрый запуск через команду `socks` из любой точки системы

---

## Установка:
```bash
wget -q -O install.sh https://raw.githubusercontent.com/distillium/socks5-proxy-manager/main/install.sh && chmod +x install.sh && sudo ./install.sh
```

## Шаблоны профилей:
Стандартное отображение:
```
IP: xxx.xxx.xxx.xxx
Порт: 12345
Логин: username
Пароль: password
```

Готовый вывод для антидетект-браузеров:
```
xxx.xxx.xxx.xxx:12345:username:password
username:password@xxx.xxx.xxx.xxx:12345
```

## Команды:
`socks menu` - открыть главное меню  
`socks list` - список подключений  
`socks available` - быстрый список доступных прокси и активных пользователей  
`socks create` - создать новое подключение  
`socks delete` - удалить подключение

## Установка скрипта на Ubuntu:
```bash
sudo apt update && sudo apt install -y curl
curl -fsSL https://raw.githubusercontent.com/distillium/socks5-proxy-manager/main/install.sh -o install.sh
chmod +x install.sh
sudo ./install.sh
```

## Автор:
Создано [distillium](https://github.com/distillium)
