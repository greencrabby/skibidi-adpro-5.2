# skibidi-adpro-5.2

## How much data your publisher program will send to the message broker in one run?
In one run, the publisher program is designed to send a total of 5 separate messages to the message broker. Each message represents a piece of data that will be delivered to the broker for processing or distribution to consumers. Therefore, the total amount of data sent by the publisher during a single execution consists of these 5 individual messages.

## The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
If the URL `amqp://guest:guest@localhost:5672` is the same in both the publisher and subscriber programs, it means that both programs are connecting to the same RabbitMQ message broker, using the same credentials and server location. This setup allows the publisher to send messages to the broker, and the subscriber to receive those messages from the broker, enabling message-based communication between them.

## Screen RabbitMQ
![alt text](assets/SS1.png)

- The publisher sends a total of 5 events to the message broker during its execution. These events act as messages that carry data or instructions. Once the messages arrive at the broker, they are stored in a queue and made available for any connected subscribers. The subscriber, which is set up to listen to the same queue or channel, retrieves these events one by one. After receiving them, the subscriber processes each event according to its logic
![alt text](assets/SS2.png)

- The spike seen on the message rate graph reflects a sudden increase in the number of messages sent to the message broker within a short period of time. The message rate is a metric that tracks how many messages are transmitted per second or minute. When the publisher sends multiple messages like the 5 events in this case all at once or in rapid succession, the system logs a sharp rise in activity. This results in a noticeable spike on the graph, indicating that the channel experienced a burst of message traffic. Such spikes are normal in systems where publishers send data in batches or at specific intervals and can help developers monitor the performance and load of the messaging system.
![alt text](assets/SS3.png)