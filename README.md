# PROJECT-UTS-PENGOLAHAN-CITRA
Tugas UTS Lporan. 202231026 MUHAMMAD NAUFAL ARIEF

#IDENTIFICATION COLOR (RGB)#

#LOAD IMAGE#

1.Di dalam skema warna HSV, "Hue" adalah nilai yang mewakili warna yang sebenarnya, "Saturation" adalah tingkat kecerahan warna, dan "Value" adalah tingkat kecerahan keseluruhan dari gambar.

2.Berikut adalah penjelasan singkat mengenai operasi yang Anda lakukan:

3.Membaca Gambar: Dengan menggunakan cv2.imread(), Anda membaca sebuah gambar dari file sistem. Pastikan path gambar yang diberikan benar sesuai dengan letak gambar tersebut di komputer Anda.

4.Konversi ke Skema Warna HSV: Setelah gambar dibaca, Anda menggunakan cv2.cvtColor() untuk mengonversinya dari skema warna BGR (umumnya digunakan dalam OpenCV) ke skema warna HSV. Ini dilakukan dengan menyediakan argumen cv2.COLOR_BGR2HSV yang menunjukkan konversi dari BGR ke HSV.

5..Setelah langkah-langkah ini, Anda akan memiliki gambar yang siap untuk dianalisis dalam skema warna HSV, yang biasanya digunakan untuk tugas-tugas seperti segmentasi warna, deteksi objek berdasarkan warna, dan sebagainya.


#DEFINISI DAN MENAMPILKAN#

1.Definisi Batas Warna: Anda menentukan batas-batas dalam skema warna HSV untuk warna merah, hijau, dan biru. Ini dilakukan dengan menentukan rentang nilai Hue, Saturation, dan Value yang mewakili warna yang ingin Anda deteksi.

2.Buat Mask untuk Setiap Warna: Setelah batas warna ditentukan, Anda menggunakan fungsi cv2.inRange() untuk membuat mask untuk setiap warna. Mask adalah gambar biner di mana piksel yang sesuai dengan kriteria warna berada dalam rentang yang ditentukan akan diatur ke nilai maksimum (biasanya 255), sedangkan yang lainnya diatur ke nilai minimum (biasanya 0).

3.Gabungkan Mask dengan Gambar Asli: Anda menggunakan cv2.bitwise_and() untuk menerapkan mask pada gambar asli. Ini akan menghasilkan gambar yang hanya menampilkan bagian dari gambar asli yang sesuai dengan kriteria warna yang ditentukan.

4.Tampilkan Gambar Hasil: Anda menggunakan Matplotlib untuk menampilkan gambar asli serta hasil dari setiap deteksi warna (merah, hijau, biru) dalam satu jendela gambar. Ini dilakukan dengan menggunakan subplot untuk menampilkan setiap gambar secara terpisah.


##HISTOGRAM##

1.Ambil Saluran Warna untuk Histogram: Anda menggunakan slicing untuk mengambil saluran warna merah, hijau, dan biru dari gambar. Ini adalah pendekatan yang benar karena dalam gambar OpenCV, saluran warna tersusun dalam urutan BGR, bukan RGB.

2.Tampilkan Histogram untuk Semua Saluran Warna dalam Subplot Pertama: Ini adalah langkah yang baik untuk melihat histogram untuk semua saluran warna secara bersamaan. Namun, perlu diperhatikan bahwa operasi ini harus dilakukan sebelum menampilkan subplot untuk histogram individual untuk setiap saluran warna.

3.Subplot untuk Histogram Gambar Asli: Subplot pertama seharusnya menampilkan histogram untuk semua saluran warna, sehingga kami menggabungkan tiga histogram menjadi satu subplot.

4.Menampilkan Histogram untuk Setiap Saluran Warna: Setelah menampilkan histogram untuk gambar asli, kita bisa menampilkan histogram untuk setiap saluran warna secara terpisah dalam subplot yang berbeda.

5.Penyajian Histogram: Terakhir, kami memastikan untuk membuat gambar terlebih dahulu dengan plt.figure(figsize=(15, 5)) sebelum menampilkan subplot, karena hal ini mempengaruhi tata letak keseluruhan.


#RECOGNATION RBG#

1.Membaca Gambar: Pertama, gambar dibaca dari path yang diberikan menggunakan cv2.imread(image_path).

2.Konversi ke HSV: Gambar kemudian dikonversi ke skema warna HSV menggunakan cv2.cvtColor(image, cv2.COLOR_BGR2HSV). Ini penting karena analisis warna akan dilakukan dalam skema warna HSV yang lebih sesuai daripada dalam skema warna RGB.

3.Definisikan Rentang Warna: Rentang warna untuk biru, merah, dan hijau dalam skema HSV ditentukan dengan menentukan nilai batas bawah dan atas untuk setiap warna.

4.Buat Mask: Mask dibuat untuk setiap warna menggunakan cv2.inRange() untuk mengekstraksi area dalam gambar yang sesuai dengan kriteria warna yang ditentukan.

5.Gabungkan Mask: Mask untuk warna merah kadang-kadang memerlukan penggabungan dari dua rentang warna karena nilai Hue merah memisah di ujung skala warna. Jadi, mask untuk merah diperoleh dengan menggabungkan dua mask menggunakan operasi bitwise OR.

6.Aplikasikan Mask ke Gambar Asli: Mask yang telah dibuat untuk setiap warna kemudian diterapkan ke gambar asli menggunakan cv2.bitwise_and() untuk mendapatkan area dalam gambar yang sesuai dengan kriteria warna.

7.Tampilkan Hasil: Hasil dari setiap warna yang diidentifikasi ditampilkan dalam subplot Matplotlib. Ini termasuk gambar asli dalam skema warna RGB dan hasil dari setiap warna yang diidentifikasi, yang telah dikonversi ke citra grayscale untuk ditampilkan. Penyertaan citra grayscale membantu untuk menyoroti area yang sesuai dengan warna yang diidenti
