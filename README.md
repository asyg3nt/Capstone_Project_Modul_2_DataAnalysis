# **NYC Green Taxi Demand Analysis**

Capstone Project Module 2 — JCDS Purwadhika  
Oleh: Muhammad Mirza Asyrafi  
### Latar Belakang
**Tantangan Operasional di Industri Taksi NYC**  
Setiap hari, ribuan pengemudi taksi harus memutuskan di mana mereka akan beroperasi dan kapan mereka akan bekerja untuk memaksimalkan penghasilan. Sementara itu, TLC dan operator fleet taksi dihadapkan dengan tantangan logistik yang kompleks:   

* **Ketidakseimbangan armada:**  
Pengemudi sering menumpuk di area dengan demand tinggi (seperti pusat kota atau area komersial), sementara area perumahan atau pinggiran kota kekurangan armada saat demand tinggi.  

* **Waktu operasional yang tidak efisien:**   
Tidak semua waktu dalam sehari memiliki demand yang sama. Jam sibuk pagi dan sore berbeda dengan tengah malam. Tanpa pemahaman pola demand, armada tidak dialokasikan secara optimal.  

* **Pengalaman penumpang yang buruk:**     
Ketidaksesuaian antara supply dan demand mengakibatkan waktu tunggu yang lama bagi penumpang atau kesulitan menemukan taksi di area tertentu.  
  
* **Efisiensi ekonomi:**    
Pengemudi yang tidak berada di lokasi dengan demand tinggi akan memiliki pendapatan lebih rendah, yang berdampak pada kepuasan pengemudi dan tingkat pergantian karyawan.   
  
### **Pertanyaan Bussines:**    
* Bagaimana pola permintaan layanan Taxi di NYC berdasarkan waktu, lokasi, perilaku penumpang? serta insight apa yang dapat membantu distribusi armada serta strategi operasional yang lebih baik?  
  
### **Tujuan Analisis:**  
* mencari pola demand per jam, hari, dan lokasi sehingga armada bisa dialokasikan lebih strategis.  
* memberikan rekomendasi actionable untuk operasional TLC, seperti peningkatan armada di area/waktu tertentu atau strategi pricing dinamis.  
* membantu driver membuat keputusan lebih baik tentang di mana dan kapan beroperasi untuk memaksimalkan penghasilan.  
* mencari peluang pertumbuhan di area yang underserved atau waktu dengan potential tinggi.  
  
### **Bussines Understanding :**
Taksi resmi di NYC diatur oleh pihak TLC dan dibagi menjadi dua jenis. Pertama, Yellow Taxi yang fokus beroperasi di pusat Manhattan dan bandara. Kedua, Green Taxi yang diluncurkan pada tahun 2013 khusus untuk melayani area pinggiran (outer boroughs) yang tidak sering diakses oleh taksi kuning.  
  
Setelah riset lebih jauh,   
Dikarenakan terdapat kolom dengan nama lpep, maka dapat disimpulkan bahwa    
Dataset ini berfokus pada Green Taxi.     

### **Ringkasan Dataset**
* Sumber Data: NYC TLC Trip Record Data  
* Sumber data tambahan = lookup_zone.csv (https://d37ci6vzurychx.cloudfront.net/misc/taxi_zone_lookup.csv)
* Periode: Januari 2023
* Total data mentah: 68.211 baris (20 kolom)
* Total data bersih: 59.811 baris (26 kolom, setelah penambahan kolom baru)

### **Proses Analisis**

* Analisis ini dikerjakan melalui beberapa tahapan:
* Memahami struktur awal data dan mengecek anomali.
* Membersihkan data dari missing value, outlier, durasi yang tidak masuk akal.
* Mengekstrak kolom baru seperti pembagian jam, nama hari, dan shift kerja untuk memperdalam analisis.
* Melakukan uji statistik (Spearman, Mann-Whitney, Kruskal-Wallis) untuk memastikan secara statistik.
* tahapan EDA dan Memvisualisasikan hasil.

### **Temuan Utama**
* Jam 18:00 adalah waktu paling sibuk, menyumbang hampir 8% dari total tarikan seharian
* Manhattan mendominasi 60,9% total perjalanan
* dua zona di East Harlem menyumbang hingga 35% dari total seluruh perjalanan
* Hari kerja didominasi rute komuter jarak pendek
* akhir pekan orang cenderung bepergian lebih jauh
* Pesanan dispatch jumlahnya sangat kecil (1,3%)
