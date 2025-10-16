Data Cuaca (Weather)

📝 Deskripsi

Aplikasi web sederhana untuk menampilkan data cuaca suatu kota menggunakan API dari OpenWeatherMap.
Dapat mencari kota/negara mana pun dan menampilkan suhu, kondisi cuaca, kecepatan angin, kuantitas awan, dan koordinat geografis.

🚀 Cara Menjalankan

Mengambil API key di https://openweathermap.org/api

Buka weather.html di browser dan masukkan nama kota/negara.

🧠 Teknologi yang Digunakan

HTML, CSS, dan JavaScript

OpenWeatherMap API

Ketik “Jambi” → muncul suhu (°C), kondisi (“Cloudy”), kecepatan angin, kuantitas awan, dan koordinat geografis.



🧩 Alur Logika Proyek

Input Data (Nama Kota / Negara)
Pengguna mengetik nama kota atau negara di kolom pencarian, misalnya “Jambi”, lalu menekan tombol “Cari” atau “Enter”.

Mengirim Permintaan ke API
JavaScript akan menangkap input tersebut dan membuat permintaan (fetch) ke OpenWeatherMap API menggunakan URL yang berisi:

https://api.openweathermap.org/data/2.5/weather?q={namaKota}&appid={API_KEY}&units=metric


Parameter:

q: nama kota dari input pengguna

appid: API key pribadi dari OpenWeatherMap

units=metric: agar suhu ditampilkan dalam derajat Celsius

Menerima dan Mengolah Respons API
Setelah permintaan dikirim, API mengembalikan data dalam format JSON, yang berisi informasi seperti suhu, kondisi cuaca, kecepatan angin, persentase awan, serta koordinat geografis (latitude dan longitude).

Menampilkan Data ke Halaman Web
JavaScript mengambil data yang relevan dari JSON tersebut, lalu menampilkannya di elemen HTML seperti:

🌡️ Suhu: main.temp

🌤️ Kondisi Cuaca: weather[0].description

💨 Kecepatan Angin: wind.speed

☁️ Kuantitas Awan: clouds.all

📍 Koordinat: coord.lat dan coord.lon

Dengan alur ini, aplikasi berjalan sederhana tapi jelas:
Input → Request ke API → Terima Data JSON → Tampilkan ke UI.
