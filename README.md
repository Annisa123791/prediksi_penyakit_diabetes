# Laporan Proyek ML - Annisa Saninah

## Domain Proyek

## Latar Belakang

**Diabetes mellitus** adalah sekumpulan gangguan yang melibatkan aspek autoimun, metabolik, dan genetik, yang ditandai dengan kondisi utama yaitu hiperglikemia atau kadar gula darah yang tinggi. Metode pengukuran glukosa plasma serta batas ambang untuk menentukan kadar normal atau abnormal telah mengalami beberapa revisi selama beberapa dekade terakhir. Artikel ini membahas berbagai rekomendasi terbaru dan definisi terkini mengenai diabetes mellitus serta kondisi hiperglikemia pada tingkat sedang. Selain itu, artikel ini juga menguraikan perbedaan pendekatan antara Amerika Serikat dan negara-negara lain di dunia.

---

### Apa itu Diabetes?

Diabetes mellitus bukanlah sebuah penyakit tunggal, melainkan kumpulan kondisi metabolik yang ditandai oleh hiperglikemia akibat kekurangan insulin, baik sebagian maupun total. Hiperglikemia yang berlangsung lama dapat menimbulkan komplikasi mikro-vaskular seperti:

- Kerusakan pada retina

- Kerusakan ginjal

- Gangguan pada saraf perifer

Walaupun komplikasi tersebut sering ditemukan pada penderita diabetes, mereka **tidak dijadikan dasar untuk diagnosis** karena kemunculannya yang relatif lambat.

---

### Bagaimana Diabetes Diklasifikasikan?

Terdapat **empat kategori utama** diabetes mellitus:

1. **Diabetes tipe 1**  
   
   Diabetes mellitus dibagi menjadi **empat kategori utama**, yaitu:
   
   1. **Diabetes tipe 1**
      
      - Kerusakan pada sel β pankreas yang umumnya disebabkan oleh mekanisme inflamasi autoimun.
      
      - Terdapat penanda autoimun dalam serum, seperti:
        
        - Antibodi terhadap sel islet
        
        - Antibodi terhadap GAD
        
        - Insulin
        
        - IA-2 dan IA-2β
        
        - Transporter seng ZnT8
      
      - Proses ini biasanya mengakibatkan kekurangan insulin secara total.
   
   2. **Diabetes tipe 2**
   
   3. **Tipe diabetes khusus lainnya**
   
   4. **Diabetes gestasional**

### Bagaimana Diagnosis Diabetes Dibuat?

Diagnosis diabetes dapat dibuat jika salah satu dari kriteria berikut terpenuhi:

- Glukosa plasma acak mencapai atau melebihi 11,1 mmol/l disertai gejala khas hiperglikemia seperti:
  
  - Rasa haus yang berlebihan (polidipsia)
  
  - Sering buang air kecil (poliuria)
  
  - Penurunan berat badan (biasanya menandakan kekurangan insulin)

- Glukosa plasma puasa (tidak makan selama minimal 8 jam) sebesar atau lebih dari 7,0 mmol/l

- Glukosa plasma mencapai atau melebihi 11,1 mmol/l dua jam setelah pemberian tes toleransi glukosa (beban glukosa)

---

### Apa itu Pre-Diabetes?

Kondisi yang berada di antara keadaan normal dan diabetes dikenal dengan istilah:

- **Impaired Fasting Glucose (IFG)**

- **Impaired Glucose Tolerance (IGT)**

Meskipun bukan merupakan gangguan klinis, istilah *pre-diabetes* sering digunakan untuk menggambarkan kondisi ini. Hal ini penting karena:

- Menjadi penanda risiko tinggi untuk berkembangnya diabetes di masa mendatang

- Risiko penyakit kardiovaskular juga meningkat pada tahap ini

### Referensi

- [Understanding diabetes mellitus: biochemical and clinical perspectives – ScienceDirect](https://www.sciencedirect.com/science/article/abs/pii/S1357303918302627)

## Business Understanding

### Problem Statement

Berdasarkan latar belakang masalah yang telah dijelaskan sebelumnya, rumusan masalah (*problem statements*) dalam proyek ini adalah sebagai berikut:

1. Bagaimana cara memprediksi penyakit diabetes mellitus menggunakan algoritma machine learning?

2. Bagaimana mengembangkan model machine learning yang efektif untuk prediksi penyakit diabetes?

3. Bagaimana evaluasi kinerja model machine learning yang telah dibuat dalam memprediksi penyakit diabetes?

### Goals

Berdasarkan rumusan masalah (*problem statements*) yang telah disusun sebelumnya, tujuan (*goals*) dari proyek machine learning ini adalah sebagai berikut:

1. Memahami penerapan algoritma machine learning dalam prediksi penyakit diabetes mellitus.

2. Memahami tahapan proses pengembangan model machine learning dari awal hingga selesai untuk memprediksi penyakit diabetes mellitus.

3. Menilai performa atau melakukan evaluasi terhadap model machine learning yang telah dikembangkan dalam memprediksi penyakit diabetes.

### Solution Statements

Berdasarkan *problem statements* dan *goals* yang telah dijelaskan sebelumnya, berikut adalah *solution statements* dalam proyek machine learning ini:

1. Melaksanakan proses pengembangan model machine learning secara menyeluruh, mulai dari *data wrangling*, *Exploratory Data Analysis* (EDA), pembuatan model (*modelling*), hingga evaluasi (*evaluation*).

2. Mengembangkan model machine learning dengan menggunakan algoritma klasifikasi yang sesuai untuk memprediksi kelas (diabetes atau non-diabetes) berdasarkan dataset yang tersedia. Algoritma yang digunakan dalam proyek ini antara lain:
   
   - *Random Forest Classification*: algoritma ensemble learning yang menggabungkan banyak pohon keputusan (decision trees) untuk meningkatkan akurasi dan performa prediksi.
   
   - *Hyperparameter Tuning* menggunakan *Grid Search* untuk menemukan konfigurasi terbaik dalam pelatihan model machine learning.

3. Melakukan evaluasi model untuk mengukur performa dengan menggunakan metrik evaluasi yang telah ditetapkan. Evaluasi ini bertujuan untuk menentukan seberapa baik model yang dikembangkan dalam memprediksi diabetes, sehingga dapat dipilih model machine learning yang paling efektif untuk keperluan tersebut.

## Data Understanding

Dataset yang digunakan dalam proyek ini adalah dataset diabetes yang memuat informasi medis pasien, termasuk beberapa parameter penting seperti kadar glukosa, tekanan darah, BMI, dan lainnya. Dataset ini mengandung data tentang apakah seseorang mengidap diabetes (Outcome 1) atau tidak (Outcome 0). Dataset tersebut berformat csv (comma-separated values) dengan ukuran 23.88 kB. Dataset tersebut terdiri dari 768 data records dengan 9 feature column.

Link dataset: [Diabetes Dataset](https://www.kaggle.com/datasets/whenamancodes/predict-diabities)

### Variabel-variabel pada dataset adalah sebagai berikut:

| Kolom                        | Deskripsi                                                           |
| ---------------------------- | ------------------------------------------------------------------- |
| **Pregnancies**              | Jumlah kehamilan yang pernah dialami                                |
| **Glucose**                  | Tingkat glukosa dalam darah                                         |
| **BloodPressure**            | Tekanan darah (dalam mm Hg)                                         |
| **SkinThickness**            | Ketebalan lipatan kulit (dalam mm)                                  |
| **Insulin**                  | Kadar insulin dalam darah (dalam mu U/ml)                           |
| **BMI**                      | Indeks massa tubuh (Body Mass Index)                                |
| **DiabetesPedigreeFunction** | Skor riwayat keturunan diabetes                                     |
| **Age**                      | Usia pasien (dalam tahun)                                           |
| **Outcome**                  | Hasil diagnosa (1 = Mengidap diabetes, 0 = Tidak mengidap diabetes) |

### Visualization & Analysis

- **Univariate Analysis**
  
  <p align='center'><img src ="https://raw.githubusercontent.com/Synjoestar/diabetesprediksi/main/images/1.png?raw=true" width="300"></p>
  <p align='center'>Gambar 1. Pie-Chart Diabetes & Non-Diabetes</p> 
  Berdasarkan visualisasi grafik *pie-chart* pada gambar 1 di atas menunjukkan bahwa jumlah penderita penyakit diabetes yaitu 268 orang (34,9 %). Sedangkan jumlah orang yang non-diabetes yaitu  500 orang (65,1%) dari total keseluruhan jumlah orang dalam dataset (768 orang).

<p align='center'><img src ="https://raw.githubusercontent.com/Synjoestar/diabetesprediksi/main/images/2.png?raw=true"  width="400"></p>
<p align='center'>Gambar 2. Visualisasi feature numerik</p>
<br>
Berdasarkan visualisasi untuk *feature* numerik pada dataset yang dapat dilihat pada histogram di atas, dapat diketahui beberapa informasi, yaitu : sebagaian besar orang memiliki glukosa dengan tingkat 100-150; sebagian besar orang memiliki *BloodPressure* pada tingkat 60-90; sebagian besar orang memiliki BMI berkisar dari 25-40; sebagian besar orang memiliki *DiabetesPedigreeFunction* berkisar dari 0.0 hingga 0.75; dan sebagian besar orang berumur 20-30 tahun. <br><br>

- **Multivariate Analysis**<br>
  Visualisasi pada gambar 3 di bawah menggambarkan hubungan antar fitur dalam dataset. Dari gambar tersebut, terlihat bahwa tingkat korelasi antar fitur bervariasi; beberapa fitur menunjukkan korelasi yang lemah atau bahkan tidak memiliki korelasi sama sekali, sementara beberapa fitur lain memiliki korelasi meskipun tidak terlalu kuat.
  
  <p align='center'>Gambar 3. Visualisasi multivariate analysis</p>
  <p align='center'><img src ="https://raw.githubusercontent.com/Synjoestar/diabetesprediksi/main/images/3.png?raw=true"  width="400"></p>

- **Outliers**
  Visualisasi boxplot di atas bertujuan untuk mendeteksi adanya pencilan (outliers) dalam dataset yang digunakan pada proyek machine learning. Hal ini penting karena keberadaan outliers dapat menyebabkan bias atau menurunkan akurasi model dalam melakukan prediksi.

<p align='center'>Gambar 4. Mengecek outliers</p>
<p align='center'><img src ="https://raw.githubusercontent.com/Synjoestar/diabetesprediksi/main/images/4.png?raw=true"  width="400"></p>

## Data Preparation

*Data preparation* adalah proses mengolah data mentah agar menjadi format yang tepat untuk analisis atau proses selanjutnya. Beberapa teknik yang digunakan dalam tahap persiapan data pada proyek ini antara lain:

1. **Penanganan outliers**
- *Outliers* adalah nilai-nilai yang menyimpang jauh dari nilai-nilai lain dalam dataset. Nilai-nilai ini muncul sebagai anomali yang tidak mengikuti pola umum data. Outliers bisa berupa nilai yang jauh lebih tinggi atau lebih rendah dibandingkan data lainnya, dan dapat disebabkan oleh kesalahan pengukuran, kejadian yang jarang terjadi, atau faktor tak terduga lainnya.

- Tujuan dari penanganan outliers adalah untuk memastikan bahwa nilai-nilai ekstrem tersebut tidak mengganggu analisis statistik atau model machine learning yang dikembangkan. Karena outliers berpotensi memberikan informasi yang menyesatkan dan mempengaruhi hasil analisis, penting untuk menanganinya agar hasil yang diperoleh lebih akurat dan dapat diandalkan.

- Beberapa cara yang dapat digunakan untuk menangani outliers meliputi identifikasi outliers, transformasi data, penghapusan outliers, dan imputasi data. Pada proyek ini, penanganan outliers dilakukan dengan metode imputasi menggunakan pendekatan *IQR method*. Hasil dari metode imputasi ini dapat dilihat pada gambar 5 berikut:

<p align='center'>Gambar 5. handling outliers</p>
<p align='center'><img src ="https://raw.githubusercontent.com/Synjoestar/diabetesprediksi/main/images/5.png?raw=true"  width="400"></p>

2. **Handling imbalanced data**
   
   - *Imbalanced data* adalah kondisi di mana distribusi jumlah kelas dalam dataset tidak merata.
   
   - Tujuan penanganan data tidak seimbang adalah untuk meningkatkan kemampuan model dalam memprediksi kelas yang jumlahnya lebih sedikit (kelas minoritas).
   
   - Ada beberapa metode untuk mengatasi masalah ini. Salah satunya adalah *oversampling*, yaitu memperbanyak sampel dari kelas minoritas agar jumlahnya menjadi seimbang dengan kelas mayoritas, baik dengan menggandakan data yang ada atau membuat data sintetis baru. Metode lain adalah *undersampling*, yaitu mengurangi jumlah sampel pada kelas mayoritas agar seimbang dengan kelas minoritas, biasanya dengan menghapus sebagian data kelas mayoritas.
   
   - Dalam proyek ini, penanganan data tidak seimbang dilakukan menggunakan metode *SMOTE* (*Synthetic Minority Over-sampling Technique*), yang membuat sampel sintetis untuk kelas minoritas (kelas "1" pada kolom *Outcome*). Dengan cara ini, jumlah kelas minoritas dapat disamakan dengan kelas mayoritas, sehingga mengurangi bias model terhadap kelas mayoritas dan meningkatkan performa model untuk memprediksi kelas minoritas.

<p align='center'>Gambar 6. Imbalanced data</p>
<p align='center'><img src ="https://raw.githubusercontent.com/Synjoestar/diabetesprediksi/main/images/7.png?raw=true"  width="400"></p>

3. **Data Splitting**
   
   - Data Splitting adalah proses pemisahan *dataset* menjadi beberapa bagian yang berbeda untuk keperluan tertentu dalam analisis data, seperti pelatihan, validasi, dan pengujian model.
   
   - Tujuan dari tahap ini adalah membagi data menjadi dua kelompok, yaitu satu bagian untuk melatih model (set pelatihan) dan bagian lainnya untuk menguji performa model (set pengujian).
   
   - Metode yang digunakan dalam proses ini adalah *Train-test split*.

4. **Standardization**
   
   - Standardisasi merupakan proses pengubahan data agar memiliki rata-rata (*mean*) sebesar nol dan varians (*variance*) sebesar satu.
   
   - Tujuan standardisasi adalah untuk membuat distribusi data menjadi lebih terpusat di sekitar angka nol dengan variasi yang konsisten, sehingga membantu algoritma machine learning dalam memahami dan mengolah data secara lebih efektif.
   
   - Metode yang diterapkan melibatkan pengurangan setiap nilai fitur dengan rata-rata fitur tersebut, lalu membaginya dengan standar deviasi fitur tersebut. Pada kasus ini, *StandardScaler* dari scikit-learn digunakan untuk melakukan standardisasi dengan perhitungan *z-score*.

## Modeling

Pada proyek ini algoritma machine learning yang digunakan di antaranya yaitu *`Random forest classification`* dan *`Hyperparameter Tuning Grid Search`.*

### Random Forest Classification

**Random Forest Classification* adalah algoritma *supervised learning* yang digunakan untuk masalah klasifikasi. Algoritma ini termasuk dalam kategori *ensemble learning*, yang terdiri dari sejumlah pohon keputusan (*decision tree*) yang bekerja secara kolektif untuk meningkatkan akurasi dan performa prediksi. Pada model *ensemble*, setiap pohon mengambil keputusan secara mandiri, lalu hasil prediksi dari semua pohon tersebut digabungkan untuk menghasilkan prediksi akhir. *Random Forest* menggabungkan prediksi dari banyak pohon keputusan yang dibuat secara acak.

**Kelebihan**:

- *Random Forest* populer karena kesederhanaannya sekaligus memiliki kestabilan yang baik.

- Algoritma ini lebih efektif mencegah *overfitting* dibandingkan dengan *Decision Tree* dan mampu menangani dataset besar dengan banyak fitur.

**Kekurangan**:

- Waktu pelatihan *Random Forest* lebih lama dibandingkan *Decision Tree* karena tingkat kompleksitas model yang lebih tinggi.

### Implementasi

Proses pemodelan dengan algoritma *Random Forest* dalam proyek ini, yang berfokus pada masalah klasifikasi, menggunakan fungsi *`RandomForestClassifier()`* dari pustaka *scikit-learn*. Parameter yang diterapkan dalam proyek ini adalah *`n_estimators=50`*, *`max_depth=5`*, dan *`max_features='auto'`*. Parameter *`n_estimators`* adalah *hyperparameter* yang menentukan jumlah pohon (*trees*) dalam hutan acak, dimana pada proyek ini digunakan sebanyak 50 pohon. Selanjutnya, *`max_depth`* mengacu pada kedalaman maksimal setiap pohon, yang mengatur seberapa dalam pohon dapat membelah (*splitting*) node untuk mencapai jumlah pengamatan tertentu; pada proyek ini nilai *max_depth* yang dipakai adalah 5. Parameter terakhir, *`max_features`*, adalah *hyperparameter* yang mengatur jumlah fitur maksimum yang dipertimbangkan saat mencari titik percabangan terbaik, dan pada proyek ini diatur pada nilai 'auto'.

### Hyperparameter Tuning

*Hyperparameter* digunakan untuk menyesuaikan model serta mengatur proses pelatihan agar sesuai dengan dataset atau masalah yang ingin diselesaikan. Sedangkan *hyperparameter tuning* bertujuan untuk menemukan konfigurasi terbaik yang dapat meningkatkan performa model *machine learning*. Proses tuning ini bisa dilakukan secara manual dengan mencoba berbagai kombinasi *hyperparameter* sampai ditemukan yang optimal. Alternatif lainnya adalah melakukan *hyperparameter tuning* secara otomatis dengan bantuan algoritma, salah satunya adalah *grid search*.

*Grid search* adalah algoritma yang memungkinkan proses *hyperparameter tuning* secara otomatis dengan membangun sebuah ruang pencarian *n*-dimensi yang terdiri dari *n* *hyperparameter* model. Setiap titik dalam ruang pencarian tersebut merepresentasikan satu kombinasi dari *hyperparameter*. Algoritma ini kemudian mengevaluasi setiap titik untuk menemukan konfigurasi *hyperparameter* terbaik.

Dalam proyek ini, dilakukan *Hyperparameter Tuning* menggunakan *Grid Search* untuk meningkatkan performa model *Random Forest* yang sudah dibuat. Parameter yang diatur dalam tuning ini meliputi:

- *random_state*: mengontrol generator angka acak pada model.

- *max_depth*: mengatur kedalaman maksimum pohon keputusan.

- *max_features*: menentukan jumlah maksimum fitur yang dipakai untuk mencari percabangan terbaik.

- *criterion*: metrik yang digunakan untuk menilai kualitas percabangan.

- *n_estimators*: jumlah pohon (*trees*) yang digunakan dalam algoritma *random forest*.

Dari hasil *Grid Search*, diperoleh konfigurasi terbaik yang meningkatkan performa model *Random Forest*, yaitu: `criterion: gini`, `max_depth: 8`, `max_features: auto`, dan `n_estimators: 50`.

### Pemilihan model :

Berdasarkan eksperimen selama proses pengembangan model, model *machine learning* terbaik yang diperoleh adalah *Random Forest Classification* yang dilengkapi dengan *Hyperparameter Tuning* menggunakan *Grid Search*. Hal ini dibuktikan dari hasil *confusion matrix* dan *classification report* yang menunjukkan performa model ini lebih unggul dibandingkan dengan model *Random Forest* tanpa penerapan *hyperparameter tuning*. Dengan demikian, model *machine learning* yang dikembangkan telah berhasil memenuhi tujuan yang telah dirumuskan dalam *solution statements* sebelumnya.

## Evaluation

Dalam proyek machine learning ini, evaluasi model akan dilakukan menggunakan **confusion matrix**. Confusion matrix memberikan gambaran performa model pada masing-masing kelas dengan menunjukkan jumlah prediksi yang benar (True) dan salah (False) untuk setiap label.

Dengan memanfaatkan confusion matrix, kita dapat menilai seberapa efektif model machine learning yang telah dikembangkan. Data dari confusion matrix ini juga akan digunakan untuk menghitung berbagai metrik evaluasi lain, seperti accuracy, precision, recall, dan F1-score.

- **Accuracy** mengukur tingkat keberhasilan model dalam menghasilkan prediksi yang benar dari seluruh prediksi yang dibuat.

- **Precision** menunjukkan seberapa tepat model dalam memprediksi kelas tertentu, dihitung sebagai rasio antara jumlah prediksi benar pada kelas tersebut dengan total prediksi yang diberikan untuk kelas itu.

- **Recall** mengukur kemampuan model dalam menangkap seluruh data yang termasuk dalam kelas tertentu, yaitu perbandingan antara jumlah prediksi benar untuk kelas tersebut dengan total data sebenarnya di kelas itu.

- **F1-score** merupakan gabungan dari precision dan recall, memberikan nilai keseimbangan antara keduanya untuk suatu kelas.

Berdasarkan konteks data, rumusan masalah, dan solusi yang diterapkan, metrik evaluasi yang dipilih dalam proyek ini adalah **Recall**. Recall menjadi fokus karena lebih penting untuk meminimalkan kesalahan memprediksi seseorang sebagai penderita diabetes padahal sebenarnya tidak (false positive), dibandingkan kesalahan sebaliknya, yaitu menganggap seseorang non-diabetes padahal sebenarnya dia penderita diabetes.

### Training Set Performance

Train Accuracy Score: 87.52%
CLASSIFICATION REPORT:

```
              precision    recall  f1-score   support

           0       0.87      0.95      0.91       349
           1       0.89      0.74      0.81       188

    accuracy                           0.88       537
   macro avg       0.88      0.84      0.86       537
weighted avg       0.88      0.88      0.87       537
```

<p align='center'>Gambar 7. Confusion Matrix (Train)</p>
<p align='center'><img src ="https://raw.githubusercontent.com/Synjoestar/diabetesprediksi/main/images/8.png?raw=true"  width="400"></p>

Test Accuracy Score: 74.46%
CLASSIFICATION REPORT:

```
              precision    recall  f1-score   support

           0       0.79      0.83      0.81       151
           1       0.65      0.57      0.61        80

    accuracy                           0.74       231
   macro avg       0.72      0.70      0.71       231
weighted avg       0.74      0.74      0.74       231
```

<p align='center'>Gambar 8. Confusion Matrix (Test)</p>
<p align='center'><img src ="https://raw.githubusercontent.com/Synjoestar/diabetesprediksi/main/images/9.png?raw=true"  width="400"></p>

### Training Set Performance (tuning)

**Accuracy Score:** 98.70%

**Classification Report:**

```
              precision    recall  f1-score   support

           0       0.98      1.00      0.99       349
           1       1.00      0.96      0.98       188

    accuracy                           0.99       537
   macro avg       0.99      0.98      0.99       537
weighted avg       0.99      0.99      0.99       537
```

<p align='center'>Gambar 9. Confusion Matrix (Train)</p>
<p align='center'><img src ="https://raw.githubusercontent.com/Synjoestar/diabetesprediksi/main/images/10.png?raw=true"  width="400"></p>
---

### Test Set Performance

**Accuracy Score:** 75.32%

**Classification Report:**

```
              precision    recall  f1-score   support

           0       0.82      0.79      0.81       151
           1       0.64      0.68      0.65        80

    accuracy                           0.75       231
   macro avg       0.73      0.73      0.73       231
weighted avg       0.76      0.75      0.75       231
```

<p align='center'>Gambar 10. Confusion Matrix (Test)</p>
<p align='center'><img src ="https://raw.githubusercontent.com/Synjoestar/diabetesprediksi/main/images/11.png?raw=true"  width="400"></p>
---

## Kesimpulan

- Tuning model memberikan pengaruh signifikan terhadap performa pada data pelatihan, dimana akurasi meningkat dari 87% menjadi 98%, yang menunjukkan model menjadi lebih mampu menangkap pola dalam data tersebut.

- **Namun, pada data pengujian**, peningkatan akurasi hanya terjadi secara marginal. Hal ini mengindikasikan bahwa:
  
  - Model berpotensi mengalami *overfitting*, yaitu terlalu menyesuaikan diri dengan data pelatihan.
  
  - Meskipun demikian, ada aspek positif yang terlihat, yaitu **peningkatan kemampuan model dalam mengenali penderita diabetes** yang merupakan **tujuan utama** dari model klasifikasi ini.

---
