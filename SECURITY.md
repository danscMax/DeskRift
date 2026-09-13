# Безопасность и приватность

[English below](#security-and-privacy)

## Куда DeskRift ходит в сеть

Вот весь список. Больше никуда программа не ходит и ничего о вас не отправляет.

| Когда | Куда | Зачем |
|---|---|---|
| Вы вставили ссылку или ищете ролик | YouTube, RuTube и их серверы с видео | найти ролик и включить его |
| Вы открыли готовые подборки | сайты, откуда эти подборки берутся | картинки-превью и сами обои |
| Вы нажали «Проверить обновления» | `deskrift.app/download/latest.json` | посмотреть, вышла ли версия новее |
| Раз в сутки, сам по себе | GitHub — за обновлением качалки `yt-dlp` | YouTube то и дело ломает старые версии качалки, и без свежей ролики просто перестают скачиваться |

Последняя строчка — **единственный** случай, когда программа выходит в сеть сама, без вашего участия.

## Чего нет

- **Никакой слежки.** Ни счётчиков запусков, ни сбора статистики, ни сторонних аналитик вроде Google Analytics или Sentry.
- **Никаких аккаунтов.** Регистрироваться негде, профиля на сервере нет — программа попросту не знает, кто вы.
- **Ничего не приезжает само.** Программа не дёргает сервер по расписанию и не качает обновления в фоне. Проверить версию можно только кнопкой в меню.
- **Ваши файлы остаются у вас.** Видео с диска, GIF и настройки никуда не уезжают.

## Что и где лежит на вашем диске

| Что | Где |
|---|---|
| Настройки | `%APPDATA%\com.deskrift.app` |
| Библиотека, кэш, логи | `%LOCALAPPDATA%\DeskRift` |

Логи лежат у вас на диске и сами никуда не уходят. Отправить их можно только руками: **Настройки → Логи → Экспорт**, а дальше — приложить к жалобе, если захотите. Перед этим загляните внутрь: там видны пути к вашим файлам и названия роликов.

## Куки браузера для YouTube

Некоторые ролики YouTube отдаёт только авторизованным. Для таких случаев в настройках можно разрешить приложению **читать куки вашего браузера** — они используются локально, чтобы `yt-dlp` мог представиться вам, и никуда не передаются. Работает с Firefox; Chrome и Edge с недавних версий шифруют своё хранилище так, что прочитать его снаружи нельзя в принципе.

По умолчанию эта опция выключена.

## Установщик не подписан

Сертификат подписи стоит денег, и пока его нет. Поэтому Windows показывает синее окно SmartScreen и пишет, что издатель неизвестен.

Хотите убедиться, что скачали именно наш файл, — сверьте контрольную сумму. Она написана в описании каждого [релиза](../../releases):

```powershell
Get-FileHash .\DeskRift-Setup.exe -Algorithm SHA256
```

Файл на сайте и файл в релизе совпадают байт в байт.

## Нашли уязвимость?

Напишите на **matsiyak@gmail.com**, а не в публичные жалобы. Постараюсь ответить в течение недели.

Код закрыт, так что проверить всё написанное выше по исходникам со стороны не получится. Если вам такая проверка нужна — напишите, обсудим, что можно показать.

---

# Security and privacy

## Where DeskRift connects

The complete list. Nothing beyond this is sent anywhere.

| When | Where | Why |
|---|---|---|
| You paste a link or search for a clip | YouTube, RuTube and their CDNs | find and play the video |
| You open a wallpaper catalog | the catalog sites whose collections the app shows | previews and wallpaper files |
| You click "Check for updates" | `deskrift.app/download/latest.json` | find out whether a newer version exists |
| Once a day, in the background | GitHub — `yt-dlp` itself, via its own `-U` command | YouTube keeps breaking older downloader versions; without the update, video downloads stop working |

That last row is the **only** connection that happens without an action from you.

## What there isn't

- **No telemetry, analytics or counters.** No Google Analytics, no Sentry, no home-grown launch counter.
- **No accounts.** No sign-up, no server-side profile; the app does not know who you are.
- **No auto-update.** The app never polls on a timer and never downloads anything by itself. The version check is a button in the menu.
- **No uploading of your files.** Local videos, GIFs and settings never leave your machine.

## What is stored, and where

| What | Where |
|---|---|
| Settings | `%APPDATA%\com.deskrift.app` |
| Library, cache, logs | `%LOCALAPPDATA%\DeskRift` |

Logs are written locally and go nowhere. The only way to send them is by hand — **Settings → Logs → Export** — and attaching them to an issue if you choose to. Look inside before you do: logs contain paths to your files and the titles of clips.

## Browser cookies for YouTube

Some YouTube videos are only served to signed-in users. For those cases the settings let the app **read your browser cookies** — they are used locally so `yt-dlp` can identify as you, and are never transmitted anywhere. Works with Firefox; recent Chrome and Edge encrypt their storage in a way that cannot be read from outside at all.

The option is off by default.

## The installer is not signed

A code-signing certificate is a separate expense and there isn't one yet, so Windows SmartScreen warns about an unknown publisher.

To confirm you downloaded our file, check the hash — it is published in the notes of every [release](../../releases):

```powershell
Get-FileHash .\DeskRift-Setup.exe -Algorithm SHA256
```

The file on the website and the file in the release are byte-for-byte identical.

## Found a vulnerability?

Email **matsiyak@gmail.com** — please don't open a public issue. I'll try to reply within a week.

The source is closed, so the claims above cannot be verified from outside by reading the code. If you need that kind of assurance, get in touch and we'll discuss what can be shown.
