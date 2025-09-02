# Hello World Deployment with Terraform

📌 Deskripsi
Project ini bertujuan untuk melakukan deployment sederhana menggunakan Terraform. Aplikasi yang dideploy hanya berupa halaman HTML berisi teks "Hello World" yang akan ditampilkan melalui web server (Apache) pada EC2 instance di AWS.

🚀 Arsitektur
-Terraform digunakan untuk Infrastructure as Code (IaC).
-AWS EC2 sebagai compute resource untuk menjalankan web server.
-Security Group untuk membuka akses port HTTP (80).
-User Data digunakan untuk otomatisasi instalasi Apache, cloning repository, dan menyalin file HTML ke web root.
-GitHub digunakan untuk menyimpan file challenge.html.

📂 Struktur Project
.
├── README.md
├── challenge.html
├── main.tf
└── user_data.sh

⚙️ Langkah Deployment

1.Buat folder/project baru di Cloud9 atau local environment.
2.Buat file challenge.html berisi:
  <h1>Hello World</h1>
3.Push project ini ke repository GitHub.
4.Jalankan terraform init untuk inisialisasi Terraform.
5.Jalankan terraform plan untuk melihat rencana deployment.
6.Jalankan terraform apply untuk membuat resource di AWS.
7.Terraform akan otomatis membuat:
  -EC2 instance
  -Security Group (allow HTTP 80)
  -Apache Web Server
  -Deployment file challenge.html
8.Akses Public IP EC2 di browser → akan muncul Hello World.

✅ Ekspektasi Output

Setelah terraform apply, hasil yang diharapkan:
  -EC2 instance berjalan.
  -Apache aktif dan melayani request HTTP.
  -Browser menampilkan tulisan Hello World.



