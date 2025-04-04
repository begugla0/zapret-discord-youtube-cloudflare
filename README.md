<div align="center">

# <img src="https://cdn-icons-png.flaticon.com/128/5968/5968756.png" height=28 /> <a href="https://github.com/begugla0/">begugla0</a><a href="https://github.com/begugla0/zapret-discord-youtube-cloudflare">/zapret-discord-youtube-cloudflare</a> <img src="https://cdn-icons-png.flaticon.com/128/1384/1384060.png" height=28 />

*"Plug & Play"* обход блокировок Discord, YouTube и CloudFlare для Windows

Альтернатива https://github.com/bol-van/zapret-win-bundle
</div>

> [!CAUTION]
>
> ### АНТИВИРУСЫ
> WinDivert может вызвать реакцию антивируса.
> WinDivert - это инструмент для перехвата и фильтрации трафика, необходимый для работы zapret.
> Замена iptables и NFQUEUE в Linux, которых нет под Windows.
> Он может использоваться как хорошими, так и плохими программами, но сам по себе не является вирусом.
> Драйвер WinDivert64.sys подписан для возможности загрузки в 64-битное ядро Windows.
> Но антивирусы склонны относить подобное к классам повышенного риска или хакерским инструментам.
> В случае проблем используйте исключения или выключайте антивирус совсем.
>
> **Выдержка из [`readme.md`](https://github.com/bol-van/zapret-win-bundle/blob/master/readme.md#%D0%B0%D0%BD%D1%82%D0%B8%D0%B2%D0%B8%D1%80%D1%83%D1%81%D1%8B) репозитория [bol-van/zapret-win-bundle](https://github.com/bol-van/zapret-win-bundle)*

> [!IMPORTANT]
> Все файлы в папке [`bin`](./bin) взяты из [zapret-win-bundle/zapret-winws](https://github.com/bol-van/zapret-win-bundle/tree/master/zapret-winws). Вы можете это проверить с помощью хэшей/контрольных сумм.

## ⚙️Использование

1. Загрузите архив (zip/rar) со [страницы последнего релиза](https://github.com/begugla0/zapret-discord-youtube-cloudflare/releases/latest)

2. Распакуйте содержимое архива по пути, который не содержит кириллицу/спец. символы

3. Запустите нужный файл

## ℹ️Краткие описания файлов

- [**`discord.bat`**](./discord.bat) - запуск со стратегией для обхода блокировки <img src="https://cdn-icons-png.flaticon.com/128/5968/5968756.png" height=15 /> Discord

- [**`general.bat`**](./general.bat) - запуск со стратегией для обхода блокировок <img src="https://cdn-icons-png.flaticon.com/128/5968/5968756.png" height=15 /> Discord и <img src="https://cdn-icons-png.flaticon.com/128/1384/1384060.png" height=12 /> YouTube и CloudFlare

- [**`service_install.bat`**](./service_install.bat) - установка на автозапуск (как службы Windows: `zapret`, `WinDivert`), можно выбрать любую стратегию (название файла стратегии **НЕ** должно начинаться со слова `service`)
  
- [**`service_stop.bat`**](./service_stop.bat) - остановка служб `zapret` и `WinDivert`

- [**`service_remove.bat`**](./service_remove.bat) - остановка и удаление служб `zapret` и `WinDivert`

- [**`service_status.bat`**](./service_status.bat) - проверка состояния служб `zapret` и `WinDivert`


## ☑️Распространенные проблемы

### Не работает <img src="https://cdn-icons-png.flaticon.com/128/5968/5968756.png" height=18 /> Discord

- См. [#252](https://github.com/Flowseal/zapret-discord-youtube/discussions/252)

### Не работает <img src="https://cdn-icons-png.flaticon.com/128/1384/1384060.png" height=18 /> YouTube

- См. [#251](https://github.com/Flowseal/zapret-discord-youtube/discussions/251)

### Обход не работает

> [!IMPORTANT]
> **Стратегии блокировок со временем изменяются.**
> Определенная стратегия обхода zapret может работать какое-то время, но если меняется способ блокировки или обнаружения обхода блокировки, то она перестанет работать.
> В репозитории представлены множество различных стратегий для обхода. Если ни одна из них вам не помогает, то вам необходимо создать новую, взяв за основу одну из представленных здесь и изменив её параметры.
> Информацию про параметры стратегий вы можете найти [тут](https://github.com/bol-van/zapret/blob/master/docs/readme.md#nfqws).

- Проверьте другие стратегии (**`ALT`**/**`МГТС`**)

- Обновите файлы в папке [`bin`](./bin), взяв новые из [zapret-win-bundle/zapret-winws](https://github.com/bol-van/zapret-win-bundle/tree/master/zapret-winws)

- См. [#765](https://github.com/Flowseal/zapret-discord-youtube/issues/765)

### Файлы не запускаются

- См. [#522](https://github.com/Flowseal/zapret-discord-youtube/issues/522)

### Требуется цифровая подпись драйвера WinDivert (Windows 7)

- Замените файлы `WinDivert.dll` и `WinDivert64.sys` в папке [`bin`](./bin) на одноименные из [zapret-win-bundle/win7](https://github.com/bol-van/zapret-win-bundle/tree/master/win7)

### Не работает вместе с VPN

- Отключите функцию **TUN** (Tunneling) в настройках вашего VPN


### Не нашли своей проблемы

* Создайте её [тут](https://github.com/begugla0/zapret-discord-youtube-cloudflare/issues)

## 🗒️Добавление адресов прочих заблокированных ресурсов

Список блокирующихся адресов для обхода можно расширить, добавляя их в:
- [`list-general.txt`](./list-general.txt) для файлов `general *.bat`
- [`ipset-cloudflare.txt`](./list-general.txt) для файлов `general *.bat`
- [`list-discord.txt`](./list-discord.txt) для файла [`discord.bat`](./discord.bat)

> [!IMPORTANT]  
> После обновления списка адресов zapret необходимо перезапустить.

## ⭐Поддержка проекта

Вы можете поддержать проект, поставив :star: этому репозиторию (сверху справа этой страницы)


## ⚖️Лицензирование

Проект распространяется на условиях лицензии [MIT](https://github.com/begugla0/zapret-discord-youtube-cloudflare/blob/main/LICENSE)



💖 Отдельная благодарность разработчику [zapret](https://github.com/bol-van/zapret) - [bol-van](https://github.com/bol-van)
