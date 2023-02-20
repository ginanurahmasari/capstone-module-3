### **Customer Lifetime Value Prediction**
**Created by: Gina Nur Rahmasari**

#### **Problem Statement**

Sebuah perusahaan Auto Insurance ingin menaikkan revenue perusahaan dengan melakukan kegiatan marketing yang berfokus pada customer retention atau mempertahankan pelanggan. Agar kegiatan marketing yang dilakukan tepat sasaran, kita perlu melakukan penawaran/promosi kepada orang yang tepat. Kita dapat melakukannya dengan bantuan Customer Lifetime Value atau CLV. CLV menggambarkan ukuran pendapatan total yang diharapkan bisa diperoleh perusahaan dari seseorang selama ia menjadi pelanggan. Secara matematis CLV dapat dihitung dengan mengalikan rata-rata nilai pembelian, frekuensi pembelian, dan rata-rata retensi pelanggan yang diukur dalam tahun. Dengan mengetahui faktor apa saja yang berpengaruh terhadap CLV, misalnya karakteristik pelanggan atau jenis layanan asuransi, perusahaan dapat menentukan strategi marketing seperti apa yang dapat diterapkan.

#### **Goals**

Berdasarkan permasalahan tersebut, akan dibuat model machine learning yang dapat memprediksi nilai CLV berdasarkan data profil pelanggan dan layanan asuransi yang dipilih. Nilai CLV yang diperoleh akan menjadi referensi bagi perusahaan asuransi dalam menentukan tipe promosi yang tepat bagi setiap pelanggan untuk meningkatkan transaksi yang dilakukan oleh pelanggan. Hal ini diharapkan dapat mengoptimalkan biaya marketing dan meningkatkan revenue perusahaan.

#### **Conclusions**

1. Model final yang memiliki performa terbaik untuk memprediksi nilai CLV adalah GradientBoosting Regressor dengan akurasi sebesar 68.15 %. Model dapat memprediksi nilai CLV dengan cukup akurat pada nilai CLV yang rendah namun untuk angka diatas itu terutama > 16624.75007525 (outlier) terdapat banyak error pada prediksi. 
2. Berdasarkan skor MAE, rata-rata error antara nilai CLV prediksi dan aktual adalah USD 1748.36. Sedangkan berdasarkan skor RMSE, rata-rata error antara nilai CLV prediksi dan aktual adalah USD 3609.38. 
3. Berdasarkan feature of importances, Number of Policies dan Monthly Premium Auto adalah fitur yang paling berpengaruh terhadap model dalam memprediksi nilai CLV. Dengan demikian kegiatan promosi dapat difokuskan pada penambahan jumlah polis dan jumlah premi.
4. Dilihat dari nilai feature of importances, kita dapat mengetahui pengaruh karakteristik pelanggan terhadap nilai CLV meskipun nilai importances-nya tidak terlalu besar. Contohnya untuk fitur Marital Status, pelanggan yang berstatus Married berpotensi lebih besar terhadap nilai CLV, sehingga kita dapat membuat targeting promosi lebih berfokus pada pelanggan yang berstatus menikah. 

#### **Recommendations**

Dari segi bisnis:
1. Memberikan sistem loyalty reward terhadap pelanggan yang memiliki spending dalam jumlah tertentu yang besar (nilai CLV tinggi). Loyalty reward ini biasanya diberikan dalam bentuk poin dan memiliki tingkatan rank tertentu. Nantinya poin ini dapat ditukar dengan berbagai benefit misalnya dalam bentuk barang yang menarik, atau diskon khusus dalam periode waktu tertentu.
2. Perusahaan dapat melakukan penawaran saat renewal polis misalnya apakah penambahan jumlah polis dengan harga yang lebih rendah atau menaikan layanan menjadi premium kepada pelanggan yang memiliki layanan basic.
3. Promosi untuk pelanggan dengan status menikah dapat difokuskan pada benefit untuk keluarga misalnya penambahan polis yang mencakup proteksi terhadap anak saat terjadi kecelakaan mobil.

Dari segi model:

1. Menambah jumlah data agar model tidak cenderung overfitting dan nilai evaluation metrics yang dihasilkan semakin baik. 
2. Penambahan fitur yang berpengaruh terhadap nilai CLV misalnya sudah berapa lama menjadi pelanggan asuransi, informasi alamat, dan lainnya.
3. Untuk mengetahui pelanggan loyal atau tidak dapat dibuat pengembangan model klasifikasi dengan membagi nilai CLV tertentu menjadi 2 kelas yaitu pelanggan loyal dengan CLV tinggi dan tidak loyal dengan CLV rendah.
4. Sebagai fitur yang paling berpengaruh, kita ingin melihat faktor apa saja yang berpengaruh terhadap besarnya jumlah premi yang dibayarkan pelanggan. Sehingga dapat dibuat pengembangan model dengan Monthly Premium Auto sebagai variabel dependen.
