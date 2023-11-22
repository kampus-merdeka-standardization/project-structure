# Artifact Naming

## Filename

Filename merupakan nama file dari hasil project yang telah di-build. Seperti contoh pada bahasa `java` akan menghasilkan file `.jar` dengan penamaan seperti

`projectname-version.jar`

atau

`projectname-version-optional(SNAPSHOT).jar`

Dan pada bahasa pemrograman lain seperti `Go` akan menghasilkan nama file seperti

`projectname-version.exe`

## Docker name
Ini adalah aturan penamaan docker name

projectname:tag

Penjelasan
1. project name adalah nama project yang digunakan, contoh **t**-marketing-luna-account-service. Untuk aturan lebih lengkapnya dapat dilihat di [project naming](/project_naming.md)
2. tag adalah version yang digunakan, contoh v1.0.0

Berikut adalah contoh docker name:
- **t**-marketing-luna-account-service:v1.0.0
- **t**-marketing-luna-account-scheduler:v2.1.1

## Destination

lokasi direktori di server tempat artifact akan ditempatkan setelah proses build dan deployment. Struktur direktori biasanya dibagi berdasarkan lingkungan deployment seperti Development (dev), User Acceptance Testing (uat), atau Production (prod). 
Pemisahan ini memastikan bahwa ada isolasi yang jelas antara lingkungan dan memudahkan pengelolaan versi aplikasi yang berbeda dalam siklus hidup pengembangan software.

ketentuan seperti ini : 
- /directorat/appsname/dev
- /directorat/appsname/uat
- /directorat/appsname/prod


