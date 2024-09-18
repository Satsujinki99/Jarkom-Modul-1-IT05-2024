# Jarkom-Modul-1-IT05-2024

| Nama | NRP |
| ---- | :-: |
| Adlya Isriena Aftarisya | 5027231066 |
| Furqon Aryadana | 5027231024 |


## Rahasia.pcap
1. filter packet dengan frame contains “nNnM%coQuF”
   
   <img width="600" alt="Screenshot 2024-09-18 at 23 34 24" src="https://github.com/user-attachments/assets/df8d529a-7c34-466f-b71a-a526376f2e69">
   
2. Follow TCP stream
   
   <img width="600" alt="Screenshot 2024-09-18 at 23 36 39" src="https://github.com/user-attachments/assets/128e6d3c-a214-4b95-ad1f-47217a302561">

3. Jawab semua pertanyaan melalui terminal
   
   <img width="600" alt="Screenshot 2024-09-18 at 23 38 08" src="https://github.com/user-attachments/assets/cadaa236-b8f8-48b2-8845-c8a2a8593267">

Flag: JarkomIT{Tum8eN_p45SnYa_Ku4t_B1aS4Nya_xhTeEJhXJ9lyPTcQlZR0pkg1bL3q9naarUTm0YZuz6oWaTmURzDSM4h}

## Break.pcapng

1.Cari packet yang memilki info found dan ketika melakukan follow tcp tidak tertera tulisan “Username atau password salah!”

<img width="600" alt="Screenshot 2024-09-18 at 23 43 49" src="https://github.com/user-attachments/assets/29c740e6-c2f5-483f-9d23-c39755981916">


2. Jawab semua pertanyaan dari terminal berdasarkan informasi yang ada di packet yang ditemukan
   
<img width="454" alt="Screenshot 2024-09-18 at 23 44 32" src="https://github.com/user-attachments/assets/b3cf21f0-b26d-42a3-ba23-ef2e225d7c21">

Flag:JarkomIT{d34th_fr0m_th3_sky_64yKjxyPWT8YJOb6LQFMBTQq4H1Vw4NI4q1SWeWhbNT8hr5dopzQWW1}

## Sanity.pcap

1. Username: JaneD03
   Ddidapatkan dari http di nomor 67 text/html lalu follow http stream
   
<img width="600" alt="Screenshot 2024-09-18 at 23 50 00" src="https://github.com/user-attachments/assets/d3bd9cd0-5a70-44c5-a078-862b5f1724f3">

2. File yang dikirim: Clu3.txt
   a. Nemu di http no 79, disitu dia POST /upload.php -> follow http stream
   
   <img width="551" alt="Screenshot 2024-09-18 at 23 51 31" src="https://github.com/user-attachments/assets/8df21176-cd47-4aaa-a683-7815bf4f3f43">

   b.Isi pesan Clu3.txt ini diperintahkan cek peraturan soal shift, isinya adalah “cGVud29yZA==”
   
   c.Decode dengan base64 didapatkan “penword”
   
 Flag: JarkomIT{8uK4n_S4n1ty_b1a5A_5MytKj8MNLluuGunykFoymJNZSu5tQ4OUBBDMoc16XZI3xP8uD3NNIKK}



## Packet Barrage

1. Apa IP Address attacker? 
Liat source IP nya => 172.21.80.1

<img width="603" alt="Screenshot 2024-09-18 at 23 59 23" src="https://github.com/user-attachments/assets/6ffff907-5d7b-4109-867f-e66f99249979">

2. Berapa total brute force? Liat http stream terakhir ada di angka 1917

   <img width="381" alt="Screenshot 2024-09-19 at 00 00 30" src="https://github.com/user-attachments/assets/80a2ad7a-85d5-44ac-bd3e-ce228251e207">

3. Apa nama file yang didownload oleh attacker setelah berhasil login?
Liat di stream 1918 => Albatron.txt

<img width="599" alt="Screenshot 2024-09-19 at 00 01 53" src="https://github.com/user-attachments/assets/6848da73-bc47-4270-836c-85248ba5bc64">

Flag : Flag: JarkomIT{th3_fly1ng_c1rcus_0f_w4r_FUPhsDiqPGkX21zYVdhl99Lhz5StDceTWEmb7HN9S2OpCcXFvq2i8ACE}



## Corporate Breach

1. Siapa nama attacker? Follow TCP stream packet pertama
   ![image](https://github.com/user-attachments/assets/a206a348-ed37-4d2b-9691-3dcb246907d3)
   
2. Apa email yang digunakan untuk login? Filter htttp, cari yang di POST kemudian follow HTTP stream dan telusuri semua streamnya, disini kami menemukan email unik yaitu jarkomsupport@gmail.com
   ![image](https://github.com/user-attachments/assets/7e82b644-65f4-4ada-8a2a-ae93e957aa27)


3. Apa password yang digunakan untuk login? Bisa dilihat dari stream yang telah ditemukan sebelumnya, passwordnya adalah j4rk0mg4c0rbg



## Surprise
1. Apa service yang digunakan pada FTP server? Filter ftp, kemudian follow TCP stream, di bagian paling atas kami menemukan version ftp, yaitu vsFTPd 3.0.3
   ![image](https://github.com/user-attachments/assets/65c96d51-675b-44e6-a989-94821bd8fe12)

2. Apa nama file yang dikirim oleh attacker? Setelah ditelusuri kembali,pada stream 4  kami menemukan file yang dikirimkan user
   ![image](https://github.com/user-attachments/assets/0448a9b9-08f0-4414-9f49-8491d18e88f7)


3. Apa pesan yang ditinggalkan oleh attacker? Disini kami menduga bahwa pesan terdapat pada file g0tcha.cpp, maka setelah kami telusuri dan mendapatkan isi dari file cpp tersebut, kami mencoba untuk mengcompile file tersebut.
   ![image](https://github.com/user-attachments/assets/73bf4146-1dfe-47ad-9a76-8de4614443f3)




## Malicious Code
1. Berapa total attempt attacker melakukan dir listing? Karena berhubungan dengan direktori, disini kami menggunakan filter http contains “GET” dan mendapatkan semua direktori yang dikunjungi attacker. Total attempt nya adalah 52
   ![image](https://github.com/user-attachments/assets/e3f796ad-7628-4467-b0cf-b22ac992c09e)

2. Apa endpoint yang berhasil attacker dapatkan untuk login page? Disini kami menggunakan filter http dan melihat direktori di GET yang terakhir sebelum POST, yaitu /index.php. Alasan kami memilih GET terakhir sebelum POST karena pada POST attacker sudah mulai mencoba email dan password
   ![image](https://github.com/user-attachments/assets/3997c976-9bf9-4675-b799-05e166822480)


3. Pada attempt ke berapa attacker menemukan email dan password yang benar?
Untuk menjawab pertanyaan yang ini, kami melihat stream pada POST. percobaan email dan password di mulai dari stream 55, kemudian berhasil menemukan password pada stream 207, kemudian setelah kami hitung total attempt attacker adalah sebanyak 153 attempts.

4. Apa jawaban dari pertanyaan sang attacker? Untuk menemukan pertanyaan dari attacker, kami menelusuri stream kembali dan menemukan ini pada stream 221:
   ![image](https://github.com/user-attachments/assets/72264418-7c7e-4d76-904b-2aa19e50ea0d)
   Setelah ASCII tersebut di decode, akan didapatkan pesan seperti berikut:
apa warna favorit pembuat challenge? (hint: sweater)
Karena saya kurang tau, saya mencoba segala warna dan jawaban yang benar adalah merah.



## Rizzset
1. Apa nama domain dari dns query pada log?
Pertama-tama disini kami memilih protocol DNS dan follow UDP stream, domainnya adalah ww.its.ac.id
   ![image](https://github.com/user-attachments/assets/9e6ec228-1a3f-4722-9d1e-d9569f23c7f2)

2. berapa IP dari domain tersebut? Setelah kami lanjutkan penelusuran stream, kami menemukan ini:
   ![image](https://github.com/user-attachments/assets/bc5a8fb4-6ec6-4d53-b348-052be5054320)
Namun, angka tersebut salah jika langsung di submit, karena bentuknya yang terlihat kebalik, kami mencoba untuk membalik urutan angka tersebut menjadi 103.94.189.5

3. Tuliskan JARM Fingerprint yang dihasilkan dari domain tersebut. 
Untuk mendapatkan JARM Fingerprint dari domain yang telah didapatkan, saya menggunakan tools yang saya clone dari repository github. JARM fingerprint dari domain tersebut adalah ```2ad2ad16d2ad2ad22c2ad2ad2ad2ad74aaecca9f9c4a3303863dfee62b241e```
 


## Gajah Terbang (server recon)
1. Apa DBMS yang digunakan pada server tersebut? Untuk mengetahui DBMS yang digunakan, cukup melihat protocol saja, karena dari sini bisa dilihat bahwa DBMS yang digunakan adalah PostgreSQL
   ![image](https://github.com/user-attachments/assets/543da8c7-b07d-4b49-a7cb-162c36adc8d6)
   

2. Di port berapa DBMS server tersebut berjalan? Disini awalnya kami mencoba menjawab 5432, namun karena salah, kami mencoba submit 6969 dan jawabannya benar
   <img width="602" alt="image" src="https://github.com/user-attachments/assets/d7478eeb-1143-4147-adc7-be559e7dc437">

3. OS apa yang digunakan untuk server tersebut? Saat kami telusuri TCP stream, pada stream 8 kami menemukan informasi tentang OS yang digunakan, yaitu Debian
   <img width="607" alt="image" src="https://github.com/user-attachments/assets/303db3be-cdc1-4097-8bf6-9cbaa8f8a82e">

4. Apa credentials username DBMS valid yang digunakan?
Credential username yang valid bisa dilihat dari stream 8 juga, pada bagian atas:
<img width="599" alt="image" src="https://github.com/user-attachments/assets/c745e4ba-590d-4c25-a320-9c1ce6b0e5da">

5. Apa nama database yang digunakan?
Pada stream 9, nama database bisa dilihat pada bagian atas:
<img width="598" alt="image" src="https://github.com/user-attachments/assets/a92a6f74-bf11-4ed3-aaee-903e04e5edb3">

6. Ada berapa banyak users dalam database tersebut?
Banyaknya user bisa dilihat dari SELECT * FROM users;
<img width="596" alt="image" src="https://github.com/user-attachments/assets/83cfffb5-62de-4293-9038-8c928523bf9f">
Terdapat 4 users, yaitu Jojo, Kevin, Siska, dan Kunto.

7. Apa email yang digunakan oleh admin? 
Email yang digunakan oleh admin dapat dilihat dari SELECT * FROM users WHERE role=’admin’;
<img width="595" alt="image" src="https://github.com/user-attachments/assets/0b6435db-8687-4483-9c4d-0f6dbd30dbdb">

8. Apa password yang digunakan oleh admin? Sama seperti sebelumnya, password admin dapat dilihat setelah email admin, namun string tersebut masih dalam bentuk hash MD5, decode terlebih dahulu dan hasilnya adalah admin1234



## Gajah Terbang (Attacker Recon)
1. Akun apa yang dimiliki oleh penyerang dalam database tersebut, berikan emailnya!
<img width="592" alt="image" src="https://github.com/user-attachments/assets/deeb8530-dcbc-4668-8a1d-68f06e1172b0">
Jika dilihat informasi tersebut user dengan id=3 kelihatan sangat sus karena mengganti rolenya menjadi admin dan menghapus id nya dari banned_user. Maka bisa disimpulkan penyerangnya adalah kuntoajiisrillll@gmail.com

2. Apa password yang digunakan oleh penyerang?
<img width="599" alt="image" src="https://github.com/user-attachments/assets/c41cc032-0733-4237-8bfc-6527c5df22e2">
Karena passwordnya masih format hash MD5, decode terlebih dahulu agar mendapatkan password yang sebenarnya, yaitu kissme

3. Pada tanggal berapa akun penyerang diban? 
<img width="602" alt="image" src="https://github.com/user-attachments/assets/1d8e7b7b-b04c-4276-8ef9-2f8251b3ffed">
Bisa dilihat pada gambar tersebut, penyerang di ban pada tanggal 2024-06-09

4. Table apa saja yang dimodifikasi oleh penyerang?
Bisa dilihat pada gambar pada poin 1, penyerang memodifikasi tabel users dan banned_users

5. Barang apa saja yang telah dibeli oleh penyerang?
<img width="596" alt="image" src="https://github.com/user-attachments/assets/2f5b08e2-4c57-4995-9cc0-10924d2e2a29">
Karena penyerang memiliki userid=3 maka kita lihat pada tabel transactions terdapat 2 transaksi yang dilakukan userid=3, yaitu rokok dan es krim

6. Berapa total transaksi dari barang yang dibeli oleh penyerang?
Totalnya dapat dihitung dengan menjumlahkan harga rokok dan es krim yang terdapat pada tabel products, yaitu 18000 + 6500 = 24500




## 22 Nightmare
1. File yang dikirim penyerang?
<img width="595" alt="image" src="https://github.com/user-attachments/assets/1f77536e-60eb-4e6a-9206-a15558014d4c">
Disini saya menggunakan filter FTP kemudian follow TCP stream, dan pada stream 3 terdapat informasi seperti digambar. File yang dikirim oleh penyerang adalah sh1k4.jpg

2. Apa nama file yang dikirim? Pertanyaan ini sangat membuat saya bingung karena pertanyaannya sama dengan pertanyaan yang sebelumnya namun jika submit jawaban yang sama, salah. Kemudian saya coba untuk mencari file lain dengan memfilter ftp contains “STOR”
<img width="598" alt="image" src="https://github.com/user-attachments/assets/4031c80d-0d57-46d0-855d-a10f0618a1b9">
Namun noko juga bukan jawaban yang tepat. Maka setelah itu saya mencoba untuk meng-export kedua file ini:
<img width="598" alt="image" src="https://github.com/user-attachments/assets/eeeccf3f-1774-4a79-9ba7-639f8c7bc282">
Dan setelah saya lihat isi dari sh1k4 terdapat tulisan “NUN” yang kemudian saya submit dan jawabannya benar.

3. Pada stream keberapa file kedua dikirim setelah file pertama? Ini tinggal menghitung jarak dari stream yang ada STOR sh1k4 dan STOR noko. Jawabanya adalah 141

 4. Siapa asli nama pengirim?
Pada bagian ini jika dilihat dari isi noko.py:
<img width="596" alt="image" src="https://github.com/user-attachments/assets/afe6921f-43aa-48a9-97fe-4a684d916a8a">
Nampaknya diminta untuk melakukan operasi XOR dengan key NUN, hasilnya akan seperti berikut: hallo im Torako Koshi, maka jawabannya adalah Torako Koshi










   

