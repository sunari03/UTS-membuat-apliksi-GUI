# UTS-membuat-apliksi-GUI
#TekniklnformatikaUPB #UniversitasPelitaBangsa


https://www.youtube.com/watch?v=VjtwpsP4_dE


1. Step pertama buka MATLAB, yang tampilan keseluruhan window-nya kira-kira seperti berikut:

 ![image](https://user-images.githubusercontent.com/56722786/117447363-405baa80-aef2-11eb-9284-e75bb5ff1827.png)


2. Jika sudah dibuka, selanjutnya di command window-nya ketikkan perintah guide dan tekan ENTER:

![image](https://user-images.githubusercontent.com/56722786/117447760-bb24c580-aef2-11eb-9889-c61833a797fc.png)


3. Pilih aja ‘BLANK Gui (default)’ dan klik ‘OK’ yang selanjutnya Anda akan digiring menuju tampilan sebagai berikut:

![image](https://user-images.githubusercontent.com/56722786/117447971-fe7f3400-aef2-11eb-8964-8d454a436d93.png)


4. Jika sudah pencet CTRL + S atau pada menunya klik save as:

![image](https://user-images.githubusercontent.com/56722786/117448054-18b91200-aef3-11eb-8466-c206e83ed1e7.png)


5. Dan save di komputer Anda dan beri nama misalnya test1:

![image](https://user-images.githubusercontent.com/56722786/117448118-30909600-aef3-11eb-84c6-e025800f8c3a.png)


6. Jika sudah, nanti di folder itu akan terbuat (tergenerate) sebuah m file yang namanya itu menyesuaikan dengan nama .fig file yang sudah kita simpan tadi.

6

7. Dan ini secara otomatis akan tampil di editor MATLAB:

7

8. Hal yang perlu pembaca pahami adalah di file editor ini kita tidak boleh melakukan pengeditan secara sembarangan, karena nama-nama variabel atau function di file ini sudah disesuaikan dengan file .fig yang menjadi pasangannya.  Di dalam m file ini terdapat opening-function yang dieksekusi ketika GUI nya pas mulai tampil. Dan ini fungsinya hampir miriplah dengan konstruktor di bahasa java. Untuk saya pribadi biasanya di opening-function ini saya taruh perintah clc, jadi ketika GUI nya tampil,  maka command-windownya dibersihkan dulu.

8

9. Kita kemudian menambahkan beberapa control pada file fig nya tadi, misalnya sebuah button dan sebuah textfield (atau dalam terminologi MATLAB nya disebut sebagai static text), caranya tinggal di drag n drop aja dari panel sebelah kiri:

9

10. Selanjutnya untuk mengeset nilai dari control-control tadi, tinggal klik kanan kemudian ‘Property Inspector’ dan kemudian muncul window buat pengaturan properties-nya:

10
11

11. Di window property inspector itu selanjutnya kita bisa mengatur beberapa hal, misalnya dengan mengganti text dari button-nya menjadi sesuatu yang lain, contoh kita ganti textnya menjadi ‘BUTTON MAKAN’, caranya lihat ke baris String, dan pada kolom di kanannya berikan text sesuai dengan yang Anda kehendaki, setelah itu CTRL + S:

12

12. Jadi Button tadi sudah berubah tampilan

13

13. Untuk memberikan fungsi pada tombol tadi, misalnya jika dia di-klik akan menghasilkan nilai tertentu, maka hal yang dilakukan adalah mengatur variabel pada property inspector nya yakni pada baris CallBack. Nah di situ kan di kolom sebelah kanan ada icon tertentu yang Anda boleh klik:

14

14. Jika sudah di-klik, nanti di m file nya ter-generate (maaf saya kurang tahu apa bahasa Indonesia yang tepat untuk menerjemahkan kata generate, tapi menurut Prof. Bobby Eka Gunara yang jadi dosen di ITB, itu diterjemahkan sebagai membangkitkan, tapi berhubung ini membahas MATLAB maka saya abaikan dulu ajaran beliau itu) sebuah fungsi yang disesuaikan dengan nama dari tombol tadi. Nama tombol ini bisa dilihat pada baris tag pada property inspector:

15

16

15. Jadi jika kita meng-klik tombol/button tadi, maka apapun perintah yang valid yang ditempatkan di dalam fungsi pushbutton1_Callback ini akan dieksekusi.
16. Selain itu, fungsi utama dari baris Tag dari property Inspector ini adalah agar kita bisa mengakses button tadi dari m-file. Misalnya kita ingin mengeprint  text pada button tadi ketika button tersebut di klik, maka yang dilakukan adalah tempatkan perintah berikut pada function pushbutton1_Callback:

17

Jadi dapat kita lihat, bahwa handles  di sini mengacu pada parameter ketiga dari  function pushbutton1_Callback, yang mana ini menyimpan global variabel dari m file nya yang merupakan nilai-nilai yang diset pada fig file. Jadi dalam kasus pushbutton1, handles.pushbutton1 merupakan tag dari button ini. Itu yang kita panggil dan kita tampung dalam variabel y. Kemudian dengan get(y, ‘string’) maka kita mengambil nilai string nya atau text yang ditampilan pada pushbutton1. Dan ini akan ditampilkan pada output.
Sebenarnya banyak hal sih yang bisa kita atur dari property inspector ini.


di 5:04 AM 1 Comment
Label: MATLAB 
Email This
BlogThis!
Share to Twitter
Share to Facebook
Share to Pinterest

