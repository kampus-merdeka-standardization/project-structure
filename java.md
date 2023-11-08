# Project Structure
Project Structure Definition

## Structure Example

```
tsel-directorat-appsname-domainname-service/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com.nama.group/
│   │   │       ├── config/
│   │   │       │   └── ContohConfig.java
│   │   │       ├── controller/
│   │   │       │   └── ContohController.java
│   │   │       ├── dto/
│   │   │       │   ├── request/
│   │   │       │   │   └── ContohRequest.java
│   │   │       │   └── response/
│   │   │       │       └── ContohResponse.java
│   │   │       ├── entity/
│   │   │       │   └── User.java /* dalam bentuk tunggal, bukan jamak */
│   │   │       ├── repository/
│   │   │       │   └── ContohRepository.java
│   │   │       ├── security/
│   │   │       ├── service/
│   │   │       │   ├── impl
│   │   │       │   │   └── ContohServiceImpl.java /* interface implementation */
│   │   │       │   └── ContohService.java /* interface */
│   │   │       ├── TselDirectoratAppsnameDomainnameServiceApplication.java
│   │   │       └── util/
│   │   │           └── ContohUtil.java
│   │   └── resources/
│   │       ├── application.yaml
│   │       └── static
│   └── test/
│       └── java/
│           └── com.nama.group/
│               ├── config/
│               │   └── ContohConfigTest.java
│               ├── controller/
│               │   └── ContohControllerTest.java
│               ├── dto/
│               │   ├── request/
│               │   │   └── ContohRequestTest.java
│               │   └── response/
│               │       └── ContohResponseTest.java
│               ├── entity/
│               │   └── UserTest.java 
│               ├── repository/
│               │   └── ContohRepositoryTest.java
│               ├── security/
│               ├── service/
│               │   └── ContohServiceTest.java
│               └── util/
│                   └── ContohUtilTest.java
├── .gitignore
├── Makefile
├── mvnw
├── mvnw.cmd
├── pom.xml
└── README.md
```


## Structure Definition

Berikut adalah struktur proyek yang disarankan untuk proyek Spring Boot:

1. **Nama Project**: 
    - tsel-directorat-appsname-domainname-service, atau
    - tsel-directorat-appsname-domainname-scheduler

2. **src/main/java**: Direktori ini berisi kode sumber utama Anda.
    - **com/nama/group**: Gantilah ini dengan nama domain organisasi. misal `com.telkomsel`.
        - **controller**: Berisi kontroler Spring MVC yang menangani permintaan HTTP. Kelas-kelas ini biasanya dianotasi dengan `@Controller`
        
        - **service**: Berisi kelas _service_, yaitu kelas yang berisi logika bisnis. Kelas-kelas ini biasanya dianotasi dengan `@Service`

        - **repository**: Berisi kelas repositori, yaitu kelas yang berisi kode yang berinteraksi langsung dengan basis data. Kelas-kelas ini biasanya dianotasi dengan `@Repository`

        - **entity**: Berisi kelas entity, yaitu kelas yang mewakili tabel dalam basis data. Kelas-kelas ini biasanya dianotasi dengan `@Entity`

        - **security**: Berisi kelas yang berhubungan dengan keamanan aplikasi, seperti autenticasi dan otorisasi.

        - **config**: Berisi kelas konfigurasi aplikasi. Kelas-kelas ini biasanya dianotasi dengan `@Configuration`

        - **dto**: DTO, atau _Data Transfer Object_, adalah objek yang digunakan untuk mengemas data yang akan ditransfer antara proses atau antara lapisan dalam aplikasi. Biasanya untuk mengemas `Request` & `Response` API.
        
        - **util**

    - **Application.java**: File ini mendeklarasikan metode utama, bersama dengan @SpringBootApplication.

3. **src/main/resources**: Direktori ini berisi sumber daya statis, template, dan file properti.
    - **static**: Berisi sumber daya statis seperti CSS, js, dan gambar.

4. **src/test**: Direktori ini berisi kode tes Anda.

5. **target**: Berisi file yang dihasilkan secara otomatis sebagai hasil dari proses build. Ketika aplikasi telah di-_build_, maka akan menghasilkan aplikasi yang berekstensi `.jar` dengan nama file `projectname-version.jar`

6. **.gitignore**:  File ini adalah konfigurasi untuk sistem kontrol versi Git. File ini berisi daftar file atau direktori yang akan diabaikan oleh Git saat melakukan commit. Dalam konteks proyek Spring Boot, direktori target biasanya ditambahkan ke .gitignore karena direktori ini berisi file yang dihasilkan saat build dan tidak perlu disertakan dalam repositori.

7. **Makefile**: Adalah file yang digunakan oleh utilitas make untuk membangun otomatis aplikasi. Makefile dapat digunakan untuk mendefinisikan serangkaian tugas untuk membangun dan menjalankan aplikasi1. Misalnya, Anda mungkin memiliki perintah untuk mengkompilasi kode Java Anda, menjalankan tes, dan membuat paket JAR.

8. **mvnw dan mvnw.cmd**:  File ini adalah skrip wrapper Maven. Skrip ini memungkinkan kita menjalankan perintah Maven tanpa harus menginstal dan menambahkan Maven ke PATH. Jika Maven tidak ditemukan di PATH, skrip ini akan mendownload dan menginstal Maven di lokasi default (direktori home pengguna). File mvnw digunakan untuk sistem operasi Unix-like (seperti Linux atau Mac), sedangkan mvnw.cmd digunakan untuk Windows.

9. **pom.xml**: File ini adalah file konfigurasi utama untuk proyek Maven. File ini mendefinisikan semua dependensi, plugin, versi, dan pengaturan lain yang diperlukan untuk membangun proyek kita.

10. **README.MD**: File ini biasanya berisi informasi tentang proyek, seperti deskripsi proyek, cara membangun dan menjalankan proyek, dan informasi lain yang mungkin berguna bagi pengguna atau pengembang lain.