# skibidi-adpro-5.2

## How much data your publisher program will send to the message broker in one run?
In one run, the publisher program is designed to send a total of 5 separate messages to the message broker. Each message represents a piece of data that will be delivered to the broker for processing or distribution to consumers. Therefore, the total amount of data sent by the publisher during a single execution consists of these 5 individual messages.

## The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
If the URL `amqp://guest:guest@localhost:5672` is the same in both the publisher and subscriber programs, it means that both programs are connecting to the same RabbitMQ message broker, using the same credentials and server location. This setup allows the publisher to send messages to the broker, and the subscriber to receive those messages from the broker, enabling message-based communication between them.

## Screen RabbitMQ
![alt text](assets/SS1.png)