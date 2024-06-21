# Tugas 2 | Pembuatan API Subscription Sederhana
# Nama Anggota Kelompok
Nama    : I Nyoman Gede Candra Wikananta
NIM     : 2305551065

Nama    : Made Septino Budi Putrawan 
NIM     : 2305551083

## Perkenalan
Tugas 2 ini merupakan tugas yang mengharuskan mahasiswa untuk membuat sebuah backend API menggunakan bahasa pemrograman Java untuk sebuah sistem Subscrption sederhana. API ini nantinya akan digunakan untuk memanipulasi dan mengakses data pada sebuah database. API ini juga dapat meng-handle GET, POST, PUT, dan DELETE. Database nantinya akan disimpan pada software SQLite. Respon yang diberikan oleh server API dalam format JSON. Dan pengujian API dilakukan dengan software Postman.

## Struktur Program
API ini memiliki beberapa class yaitu class Controller, class Models, dan class Server. Masing - masing class memiliki fungsinya sendiri. Class untuk penempatan entitas ada pada class Models, class untuk keperluan database ada pada class Controller, dan untuk keperluan API ada pada class Server.

## Test Program dengan POSTMAN

### GET
GET/Customer
</br>

`http://localhost:9065/Customer`
</br>
Untuk mendapatkan daftar semua pelanggan atau customer. 
</br>
![alt text](<IMG/Screenshot (123).png>)

GET/Customer/{id}
`http://localhost:9065/Customer/1`
Untuk mendapatkan informasi lengkap milik salah satu pelanggan menggunakan id.
![alt text](<IMG/Screenshot (125).png>)

GET/Customer/{id}/Cards
`http://localhost:9065/Customer/1/Cards`
Untuk mendapatkan informasi daftar kartu kredit salah satu pelanggan menggunakan id.
![alt text](<IMG/Screenshot (127).png>)

GET/Customer/{id}/Subscriptions
`http://localhost:9065/Customer/1/Subscriptions`
Untuk mendapatkan daftar langganan atau subscription milik salah satu pelanggan menggunakan id.
![alt text](<IMG/Screenshot (128).png>)

GET/Customer/{id}/Subscriptions?Subscriptions_status=active
`http://localhost:9065/Customer/1/Subscriptions?Subscriptions_status=active`
Untuk mendapatkan daftar semua subscription milik pelanggan yang berstatus tertentu (active/cancelled).
![alt text](<IMG/Screenshot (129).png>)

GET/Subscriptions
`http://localhost:9065/Subscriptions`
Untuk mendapatkan daftar semua langganan atau subscriptions.
![alt text](<IMG/Screenshot (130).png>)

GET/Subscriptions?sort_by=current_term_end&sort_type=desc
`http://localhost:9065/Customer/1/Subscriptions`
Untuk mendapatkan daftar semua subscriptions atau langganan yang diurutkan berdasarkan current_term_end.
![alt text](<IMG/Screenshot (131).png>)

GET/Subscriptions/{id}
`http://localhost:9065/Subscriptions/1`
Untuk mendapatkan daftar langganan atau subscriptions berdasarkan salah satu id.
![alt text](<IMG/Screenshot (132).png>)

GET/Items
`http://localhost:9065/Items`
Untuk mendapatkan daftar semua items atau barang.
![alt text](<IMG/Screenshot (133).png>)

GET/Items?Is_active=true
`http://localhost:9065/Items?Is_active=true`
Untuk mendapatkan daftar semua barang atau produk yang masih meiliki status aktif.
![alt text](<IMG/Screenshot (134).png>)

GET/Items/{id}
`http://localhost:9065/Items/1`
Untuk mendapatkan informasi mengenai suatu items atau produk berdasarkan id.
![alt text](<IMG/Screenshot (135).png>)

### POST
POST/Customers
`http://localhost:9065/Customer`
Untuk membuat daftar pelanggan atau customer baru.
![alt text](<IMG/Screenshot (136).png>)

POST/Subscriptions
`http://localhost:9065/Items`
Untuk menambahkan daftar langganan atau subscriptions baru.
![alt text](<IMG/Screenshot (137).png>)

POST/Items
`http://localhost:9065/Subscriptions`
Untuk menambahkan daftar items atau barang baru.
![alt text](<IMG/Screenshot (138).png>)

### PUT
PUT/Customers/{id}
`http://localhost:9065/Customer/1`
Untuk mempebarui data pelanggan atau customer yang sudah ada.
![alt text](<IMG/Screenshot (139).png>)

PUT/Customers/{id}/Shipping_addresses/{id}
`http://localhost:9065/Customer/1/Shipping_addresses/1`
Untuk memperbarui data shipping addresses atau alamat pengiriman seorang pelanggan atau customer yang sudah ada.
![alt text](<IMG/Screenshot (140).png>)

PUT/Items/{id}
`http://localhost:9065/Items/1`
Untuk memperbarui data item atau produk yang sudah ada.
![alt text](<IMG/Screenshot (141).png>)


### DELETE
DELETE/Items/{id}
`http://localhost:9065/Items/6`
Untuk menghapus data item atau produk yang sudah ada berdasarkan id.
![alt text](<IMG/Screenshot (142).png>)

DELETE/Customers/{id}/Cards/{id}
`http://localhost:9065/Customer/1/Cards/2`
Untuk menghapus data kartu pelanggan atau customer yang sudah ada berdasarkan id.
![alt text](<IMG/Screenshot (143).png>)

### Error 404 dan 400
404 
`http://localhost:9065/Customer/13`
Data customer dengan Id 13(Datanya tidak tersedia pada database).
![alt text](<IMG/Screenshot (144).png>)

400
`http://localhost:9065/Customer/13:12`
(Format Id yang tidak sesuai).
![alt text](<IMG/Screenshot (145).png>)