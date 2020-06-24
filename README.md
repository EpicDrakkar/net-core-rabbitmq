﻿# net-core-rabbitmq

A simple example to use RabbitMQ.

Entities:

Worker:
Send messages to the Publisher API and have an event listener for the Queue name.
Is where the Real Business Logic Implementation Should be.

Publish API:
Has a POST method to push content to the QUEUE, so the Worker can eventyally get the event and run any code.

RabbitMQ Monitor:
Can be accessed by: http://localhost:15672

To Compose:
>docker-compose up --build

Ctrl+Shift+D: To Debug, we can create a console debug or a web debug.

Rule:
Usually is ONE QUEUE for ENDPOINT (So you dont have to manage resposibilities with switch's)
If we eventyally need to manage a callback, we can use RPC:
https://www.rabbitmq.com/tutorials/tutorial-six-dotnet.html
