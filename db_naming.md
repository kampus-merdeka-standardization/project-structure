# DB Naming

## Database Naming

Dalam penamaan database, sangat penting untuk menggunakan nama yang intuitif dan deskriptif sehingga memudahkan identifikasi dan pengelolaan. Nama database harus singkat namun informatif, menghindari penggunaan singkatan yang tidak jelas atau kepanjangan yang tidak perlu. Sebaiknya gunakan underscore (_) untuk memisahkan kata jika diperlukan, daripada menggunakan spasi atau karakter khusus lainnya. Penamaan yang konsisten dan standar akan memudahkan dalam proses backup, pemeliharaan, dan manajemen database.

Contoh:

- sales_data
- hr_management
- inventory_system


## Table Naming

Secara umum, nama tabel cenderung menggunakan bentuk jamak (plural) untuk mencerminkan bahwa mereka berisi kumpulan data, seperti "users" untuk menyimpan informasi pengguna. Nama tabel juga seharusnya bersifat deskriptif, mencerminkan dengan jelas isi dan fungsi tabel tanpa perlu melihat detail skema database. Penting untuk hindari penggunaan spasi dan karakter khusus dalam penamaan tabel. Konsistensi dalam penggunaan konvensi penamaan membantu membangun struktur basis data yang terorganisir dan mempermudah kolaborasi antar anggota tim pengembang.

Contoh:
- products
- customer_orders
- users

## Column Naming

Untuk penamaan kolom, ada beberapa hal yang perlu diperhatikan:

- Nama kolom harus mencerminkan jenis data dan makna yang disimpan di dalamnya. Misalnya, jika kolom berisi nama depan pengguna, maka nama kolomnya bisa `first_name`. Gunakanlah bahasa inggris.

- Penulisan dilakukan dengan `snake_case`, yaitu penulisan dengan huruf kecil dan menggunakan _undescore_ `_` sebagai pemisah.

- Nama kolom harus singkat namun jelas, menghindari penggunaan singkatan yang tidak baku atau kepanjangan yang tidak perlu. Sebaiknya gunakan kata-kata umum yang mudah dimengerti dan diingat.

- Nama kolom harus unik dalam tabel, tidak boleh ada dua kolom yang memiliki nama yang sama. Hal ini akan memudahkan dalam menulis query dan menghindari ambiguitas.

- Apabila ada kolom sebagai representasi dari baris pada tabel lain, gunakan dengan format `namatabel_namakolom`, misal `customer_id`.