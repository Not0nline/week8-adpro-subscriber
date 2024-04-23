# week8-adpro-subscriber

7.Try to answer the following questions, and write the answer in the and new file readme.md in you repository.

a. what is amqp?

AMQP is an acronym for Advanced Message Queuing Protocol. It means that client applications are designed to communicate with the source application that sends information/data. This data is sent using messaging middleware where clients will get the data they need from this middleware. In the link amqp://guest:guest@localhost:567, AMQP is the protocol used to carry out data transactions.

b. what it means? guest:guest@localhost:5672 , what is the first quest, and what is the second guest, and what is localhost:5672 is for?

guest:guest is the username and password used to be authenticated by the server. For ‘localhost:5672’, localhost refers to the hostname of the server where the host is now our own device and 5672 is the port used for AMQP.

- simulation slow subscriber

![img_3.png](img_3.png)

This graph shows that there is an increase in messages over a certain time interval. This is related to the cargo run that is executed in the publisher project. It can be observed that each time the publisher is run, there will be an increase in the message rate on RabbitMQ, which serves as its message queue.

- Running at least 3 subscriber

![img_5.png](img_5.png)

The image above shows that at one point there were 25 messages in the queue. This happened because the subscriber needed more time to manage each event in the message queue, resulting in a pile-up of messages because the publisher published messages faster than the subscriber could process them.

![img_4.png](img_4.png)