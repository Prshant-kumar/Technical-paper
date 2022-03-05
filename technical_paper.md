# <pre>                       **MESSAGING QUEUE**


# INTRODUCTION


    Messaging Queue is a storage for an asynchronous communication between different parts of a system.
    Those parts can also be referd as "Producers" and "Consumers".There are several producers(request for service) and several consumers(processes request). Messaging Queue provides storage for the request made by the producer and consumers fetch the message in a sequence of FIFO and process the request accordingly.


<p align="center">
  <img src="./images/MQ architecture.png" alt ="simple message queue architecture">

</p>

<br><br><br><br><br>

# TABLE OF CONTENT


  >-    Synchronous and Asynchronous communication.
  >-    Messaging Queue
  >-    Message Queue used models
  >-    Why Message queue is used
  >-    Popular tools




<br><br><br><br><br>




## 1. *Synchronous and Asynchronous communication*


    In order to understand MQ we first need to know what is "Synchronous and Asynchronous communication" ?
  - ###  Synchronous Communication-
      It is a communication when the producer and the consumer are in sync.<br>
      Means one who is requesting service(Producer) and the one who is receiving request(Consumer) are responding at the same instance.<br>
      Example-<br>
      Tow or more people communicating thrrough mobile phone.
  - ### Asynchronous communication-
      It is a communication in which the **Producer** and the **Consumer** do not necessarily need to be present at the same instance to respond to the request.<br>
      Example-<br>
      Text message send to a friend who is not connected to a network, but receives message when connected to the network.


<br><br><br><br>

## 2. *Messaging Queue*


  Messaging Queue allows different parts of a system(Producer and Consumer) to communicate Asynchronously.
  MQ is a sequential line of data block which has data structure  and memory to store request. These request are messages and this is called a message queue.Message queue acts as a medium to communicate between the parts of a system.

  Simply put, MQ is a storage where producer sends there request, that request is stored at the tail(End) of the queue and the condumer takes the messages from the head(Start) of the queue and process accordingly.
  

  **WORKING**
- Producer makes the request as messages.
- Those messages goes at the end of a queue as it is a FIFO storage device(Queue).
- Consumer fetches the message. 
- Each messsage is processed only once by a single consumer.
- And the request is carried out according to the message.

<p align="center">
  <img src="./images/Message queue defination.png" alt ="simple message queue architecture">

</p>


<br><br><br><br>

## 3. *Message Queue used models*
    There are two models in which message queues are used.
  - #### **One-To-One model.** 
  - #### **Pub/Sub model.**<br>
  1. One-To-One model-<br>
    In One-To-One model a single request is processed by a **_Single Customer_**.<br>
    If the number of request increses even then a single request is processed by a **_Single Customer_**.<br>
    <br>
    Example-<br>
    Sending an e-mail to a friend.That e-mail is processed by a single consumer and only once.
  <p align="center">
    <img src="./images/onetoone.jpg" alt ="One-To-One model">

  </p>
  2. Pub/Sub model-<br>
    Pub/Sub model also known as Publish Subscriber model.<br>
    In this modle a single message is decoupled and a copy of message is send to **_many subscriber_** associciated to carry out different processes for the message fetched.<br>
    <br>Example-<br>
    An order placed on an online shoping store.<br>
    The message is just the order. But there are many processes to be carried out.<br>
    Like-<br>
    Sending confirmation SMS, sending confirmation e-mail, the invoice message, etc.
    <br>
    So for each processes in the message there are system called subscribers to carry out a single process out of many.


  <p align="center">
    <img src="./images/pubsub.png" alt ="Pub/Sub model">

  </p>

-  *The difference between the above two model is that, in case of One-To-One model there is a single consumer(subscriber) to process a single request.*


    *whereas in Pub/Sub model there are many subscriber to process different request in a single message*


<br><br><br><br>


## 4. *Why Message queue is used*


Message Queue is used to establish Asynchronous Communication.
<br>
Because of the following advantages over  synchronous communication-
<br>
  - Scalable-<br>
  Can handle load increase (If the number of message increases, they are pushed to the end of the que for processing).
  <br>
  We dont have to cancel the request, insted take the request and delay it for some time.

  - Higly available-<br>
  If a consumer(server)/network fails there are other consumer(servers) to handle the process.
  
  - Durable- <br>
  Once a request is made data is not lost until it is processed. 


<br><br><br><br>


## 4. *Popular tools for Messaging Queue*

Some of the popular tools for messaging queue are-
- Kafka
- ACTIVEMQ
- RabbitMQ
- amaon SNS
<br>
[Refer for above](https://medium.com/double-pointer/kafka-vs-activemq-vs-rabbitmq-vs-amazon-sns-vs-amazon-sqs-vs-google-pub-sub-4b57976438db
)


