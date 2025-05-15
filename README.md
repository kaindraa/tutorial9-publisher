> a. How much data your publisher program will send to the message broker in one
run?

Publisher mengirimkan 5 messages yang berupa `UserCreatedEventMessage`.

> b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber
program, what does it mean?
 
 Artinya adalah publisher dan subscriber terkoneksi ke message broker amqp yang sama. Keduanya sama-sama menggunakan kredensial `guest` dan mengakses ke mesin `localhost` menggunakan port default amqp 5672.