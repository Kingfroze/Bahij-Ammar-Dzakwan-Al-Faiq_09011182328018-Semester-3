# TUGAS 6 PRAKTIKUM 5
## JOB CONTROL

Eksekusi seluruh profile yang ada :

a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut :

echo “Profile dari /etc/profile”

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_17-19-03.png)

b. Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu :

/home/stD02001/.bash_profile
![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_19-32-34.png)

/home/. stD02001/.bash_login
![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_19-35-40.png)

/home/mahasiswa/.profile
![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_19-37-00.png)

/home/mahasiswa/.bashrc
![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_20-08-55.png)

Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap

file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile :

echo “Profile dari .bash_profile”

Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yangbersangkutan.


c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:

$ su mahasiswa

$ exit

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_21-29-21.png)

kemudian gunakan opsi – sebagai berikut :

$ su – mahasiswa

$ exit

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_21-33-15.png)

Jelaskan perbedaan kedua utilitas tersebut.

1. su mahasiswa:  
Perintah su mahasiswa digunakan untuk beralih ke akun pengguna bernama "mahasiswa" tanpa mengubah lingkungan shell secara penuh. Dalam hal ini, hanya identitas pengguna yang berubah, tetapi variabel lingkungan (seperti $PATH, alias, dan pengaturan shell lainnya) tetap milik pengguna saat ini. Ini berarti beberapa program atau perintah mungkin tidak berfungsi dengan benar karena masih menggunakan konfigurasi dari pengguna asli.

2. su - mahasiswa:   
Sedangkan su - mahasiswa tidak hanya mengubah identitas pengguna, tetapi juga memulai sesi shell baru seperti halnya ketika pengguna "mahasiswa" masuk secara langsung. Semua variabel lingkungan akan direset sesuai dengan pengaturan default pengguna "mahasiswa", termasuk $HOME, $PATH, dan lainnya. Ini memberikan pengalaman yang lebih lengkap dan aman, seolah-olah Anda baru saja login sebagai "mahasiswa".

2. Prompt String (PS)

a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan
parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell

PS1=‟> „

export PS1

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-26_06-18-05.png)

b. Eksperimen hasil PS1 :

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_21-44-55.png)

3. Logout
Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout

Echo “Terima kasih atas sesi yang diberikan”

Sleep 5

clear

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_21-46-19.png)

4. Bash script

a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :

p1.sh

#! /bin/bash

echo “Program p1”

ls –l

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_21-47-32.png)


p2.sh

#! /bin/bash

echo “Program p2”

who

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_21-56-34.png)


p3.sh

#! /bin/bash

echo “Program p3”

ps x

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_21-57-45.png)

b. Jalankan script tersebut sebagai berikut :

./p1.sh ; ./p3.sh ; ./p2.sh

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_22-04-28.png)

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_22-05-00.png)

./p1.sh &

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_22-08-32.png)

./p1.sh $ ./p2.sh & ./p3.sh &

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_22-11-35.png)

( ./p1.sh ; ./p3.sh ) &

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_22-32-55.png)

5. Jobs

a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh,

setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil.

#!/bin/bash

while [ true ]

do

  date >> hasil
  
  sleep 10
  
done

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_22-42-31.png)

b. Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background
sebagai berikut :

$ jobs

$ find / -print > files 2>/dev/null &

$ jobs

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_22-58-32.png)

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_23-00-03.png)

c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut kebackground

$ fg %1

$ bg

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_23-01-11.png)

d. Stop program background dengan utilitas kil

$ ps x

$ kill [Nomor PID]

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_23-05-11.png)

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_23-05-28.png)

6. History
   
a. Ganti nilai HISTSIZE dari 1000 menjadi 20

$ HISTSIZE=20

$ h

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_23-07-17.png)

b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir dilakukan

$ !-5

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_23-17-46.png)

c. Ulangi instruksi yang terakhir. Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer

$ !!

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_23-18-44.png)

d. Ulangi instruksi pada history bufer nomor 150

$ !150

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_23-19-29.png)

e. Ulangi instruksi dengan prefix “ls”

$ !ls

![Alt Text](https://github.com/Kingfroze/Bahij-Ammar-Dzakwan-Al-Faiq_09011182328018-Semester3_Praktikum-SO/blob/main/galeri%20tugas%206%20praktikum%205/Screenshot_2024-09-25_23-20-44.png)
