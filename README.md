# TECHNICAL TEST Frontend Challenge PT EIGEN TRI MATHEMA 

 

1. Terdapat string "NEGIE1", silahkan reverse alphabet nya dengan angka tetap diakhir kata Hasil = "EIGEN1" 

   Hasil pekerjaan dari saya : 

   ```JavaScript
    // Kata yang akan dibalikkan
   const kata = "NEGIE23";

   // Mencari posisi huruf terakhir dalam kata
   let lastHuruf = kata.length - 1;
   while (!isNaN(parseInt(kata[lastHuruf]))) {
     lastHuruf--;
   }

   // Membuat array dari huruf-huruf dalam kata
   const huruf = kata.slice(0, lastHuruf + 1).split("");

   // Membalikkan urutan array huruf
   const hurufTerbalik = huruf.reverse();

   // Menggabungkan kembali array huruf yang sudah dibalikkan dengan angka di belakangnya
   const kataTerbalik = hurufTerbalik.join("") + kata.slice(lastHuruf + 1);

   // Menampilkan hasilnya
   console.log(kataTerbalik);
   ```

   > Dalam kode di atas, kita memulai dengan mendefinisikan kata yang akan dibalikkan 	(dalam hal ini _**"NEGIE23"**_). Kemudian, kita mencari posisi huruf terakhir   dalam kata 	menggunakan sebuah _**loop**_ yang menghindari angka di belakangnya. 

   > Setelah itu, kita memisahkan setiap huruf dalam kata (tanpa angka di belakangnya) menggunakan metode _**slice()**_ dan menyimpannya dalam _**array**_ huruf. 

   > Selanjutnya, kita membalikkan urutan _**array**_ huruf dengan menggunakan metode _**reverse()**_ dan menyimpannya dalam _**array hurufTerbalik**_. Setelah itu, kita menggabungkan kembali _**array hurufTerbalik**_ menjadi satu _**string**_ menggunakan metode _**join()**_, dan menambahkan angka di belakangnya yang kita ambil sebelumnya menggunakan _**slice()**_. 

   > Terakhir, kita mencetak hasilnya menggunakan _**console.log()**_. 

 

2. Diberikan contoh sebuah kalimat, silahkan cari kata terpanjang dari kalimat tersebut, jika ada kata dengan panjang yang sama silahkan ambil salah satu : 

   Hasil Pekerjaan saya : 

    ```JavaScript
    const kalimat = "Saya sangat senang mengerjakan soal algoritma";
   const kataTerpanjang = kalimat.split(" ").sort((a, b) => b.length - a.length || a.localeCompare(b))[0];
   console.log("Kata terpanjang: " + kataTerpanjang);
   console.log("Ada: " + kataTerpanjang.length + "  karakter")
   ```

   > Dalam kode di atas, kita menggunakan _**split()**_ untuk memisahkan setiap kata dalam kalimat dan menghasilkan _**array**_ dari setiap kata tersebut. Kemudian, kita menggunakan metode _**sort()**_ untuk mengurutkan kata-kata dalam _**array**_ berdasarkan panjangnya dari yang terpanjang ke yang terpendek. 

   > Karena kita hanya ingin mengambil kata terpanjang pertama jika ada lebih dari satu kata dengan panjang yang sama, kita menggunakan operator _**||**_ untuk menambahkan pembandingan huruf _**(localeCompare())**_ sebagai kriteria kedua untuk memastikan bahwa kita selalu mengambil kata pertama dalam urutan abjad jika ada dua kata dengan panjang yang sama. 

   > Akhirnya, kata terpanjang tersebut disimpan dalam variabel kataTerpanjang dan dicetak menggunakan _**console.log()**_. 


 

3. Terdapat dua buah array yaitu array INPUT dan array QUERY, silahkan tentukan berapa kali kata dalam QUERY terdapat pada array INPUT 

   Hasil yang saya kerjakan: 

    ```JavaScript
    const INPUT = ['xc', 'dz', 'bbb', 'dz'];
   const QUERY = ['bbb', 'ac', 'dz'];

   for (let i = 0; i < QUERY.length; i++) {
     let count = 0;
     for (let j = 0; j < INPUT.length; j++) {
       if (QUERY[i] === INPUT[j]) {
         count++;
       }
     }
     console.log("Kata '" + QUERY[i] + "' ada " + count + " di dalam array INPUT.");
   }
   ```
 

   > Dalam kode di atas, kita menggunakan _**loop**_ pertama untuk mengiterasi setiap kata dalam _**array QUERY**_. Di dalam _**loop**_ tersebut, kita membuat _**variabel count**_ dan menginisialisasinya dengan nilai _**0**_ untuk menyimpan jumlah kemunculan setiap kata dalam _**array INPUT**_. 

   > Kemudian, kita menggunakan _**loop**_ kedua untuk mengiterasi setiap kata dalam array _**INPUT**_. Di dalam _**loop**_ tersebut, kita menggunakan _**if**_ untuk > membandingkan setiap kata dalam _**array INPUT**_ dengan kata saat ini dalam _**array QUERY**_. Jika kata yang sama ditemukan, variabel _**count**_ akan ditambah dengan _**1**_. 

   > Setelah _**loop**_ kedua selesai dijalankan, kita mencetak pesan dengan jumlah kemunculan setiap kata dalam _**array QUERY**_ di dalam _**array INPUT**_. 

 

4. Silahkan cari hasil dari pengurangan dari jumlah diagonal sebuah matrik NxN dari Contoh soal: 

   Hasil pekerjaan dari saya : 

    ```JavaScript
    const matrix = [[1, 2, 0], [4, 5, 6], [7, 8, 9]];
   let diagonal1 = 0;
   let diagonal2 = 0;

   for (let i = 0; i < matrix.length; i++) {
     diagonal1 += matrix[i][i];
     diagonal2 += matrix[i][matrix.length - 1 - i];
   }

   const result = diagonal1 - diagonal2;

   console.log("Hasil pengurangan diagonal: " + result);
   ```

   > Dalam kode di atas, kita menginisialisasi MATRIX MATRIX dengan nilai yang diberikan. Kemudian, kita membuat dua variabel untuk menyimpan jumlah diagonal pertama dan diagonal kedua, yaitu _**diagonal1**_ dan _**diagonal2**_. 

   > Kita menggunakan _**loop**_ untuk mengiterasi setiap elemen di dalam MATRIX MATRIX. Di dalam _**loop**_, kita menambahkan nilai diagonal pertama dengan nilai elemen matriks pada indeks yang sama di baris dan kolom. Sedangkan, nilai diagonal kedua ditambahkan dengan nilai elemen matriks pada indeks yang membentuk diagonal kedua. 

   > Setelah _**loop**_ selesai, kita menghitung hasil pengurangan dari kedua nilai diagonal dan menyimpannya dalam variabel _**result**_. Akhirnya, kita mencetak hasil pengurangan diagonal menggunakan _**console.log()**_. 
