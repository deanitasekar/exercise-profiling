# Advanced Programming Module 5 - Java Profiling
###### Deanita Sekar Kinasih
###### 2306229405

### Test Results
### *Endpoint* `/all-student`
Test Result:
![](/reports_testresults/testresults1.png)
Before Optimization:
![](/reports_testresults/before-all-student.png)
After Optimization:
![](/reports_testresults/after-all-student.png)

### *Endpoint* `/all-student-name`
Test Result:
Test Result:
![](/reports_testresults/testresults2.png)
Before Optimization:
![](/reports_testresults/before-all-student-name.png)
After Optimization:
![](/reports_testresults/after-all-student-name.png)

### *Endpoint* `/highest-gpa`
Test Result:
![](/reports_testresults/testresults3.png)
Before Optimization:
![](/reports_testresults/before-highest-gpa.png)
After Optimization:
![](/reports_testresults/after-highest-gpa.png)

Berdasarkan hasil tersebut, terlihat bahwa `Sample Time` sebelum dioptimasi menunjukkan waktu yang lebih lama dibandingkan setelah optimasi, dengan peningkatan performa berdasarkan waktu eksekusi yang diperoleh. Oleh karena itu, dapat disimpulkan bahwa proses optimasi yang dilakukan dengan bantuan JMeter dan Intellij Profiler terbilang berhasil untuk membuat kode lebih efektif dan efisien.

### Reflection
#### 1. What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?

Perfomance Testing dengan JMeter dan profiling with IntelliJ Profiler merupakan hal yang berbeda dalam konteks pengembangan aplikasi. JMeter berfokus pada evaluasi sistem secara keseluruhan dengan tujuan menguji kemampuan sistem dalam menghadapi berbagai beban dan tekanan, serta melakukan verifikasi kesesuaiannya dengan _Service Level Agreements_ (SLA). Di samping itu, profiling with IntelliJ Profiler dilakukan sebagai tindak lanjut setelah ditemukannya masalah dalam pengujian. Profiling berfungsi untuk mendeteksi komponen-komponen spesifik dalam sistem yang menjadi penyebab utama masalah performa dan memberikan panduan tentang perbaikan.

#### 2. How does the profiling process help you in identifying and understanding the weak points in your application?

Profiling membantu saya sebagai developer dengan cara mengidentifikasi dan menyoroti bagian-bagian kode yang menggunakan _resource_ secara berlebihan. Dengan informasi ini, developer dapat melaksanakan optimalisasi kode secara efektif dan efisien sehingga dapat meningkatkan performa aplikasi. Metode profiling menjadi krusial, khususnya ketika berhadapan dengan sistem kompleks, dimana penemuan _bottlenecks_ tanpa bantuan profiling akan menjadi tantangan yang signifikan. 

#### 3. Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?

Ya, IntelliJ Profiler bermanfaat abgi saya sebagai developer dalam memudahkan identifikasi dan analisis titik-titik _bottlenecks_ secara efektif. IntelliJ Profiler menyediakan berbagai representasi visual dari hasil evaluasi performa, termasuk `Flame Graph`, `Method List`, dan lainnya. Informasi yang diberikan juga meliputi `CPU Time`, `Total Time`, dan `Memory` yang digunakan. Dengan memanfaatkan IntelliJ Profiler, proses evaluasi performa kode menjadi lebih tepat guna dan hemat waktu. 

#### 4. What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?

Salah satu tantangan utama yang saya hadapi adalah kesulitan dalam menginterpretasikan visualisasi data seperti `Flame Graph` dan teknis khusus lainnya. Selain itu, adanya kompleksitas dalam memahami istilah baru seperti perbedaan antara `CPU Time` dan `Total Time`. Tak hanya itu, terdapat tantangan dalam melakukan evaluasi efisiensi method ketika hanya dijasikan satuan waktu (ms) tanpa standar perbadingan. 

Untuk mengatasi tantangan yang dihadapi, saya perlu melakukan review kembali module yang disediakan secara lebih mendalam dan melakukan belajar mandiri melalui berbagai sumber. Selain itu, saya juga perlu memperbanyak pengalaman dalam _refactoring_ code untuk meningkatkan pengetahuan tentang standar _running time_ dan penggunaan resources yang normal dari sebuah method. 

#### 5. What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?

Keunggulan utama penggunaan IntelliJ Profiler terletak pada integrasi yang kuat antara IDE dengan Profiler, yang menyederhanakan proses analisis kode. Selain itu, antarmuka yang intuitif dan ramah pengguna memudahkan interpretasi hasil evaluasi. IntelliJ Profiler juga menyajikan data komprehensif yang mencakup CPU Time, Total Time, dan Memory, sehingga memungkinkan saya sebagai developer untuk mengidentifikasi kode yang memerlukan optimasi dan melakukan perbaikan secara efisien. 

#### 6. How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?

Meskipun jarang ditemui, terdapat beberapa langkah yang dapat dilakukan apabila hasil profiling dengan IntelliJ Profiler tidak konsisten dengan hasil temuan performance testing menggunakan JMeter, yaitu:
- Melakukan verifikasi menyeluruh terhadap konfigurasi dan parameter yang diimplementasikan dalam kedua proses
- Memastikan kondisi dan konfigurasi serupa, lalu analisis perbedaan environment
- Meneliti hasil dari kedua proses secara menyeluruh, lalu cari pola atau anomali
- Apabila diperlukan, dapat dilakukan pengujian ulang dan konsultasi dengan ahli

#### 7. What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?

Terdapat beberapa strategi yang dapat dilakukan untuk mengoptimalkan kode:
- Melakukan analisis hasil profiling untuk menemukan method yang menghabiskan paling banyak waktu dan resource
- Berfokus untuk memahami kode dan mengidentifikasi bagian yang dapat dioptimasi
- Memilih algoritma dan struktur data yang paling efisien untuk method tersebut
- Mendeteksi kode yang dapat dijalankan secara paralel dan menerapkan _threading_ atau _multiprocessing_
