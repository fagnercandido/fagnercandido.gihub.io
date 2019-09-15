---
layout: post
title:  "Criando um bot para o Telegram usando Python"
description: Um exemplo usando Python para criar um bot Telegram
date:   2019-09-15 10:27:36 +0530
categories: Python Bot Telegram
---
O Telegram é um aplicativo fantástico, isso é fato. E criar bots para ele é fácil e ele mesmo ajuda a criação de bots com seu @BotFather.
Para tanto, inicialmente invoque o @BotFather com /start e siga os passos.
Ao fim destes passos, guarde o token informado. Aqui, o mesmo foi criado como variável de ambiente com:

```sh
export BOT_READ_ALL_MESSAGES="<TOKEN GERADO>"
```

Para este exemplo vamos usar o pyTelegramBotAPI, para a instalação use o pip:
```sh
pip3 install pyTelegramBotAPI
```

A seguir, vamos codificar o bot em si, o exemplo será em Python. Vamos por partes:
###Imports
```python
import os
import telebot
from telebot import types
import urllib
import json
```

Os imports acima incluem o telebot, que será a API usada para criação do bot.
###Lendo o Token
```python
botRead = telebot.TeleBot(os.environ["BOT_READ_ALL_MESSAGES"])
```

No código acima, criamos uma referência para o Telebot e inserido o token.
###Decoradores
```python
@botRead.message_handler(commands=['start', 'help'])
def send_start_message(message):
    botRead.reply_to(message, "Olá, eu sou o Bot 'Read All Messages' \n"
                          "Diariamente irei enviar as mensagens não lidas para seu e-mail")

@botRead.message_handler(func=lambda message: True)
def get_handle_chats(message):
    botRead.reply_to(message, message.chat.id)
```

Acima, usando os Decorators do Python, informamos quais métodos vão ser escutados. No primeiro método, escutamos os /start e /help e retornamos a mensagem mostrado.

O segundo método, somente faz um echo.
###Polling
```python
botRead.polling()
```

Por fim, é feito o polling para iniciar o bot. Pronto. Rode o bot e use o Bot:
```python
python3 meuBot.py
```

Pronto, temos um bot.

Qualquer dúvida, problema ou sugestão é só dizer.

Seguem os fontes: [Fontes](https://github.com/fagnercandido/ReadAllMessagesBot)