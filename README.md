> a. How much data your publisher program will send to the message broker in one
run?

Publisher mengirimkan 5 messages yang berupa `UserCreatedEventMessage`.

> b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber
program, what does it mean?
 
 Artinya adalah publisher dan subscriber terkoneksi ke message broker amqp yang sama. Keduanya sama-sama menggunakan kredensial `guest` dan mengakses ke mesin `localhost` menggunakan port default amqp 5672.

 ## Running RabbitMQ
![Running RabbitMQ](images/running_rabbitmq.png)

## Sending and Processing Event
![Console Subscriber](images/console_subscriber.png)
---
![Console Publisher](images/console_publisher.png)

Ketika `cargo run` di konsol publisher (gambar bawah), publisher mengirimkan data ke broker RabbitMQ melalui koneksi protokol AMQP. Setelah itu, subscriber yang memang sudah berjalan dengan `cargo run` akan menerima dan memproses event dari publisher melalui RabbitMQ.