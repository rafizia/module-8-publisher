Nama: Muhammad Rafi Zia Ulhaq<br>
NPM: 2206814551<br>
Kelas: Pemrograman Lanjut B<br>

# Module 8 - Publisher

### Reflection 1
a. Publisher akan mengirimkan 5 data ke broker pesan dalam satu kali run. Hal ini karena terdapat 5 panggilan ke `publish_event` yang mengirimkan pesan ke antrian "user_created".<br>
b. `amqp://` menunjukkan protokol yang digunakan, yaitu AMQP (Advanced Message Queuing Protocol), `guest:guest` adalah nama pengguna dan kata sandi yang digunakan untuk mengotentikasi koneksi ke server AMQP. `@localhost:5672` adalah alamat dan port dari server AMQP yang akan diakses. "localhost" menunjukkan bahwa server AMQP berjalan di _local machine_, sedangkan "5672" adalah nomor port default untuk koneksi AMQP.

### RabbitMQ
![alt text](https://github.com/rafizia/module-8-publisher/blob/master/image/RabbitMQ-1.png?raw=true)

### Reflection 2
![alt text](https://github.com/rafizia/module-8-publisher/blob/master/image/Subscriber-Publisher.png?raw=true)

Pesan tersebut mengindikasikan bahwa subscriber berhasil menerima dan memproses lima pesan yang dikirim oleh publisher. Setiap pesan mengandung informasi tentang pembuatan pengguna baru dengan ID dan nama pengguna yang sesuai.

### Reflection 3
![alt text](https://github.com/rafizia/module-8-publisher/blob/master/image/RabbitMQ-Spike.png?raw=true)

Spike pada grafik Message rate di RabbitMQ menunjukkan peningkatan jumlah pesan yang sedang dikirim ke broker RabbitMQ saat menjalankan publisher. Setiap kali menjalankan publisher dengan `cargo run`, publisher mengirim serangkaian pesan ke queue yang terdapat pada RabbitMQ yang akan direpresentasikan sebagai sebuah spike pada grafik Message rate.