2. Berikut adalah penjelasan mengenai langkah-langkah analisis yang dilakukan:

#CITRA#
Definisi Batas Warna dalam Skema Warna HSV:

Anda menentukan rentang nilai untuk Hue, Saturation, dan Value (disebut juga Hue, Saturation, dan Brightness) dalam skema warna HSV untuk setiap warna yang ingin diidentifikasi. Rentang ini menentukan wilayah warna dalam skema HSV yang akan dianggap sebagai warna merah, hijau, dan biru.
Buat Mask untuk Setiap Warna:

Setelah menentukan rentang warna dalam skema HSV, Anda menggunakan fungsi cv2.inRange() untuk membuat mask untuk setiap warna. Mask adalah gambar biner di mana piksel yang berada dalam rentang warna yang ditentukan akan diatur ke nilai maksimum (biasanya 255), sedangkan piksel di luar rentang akan diatur ke nilai minimum (biasanya 0). Dengan demikian, mask akan menyoroti area dalam gambar yang sesuai dengan warna yang ditentukan.
Gabungkan Mask dengan Gambar Asli:

Mask untuk setiap warna kemudian diterapkan ke gambar asli menggunakan operasi bitwise AND dengan fungsi cv2.bitwise_and(). Ini menghasilkan gambar yang hanya menampilkan bagian dari gambar asli yang sesuai dengan kriteria warna yang ditentukan.
Tampilkan Hasil dalam Satu Jendela Gambar:

Rentang Warna Merah!!:

Anda menetapkan rentang Hue dari 0 hingga 10, yang berarti Anda memilih warna yang berada di sekitar ujung spektrum warna merah (yang juga termasuk nilai yang mendekati 0 setelah 180 dalam skema warna HSV karena HSV berulang). Rentang ini mencakup warna merah murni.
Rentang Saturation dan Value dari 100 hingga 255 menunjukkan bahwa Anda ingin memilih warna merah dengan kecerahan (saturation) dan intensitas (value) yang cukup tinggi. Rentang ini memungkinkan Anda untuk mengabaikan warna merah yang sangat gelap atau pucat.

Rentang Warna Hijau!!:

Rentang Hue dari 50 hingga 70 menunjukkan bahwa Anda ingin mendeteksi warna yang berada di sekitar spektrum warna hijau. Rentang ini mencakup warna hijau murni serta warna yang sedikit mendekati kuning dan biru karena nilai Hue berada di antara kedua warna tersebut.
Seperti dalam rentang warna merah, rentang Saturation dan Value dari 100 hingga 255 menunjukkan bahwa Anda ingin memilih warna hijau dengan kecerahan dan intensitas yang cukup tinggi.

Rentang Warna Biru:

Rentang Hue dari 110 hingga 130 menunjukkan bahwa Anda ingin mendeteksi warna yang berada di sekitar spektrum warna biru. Rentang ini mencakup warna biru murni serta warna yang sedikit mendekati ungu dan hijau karena nilai Hue berada di antara kedua warna tersebut.
Rentang Saturation dan Value dari 100 hingga 255 menunjukkan bahwa Anda ingin memilih warna biru dengan kecerahan dan intensitas yang cukup tinggi, serupa dengan yang telah dijelaskan sebelumnya.
Dengan menggunakan rentang war


#HISTOGRAM

Histogram Gambar Asli:

Histogram untuk saluran warna merah ditampilkan dalam warna merah dengan alpha 0.5 untuk transparansi. Ini memberikan visualisasi distribusi intensitas piksel merah dalam gambar.
Histogram untuk saluran warna hijau ditampilkan dalam warna hijau dengan alpha 0.5. Ini memberikan visualisasi distribusi intensitas piksel hijau dalam gambar.
Histogram untuk saluran warna biru ditampilkan dalam warna biru dengan alpha 0.5. Ini memberikan visualisasi distribusi intensitas piksel biru dalam gambar.
Rentang sumbu x dari 0 hingga 256 mewakili nilai intensitas piksel dalam skala 8-bit (0-255).
Rentang sumbu y menunjukkan jumlah piksel dalam gambar yang memiliki nilai intensitas tertentu.
Label legenda 'Red', 'Green', dan 'Blue' di sudut atas kiri menunjukkan saluran warna yang sesuai dengan histogram.

Histogram Saluran Warna Merah:

Histogram untuk saluran warna merah ditampilkan dalam subplot kedua.
Rentang sumbu x dari 0 hingga 256 mewakili nilai intensitas piksel dalam skala 8-bit (0-255).
Rentang sumbu y menunjukkan jumlah piksel dalam gambar yang memiliki nilai intensitas merah tertentu.
Warna histogram adalah merah, menunjukkan distribusi intensitas piksel merah dalam gambar.
Judul histogram adalah 'Histogram Red'.

Histogram Saluran Warna Hijau:

Histogram untuk saluran warna hijau ditampilkan dalam subplot ketiga.
Rentang sumbu x dari 0 hingga 256 mewakili nilai intensitas piksel dalam skala 8-bit (0-255).
Rentang sumbu y menunjukkan jumlah piksel dalam gambar yang memiliki nilai intensitas hijau tertentu.
Warna histogram adalah hijau, menunjukkan distribusi intensitas piksel hijau dalam gambar.
Judul histogram adalah 'Histogram Green'.
Histogram Saluran Warna Biru:

Histogram untuk saluran warna biru:
Rentang sumbu x dari 0 hingga 256 mewakili nilai intensitas piksel dalam skala 8-bit (0-255).
Rentang sumbu y menunjukkan jumlah piksel dalam gambar yang memiliki nilai intensitas biru tertentu.
Warna histogram adalah biru, menunjukkan distribusi intensitas piksel biru dalam gambar.
Judul histogram adalah 'Histogram Blue'.

#COLOR RECOGNATION#

#IDENTIFIER FUNCTION
Baca Gambar dan Konversi ke Ruang Warna HSV:

Pertama, fungsi membaca gambar dari path yang diberikan menggunakan OpenCV (cv2.imread()).
Gambar tersebut kemudian dikonversi ke ruang warna HSV menggunakan cv2.cvtColor() untuk memfasilitasi identifikasi warna berdasarkan skema warna Hue, Saturation, dan Value (HSV).
Definisikan Rentang Warna untuk Setiap Warna:

Rentang warna yang ditetapkan dalam skema warna HSV untuk setiap warna adalah:
Biru: Hue dari 110 hingga 130, Saturation dari 100 hingga 255, dan Value dari 100 hingga 255.
Merah: Rentang merah didefinisikan dalam dua rentang (0-10 dan 160-180) untuk menangani kasus di mana warna merah melintasi batas 0 dan 180 dalam skema warna HSV. Rentang Saturation dan Value adalah sama dengan biru.
Hijau: Hue dari 50 hingga 70, Saturation dari 100 hingga 255, dan Value dari 100 hingga 255.
Buat Mask untuk Setiap Warna:

Mask dibuat untuk setiap rentang warna menggunakan cv2.inRange() untuk mengidentifikasi area dalam gambar yang sesuai dengan rentang warna yang ditetapkan.
Gabungkan Hasil Mask untuk Setiap Warna:

Hasil mask untuk setiap warna kemudian digabungkan menggunakan operasi bitwise AND (cv2.bitwise_and()) dengan gambar asli. Ini menghasilkan gambar yang hanya menampilkan area yang sesuai dengan warna yang telah diidentifikasi.
Kembalikan Hasil Identifikasi Warna:

Fungsi mengembalikan tiga gambar terpisah yang mewakili area yang memiliki warna biru, merah, dan hijau dalam gambar asli.
