# TELEGRAM

OPTIMUS integrates with Telegram application to provide notification and remote bot services.  
Here are some things you can do with this integration:  

1. Telegram Notification

2. Remote Bot Services

## Telegram Notification

Sends a message via telegram to specified telegram user or chat id.

![Telegram notification](../assets/images/telegram_notification.png)

Telegram notification bot is a service created by RPA Python / TagUI (Ken Soh).  
The bot can be accessed via Telegram mobile or web application from this link (https://t.me/rpapybot).
Or by scanning the QR code - should launch the service in your web app or mobile app.

![Telegram notification QR](../assets/images/qr_rpapybot.png)

The service can be called from OPTIMUS via the keyword `telegram`:

```
telegram: -4661161234 , This is a message from OPTIMUS
telegram: 1234567890 , Hello World. Olá Mundo. नमस्ते दुनिया. 안녕하세요 세계. 世界,你好。
telegram: 1234567890 , Use backslash n for new line\nThis is line 2 of the message
```

## Remote Bot Services

Optimus bot allows you to perform remote services with your OPTIMUS installation via telegram.  Some of the actions you can remotely perform are:  

1. `List` - to monitor automation jobs remotely.  Supports monitoring across multiple installations or instances of OPTIMUS robots if you set up the federation of robots accordingly on a common "message bus".

2. `Task` - to run automation tasks remotely.  As above, you need to setup the federation of robots with a common "message bus" if you wish to execute tasks across various robots.

![Optimus bot](../assets/images/optimus_bot.PNG)

To access your instance of Optimus RPA bot, scan the following QR code:

![Remote bot QR](../assets/images/qr_optimusrpa_bot.png)
