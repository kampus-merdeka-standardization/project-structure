# Project Structure
Berikut ini merupakan tata letak dasar untuk proyek aplikasi NestJS. ini bukan standar resmi yang ditetapkan oleh tim pengembang NestJS, namun ini merupakan sejumlah pola tata letak proyek historis dan terkini yang umumnya digunakan dalam ekosistem NestJS. Beberapa pola ini lebih populer daripada yang lain.

## Structure Example
```bash
.project-name
├── Makefile
|   # file Makefile berisi perintah yang dapat Anda jalankan dengan `make`.
├── package.json
|   # File package.json berisi konfigurasi proyek Node.js termasuk dependencies dan scripts.
|
├── tsconfig.json
|   # File tsconfig.json berisi konfigurasi TypeScript compiler.
|
├── node_modules/
|   # Folder node_modules berisi semua paket yang diinstal melalui npm atau yarn.
|
├── dist/
|   # Folder dist berisi file JavaScript yang dikompilasi dari TypeScript siap untuk produksi.
|
├── src/
|   # Folder src adalah tempat utama dimana kode TypeScript aplikasi berada.
|   |
│   ├── app.module.ts
|   |   # File app.module.ts adalah modul root yang menghubungkan semua modul lain.
|   |
│   ├── main.ts
|   |   # File main.ts adalah titik masuk aplikasi yang mem-bootstrapping modul root.
|   |
│   ├── modules/
|   |   # Folder modules berisi kode yang dibagi per fitur atau domain.
|   |
│   ├── common/
|   |   # Folder common berisi fungsi atau komponen yang digunakan secara umum di aplikasi.
|
├── test/
|   # Folder test berisi pengujian aplikasi, baik itu unit test atau e2e test.
|
├── config/
|   # Folder config berisi file konfigurasi untuk berbagai environment aplikasi.
|
├── public/
|   # Folder public berisi file statis yang dapat diakses publik, seperti robots.txt atau favicon.
|
├── views/
|   # Folder views berisi template untuk aplikasi yang melayani HTML secara langsung.
|
├── assets/
|   # Folder assets berisi sumber daya seperti gambar, stylesheet, dan JavaScript yang digunakan oleh views.
|
├── .env
|   # File .env digunakan untuk menyimpan variabel lingkungan yang tidak seharusnya dikomit ke repositori.

```


## Structure Definition
### Direktori Utama Aplikasi

#### `/src`

Direktori ini berisi kode sumber aplikasi Anda. Ini adalah tempat utama di mana kode TypeScript aplikasi berada.

#### `/src/config`

Direktori ini berisi konfigurasi aplikasi Anda. Anda dapat mengatur variabel lingkungan dan konfigurasi lainnya di sini.

#### `/src/entity`

Direktori ini berisi entitas database Anda. Entitas adalah kelas yang memetakan ke tabel database.

#### `/src/auth`

Direktori ini berisi kode untuk otentikasi. Ini biasanya mencakup hal-hal seperti strategi otentikasi, pengecekan peran, dan lainnya.

#### `/src/common`

Direktori ini berisi modul global NestJS dan beberapa konstanta, antarmuka, dan lainnya. Ini biasanya mencakup hal-hal yang digunakan di banyak tempat dalam aplikasi Anda.

#### `/src/shared`

Direktori ini berisi modul NestJS yang dibagi. Ini biasanya mencakup hal-hal yang digunakan di banyak modul dalam aplikasi Anda.

#### `/src/gql`

Direktori ini berisi struktur GraphQL. Ini biasanya mencakup skema GraphQL, resolver, dan lainnya.

### Direktori Tambahan Aplikasi

#### `/test`

Direktori ini berisi pengujian aplikasi, baik itu unit test atau e2e test. Biasanya, setiap modul atau layanan memiliki file test tersendiri.

#### `/config`

Direktori ini berisi file konfigurasi untuk berbagai environment aplikasi. Anda dapat mengatur variabel lingkungan dan konfigurasi lainnya di sini.

#### `/public`

Direktori ini berisi file statis yang dapat diakses publik, seperti robots.txt atau favicon.

#### `/views`

Direktori ini berisi template untuk aplikasi yang melayani HTML secara langsung. Ini biasanya digunakan jika Anda menggunakan template engine seperti Pug atau EJS.

#### `/assets`

Direktori ini berisi sumber daya seperti gambar, stylesheet, dan JavaScript yang digunakan oleh views.

### File Utama Aplikasi

#### `Makefile`

File ini berisi perintah yang dapat Anda jalankan dengan `make`. Ini biasanya digunakan untuk menyederhanakan dan mengotomatiskan tugas-tugas seperti membangun, menjalankan, atau menguji aplikasi Anda.

#### `package.json`

File ini berisi metadata aplikasi dan daftar dependensi. Ini adalah file konfigurasi utama untuk proyek Node.js.

#### `tsconfig.json`

File ini berisi konfigurasi TypeScript compiler. Ini memberitahu compiler bagaimana mengubah kode TypeScript Anda menjadi JavaScript.

#### `.env`

File ini digunakan untuk menyimpan variabel lingkungan yang tidak seharusnya dikomit ke repositori. Ini biasanya digunakan untuk menyimpan rahasia seperti kunci API atau kredensial database.
