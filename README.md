# SIG_Teori_Basic14
 
# Making a Map (QGIS3)
1.	Kita download terlebih dahulu Natural Earth quick start
2.	Kemudian klik properties -> variable dan cari project_languenge (nama_en) Kemudian kita refresh
3.	Klik layer kemudian centang bagian z5 1:18m
4.	Klik project -> new print layout (ctrl p)
5.	Di jendela Tata Letak Cetak, klik tombol penuh Zoom untuk menampilkan seluruh tata letak.
6.	Sekarang kita harus membawa tampilan peta yang kita lihat di Kanvas QGIS ke tata letak. Pergi ke Tambahkan Item ->add map.
7.	Setelah klik add map aktif, tahan tombol kiri mouse dan seret persegi panjang tempat Anda ingin memasukkan peta.
8.	Gunakan Edit -> Pilih/Pindahkan item dan Edit -> Pindahkan opsi Konten untuk menggeser peta di jendela dan memusatkannya di komposer.
9.	Kemudian kita menyesuaikan tingkat zoom untuk peta. Klik pada tab Properti Item dan masukkan 100000000 sebagai nilai Skala.
10.	Sekarang kita akan menambahkan inset peta yang menunjukkan tampilan yang diperbesar untuk area Tokyo. Sebelum kita membuat perubahan apa pun pada layer di jendela QGIS utama, centang kotak Lock layers dan Lock styles untuk layers. Ini akan memastikan bahwa jika kita mematikan beberapa layer atau mengubah gaya mereka, tampilan ini tidak akan berubah.
11.	Kemudian Alihkan jendela Tata Letak Cetak. lalu Tambahkan Item ->Tambahkan Peta.
12.	Seret persegi panjang di tempat kita ingin menambahkan inset peta.kita sekarang akan melihat bahwa kita memiliki 2 objek peta di Tata Letak Cetak. Saat membuat perubahan, pastikan Anda telah memilih peta yang benar.
13.	Pilih objek Map 2 yang baru saja kita tambahkan dari panel Items. Pilih tab Properti item. Gulir ke bawah ke panel Bingkai dan centang kotak di sebelahnya. kita dapat mengubah warna dan ketebalan batas bingkai sehingga mudah dibedakan dengan latar belakang peta.
14.	Salah satu fitur yang rapi dari Print Layout adalah dapat secara otomatis menyorot area dari peta utama yang diwakili dalam inset. Pilih objek Peta 1 dari panel Item. Di tab Properti item, gulir ke bawah ke bagian Gambaran Umum. Klik tombol Tambahkan gambaran umum baru.
15.	Pilih Peta 2 sebagai Bingkai Peta. Ini memberi tahu Tata Letak Cetak untuk menyorot objek saat ini Peta 1 dengan luas peta yang ditunjukkan pada objek Peta 2.
16.	Sekarang setelah kita menyiapkan inset peta, kita akan menambahkan grid ke peta utama. Pilih objek Peta 1 dari panel Item. Di tab Properti item, gulir ke bawah ke bagian Kisi. Klik tombol Tambahkan kisi baru, diikuti oleh Ubah kisi.
17.	Secara default, garis kisi menggunakan unit dan proyeksi yang sama dengan proyeksi peta yang saat ini dipilih. Namun, lebih umum dan berguna untuk menampilkan garis kisi dalam derajat. Kita dapat memilih CRS yang berbeda untuk grid. Klik pada Perubahan... di sebelah CRS.
18.	Pilih nilai Interval sebagai 5 derajat dalam arah X dan Y. kita dapat menyesuaikan Offset untuk mengubah di mana garis kisi muncul.
19.	Gulir ke bawah ke bagian Bingkai kisi dan centang kotak Gambar koordinat. Format default adalah Derajat tetapi muncul sebagai angka. Kita dapat menyesuaikan adalah menambahkan simbol ° . Pilih Kustom dan klik tombol Ekspresi di sampingnya.
20.	Masukkan ekspresi berikut untuk membuat string yang mengambil nomor kisi dan menambahkan simbol ° ke dalamnya concat(to_string(@grid_number), '° ')
21.	Sekarang kita akan menambahkan bingkai Persegi Panjang untuk menahan elemen peta lain seperti panah utara, skala dan label. Pergi ke Tambahkan Item -> Tambahkan Bentuk ‣ Tambahkan Persegi Panjang.
22.	Anda dapat mengubah Gaya persegi panjang agar sesuai dengan latar belakang peta.
23.	Sekarang kita akan menambahkan Panah Utara ke peta. QGIS hadir dengan koleksi gambar terkait peta yang bagus termasuk banyak jenis Panah Utara. Klik Tambahkan Item -> Tambahkan Gambar.
24.	Sambil menahan tombol kiri mouse, gambar persegi panjang. Di panel sebelah kanan, klik pada tab Properti Item dan perluas bagian Direktori pencarian dan pilih gambar yang Anda sukai.
25.	Sekarang kita akan menambahkan bilah skala. Klik Tambahkan Item ‣ Tambahkan Scalebar.
26.	Klik pada tata letak di mana Anda ingin bilah skala muncul. Di tab Properti Item, pastikan Anda telah memilih elemen peta yang benar Peta 1 untuk menampilkan bilah skala. Pilih Gaya yang sesuai dengan kebutuhan Anda. Di panel Segmen, ubah Lebar tetap menjadi 200 unit dan sesuaikan segmen sesuai keinginan Anda.
27.	Sudah waktunya untuk memberi label pada peta kita. Klik Tambahkan Item -> Tambahkan Label.
28.	Klik pada peta dan gambar kotak di mana label seharusnya berada. Di tab Properti Item, perluas bagian Label dan masukkan label untuk peta. Demikian pula tambahkan label lain untuk kredit data dan perangkat lunak.
29.	Setelah kita puas dengan peta, Anda dapat mengekspornya sebagai Gambar, PDF atau SVG. Untuk tutorial ini, mari kita ekspor sebagai gambar. Klik Tata Letak -> Ekspor sebagai Gambar.
30.	Simpan gambar dalam format yang Anda sukai. Di bawah ini adalah gambar PNG yang diekspor.
linknya https://github.com/miaaprilia18/SIG_Teori_Basic_GIS_operations/blob/main/Project%201.jpeg

# Working with Attributes (QGIS3)
1.	Pertama kita download terlebih dahulu https://www.qgistutorials.com/downloads/ne_10m_populated_places_simple.zip
2.	Temukan file yang kita download ne_10m_populated_places_simple.zip di Browser QGIS dan perluas. Pilih file ne_10m_populated_places_simple.shp dan seret ke kanvas.
3.	Lapisan baru ne_10m_populated_places_simple sekarang akan dimuat di QGIS dan Anda akan melihat banyak titik yang mewakili tempat-tempat berpenduduk di dunia. Tampilan default di kanvas QGIS menunjukkan geometri lapisan GIS. Setiap poin juga memiliki atribut terkait. Mari kita lihat mereka. Temukan Toolbar Atribut. Toolbar ini berisi banyak alat yang berguna untuk memeriksa, melihat, memilih, dan memodifikasi atribut lapisan.
4.	Klik tombol Identifikasi pada Toolbar Atribut. Setelah alat dipilih, klik pada titik mana pun di kanvas. Atribut terkait dari titik tersebut akan ditampilkan di panel Identifikasi Hasil baru. Setelah Anda selesai menjelajahi atribut dari poin yang berbeda, Anda dapat mengklik tombol Tutup.
5.	Klik tombol Buka Tabel Atribut pada Toolbar Atribut. Anda juga dapat mengklik kanan layer ne_10m_populated_places_simple dan memilih Open Attribute Table.
6.	You can scroll horizontally and locate the pop_max column. This field contains the population of the associated place. You can click twice on the field header to sort the column in descending order.
7.	Sekarang kita siap untuk melakukan kueri kita pada atribut ini. QGIS menggunakan ekspresi seperti SQL untuk melakukan kueri. Klik Pilih fitur menggunakan tombol ekspresi.
8.	Di jendela Pilih Menurut Ekspresi, perluas bagian Bidang dan Nilai dan klik ganda label pop_max. Anda akan melihat bahwa itu ditambahkan ke bagian ekspresi di bagian bawah. Jika Anda tidak yakin tentang nilai bidang, Anda dapat mengklik tombol Semua Unik untuk melihat apa nilai atribut yang ada dalam himpunan data. Untuk latihan ini, kami ingin menemukan semua fitur yang memiliki populasi lebih dari 1 juta. Jadi lengkapi ekspresi seperti di bawah ini dan klik Pilih Fitur lalu Tutup.
9.	Anda akan melihat bahwa beberapa baris dalam tabel atribut sekarang dipilih. Jendela label juga berubah dan menunjukkan jumlah fitur yang dipilih.
10.	Tutup jendela tabel atribut dan kembali ke jendela QGIS utama. Anda akan melihat bahwa subset poin sekarang diberikan dalam warna kuning. Ini adalah hasil dari kueri kami dan poin yang dipilih adalah poin yang memiliki nilai atribut pop_max lebih besar dari 10000000.
11.	Mari kita perbarui kueri kami untuk menyertakan syarat bahwa tempat tersebut juga harus menjadi modal selain memiliki populasi yang lebih besar dari 1 juta. Untuk masuk ke editor ekspresi dengan cepat, Anda bisa menggunakan tombol Pilih Fitur menurut Ekspresi di Toolbar Atribut.
12.	Bidang yang berisi data tentang huruf kapital adalah adm0cap. Nilai 1 menunjukkan bahwa tempat itu adalah modal. Kita dapat menambahkan kriteria ini ke ekspresi kita sebelumnya menggunakan dan operator. Masukkan ekspresi seperti di bawah ini dan klik Pilih Fitur lalu Tutup.
13.	Return to the main QGIS window. Now you will see a smaller subset of the points selected. This is the result of the second query and shows all places from the dataset that are country capitals as well as have population greater than 1 million.
14.	Sekarang kita akan mengekspor fitur yang dipilih sebagai layer baru. Klik kanan layer ne_10m_populated_places_simple dan pergi ke Export -> Save Selected Features As
15.	Anda dapat memilih format apa pun yang Anda sukai sebagai Format. Untuk latihan ini, kami akan memilih GeoJSON. GeoJSON adalah format berbasis teks yang digunakan secara luas dalam pemetaan web. Klik tombol ... di sebelah Nama file dan masukkan populated_capitals.geojson sebagai file output.
16.	The input data has many columns. You are able to choose only a subset of the original columns for export. Expand the Select fields to export and their export options section. Click Deselect All and check the name and pop_max columns. Click OK.
17.	Data input memiliki banyak kolom. Anda hanya dapat memilih subset dari kolom asli untuk diekspor. Perluas bagian Pilih bidang untuk diekspor dan opsi ekspornya. Klik Batal pilih Semua dan periksa nama dan kolom pop_max. Klik Oke.
18.	Layer baru populated_capitals akan dimuat di QGIS. Anda dapat menghapus centang pada layer ne_10m_populated_places_simple untuk menyembunyikannya dan melihat titik-titik dari layer yang baru diekspor.
linknya https://github.com/miaaprilia18/SIG_Teori_Basic_GIS_operations/blob/main/Working%20with%20Attributes%20T2.qgz dan https://github.com/miaaprilia18/SIG_Teori_Basic_GIS_operations/blob/main/projek%202.png

# Importing Spreadsheets or CSV files (QGIS3)
1.	Pertama kita download terlebih dahulu https://www.qgistutorials.com/downloads/earthquakes_2021_11_25_14_31_59_+0530.tsv file ini
2.	Klik tombol Buka Manajer Sumber Data pada Toolbar Sumber Data. Anda juga dapat menggunakan pintasan keyboard Ctrl + L.
3.	Dalam kotak dialog Manajer Sumber Data, beralihlah ke tab Teks Terbatas. Klik tombol ... di sebelah Nama file.
4.	Tergantung pada sistem operasi, Anda mungkin atau mungkin tidak melihat file di lokasi yang diunduh. Dalam Format file, beralihlah ke Semua file (*; .) untuk melihat file tsv.
5.	Sekarang Anda akan melihat file yang diunduh. Pilih itu dan klik Buka.
6.	Dalam kotak dialog Manajer Sumber Data, jalur ke file akan tersedia di Nama File. Ubah nama Layer menjadi 1900_2000_earthquakes. Di bagian Format file, pilih Pembatas kustom dan centang Tab. Di bagian Definisi geometri, pilih Koordinat titik. Secara default bidang X dan nilai bidang Y akan diisi secara otomatis jika menemukan bidang nama yang sesuai di input. Anda dapat mengubahnya jika impor memilih bidang yang salah. Anda dapat membiarkan Geometry CRS ke EPSG:4326 - WGS 84 CRS default. Jika file Anda berisi koordinat dalam CRS yang berbeda, Anda dapat memilih CRS yang sesuai di sini. Klik Tambahkan.
7.	Anda sekarang akan melihat bahwa data akan diimpor dan ditampilkan di kanvas QGIS sebagai layer baru yang disebut 1900_2000_earthquakes dengan CRS EPSG:4326.
linknya https://github.com/miaaprilia18/SIG_Teori_Basic_GIS_operations/blob/main/project3.png dan https://github.com/miaaprilia18/SIG_Teori_Basic_GIS_operations/blob/main/project3.png

# Basic Vector Styling (QGIS3)
1.	Buka zip kedua himpunan data ke folder di komputer Anda. Di Panel Browser QGIS, cari direktori tempat Anda mengekstrak data. Perluas folder dan pilih layer. Seret layer ke kanvas.ne_10m_landne_10m_land.shp
2.	Anda akan mendapatkan layer baru yang ditambahkan ke panel Layers. Database pembangkit listrik global hadir sebagai file CSV, jadi kita perlu mengimpornya. Klik tombol Buka Manajer Sumber Data pada Toolbar Sumber Data. Anda juga dapat menggunakan pintasan keyboard.ne_10m_landCtrl + L
3.	Di jendela Manajer Sumber Data, beralihlah ke tab Teks Terbatas. Klik tombol ... di sebelah Nama file dan telusuri ke direktori tempat Anda mengekstrak file. Pilih file . QGIS akan secara otomatis mendeteksi bidang pembatas dan geometri. Biarkan Geometri CRS ke nilai default . Klik Tambahkan diikuti oleh Tutup.globalpowerplantdatabasev120.zipglobal_power_plant_database.csvEPSG:4326 - WGS84
4.	Layer baru akan ditambahkan ke panel Layers dan Anda akan melihat titik-titik yang mewakili pembangkit listrik di kanvas. Sekarang kita siap untuk menata kedua lapisan ini. Klik tombol Open the Layer Styling panel di bagian atas panel Layers.global_power_plant_database
5.	Panel Layer Styling akan terbuka di sebelah kanan. Pilih layer terlebih dahulu. Ini akan menjadi lapisan dasar kita sehingga kita dapat menjaga gaya minimalis sehingga tidak mengganggu. Klik dan gulir ke bawah. Pilih warna Isian sesuai keinginan Anda. Klik drop-down di samping Warna goresan dan pilih . Ini akan mengatur garis besar poligon tanah menjadi transparan. Anda akan melihat hasil seleksi Anda diterapkan segera ke layer.ne_10m_landSimple fillTransparent Stroke
6.	Selanjutnya pilih layer. Klik dan gulir ke bawah. Pilih penanda segitiga.global_power_plant_databaseSimple marker
7.	Gulir ke atas dan pilih warna Isian yang Anda sukai. Teknik kartografi yang berguna adalah memilih versi warna isian yang sedikit lebih gelap sebagai warna Stroke. Daripada mencoba untuk memilih secara manual, QGIS memberikan ekspresi untuk mengontrol ini lebih tepat. Klik tombol Penggantian yang ditentukan data dan pilih Edit.
8.	Masukkan ekspresi berikut untuk mengatur warna menjadi 30% lebih gelap dari warna isian dan klik OK.
9.	Anda akan melihat bahwa tombol Data defined override di sebelah warna Stroke telah berubah menjadi kuning - menunjukkan bahwa properti ini dikendalikan oleh override. Rendering simbol tunggal dari lapisan pembangkit listrik tidak terlalu berguna. Itu tidak menyampaikan banyak informasi kecuali lokasi pembangkit listrik. Mari kita gunakan perender yang berbeda untuk membuatnya lebih berguna. Klik drop-down Simbologi dan pilih perender.Categorized
10.	Lapisan berisi atribut yang menunjukkan bahan bakar utama yang digunakan di setiap pembangkit listrik. Kita dapat membuat gaya di mana setiap jenis bahan bakar unik ditampilkan dalam warna yang berbeda. Pilih sebagai kolom. Klik Klasifikasikan. Anda akan muncul beberapa kategori dan rendering peta berubah sesuai dengan itu.global_power_plant_databaseprimary_fuel
11.	Sementara tampilan Kategori berguna, lapisan ini berisi terlalu banyak kategori bagi seseorang untuk menafsirkan peta secara bermakna. Pendekatan yang lebih baik adalah mengelompokkan jenis kategori bahan bakar tertentu dan mengurangi jumlah kelas. Mari kita coba membuat 3 kategori - Bahan bakar terbarukan, Bahan bakar tidak terbarukan dan Lainnya. Pilih perender. Pilih semua kecuali satu aturan dengan menahan tombol dan mengklik setiap baris. Setelah dipilih, klik tombol Hapus aturan yang dipilih untuk menghapusnya.Rule-basedCtrl
12.	Pilih aturan yang tersisa dan klik Edit aturan saat ini.
13.	Masukkan sebagai label. Klik tombol Ekspresi di samping Filter.Renewable fuel
14.	Dalam dialog Penyusun String Ekspresi, masukkan ekspresi berikut dan klik OK. Di sini kami mengelompokkan beberapa kategori energi terbarukan ke dalam satu kategori.
15.	Gulir ke bawah dan klik Penanda sederhana. Pilih warna Isian yang sesuai. Setelah selesai, klik tombol Kembali.
16.	Anda akan melihat satu aturan diterapkan pada lapisan untuk kategori bahan bakar terbarukan. Klik kanan baris dan pilih Salin. Klik kanan lagi dan pilih Tempel.
17.	Salinan aturan yang ada akan ditambahkan. Pilih baris yang baru ditambahkan dan klik Edit aturan saat ini.
18.	Masukkan sebagai label. Klik tombol Ekspresi di samping Filter.Non-renewable fuel
19.	Dalam dialog Penyusun String Ekspresi, masukkan ekspresi berikut dan klik OK.
20.	Gulir ke bawah dan klik Penanda sederhana. Pilih warna Isian yang sesuai. Setelah selesai, klik tombol Kembali.
21.	Ulangi proses Salin/Tempel untuk menambahkan aturan ketiga. Pilih dan klik Edit aturan saat ini.
22.	Masukkan sebagai label. Pilih Lainnya - Tangkap semua untuk fitur lain alih-alih Filter. Ini akan memastikan bahwa setiap kategori yang terlewatkan dalam 2 aturan sebelumnya, akan ditata oleh aturan ini. Gulir ke bawah dan klik Penanda sederhana. Pilih warna Isian yang sesuai. Setelah selesai, klik tombol Kembali.Othe
23.	Kategorisasi ulang selesai sekarang. Anda akan melihat pandangan yang jauh lebih bersih yang menunjukkan distribusi sumber bahan bakar terbarukan vs. tidak terbarukan yang digunakan oleh pembangkit listrik dan distribusinya di seluruh negara. Namun ini tidak memberikan gambaran yang lengkap. Kita dapat menambahkan variabel lain ke styling. Daripada menampilkan semua spidol dengan ukuran seragam, kita dapat menunjukkan ukuran yang sebanding dengan kapasitas pembangkit listrik setiap pabrik. Teknik kartografi ini disebut pemetaan Multivariat. Klik kanan aturan dan pilih Ubah Ukuran.Renewable fuel
24.	Klik tombol Penggantian yang ditentukan data di sebelah Ukuran. Pilih Edit.
25.	Karena kapasitas pembangkit listrik sangat bervariasi di antara himpunan data kami, cara yang efektif untuk mendapatkan kisaran kecil untuk ukuran adalah dengan menggunakan fungsi ini. Anda dapat bereksperimen dengan ekspresi yang berbeda untuk sampai pada apa yang paling cocok untuk visualisasi pilihan Anda. Masukkan ekspresi berikut dan klik OK.log10
26.	Ulangi proses yang sama untuk aturan lain.
27.	Setelah puas, Anda dapat menutup panel Layer Styling.
28.	Melihat visualisasi akhir kami, Anda dapat langsung melihat pola dalam himpunan data. Misalnya, di Eropa ada lebih banyak pembangkit listrik yang menggunakan sumber energi terbarukan, tetapi kapasitasnya lebih rendah daripada pembangkit yang menggunakan sumber energi tak terbarukan. 
linknya https://github.com/miaaprilia18/SIG_Teori_Basic_GIS_operations/blob/main/project%204.qgz dan https://github.com/miaaprilia18/SIG_Teori_Basic_GIS_operations/blob/main/project%204.png

# Calculating Line Lengths and Statistics (QGIS3)
1.	Temukan file yang diunduh di panel Browser dan perluas. Seret file ke kanvas.ne_10m_railroads_north_america.zipne_10m_railroads_north_america.shp
2.	melihat layer baru dimuat di panel Layers. Anda akan melihat bahwa lapisan tersebut memiliki garis yang mewakili jalur kereta api untuk seluruh Amerika Utara. Sekarang, mari kita hitung panjang setiap fitur baris. Pergi ke Pemrosesan ‣ Kotak Alat.ne_10m_railroads_north_america.
3.	Cari dan temukan geometri Vektor ‣ Tambahkan algoritma atribut geometri. Klik dua kali untuk meluncurkannya.
4.	Dalam dialog Tambahkan Atribut Geometri, pilih sebagai lapisan Input. Sistem Referensi Koordinat (CRS) lapisan input adalah EPSG:4326 WGS84. Ini adalah CRS Geografis dengan Lintang dan Bujur sebagai koordinat, WGS84 sebagai ellipsoid dan derajat sebagai satuan. Karena lintang dan bujur tidak memiliki panjang standar, Anda tidak dapat mengukur jarak atau area secara akurat menggunakan fungsi geometri planar. Untungnya, QGIS menyediakan cara yang lebih baik untuk menghitung jarak menggunakan geometri ellipsoidal, yang merupakan metode paling akurat untuk lapisan yang mencakup area yang luas seperti ini. Pilih sebagai opsi Hitung menggunakan. Klik Jalankan. Setelah proses selesai, klik Tutup.ne_10m_railroads_north_americaEllipsoidal
5.	Anda akan melihat layer baru dimuat di panel Layers. Ini adalah salinan layer input dengan kolom baru ditambahkan untuk jarak. Klik kanan layer dan pilih Open Attribute Table.Added geom infoAdded geom info
6.	Dalam Tabel Atribut, Anda akan melihat kolom baru yang disebut jarak. Ini berisi panjang setiap fitur baris dalam meter. Perhatikan juga bahwa atribut sov_a3 yang berisi kode negara untuk setiap fitur. Tutup jendela Tabel Atribut.
7.	Sekarang kita memiliki panjang segmen jalur kereta api individu, kita dapat menambahkannya untuk menemukan total panjang rel kereta api. Tetapi karena pernyataan masalah menuntut kita membutuhkan panjang kereta api total di Amerika Serikat, kita harus menggunakan hanya segmen yang terkandung di AS. Kita dapat menggunakan nilai kode negara di kolom sov_a3 untuk memfilter layer. Klik kanan layer dan pilih Filter.Added geom info
8.	Dalam dialog Penyusun Kueri, masukkan ekspresi berikut dan klik OK.
9.	melihat ikon Filter muncul di sebelah layer di panel Layers yang menunjukkan bahwa filter diterapkan ke layer. Anda juga dapat mengonfirmasi secara visual bahwa layer sekarang berisi segmen garis hanya untuk Amerika Serikat. Sekarang kita siap untuk menghitung jumlahnya. Klik tombol Tampilkan ringkasan statistik pada Toolbar Atribut.Added geom info
10.	Panel Statistik baru akan terbuka. Pilih layer dan kolom.Added geom infolength
11.	 berbagai statistik ditampilkan di panel. Satuan statistik sama dengan satuan kolom - meter. Mari kita ubah perhitungan untuk menggunakan kilometer sebagai gantinya. Klik ikon Ekspresi di sebelah menu tarik-turun bidang di panel Statistik.length
12.	Masukkan ekspresi berikut dalam Dialog Ekspresi yang mengonversi panjang menjadi kilometer. Length /1000
13.	Nilai Sum yang ditampilkan adalah total panjang rel kereta api di AS
link https://github.com/miaaprilia18/SIG_Teori_Basic_GIS_operations/blob/main/project5.qgz dan https://github.com/miaaprilia18/SIG_Teori_Basic_GIS_operations/blob/main/project5.png

# Basic Raster Styling and Analysis (QGIS3)
1.	Buka QGIS dan cari file yang diunduh di panel Browser. Perluas file dan seret file ke kanvas.gpw-v4-population-count-rev11_2000_2pt5_min_tif.zipgpw-v4-population-count-rev11_2000_2pt5_min.tif
2.	Layer baru akan ditambahkan ke panel Layers. Demikian pula, cari file dan seret file ke kanvas.gpw-v4-population-count-rev11_2000_2pt5_mingpw-v4-population-count-rev11_2010_2pt5_min_tif.zipgpw-v4-population-count-rev11_2010_2pt5_min.tif
3.	Mari kita jelajahi lapisan-lapisan ini. Klik tombol Identifikasi pada Toolbar Atribut. Setelah alat dipilih, klik pada titik mana pun di kanvas.
4.	Nilai yang terkait dengan piksel tersebut akan ditampilkan di panel Identifikasi Hasil baru. Di panel Identifikasi Hasil, ubah Mode menjadi . Ini akan menampilkan nilai piksel dari semua raster, bukan hanya lapisan paling atas. Bandingkan nilai dari kedua lapisan. Karena resolusi raster sekitar 5km x 5km, nilai piksel mewakili total populasi di area tersebut (25 km persegi) yang diwakili oleh piksel.Top down
5.	Tutup panel Identifikasi Hasil. Mari kita buat visualisasi layer yang lebih baik. Klik tombol Open the layer Styling panel di panel Layers.
6.	Di panel Layer Styling, klik dropdown Render type dan pilih renderer.Singleband pseudocolor
7.	Perender ini akan menata layer menggunakan ramp warna. Ramp warna default adalah putih-merah di mana nilai minimum akan ditetapkan warna putih dan nilai maksimum pada layer akan diberi warna merah. Nilai menengah akan diberi warna interpolasi linier merah. Perluas Pengaturan Nilai Min / Maks dan pilih opsi. Anda akan melihat bahwa visualisasi peta jauh lebih baik sekarang. Rentang data standar diatur dari 2% hingga 98% dari nilai data, yang berarti bahwa outlier tidak akan digunakan untuk mengatur nilai minimum dan maksimum, menghasilkan visualisasi yang jauh lebih representatif.Cumulative count cut
8.	Tutup panel Layer Styling. Kita dapat menerapkan gaya yang serupa ke lapisan lain juga. Tetapi ada cara yang lebih mudah untuk mentransfer gaya dari satu lapisan ke lapisan lainnya. Klik kanan layer dan pilih Styles ‣ Copy Style.gpw-v4-population-count-rev11_2010_2pt5_min
9.	Sekarang klik kanan layer un-styled dan pilih Styles ‣ Paste Style.gpw-v4-population-count-rev11_2000_2pt5_min
10.	Parameter gaya yang sama akan diterapkan ke lapisan lain. Fitur ini sangat berguna ketika Anda ingin membandingkan lapisan yang berbeda menggunakan kategorisasi yang sama. Saat Anda mengubah visibilitas lapisan atas, Anda dapat melihat perubahan populasi secara visual.
11.	Tugas kita adalah membuat peta tematik tentang perubahan populasi. Mari kita hitung perbedaan antara 2 lapisan dan buat raster lain di mana setiap piksel mewakili perubahan dalam populasi. Pergi ke Raster ‣ Kalkulator raster.
12.	Di bagian Raster bands, Anda dapat memilih layer dengan mengklik dua kali pada mereka. Band-band tersebut diberi nama sesuai dengan nama raster diikuti dengan dan nomor band. Karena masing-masing raster kami hanya memiliki 1 band, Anda akan nama dengan ditambahkan ke nama layer. Kalkulator raster dapat menerapkan operasi matematika pada piksel raster. Dalam hal ini kami ingin memasukkan rumus sederhana untuk mengurangi populasi 2010 dari tahun 2000. Masukkan ekspresi berikut. Selanjutnya, klik tombol ... di sebelah layer Output.@@1
13.	Masukkan sebagai file Output. Klik OK untuk memulai komputasi.population_change_2010_2000.tif
14.	Setelah selesai, layer baru akan ditambahkan ke panel Layers. Mari kita ubah gaya sehingga perubahan populasi negatif dan positif divisualisasikan dengan lebih baik. Klik tombol Open the layer Styling panel di panel Layers.population_change_2010_2000
15.	Salah satu pilihannya adalah menggunakan teknik styling yang serupa seperti sebelumnya dan memilih ramp warna yang berbeda. Klik drop-down Color ramp dan pilih ramp. Klik drop-down lagi dan pilih untuk menetapkan blues ke nilai rendah dan merah ke nilai tinggi.SpectralInvert Color Ramp
16.	Ini adalah visualisasi yang bagus, tetapi tidak mudah ditafsirkan. Mari kita buat peta yang lebih baik dengan 4 kategori diskrit, , , dan . Gulir ke bawah ke tabel dengan kelas. Tahan tombol dan pilih semua baris. Klik tombol Hapus baris yang dipilih.DeclineNeutralGrowthHigh GrowthShift
17.	Ubah mode Interpolasi menjadi . Sekarang kita akan membuat peta warna secara manual. Klik tombol Tambahkan nilai secara manual. Masukkan sebagai nilai dan sebagai label. Tetapkan warna biru ke kategori ini. Cara kerja peta warna adalah bahwa semua nilai yang lebih rendah dari nilai yang dimasukkan akan diberi warna entri tersebut. Anda akan melihat kanvas hanya akan menunjukkan daerah-daerah dengan perubahan populasi negatif.Discrete-100Decline
18.	Lengkapi peta warna dengan nilai yang sesuai. Saya memilih , dan sebagai batas atas untuk , dan kategori masing-masing. Tetapkan warna untuk setiap kategori yang dibuat, misalnya krem, oranye, dan merah.1001000100000NeutralGrowthHigh Growth
19.	Setelah  puas dengan visualisasi, tutup panel Layer Styling.  sekarang memiliki peta tematik global tentang perubahan populasi.
link https://github.com/miaaprilia18/SIG_Teori_Basic_GIS_operations/blob/main/project%206.png

# Raster Mosaicing and Clipping (QGIS3)
1.	Buka QGIS dan cari file yang diunduh di panel Browser. Perluas file zip individual untuk menampilkan file. Tahan tombol dan pilih semua file individual. Setelah dipilih, seret ke kanvas..hgtCtrl
2.	 akan melihat 11 layer individu dimuat di panel Layers dan ditampilkan di kanvas. Kami akan menggabungkan ubin individu ini menjadi satu mosaik. Pergi ke Pemrosesan ‣ Kotak Alat.
3.	Cari dan temukan GDAL ‣ Raster lain-lain ‣ Alat gabungan. Klik dua kali untuk meluncurkannya.
4.	Dalam dialog Gabungkan, klik tombol ... di sebelah layer Input. Klik Pilih Semua untuk memilih semua lapisan individual.
5.	Seperti yang disebutkan dalam detail lapisan himpunan data, tipe data input adalah bilangan bulat bertanda tangan 16-bit. Untuk menjaga integritas data, kita harus menyimpan tipe data yang sama untuk layer yang digabungkan. Pilih sebagai tipe data Output. Juga format data keluaran default adalah GeoTiff. File GeoTiff bisa menjadi sangat besar jika tidak dikompresi. Pilih sebagai profil. Klik Jalankan.Int16High Compression
6.	Setelah pemrosesan selesai, layer baru akan ditambahkan ke panel Layers. Jika layer tidak berada di bagian atas tumpukan, pilih dan seret ke bagian atas panel Layers.OUTPUT
7.	Anda akan melihat bahwa layer berisi data elevasi yang digabungkan dari ubin input individu. Visualisasi default hanya menampilkan nilai piksel dalam rentang dari 0-255. Tetapi data kami berisi piksel dengan nilai -14 hingga 2371, menghasilkan rendering kontras yang rendah. Mari kita ubah visualisasi yang lebih baik. Klik tombol Open the layer Styling panel di panel Layers.OUTPUT
8.	Di panel Layer Styling, klik dropdown Render type dan pilih renderer. Opsi rendering ini sangat cocok untuk data ketinggian.Hillshade
9.	Operasi umum lainnya saat bekerja dengan raster adalah memotong raster ke area yang Anda minati. Untuk tutorial ini, kita akan memotong layer gabungan ke batas negara untuk Sri Lanka. Temukan file yang diunduh dan perluas. Seret file ke kanvas.ne_10m_admin_0_countries.zipne_10m_admin_0_countries.shp
10.	Pilih layer yang baru ditambahkan di panel Layers. Klik tombol Pilih Fitur berdasarkan area atau klik tunggal pada Toolbar Atribut. Setelah dipilih, klik poligon untuk Sri Lanka untuk memilihnya.ne_10m_admin_0_countries
11.	Pertahankan pilihan apa adanya dan buka Pemrosesan ‣ Toolbox. Cari dan temukan GDAL ‣ Ekstraksi raster ‣ Klip raster dengan alat lapisan topeng. Klik dua kali untuk meluncurkannya.
12.	Dalam dialog Clip Raster by Mask Layer, atur sebagai Layer Input. Pilih sebagai layer Mask, dan centang kotak Hanya fitur yang dipilih. Masukkan sebagai Tetapkan nilai nodata tertentu ke band output. Seperti sebelumnya, pilih sebagai Profil. Klik Jalankan.OUTPUTne_10m_admin_0_countries0.0000High compression
13.	Layer baru akan ditambahkan ke panel Layers. Pada titik ini, mungkin sulit untuk melihat output karena kita memiliki terlalu banyak lapisan tumpang tindih yang terlihat. Klik tombol Manage Map Themes di panel Layers dan pilih .OUTPUTHide All Layers
14.	Nyalakan hanya layer terbaru dan beri gaya dengan perender seperti yang dilakukan sebelumnya.OUTPUTHilshade
15.	Lapisan elevasi output yang digabungkan dan disubset untuk Sri Lanka sudah siap.

# Working with Terrain Data (QGIS3)

1.	Pergi ke USGS Earthexplorer. Di tab Kriteria Pencarian, klik Fitur Dunia. Di Feature Name masukkan Everest, di Country masukkan NEPAL, klik Show. Ini akan menampilkan tabel dengan informasi lokasi. Pilih Everest di bawah Nama Tempat.
2.	Sekarang kanvas akan pindah ke lokasi Gunung Everest. Klik pada Kumpulan Data.
3.	Perluas grup Digital Elevation, dan periksa GMTED2010. Klik pada Hasil.
4.	Click the Download Options button.
5.	Pilih opsi 30 ARC SEC dan klik Unduh. Anda sekarang akan memiliki file bernama GMTED2010N10E060_300.zip. Data elevasi didistribusikan dalam berbagai format raster seperti ASC, BIL, GeoTiff, dll. QGIS mendukung berbagai format raster melalui pustaka GDAL. Data GMTED datang sebagai file GeoTiff yang terkandung dalam arsip zip ini. Untuk kenyamanan, Anda dapat mengunduh salinan data langsung dari bawah. GMTED2010N10E060_300.zip
6.	Buka Lapisan Tambah Lapisan Tambahkan Lapisan Raster.
7.	Klik pada … di bawah Sumber, cari dan pilih file bernama 10n060e_20101117_gmted_mea300.tif.
8.	Anda akan melihat data medan yang ditampilkan di Kanvas QGIS. Setiap piksel dalam raster medan mewakili ketinggian rata-rata dalam meter di lokasi tersebut. Piksel gelap mewakili area dengan ketinggian rendah dan piksel yang lebih terang mewakili area dengan ketinggian tinggi.
9.	Mari temukan bidang minat kita. Dari Wikipedia, kami menemukan bahwa koordinat untuk area yang kami minati - Gunung Everest - terletak pada koordinat 27.9881° LU, 86.9253° BT. Perhatikan bahwa QGIS menggunakan koordinat dalam format (X, Y), jadi Anda harus menggunakan koordinat sebagai (Bujur, Lintang). Tempelkan 86.9253,27.9881 ini di bagian bawah jendela QGIS di mana tertulis Koordinasi dan tekan Enter. Area pandang akan dipusatkan pada koordinat ini. Untuk memperbesar, Masukkan 1:1000000 di bidang Skala dan tekan Enter. Anda akan melihat viewport zoom ke area sekitar Himalaya.
10.	Kami sekarang akan memotong raster ke area yang diminati ini. Cari Klip di Processing Toolbox. Pilih Clip Raster berdasarkan luasnya di bawah algoritma GDAL.
11.	Di jendela Clip Raster by Extent, pilih 10n060e_20101117_gmted_mea300 sebagai Input Layer, klik ... di Clipping extent dan pilih Use Map canvas extent, klik ... di Clipped (extent) dan masukkan nama sebagai mt_everest.tif. Klik Jalankan.
12.	Lapisan baru mt_everest akan muncul di kanvas. Cari Hill di Processing Toolbox. Pilih algoritma Hillshade di bawah algoritma GDAL.
13.	Di jendela Hillshade, pilih mt_everest sebagai Elevation Layer, masukkan 315.000 di Azimuth (sudut horizontal), masukkan 45.000 di sudut Vertikal. Klik ... di Hillshade dan masukkan namanya sebagai mt_everest_hillshade.tif. Klik Jalankan.
14.	Lapisan baru mt_everest_hillshade akan muncul di kanvas.
15.	Cari Kontur di Processing Toolbox. Pilih algoritma Kontur di bawah algoritma GDAL.
16.	Di jendela Contour, pilih mt_everest sebagai Input Layer, masukkan 250 di Interval antara garis kontur. Klik ... di Contours dan masukkan namanya sebagai mt_everest_contour.gpkg. Klik Jalankan.
17.	Lapisan baru mt_everest_contour akan muncul di kanvas. Klik kanan pada layer dan klik Open Attribute Table.
18.	Anda akan melihat bahwa setiap fitur baris memiliki atribut bernama ELEV. Ini adalah ketinggian dalam meter yang diwakili oleh setiap garis. Klik pada tajuk kolom beberapa kali untuk mengurutkan nilai dalam urutan menurun. Di sini Anda akan menemukan garis yang mewakili elevasi tertinggi dalam data kami, yaitu Gunung Everest.
19.	Pilih baris atas, dan klik tombol Zoom to selection.
20.	Beralih ke jendela QGIS utama. Anda akan melihat garis kontur yang dipilih disorot dengan warna kuning. Ini adalah area elevasi tertinggi dalam dataset kami.
21.	Cari Smooth di Processing Toolbox. Pilih Halus di bawah geometri Vektor.
22.	Di jendela Smooth, pilih mt_everest_contour sebagai Input Layer, masukkan 5 di Iterasi. Klik Jalankan.
23.	Sebuah layer baru Smoothed akan muncul di kanvas. Lapisan ini akan memiliki tepi yang lebih halus dibandingkan dengan lapisan mt_everest_contour.
24.	Anda juga dapat memvisualisasikan lapisan kontur dan memverifikasi analisis Anda dengan mengekspor lapisan kontur sebagai KML dan melihatnya di Google Earth. Klik kanan pada layer yang dihaluskan, pilih Export Save Feature As….
25.	Pilih Bahasa Markup Lubang Kunci [KML] sebagai Format. Klik ... di File name dan masukkan namanya sebagai contour_smoothed.kml. Klik Oke.
26.	Jelajahi file keluaran pada disk Anda dan klik dua kali untuk membuka Google Earth Pro.

# Working with WMS Data (QGIS3)
1.	Buka QGIS dan klik Open Data Source Manager.
2.	Di kotak dialog Pengelola Sumber Data beralih ke WMS/WMTS, klik New.
3.	Di kotak dialog Buat Koneksi WMS/WMTS Baru di bawah Detail Koneksi, masukkan Nama sebagai SEDAC, dan tempel URL yang disalin di kotak teks URL. Klik Oke. Jika Anda mendapatkan kesalahan dengan URL yang disalin, coba dengan URL alternatif https://sedac.ciesin.columbia.edu/geoserver/ows.
4.	Sekarang di kotak dialog Data Source Manager, klik Connect. Semua lapisan yang tersedia akan dimuat. Anda akan melihat ID berbeda yang tercantum di sebelah lapisan. ID 0 berarti Anda mendapatkan peta dari semua lapisan. Jika Anda tidak menginginkan semua lapisan, Anda dapat memperluas daftar dengan mengeklik ikon ▸ dan memilih lapisan yang diinginkan.
5.	Untuk tutorial ini, kami tertarik pada lapisan tertentu. Cari Probabilities of Urban Expansion to 2030. Pilih versi default lapisan ekspansi perkotaan 2030.
6.	Di bagian Pengkodean Gambar, Anda harus memilih format gambar. Format gambar itu penting, dan itu tergantung pada kasus penggunaan. Berdasarkan perspektif pengguna berikut adalah beberapa petunjuk,
•	Kualitas: Kompresi file untuk PNG adalah lossless, untuk JPEG ini adalah kompresi lossy dan TIFF dapat berupa keduanya. Itu berarti kualitas PNG akan lebih baik dibandingkan dengan JPEG. Jika tujuan utama Anda adalah mencetak peta, gunakan PNG.
•	Kecepatan: Karena gambar PNG tidak terkompresi dan dengan demikian ukurannya lebih besar, mereka akan membutuhkan waktu lebih lama untuk dimuat. Jika Anda menggunakan lapisan dalam proyek Anda sebagai lapisan referensi dan perlu banyak memperbesar/menggeser, gunakan JPEG.
•	Dukungan Klien: QGIS mendukung sebagian besar format, tetapi jika Anda mengembangkan aplikasi web, browser biasanya tidak mendukung TIFF, jadi Anda harus memilih format lain.
•	Jenis data: Jika lapisan Anda sebagian besar adalah vektor, PNG akan memberikan hasil yang lebih baik. Untuk lapisan citra, JPEG biasanya merupakan pilihan yang lebih baik.
7.	Sekarang lapisan Probabilities of Urban Expansion to 2030 akan dimuat di kanvas. Gunakan alat Zoom/Pan untuk menjelajahi lapisan. Cara kerja layanan WMS adalah setiap kali Anda memperbesar/menggeser, ia mengirimkan koordinat area pandang Anda ke server dan server membuat gambar untuk area pandang tersebut dan mengembalikannya ke klien. Jadi, akan ada beberapa penundaan sebelum Anda melihat gambar untuk area tersebut setelah Anda memperbesar. Oleh karena itu, koneksi internet selalu diperlukan untuk mengakses lapisan ini.
8.	Sekarang, perbesar ke tempat yang diketahui dan klik ikon Identify Features di bilah alat.
9.	Klik pada piksel apa saja di kanvas, itu akan memunculkan kotak dialog dengan nilai sel. Ini adalah nilai piksel dalam lapisan - yang mewakili kemungkinan bahwa piksel tersebut akan mengalami urbanisasi pada tahun 2030. Karena lapisan tersebut tidak disimpan secara lokal, nilai ini diambil dari penyedia layanan. Anda dapat melihat hasilnya lebih baik dengan memilih Format as HTML dan View as Tree.
10.	Untuk melihat, informasi tambahan tentang layer klik kanan pada layer dan pilih Properties….
11.	Di kotak dialog Layer Properties, alihkan ke tab Informasi di sini semua informasi seperti penyedia data, proyeksi, jangkauan dapat ditemukan. Klik OK untuk menutup kotak dialog setelah menjelajah.
12.	Di Browser QGIS, cari Ubin XYZ dan klik dan seret OpenStreetMap ke kanvas.
13.	Klik pada ikon panel Open the Layer Styling dan beralih ke Transparency.
14.	Atur opasitas Global menjadi 50%
15.	Sekarang di kanvas, lapisan Urban dapat dieksplorasi dengan referensi geografis.
16.	Untuk mendapatkan lebih banyak akses ke transparansi layer, klik kanan pada layer dan pilih Properties….
17.	Di kotak dialog Properties Lapisan, alihkan ke tab Legend, di bawah Widget yang tersedia pilih penggeser Opasitas dan klik Tambahkan ikon widget yang dipilih. Klik OK.
18.	Sekarang widget penggeser akan tersedia untuk mengontrol opacity layer.

# Working with Projections (QGIS3)
1.	Buka QGIS dan klik Open Data Source Manager.
2.	Di kotak dialog Pengelola Sumber Data beralih ke WMS/WMTS, klik New.
3.	Di kotak dialog Buat Koneksi WMS/WMTS Baru di bawah Detail Koneksi, masukkan Nama sebagai SEDAC, dan tempel URL yang disalin di kotak teks URL. Klik Oke. Jika Anda mendapatkan kesalahan dengan URL yang disalin, coba dengan URL alternatif https://sedac.ciesin.columbia.edu/geoserver/ows.
4.	Sekarang di kotak dialog Data Source Manager, klik Connect. Semua lapisan yang tersedia akan dimuat. Anda akan melihat ID berbeda yang tercantum di sebelah lapisan. ID 0 berarti Anda mendapatkan peta dari semua lapisan. Jika Anda tidak menginginkan semua lapisan, Anda dapat memperluas daftar dengan mengeklik ikon ▸ dan memilih lapisan yang diinginkan.
5.	Untuk tutorial ini, kami tertarik pada lapisan tertentu. Cari Probabilities of Urban Expansion to 2030. Pilih versi default lapisan ekspansi perkotaan 2030.
6.	Di bagian Pengkodean Gambar, Anda harus memilih format gambar. Format gambar itu penting, dan itu tergantung pada kasus penggunaan. Berdasarkan perspektif pengguna berikut adalah beberapa petunjuk,
•	Kualitas: Kompresi file untuk PNG adalah lossless, untuk JPEG ini adalah kompresi lossy dan TIFF dapat berupa keduanya. Itu berarti kualitas PNG akan lebih baik dibandingkan dengan JPEG. Jika tujuan utama Anda adalah mencetak peta, gunakan PNG.
•	Kecepatan: Karena gambar PNG tidak terkompresi dan dengan demikian ukurannya lebih besar, mereka akan membutuhkan waktu lebih lama untuk dimuat. Jika Anda menggunakan lapisan dalam proyek Anda sebagai lapisan referensi dan perlu banyak memperbesar/menggeser, gunakan JPEG.
•	Dukungan Klien: QGIS mendukung sebagian besar format, tetapi jika Anda mengembangkan aplikasi web, browser biasanya tidak mendukung TIFF, jadi Anda harus memilih format lain.
•	Jenis data: Jika lapisan Anda sebagian besar adalah vektor, PNG akan memberikan hasil yang lebih baik. Untuk lapisan citra, JPEG biasanya merupakan pilihan yang lebih baik.
7.	Sekarang lapisan Probabilities of Urban Expansion to 2030 akan dimuat di kanvas. Gunakan alat Zoom/Pan untuk menjelajahi lapisan. Cara kerja layanan WMS adalah setiap kali Anda memperbesar/menggeser, ia mengirimkan koordinat area pandang Anda ke server dan server membuat gambar untuk area pandang tersebut dan mengembalikannya ke klien. Jadi, akan ada beberapa penundaan sebelum Anda melihat gambar untuk area tersebut setelah Anda memperbesar. Oleh karena itu, koneksi internet selalu diperlukan untuk mengakses lapisan ini.
8.	Sekarang, perbesar ke tempat yang diketahui dan klik ikon Identify Features di bilah alat.
9.	Klik pada piksel apa saja di kanvas, itu akan memunculkan kotak dialog dengan nilai sel. Ini adalah nilai piksel dalam lapisan - yang mewakili kemungkinan bahwa piksel tersebut akan mengalami urbanisasi pada tahun 2030. Karena lapisan tersebut tidak disimpan secara lokal, nilai ini diambil dari penyedia layanan. Anda dapat melihat hasilnya lebih baik dengan memilih Format as HTML dan View as Tree.
10.	Untuk melihat, informasi tambahan tentang layer klik kanan pada layer dan pilih Properties….
11.	Di kotak dialog Layer Properties, alihkan ke tab Informasi di sini semua informasi seperti penyedia data, proyeksi, jangkauan dapat ditemukan. Klik OK untuk menutup kotak dialog setelah menjelajah.
12.	Di Browser QGIS, cari Ubin XYZ dan klik dan seret OpenStreetMap ke kanvas.
13.	Klik pada ikon panel Open the Layer Styling dan beralih ke Transparency.
14.	Atur opasitas Global menjadi 50%
15.	Sekarang di kanvas, lapisan Urban dapat dieksplorasi dengan referensi geografis.
16.	Untuk mendapatkan lebih banyak akses ke transparansi layer, klik kanan pada layer dan pilih Properties….
17.	Di kotak dialog Properties Lapisan, alihkan ke tab Legend, di bawah Widget yang tersedia pilih penggeser Opasitas dan klik Tambahkan ikon widget yang dipilih. Klik OK.
18.	Sekarang widget penggeser akan tersedia untuk mengontrol opacity layer.


# Georeferencing Topo Sheets and Scanned Maps (QGIS3)
1.	Buka QGIS dan klik Raster ‣ Georeferencer untuk membuka alat ini.
2.	Georeferencer dibagi menjadi 2 bagian. Bagian atas tempat gambar akan ditampilkan dan bagian bawah tempat tabel yang menunjukkan GCP Anda akan muncul.
3.	Sekarang kita akan membuka gambar JPG kita. Pergi ke File ‣ Buka Raster. Telusuri ke gambar yang diunduh dari peta yang dipindai dan klik Buka.
4.	Anda akan melihat gambar akan dimuat di bagian atas. Anda dapat menggunakan kontrol zoom/pan di toolbar untuk mempelajari lebih lanjut tentang peta.
5.	Sekarang kita perlu menetapkan koordinat ke beberapa titik di peta ini. Jika Anda melihat lebih dekat, Anda akan melihat kisi koordinat dengan tanda. Ini adalah garis kisi Lintang dan Bujur.
6.	Sebelum menambahkan Ground Control Points (GCP), kita perlu mendefinisikan Pengaturan Transformasi. Klik ikon roda gigi di jendela georeferensi untuk membuka dialog Pengaturan transformasi.
7.	Sebelum menambahkan Ground Control Points (GCP), kita perlu mendefinisikan Pengaturan Transformasi. Klik ikon roda gigi di jendela georeferensi untuk membuka dialog Pengaturan transformasi.
8.	Jika Anda melakukan referensi geografis pada peta yang dipindai seperti ini, Anda dapat memperoleh informasi CRS dari peta itu sendiri. Melihat gambar peta kita, koordinatnya berada di Lintang / Bujur. Tidak ada informasi datum yang diberikan, jadi kita harus mengasumsikan yang sesuai. Karena ini adalah India dan petanya sudah cukup tua, kita bisa bertaruh datum Everest 1830 akan memberi kita hasil yang baik. Cari dan pilih CRS dengan definisi tertua dari datum Everest (EPSG:4042). Klik Oke.everest
9.	Beri nama raster keluaran Anda sebagai . Pilih sebagai Kompresi. Periksa poin Simpan GCP untuk menyimpan poin sebagai file terpisah untuk tujuan di masa mendatang. Pastikan opsi Load in QGIS when done dicentang. Klik Oke.1870_southern_india_modified.tifLZW
10.	Sekarang kita bisa mulai menambahkan Ground Control Points (GCP). Klik pada tombol Add Point.
11.	Sekarang tempatkan rambut silang di persimpangan garis kisi dan klik kiri, ini akan berfungsi sebagai kebenaran dasar dalam kasus kami. Saat garis kisi diberi label, kita dapat menentukan koordinat X dan Y dari titik-titik yang menggunakannya. Di jendela pop-up, masukkan koordinat. Ingatlah bahwa X=bujur dan Y=lintang. Klik Oke.
12.	Anda akan melihat tabel GCP sekarang memiliki baris dengan detail GCP pertama Anda.
13.	Demikian pula, tambahkan lebih banyak GCP yang mencakup seluruh gambar. Semakin banyak poin yang Anda miliki, semakin akurat gambar Anda terdaftar ke koordinat target. Transformasi ini membutuhkan setidaknya 6 GCP. Setelah Anda menambahkan jumlah poin minimum yang diperlukan untuk transformasi, Anda akan melihat bahwa GCP sekarang memiliki nilai kesalahan dan bukan nol. Jika GCP tertentu memiliki nilai kesalahan yang luar biasa tinggi, itu biasanya berarti kesalahan manusia dalam memasukkan nilai koordinat. Jadi, Anda dapat menghapus GCP tersebut dan menangkapnya lagi. Anda juga dapat mengedit nilai koordinat di Tabel GCP dengan mengklik sel di kolom Dest. X atau Dest. Y.Polynomial 2dXdYResidual
14.	Setelah Anda puas dengan GCP, klik tombol Mulai Georeferensi. Ini akan memulai proses warping gambar menggunakan GCP dan membuat raster target.
15.	Setelah proses selesai, Anda akan melihat layer georeferensi dimuat di QGIS. Georeferensi sekarang selesai. Selain itu, Anda akan melihat Project CRS di kanan bawah diatur ke EPSG:4042 seperti yang dijelaskan dalam Pengaturan Transformasi.
16.	Seret dan lepas Peta Dasar as dari dropdown XYZ Tiles di bagian bawah panel Browser untuk memverifikasi lapisan georeferensi. Untuk mengatur transparansi, klik ikon Open layer styling panel dan pilih tab Transparency. Atur transparansi ke . Sekarang gambar georeferensi harus overlay dengan garis besar peta dasar.OpenStreetMap40 %
17.	Jika georeferensi membutuhkan lebih banyak penyesuaian, kita dapat mulai dari poin GCP yang dikumpulkan. Jelajahi lokasi file. Anda dapat menemukan file tambahan, . File ini akan berisi informasi poin GCP.1870_southern_india_modified.tif1870_southern_india_modified.tif.points
18.	Buka alat georeferensi di QGIS, klik File ‣ Load GCP Points, dan pilih file . Ini akan memuat GCP yang dibuat sebelumnya. Kemudian muat untuk menyempurnakan pekerjaan Anda.1870_southern_india_modified.tif.points1870_southern_india_modified.tif
link https://github.com/miaaprilia18/SIG_Teori_Basic_GIS_operations/blob/main/project%2011.qgz

# Georeferencing Aerial Imagery (QGIS3)
1.	Kita akan menggunakan basemap dari OpenStreetMap untuk menangkap koordinat georeferensi. QGIS3 dilengkapi dengan dukungan built-in untuk lapisan ubin. Ini umumnya dikenal sebagai lapisan 'XYZ' karena dibuat menggunakan ubin peta individual untuk setiap tingkat zoom (z) pada kisi koordinat x, y. Anda dapat menemukan layer di bawah XYZ Tiles di Panel Browser. Seret layer ke kanvas utama. Setelah dimuat, perhatikan Sistem Referensi Koordinat (CRS) untuk lapisan ini di urutan kanan bawah. Ini diatur sebagai . Ini penting karena koordinat yang kita simpulkan dari lapisan ini selama georeferensi akan berada di CRS ini.OpenStreetMapEPSG 3857 Pseudo Mercator
2.	Gambar yang kami georeferensikan adalah untuk . Anda dapat memperbesar / menggeser untuk menemukan taman ini di peta. Tapi itu rumit dan tidak praktis. Dari QGIS versi 3.20 dan seterusnya, ada dukungan bawaan untuk Nominatim Geocoder berbasis OpenStreetMap. Klik bilah pencarian di kiri bawah jendela QGIS. Untuk menggunakan ini sebagai awalan geocoder, tempat pencarian dengan . Pencarian akan memunculkan daftar alamat untuk dipilih. Klik alamat pertama.Washington Square Park, New York>> Washington Square Park
3.	Kanvas peta akan dipusatkan ke Square Park. Sekarang mari kita mulai georeferensi. Luncurkan Georeferencer dari Raster ‣ Georeferencer.
4.	Untuk georeferensi gambar udara, kita harus memilih titik koordinat dari OpenStreetMap, jadi mari kita docking alat Georeferencer ke jendela utama QGIS. Pilih Konfigurasikan Georeferensi dari Pengaturan ‣ Konfigurasikan Georeferensir.
5.	Centang Tampilkan jendela georeferensir yang ditambatkan dan klik OK.
6.	Jendela Georeferencer akan ditambatkan di bagian bawah jendela utama QGIS. Mari kita muat file gambar dengan mengklik Buka Raster ikon di jendela Georeferencer dan menavigasi ke file JPG yang diunduh. Klik Buka.
7.	Sebelum menambahkan Ground Control Points (GCP), kita perlu mendefinisikan Pengaturan Transformasi. Klik ikon Pengaturan Transformasi untuk membuka dialog Pengaturan Transformasi. Pilih jenis Transformasi sebagai . Lihat Dokumentasi QGIS untuk mempelajari tentang berbagai jenis transformasi dan penggunaannya. Seperti disebutkan sebelumnya, peta dasar kita ada di CRS, jadi tetapkan itu sebagai Target CRS. Anda dapat membiarkan nama raster Output ke default dan memilih sebagai Kompresi. Periksa Gunakan 0 untuk transparansi bila diperlukan. Periksa poin Simpan GCP untuk menyimpan poin sebagai file terpisah untuk tujuan mendatang. Pastikan opsi Load in QGIS when done dicentang. Klik Oke.Polynomial 2EPSG 3857 Pseudo MercatorLZW
8.	Sekarang klik tombol Add Point pada toolbar dan pilih lokasi yang mudah diidentifikasi pada gambar. Sudut, persimpangan, tiang, dll., Membuat titik kontrol yang baik. Setelah Anda mengklik gambar di lokasi titik kontrol, Anda akan melihat pop-up yang meminta Anda untuk memasukkan koordinat peta. Klik tombol Dari kanvas peta.
9.	Di layer, klik pada lokasi yang tepat di layer referensi. Koordinat akan diisi secara otomatis dari klik Anda pada kanvas peta. Klik Oke.OpenStreetMap
10.	Demikian pula, pilih setidaknya 6 titik pada gambar dan tambahkan koordinatnya dari lapisan referensi. Setelah Anda menambahkan jumlah poin minimum yang diperlukan untuk transformasi, Anda akan melihat bahwa GCP sekarang memiliki nilai bukan nol, , dan kesalahan. Jika GCP tertentu memiliki nilai kesalahan yang luar biasa tinggi, itu biasanya berarti kesalahan manusia dalam memasukkan nilai koordinat. Jadi, Anda dapat menghapus GCP tersebut dan menangkapnya lagi.dXdYResidual
11.	Setelah Anda puas dengan GCP, klik Mulai georeferensi. Ini akan memulai proses warping gambar menggunakan GCP dan membuat raster target. Setelah proses selesai, Anda akan melihat layer dimuat di QGIS. Tutup jendela Georeferencer.
12.	Sekarang klik pada Buka ikon panel styling layer dan Beralih ke tab Transparency. Tambahkan sebagai nilai Tambahan tanpa data. Ini akan menghapus batas putih di sekitar gambar. Sekarang Anda akan melihat gambar georeferensi Anda dilapis dengan baik pada lapisan dasar.255
link https://github.com/miaaprilia18/SIG_Teori_Basic_GIS_operations/blob/main/project12.png

# Digitizing Map Data (QGIS3) 
1.	Di QGIS, mari kita memuat file gambar. Pergi ke Layer ‣ Add Layer ‣ Add Raster Layer.
2.	Dalam dialog Manajer Sumber Data pilih Raster. Di bawah Sumber klik pada dan temukan yang diunduh dan klik Buka. Kemudian klik Tambahkan diikuti oleh Tutup....BX24_GeoTifv1-02.tif
3.	Ini adalah file raster besar, dan Anda mungkin memperhatikan bahwa ketika Anda memperbesar atau menggeser di sekitar peta, peta membutuhkan sedikit waktu untuk merender gambar. QGIS menawarkan solusi sederhana untuk membuat raster memuat lebih cepat dengan menggunakan Piramida Gambar. QGIS membuat ubin pra-render pada resolusi yang berbeda, dan ini disajikan kepada Anda alih-alih raster penuh. Ini membuat navigasi peta cepat dan responsif. Klik kanan layer dan pilih Properties.BX24_GeoTifv1-02
4.	Dalam dialog Layer Properties, Pilih tab Pyramids. Tahan tombol dan pilih semua resolusi yang ditawarkan di panel Resolusi. Biarkan opsi lain ke default dan klik Bangun piramida.Ctrl
5.	Dalam dialog Layer Properties, Pilih tab Pyramids. Tahan tombol dan pilih semua resolusi yang ditawarkan di panel Resolusi. Biarkan opsi lain ke default dan klik Bangun piramida.Ctrl
6.	Dalam dialog Layer Properties, Pilih tab Pyramids. Tahan tombol dan pilih semua resolusi yang ditawarkan di panel Resolusi. Biarkan opsi lain ke default dan klik Bangun piramida.Ctrl
7.	Pilih tab Digitalisasi dalam dialog Opsi. Centang bagian Aktifkan gertakan secara default di bawah Gertakan. Dalam mode snap default pilih Vertex. Ini akan memungkinkan Anda untuk mengambil ke verteks terdekat. Saya juga lebih suka mengatur toleransi gertakan Default dan radius Pencarian untuk pengeditan verteks dalam piksel daripada unit peta. Ini akan memastikan bahwa jarak gertakan tetap konstan terlepas dari tingkat zoom. Tergantung pada resolusi layar komputer Anda, Anda dapat memilih nilai yang sesuai. Klik Oke.
8.	Sekarang kita siap untuk mulai digitalisasi. Pertama-tama kita akan membuat layer jalan dan mendigitalkan jalan di sekitar area taman. Klik Layer ‣ Create Layer ‣ New GeoPackage Layer... dari Panel. GeoPackage adalah format data terbuka, non-eksklusif, platform-independen, dan berbasis standar untuk sistem informasi geografis yang diimplementasikan sebagai wadah database SQLite. Ini membuatnya lebih mudah untuk memindahkannya daripada sekelompok shapefile. Dalam tutorial ini, kita membuat beberapa layer poligon dan layer garis sehingga GeoPackage akan lebih cocok. Anda selalu dapat memuat GeoPackage dan mengekspor lapisan sebagai shapefile atau format lain yang Anda inginkan.
9.	Dalam dialog New GeoPackage Layer, klik tombol ... dan simpan database GeoPackage baru bernama . Pilih nama Tabel sebagai dan pilih sebagai tipe Geometri. Peta topografi dasar adalah CRS.digitizing.gpkgRoadsLineStringEPSG:2193 - NZGD 2000
10.	Saat membuat layer GIS, Anda harus memutuskan atribut masing-masing fitur. Karena ini adalah lapisan jalan, kita juga akan memiliki dua atribut utama - Nama dan Kelas. Di Bidang Baru Masukkan tipe Data teks, dengan panjang Maksimum dan klik Tambahkan ke daftar atribut. Sekarang buat atribut baru dari jenis Data teks, dengan panjang maksimum. Klik OKEName50Class50
11.	Setelah layer dimuat, klik Toggle Editing tombol untuk menempatkan layer dalam mode pengeditan.Roads
12.	Klik tombol Add Line Feature. Klik pada kanvas peta untuk menambahkan verteks baru. Tambahkan simpul baru bersama dengan fitur jalan. Setelah Anda mendigitalkan segmen jalan, klik kanan untuk mengakhiri fitur tersebut.
13.	Setelah Anda mengklik kanan untuk mengakhiri fitur, Anda akan mendapatkan dialog pop-up yang disebut Road - Feature Attributes. Di sini Anda dapat memasukkan atribut dari fitur yang baru dibuat. Lewati memasukkan nilai apa pun untuk fid karena ini adalah id berurutan yang akan dibuat secara otomatis. Masukkan nama jalan seperti yang muncul di peta topo. Secara opsional, tetapkan nilai Kelas Jalan juga. Klik Oke.
14.	Gaya default dari layer garis baru adalah garis tipis. Mari kita ubah untuk lebih melihat fitur digital di kanvas. Pilih layer dan klik Layer Styling Panel.Roads
15.	Di Layer Styling Panel, cari gaya layer jalan yang berbeda. Pilih. Klik Oke.topo road
16.	Di Layer Styling Panel, cari gaya layer jalan yang berbeda. Pilih. Klik Oke.topo road
17.	Sebelum kita mendigitalkan jalan yang tersisa, penting untuk memperbarui beberapa pengaturan snap penting lainnya untuk membuat lapisan bebas kesalahan. Klik kanan pada ruang mana pun di area bilah alat dan aktifkan bilah alat Gertakan.
18.	Sebelum kita mendigitalkan jalan yang tersisa, penting untuk memperbarui beberapa pengaturan snap penting lainnya untuk membuat lapisan bebas kesalahan. Klik kanan pada ruang mana pun di area bilah alat dan aktifkan bilah alat Gertakan.
19.	Sebelum kita mendigitalkan jalan yang tersisa, penting untuk memperbarui beberapa pengaturan snap penting lainnya untuk membuat lapisan bebas kesalahan. Klik kanan pada ruang mana pun di area bilah alat dan aktifkan bilah alat Gertakan.
20.	Sekarang Anda dapat mengklik tombol Tambahkan fitur dan mendigitalkan jalan lain di sekitar taman. Pastikan untuk mengklik Simpan Pengeditan setelah menambahkan fitur baru untuk menyimpan pekerjaan Anda. Alat yang berguna untuk membantu Anda mendigitalkan adalah Alat Vertex. Klik tombol Vertex Tool dan pilih .Vertex Tool (Current Layer)
21.	Setelah alat node diaktifkan, klik fitur apa pun untuk menampilkan simpul. Klik pada verteks mana saja untuk memilihnya. Verteks akan mengubah warna setelah dipilih. Sekarang Anda dapat mengklik dan menyeret mouse Anda untuk memindahkan simpul. Hal ini berguna ketika Anda ingin melakukan penyesuaian setelah fitur dibuat. Anda juga dapat menghapus verteks yang dipilih dengan mengklik tombol. ( di mac)DeleteOption+Delete
22.	Setelah Anda selesai mendigitalkan semua jalan, klik tombol Toggle Editing. Klik Simpan.
23.	Sekarang kita akan membuat layer lain untuk mendigitalkan taman sebagai poligon. Klik Layer ‣ Create Layer ‣ New GeoPackage Layer... dari Panel. Dalam dialog New GeoPackage Layer, klik tombol ... dan pilih database GeoPackage bernama . Beri nama layer baru sebagai atribut yang disebut . Pilih sebagai Tipe. Peta topografi dasar adalah CRS. Klik Oke. Di New Field Enter , dan ketik sebagai Data teks, dengan panjang Maksimum dan klik :guilabel:' Add to Fields List.'. Klik Oke.digitizing.gpkgParksMultiPolygonEPSG:2193 - NZGD 2000Name50
24.	Dialog pop-up akan muncul. Pilih tombol Add New Layer.
25.	Sekarang pilih layer lalu clickroad Toggle Editing dan klik tombol Add feature dan klik pada kanvas peta untuk menambahkan verteks poligon. Digitalisasi poligon yang mewakili taman. Pastikan Anda membentak ke simpul jalan sehingga tidak ada celah antara poligon taman dan garis jalan. Klik kanan untuk menyelesaikan poligon.Parks
26.	Masukkan nama taman di pop-up Taman - Atribut Fitur.
27.	Sekarang digitalisasi wilayah atas taman. Masukkan nama taman dan simpan perubahannya.
28.	Sekarang, sebelum mendigitalkan poligon bagian dalam, mari kita atur pengaturan yang dapat memudahkan pekerjaan ini. Lapisan Multi-Polygon menawarkan pengaturan berguna lain yang disebut Hindari persimpangan poligon baru. Pilih Aktifkan Gertakan (Ikon Magnet), klik untuk mengaktifkannya, dan klik Semua Lapisan dan pilih .Advanced Configuration
29.	Klik tombol di bilah alat gertakan.Avoid Overlap on Active layers
30.	Klik tombol di bilah alat gertakan.Avoid Overlap on Active layers
31.	Centang kotak di kolom Hindari Tumpang Tindih di baris untuk lapisan tersebut.Parks
32.	Klik fitur Add untuk menambahkan poligon. Dengan Hindari Tumpang Tindih, Anda akan dapat dengan cepat mendigitalkan poligon baru tanpa khawatir akan membentak persis ke poligon tetangga.
33.	Klik kanan untuk menyelesaikan poligon dan masukkan atribut. Ajaibnya poligon baru menyusut dan tersentak tepat ke batas poligon tetangga! Ini sangat berguna ketika mendigitalkan batas-batas kompleks di mana Anda tidak perlu tepat dan masih memiliki poligon yang benar secara topologis. Klik Toggle Editing untuk menyelesaikan pengeditan layer.Parks
34.	Sekarang saatnya untuk mendigitalkan lapisan bangunan. Buat layer poligon baru bernama dengan mengklik Layer ‣ Create Layer ‣ New GeoPackage Layer... dari Panel. Atur bangunan dan MuiltiPolygon. Pilih CRS sebagai . Klik Oke.BuildingsEPSG:2193 - NZGD 2000
35.	Setelah layer ditambahkan, matikan layer and untuk membuat peta topo dasar terlihat. Pilih layer dan klik Toggle Editing.BuildingsParksRoadsBuildings
36.	Mendigitalkan bangunan bisa menjadi tugas yang rumit, dan juga, sulit untuk menambahkan simpul secara manual sehingga ujung-ujungnya tegak lurus dan membentuk persegi panjang. Kita akan menggunakan toolbar QGIS yang disebut Shape Digitizing untuk membantu tugas ini. Klik kanan pada ruang kosong di area toolbar dan aktifkan file .Shape Digitizing Toolbar
37.	Aktifkan pengeditan dengan menekan ikon pensil Alihkan Pengeditan.
38.	Sekarang di bawah Tambahkan Persegi panjang dropdown pilih Tambahkan Persegi Panjang dari tombol Luas.
39.	Perbesar ke area dengan bangunan. Klik dan seret mouse untuk menggambar persegi panjang yang sempurna. Demikian pula, tambahkan bangunan yang tersisa.
40.	Anda akan melihat bahwa beberapa bangunan tidak vertikal, dan kita perlu menggambar persegi panjang pada sudut agar sesuai dengan jejak bangunan. Di bawah Tambahkan Persegi Turun pilih Tambahkan Persegi dari Tengah dan tombol Titik.
42.	Perbesar ke area bangunan berbentuk berlian. Klik pada bagian tengah untuk menjatuhkan titik dan seret mouse untuk menggambar persegi panjang. Kita perlu memutar persegi panjang ini agar sesuai dengan gambar di peta topo. Alat putar tersedia di bilah alat Digitalisasi Lanjutan. Klik kanan pada area kosong di bagian toolbar dan aktifkan toolbar Advanced Digitizing.
43.	Klik tombol Putar Fitur.
44.	Gunakan alat fitur Pilih Tunggal untuk memilih poligon yang ingin Anda putar. Setelah alat Rotate Feature diaktifkan, Anda akan melihat crosshairs di tengah poligon. Klik tepat pada tanda bidik itu dan seret mouse sambil menahan tombol klik kiri. Pratinjau fitur yang diputar akan muncul. Lepaskan tombol mouse saat poligon sejajar dengan tapak bangunan.
45.	Simpan layer edits dan klik Toggle Editing setelah Anda selesai mendigitalkan semua bangunan. Anda dapat menyeret layer untuk mengubah urutan penampilannya. Tugas digitalisasi sekarang selesai. Anda dapat bermain dengan opsi gaya dan pelabelan di properti lapisan untuk membuat peta yang tampak bagus dari data yang Anda buat.
link https://github.com/miaaprilia18/SIG_Teori_Basic_GIS_operations/blob/main/project13.qgz dan https://github.com/miaaprilia18/SIG_Teori_Basic_GIS_operations/blob/main/project13.png


# Searching and Downloading OpenStreetMap Data (QGIS3)
1.	Cari dan pasang plugin QuickOSM dari QGIS Official Plugin Repository. Lihat Menggunakan Plugin untuk instruksi mengunduh plugin. Pastikan Anda telah memilih kotak centang. Klik Close.
2.	Setelah diinstal, luncurkan plugin dari Vector ‣ QuickOSM ‣ QuickOSM….
3.	Di tab Kueri cepat, Anda dapat menyetel filter untuk memilih subkumpulan. Atribut fitur peta dalam database OSM disimpan sebagai Tag. Tag diwakili dengan kunci dan nilai. Kuncinya adalah topik dan nilai adalah bentuk spesifik. Lihat halaman wiki Fitur Peta OSM untuk daftar lengkap tag untuk berbagai jenis fitur. Bar direpresentasikan menggunakan tag amenity:bar dan pub dengan tag amenity:pub. Kami pertama-tama akan mengekstrak bilah. Pilih kemudahan sebagai Key dari menu drop-down.
4.	Pilih bilah dari menu tarik-turun Value.
5.	Kami dapat menghubungkan beberapa kueri dalam versi terbaru (v2.0.0 +) dari plugin QuickOSM. Klik tombol plus, bilah pemilihan kueri berikutnya akan muncul. Klik pada kotak pilihan pertama di mana kita bisa mendapatkan opsi And dan Or. And hanya akan memilih fitur yang benar untuk semua kueri. Or akan memilih semua fitur yang benar untuk salah satu kueri. Klik Or untuk memilih fitur bar dan pub.
6.	Pilih kemudahan sebagai Kunci dari menu tarik-turun. Kemudian pilih pub dari menu tarik-turun Value.
7.	Masukkan London sebagai In untuk membatasi pencarian di dalam batas kota.
8.	Perluas bagian Advanced. Dalam model data OSM, fitur direpresentasikan menggunakan nodes, ways and relations. Karena kami tertarik dengan fitur titik, Anda hanya dapat memilih Node dan Points . Klik Run kueri.
9.	Setelah kueri selesai, alihkan ke jendela utama QGIS. Anda akan melihat layer baru bernama amenity_bar_amenity_pub_London ditambahkan ke panel Layers. Kanvas akan menunjukkan lokasi bar dan pub yang diekstraksi.
10.	Buka tabel Attribute pada layer. Ada 2.091 fitur. Fasilitas kolom berisi kategori apakah fitur tersebut pub atau bar. Dengan menggunakan kolom kategoris ini, mari menata layer kita.
11.	Klik pada icon panel Open the Layer Styling, pilih Categorized lalu pada Value pilih amenity lalu klik Classify. Sekarang layer akan ditata dengan 2 warna yang menampilkan bar dan pub.
12.	Sekarang klik kanan pada layer, Export Save Feature As… untuk mengekspor layer sebagai GeoPackage.
13.	Di kotak dialog Save Vector Layer as…, di Format pilih GeoPackage, di File name klik ... dan ramban ke direktori tempat Anda ingin menyimpan data dan beri nama keluaran london.gpkg. Di Layer name masukkan bar_and_pubs. Klik OK.
14.	Sekarang lapisan GeoPackage london_bar_and_pubs akan ditambahkan ke kanvas.
link https://github.com/miaaprilia18/SIG_Teori_Basic_GIS_operations/blob/main/project14.png dan https://github.com/miaaprilia18/SIG_Teori_Basic_GIS_operations/blob/main/project14.qgz













