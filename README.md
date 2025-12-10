# clv_analysis
Capstone 2 Project

## **Business Problem Understanding**

#### ***Context***

*Customer* *Lifetime Value* (CLV) adalah sebuah total revenue yang dihasilkan oleh *customer* kepada perusahaan selama durasi tertentu yang sudah disepakati ataupun diperkirakan. CLV merupakan salah satu aspek penilaian seberapa berharga sebuah *customer* bagi perusahaan.

*Customer Lifetime Value* (CLV) menjadi dasar penting bagi perusahaan asuransi otomotif karena biaya akuisisi *customer* di industri ini cukup tinggi dan pola retensi sangat menentukan profitabilitas jangka panjang. Dengan menghitung CLV, perusahaan bisa memahami berapa besar revenue yang realistis dihasilkan seorang pemegang polis selama masa kontrak dan berapa banyak biaya yang layak dikeluarkan untuk mempertahankan mereka. 

Dalam kondisi pasar yang kompetitif dan churn yang mudah terjadi, CLV membantu perusahaan menargetkan segmen *customer* yang benar, menyesuaikan strategi pemasaran, serta mengoptimalkan distribusi resource agar setiap keputusan berbasis pada nilai jangka panjang, bukan transaksi sesaat.



#### ***Problem Statement***

Umumnya perusahaan asuransi otomotif tidak memiliki pemahaman yang jelas tentang nilai jangka panjang setiap *customer*. Mereka hanya mengandalkan usaha mereka dalam mengerahkan waktu dan biaya kepada seluruh *customer* nya tanpa melihat segmen pasarnya. Akibatnya, resource untuk marketing, waktu tim, dan biaya retention sering tidak dialokasikan secara efektif. Tanpa pemanfaatan CLV yang baik, perusahaan kesulitan menargetkan segmen *customer* yang benar, sulit membangun hubungan berkelanjutan, dan berisiko mengalami churn yang sebenarnya dapat dicegah.

#### ***Goals***

Menggunakan data CLV dengan tepat dapat membantu perusahaan memiliki benefit seperti:
1. Keuntungan yang stabil dengan mengoptimasi target market
2. Menghemat waktu yang dikerahkan kepada *customer* yang memiliki CLV tinggi lebih optimal dalam upaya upselling produk
3. Menghemat biaya yang dikerahkan untuk marketing dan retention kepada *customer* dengan segmentasi yang dapat menghasilkan revenue tertinggi
4. Membangun long-lasting connection dengan *customer* sesuai dengan market dari masing-masing segmennya.
5. Menurunkan churn dengan memahami karakter masing-masing *customer*

#### ***Analytic Approach***

Analisis dimulai dengan memetakan karakteristik customer berdasarkan fitur-fitur yang tersedia. Tujuannya adalah mengidentifikasi pola nilai jangka panjang customer, serta memahami kelompok mana yang cenderung memberikan kontribusi terbesar terhadap profit perusahaan.

Setelah struktur datanya dipahami, model prediksi CLV akan dikembangkan menggunakan pendekatan regresi atau machine learning. Model ini difungsikan untuk mengestimasi nilai CLV secara lebih akurat, terutama bagi customer baru atau customer yang belum menunjukkan pola perilaku lengkap. 

#### ***Metric Evaluation***

Kinerja model akan dievaluasi menggunakan RMSE, MAE, dan MAPE sebagai indikator utama. Ketiga metrik ini memberikan gambaran seberapa jauh prediksi CLV menyimpang dari nilai aktual, baik secara absolut maupun persentase. 

Jika model yang terpilih bersifat linear, evaluasi dapat dilengkapi dengan R-squared atau adjusted R-squared untuk melihat seberapa besar variasi CLV yang mampu dijelaskan oleh fitur yang digunakan. Untuk model non-linear, fokus evaluasi tetap diarahkan pada metrik error karena lebih representatif dalam mengukur ketepatan prediksi.

#### ***Kesimpulan***

Customer Lifetime Value menunjukkan hasil yang baik jika model prediksinya dikembangkan menggunakan model CatBoost dengan R^2 = 0.90 dan RMSE yang sangat kecil sehingga menunjukkan bahwa model ini dapat melihat hubungan yang jelas antar data prediktornya. Data yang berpengaruh terhadap nilai CLV antara lain Monthly Premium Auto dan Special Car, sehingga perusahaan perlu menaruh lebih banyak perhatian kepada customer yang memiliki premi bulanan yang lebih mahal ataupun memiliki jenis kendaraan yang spesial. Model machine learning ini memiliki perhatian fitur yang sangat tinggi terhadap Number of Policies dan Monthly Premium Auto, dan didukung dengan Income, Jenis Coverage, Total Claim, dan Education, yang berarti ada pengaruh juga dari sisi berapa policies yang dimiliki customer, berapa incomenya, apa jenis coverage yang dimiliki, total claim yang dilakukan, dan tingkat pendidikan dari customer itu sendiri.
