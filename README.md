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
`http://localhost:9065/Customer`
![alt text](<IMG/Screenshot (123).png>)
Untuk mendapatkan daftar semua pelanggan atau customer.

GET/Customer/{id}
`http://localhost:9065/Customer/1`
![alt text](<IMG/Screenshot (125).png>)
Untuk mendapatkan informasi lengkap milik salah satu pelanggan menggunakan id.

GET/Customer/{id}/Cards
`http://localhost:9065/Customer/1/Cards`
![alt text](<IMG/Screenshot (127).png>)
Untuk mendapatkan informasi daftar kartu kredit salah satu pelanggan menggunakan id.

GET/Customer/{id}/Subscriptions
`http://localhost:9065/Customer/1/Subscriptions`
![alt text](<IMG/Screenshot (128).png>)
Untuk mendapatkan daftar langganan atau subscription milik salah satu pelanggan menggunakan id.

GET/Customer/{id}/Subscriptions?Subscriptions_status=active
`http://localhost:9065/Customer/1/Subscriptions?Subscriptions_status=active`
![alt text](<IMG/Screenshot (129).png>)
Untuk mendapatkan daftar semua subscription milik pelanggan yang berstatus tertentu (active/cancelled).

GET/Subscriptions
`http://localhost:9065/Subscriptions`
![alt text](<IMG/Screenshot (130).png>)
Untuk mendapatkan daftar semua langganan atau subscriptions.

GET/Subscriptions?sort_by=current_term_end&sort_type=desc
`http://localhost:9065/Customer/1/Subscriptions`
![alt text](<IMG/Screenshot (131).png>)
Untuk mendapatkan daftar semua subscriptions atau langganan yang diurutkan berdasarkan current_term_end.

GET/Subscriptions/{id}
`http://localhost:9065/Subscriptions/1`
![alt text](<IMG/Screenshot (132).png>)
Untuk mendapatkan daftar langganan atau subscriptions berdasarkan salah satu id.

GET/Items
`http://localhost:9065/Items`
![alt text](<IMG/Screenshot (133).png>)
Untuk mendapatkan daftar semua items atau barang.

GET/Items?Is_active=true
`http://localhost:9065/Items?Is_active=true`
![alt text](<IMG/Screenshot (134).png>)
Untuk mendapatkan daftar semua barang atau produk yang masih meiliki status aktif.

GET/Items/{id}
`http://localhost:9065/Items/1`
![alt text](<IMG/Screenshot (135).png>)
Untuk mendapatkan informasi mengenai suatu items atau produk berdasarkan id.

### POST
POST/Customers
`http://localhost:9065/Customer`
![alt text](<IMG/Screenshot (136).png>)
Untuk membuat daftar pelanggan atau customer baru.

POST/Subscriptions
`http://localhost:9065/Items`
![alt text](<IMG/Screenshot (137).png>)
Untuk menambahkan daftar langganan atau subscriptions baru.

POST/Items
`http://localhost:9065/Subscriptions`
![alt text](<IMG/Screenshot (138).png>)
Untuk menambahkan daftar items atau barang baru.

### PUT
PUT/Customers/{id}
`http://localhost:9065/Customer/1`
![alt text](<IMG/Screenshot (139).png>)
Untuk mempebarui data pelanggan atau customer yang sudah ada.

PUT/Customers/{id}/Shipping_addresses/{id}
`http://localhost:9065/Customer/1/Shipping_addresses/1`
![alt text](<IMG/Screenshot (140).png>)
Untuk memperbarui data shipping addresses atau alamat pengiriman seorang pelanggan atau customer yang sudah ada.

PUT/Items/{id}
`http://localhost:9065/Items/1`
![alt text](<IMG/Screenshot (141).png>)
Untuk memperbarui data item atau produk yang sudah ada.


### DELETE
DELETE/Items/{id}
`http://localhost:9065/Items/6`
![alt text](<IMG/Screenshot (142).png>)
Untuk menghapus data item atau produk yang sudah ada berdasarkan id.

DELETE/Customers/{id}/Cards/{id}
`http://localhost:9065/Customer/1/Cards/2`
![alt text](<IMG/Screenshot (143).png>)
Untuk menghapus data kartu pelanggan atau customer yang sudah ada berdasarkan id.

### Error 404 dan 400
404 
`http://localhost:9065/Customer/13`
![alt text](<IMG/Screenshot (144).png>)
Data customer dengan Id 13(Datanya tidak tersedia pada database).

400
`http://localhost:9065/Customer/13:12`
![alt text](<IMG/Screenshot (145).png>)
(Format Id yang tidak sesuai).