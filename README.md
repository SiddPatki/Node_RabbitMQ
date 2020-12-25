# Node_RabbitMQ
Messaging Queue using NodeJs and RabbitMQ
based on- https://medium.com/swlh/how-to-implement-a-simple-message-queue-in-node-js-ee52e4ad6615

## How & Why even?

Messaging Queue enables asynchronous communication, where application(producer) puts a message onto a message queue and does not require an immediate response to continuing processing.
The producer and consumer do not interact directly with each other, but they interact through message queue.
This way of handling messages decouples the producer from the consumer so that they do not need to interact with the message queue simultaneously and immediately.

It is used wherever an immediate response in not required.

## Applications
Message queue have multiple application:
1.Live notification to user on a web site without refreshing.
2.Posting review of product after processing it through system.

## Steps:

1.npm init -y
To create a default package.json using information extracted from the current directory, use the npm init command with the --yes or -y flag. 

2.touch index.js

3.npm install –-save amqplib
Advanced Message Queuing Protocol (AMQP) 

4.install RabitMQ and erlang

5.login at localhost:15672 through Guest (id/pwd: guest) and create a queue called 'node_queue'

6.Create connection for Producer and set a channel to operate the queue and send a message in *index.js*.

7.Run *node index.js*

8.You can see Ready as 1 under messages.

9.Write consume code to create connection and channel to receive a message from the 'node_queue'

