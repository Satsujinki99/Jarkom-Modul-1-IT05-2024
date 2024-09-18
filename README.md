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



   

