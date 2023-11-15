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
1. project name adalah nama project yang digunakan, contoh tsel-marketing-luna-account-service. Untuk aturan lebih lengkapnya dapat dilihat di [project naming](/project_naming.md)
2. tag adalah version yang digunakan, contoh v1.0.0

Berikut adalah contoh docker name:
- tsel-marketing-luna-account-service:v1.0.0
- tsel-marketing-luna-account-scheduler:v2.1.1

## Destination
/directorat/appsname/dev ||
/directorat/appsname/uat ||
/directorat/appsname/prod
