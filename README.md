
1. Eksekusi seluruh profile yang ada : 

a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut : 
echo “Profile dari /etc/profile” 
![image](https://github.com/user-attachments/assets/bb5b4f9f-163a-4281-986c-0694fa3e312e)
![image](https://github.com/user-attachments/assets/73088f21-b8c0-4d0e-b3ed-0918b31ffe78)

![image](https://github.com/user-attachments/assets/eeda353e-bc38-4523-ad39-1817c6fef0e5)

b. Asumsi nama anda stD02001, maka edit semua profile yang ada 

Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap 
file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile : 
echo “Profile dari .bash_profile” 
Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang 
bersangkutan. 

-/home/stD02001/.bash_profile 

![image](https://github.com/user-attachments/assets/a0e4e9be-56c3-4bf3-a20b-4044c6a7eba3)
![image](https://github.com/user-attachments/assets/b47ae4eb-da90-4af8-a9d0-2e58df6eaccb)

![image](https://github.com/user-attachments/assets/fc3ae74d-7305-4578-83a2-cdd320f4df81)

-/home/. stD02001/.bash_login 

![image](https://github.com/user-attachments/assets/dada8fd5-5593-46a2-876c-077b955aa74b)
![image](https://github.com/user-attachments/assets/bba68842-3c4c-4e17-917a-d871b15de7ba)

![image](https://github.com/user-attachments/assets/225878fa-8eea-460f-adc3-b67283222aef)

-/home/mahasiswa/.profile 

![image](https://github.com/user-attachments/assets/90601023-b0a3-413f-acfa-37550a7b6251)
![image](https://github.com/user-attachments/assets/7fa9a68e-b8f8-4e33-a430-0d03037d2efa)

![image](https://github.com/user-attachments/assets/6bfd5935-44e1-4605-82c5-4d4deaf30099)

-/home/mahasiswa/.bashrc 

![image](https://github.com/user-attachments/assets/af46ebe0-8162-4e7a-afc5-a1c20e8825fe)
![image](https://github.com/user-attachments/assets/2ae2b082-c2a7-4bd3-b5ca-5fda6927f4d2)

![image](https://github.com/user-attachments/assets/26de372a-265b-43f8-bb1e-af25e326eea6)

c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut: 

$ su mahasiswa 

$ exit 

![image](https://github.com/user-attachments/assets/57e9b366-da69-477a-b1e7-73d4db6dc652)

kemudian gunakan opsi – sebagai berikut : 

$ su – mahasiswa

$ exit 

![image](https://github.com/user-attachments/assets/20ffc67e-7179-4d7e-a6e5-05fbe498b56d)

Jelaskan perbedaan kedua utilitas tersebut. 

2. Prompt String (PS) 

a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan 
parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell 

PS1=‟> „ 

export PS1 

![image](https://github.com/user-attachments/assets/e2a23251-d900-4e88-b58a-295070004373)

b. Eksperimen hasil PS1 :

$ PS1=“\! > “ 

69 > PS1=”\d > “ 

Mon Sep 23 > PS1=”\t > “ 

10:10:20 > PS1=”Saya=\u > “ 

Saya=mahasiswa > PS1=”\w >” 

~ > PS1=\h >” 

![image](https://github.com/user-attachments/assets/4fa31bd3-4c6f-4e94-8ee7-38e69aa11be0)

3. Logout 

Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout 

Echo “Terima kasih atas sesi yang diberikan”

Sleep 5 

clear 

![image](https://github.com/user-attachments/assets/fb0f5e4b-7847-4664-8f7b-f5f8f807895c)
![image](https://github.com/user-attachments/assets/34abb21d-1ee4-47bc-9370-e2032df4f533)

![image](https://github.com/user-attachments/assets/2bd34617-2f28-4849-a590-9f78c62a4c47)

![image](https://github.com/user-attachments/assets/6d660de5-b4ee-46b9-a1a8-88c2ffbeddb8)

![image](https://github.com/user-attachments/assets/81d10e91-efb3-4af0-86b9-a030e576e05c)

4. Bash script 

a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing : 

p1.sh 

#! /bin/bash 

echo “Program p1” 

ls –l 

![image](https://github.com/user-attachments/assets/f151442d-1f12-4eb2-8ee7-3903ae1c5e9e)
![image](https://github.com/user-attachments/assets/6f7f6cb8-b88e-489d-8632-ffc4aec0dd34)

p2.sh 

#! /bin/bash 

echo “Program p2” 

who 

![image](https://github.com/user-attachments/assets/40ffa8b3-f6e2-4e50-818e-bc5cb30f1292)
![image](https://github.com/user-attachments/assets/47bee1b3-c51b-49f5-b79a-e6333ba18fc8)

p3.sh 

#! /bin/bash 

echo “Program p3” 

ps x 

![image](https://github.com/user-attachments/assets/e972cf2c-03dc-4e94-8143-62d5962a7486)
![image](https://github.com/user-attachments/assets/3354756a-87f7-4b37-91fd-4957c914b36d)

b. Jalankan script tersebut sebagai berikut : 

$ ./p1.sh ; ./p3.sh ; ./p2.sh 

![image](https://github.com/user-attachments/assets/ea64d7e6-6a88-4e17-8c07-df03fba6c54c)

$ ./p1.sh & 

![image](https://github.com/user-attachments/assets/e7f97df1-6fae-4e48-8b56-beb8bccfbe83)

$ ./p1.sh $ ./p2.sh & ./p3.sh & 

![image](https://github.com/user-attachments/assets/b0eb379d-e603-466f-829f-57382ed5ca88)

$ ( ./p1.sh ; ./p3.sh ) & 

![image](https://github.com/user-attachments/assets/1b8bbafa-d6f1-4cde-82c1-7ff4c57be2d8)

5. Jobs 

a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh, 
setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil.

#!/bin/bash 

while [ true ] 

do 

date >> hasil 

sleep 10 

done 

![image](https://github.com/user-attachments/assets/5e17896c-28dd-4ea8-9047-ed7b39e39611)

b. Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background 
sebagai berikut : 

$ jobs 

$ find / -print > files 2>/dev/null & 

$ jobs 

![image](https://github.com/user-attachments/assets/25ba1380-cc35-4a34-b227-8ab1f317346d)

c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke 
background 

$ fg %1 

$ bg 

d. Stop program background dengan utilitas kil 
$ ps x 
$ kill [Nomor PID] 

![image](https://github.com/user-attachments/assets/a360c079-4881-4310-a603-3ef8e0528cec)
![image](https://github.com/user-attachments/assets/f205e83d-90f4-4584-9d78-1ce646b9aeaa)

6. History 
a. Ganti nilai HISTSIZE dari 1000 menjadi 20 
$ HISTSIZE=20 
$ h 
b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir
dilakukan 
$ !-5 
c. Ulangi instruksi yang terakhir. Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer 
$ !! 
d. Ulangi instruksi pada history bufer nomor 150 
$ !150 
e. Ulangi instruksi dengan prefix “ls” 
$ !ls
