[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/174iODBg)
# Resume Finger Simulation Experiment - F1D022146


## Data Understanding
_Jelaskan mengenai data yang digunakan dalam project kalian, seperti jumlah data, jumlah kelas, serta bagaimana cara kalian mendapatkan data tersebut._

_Jadi data yang digunakan pada project kali ini yaitu yaitu data berupa finger yang dimana memiliki jumlah data yaitu 2.164 data yang dimana terbagi menjadi 5 kelas yaitu  finger 1 sampai dengan finger 5. Cara mendapatkan data yang ada yaitu dengan mengambil gambar dari sebuah drive yang telah disediakan oleh asisten praktikum yang dimana masing masing praktikan harus meng-upload masing masing kelas yang ada yaitu finger 1 sampai dengan finger 5 dengan 3 posisi yang berbeda._

## Data Preparation

### Image Augmentation

_Dari setiap percobaan yang telah kalian lakukan, jelaskan bagaimana cara kalian menemukan preprocessing yang paling tepat. Jelaskan alasan kalian menggunakan teknik tersebut dan berikan alasan mengapa preprocessing diperlukan.._

_Teknik augmentasi gambar yang digunakan dalam project kali ini yaitu meliputi beberapa transformasi dasar yang menghasilkan variasi dari satu gambar asli. Pertama, gambar asli dirotasi sebesar 180 derajat untuk memberikan variasi sudut pandang. Kedua, gambar tersebut dibalik secara horizontal, menghasilkan gambar cermin dari kiri ke kanan. Teknik ketiga adalah membalik gambar secara vertikal, sehingga gambar terlihat terbalik dari atas ke bawah. Selain itu, gambar dirotasi 90 derajat searah jarum jam, memberikan perspektif baru. Selanjutnya, gambar dirotasi 90 derajat berlawanan arah jarum jam untuk menambah variasi. Hasil dari kombinasi ini adalah tujuh gambar baru dari satu gambar asli. Dengan augmentasi ini, setiap gambar asli akan menghasilkan delapan gambar total (satu gambar asli dan tujuh gambar yang teraugmentasi)._

### Preprocessing

_Dari setiap percobaan yang telah kalian lakukan, jelaskan bagaimana cara kalian menemukan preprocessing yang paling tepat. Jelaskan alasan kalian menggunakan teknik tersebut dan berikan alasan mengapa preprocessing diperlukan._

_Pada percobaan 1, menggunakan teknik konversi gambar ke grayscale. Grayscale juga mengurangi kompleksitas data, mempercepat komputasi, dan mengurangi kebutuhan memori. Selanjutnya, gambar diubah ukurannya ke 150x150 piksel untuk menyatukan resolusi, memastikan konsistensi input ke model. Pada percobaan 2, Teknik yang digunakan adalah konversi gambar ke grayscale diikuti dengan thresholding. Konversi ke grayscale mengurangi kompleksitas data dan mempercepat proses komputasi. Thresholding kemudian diterapkan untuk binarisasi gambar, membuat kontras lebih jelas. Pada percobaan 3 digunakan teknik preprocessing yaitu grayscale diikuti dengan dilasi menggunakan kernel. Grayscale mengurangi kompleksitas data dan mempercepat proses komputasi, sementara dilasi membantu memperjelas gambar, meningkatkan kontras dan mempertegas fitur penting pada gambar. Teknik ini juga membantu menghilangkan noise, membuat pola lebih konsisten dan mudah dikenali oleh model. Preprocessing diperlukan untuk menyederhanakan data, meningkatkan kualitas input ke model, dan memastikan konsistensi di seluruh dataset, yang pada akhirnya meningkatkan akurasi dan keandalan model dalam mengenali pola. Evaluasi performa model setelah preprocessing menunjukkan peningkatan yang signifikan dalam akurasi prediksi. Dengan preprocessing yang baik, data menjadi lebih mudah dikelola dan relevan untuk analisis lebih lanjut._

### Feature Selection

_Jelaskan bagaimana kalian menemukan fitur yang paling tepat untuk digunakan. Jelaskan alasan kalian menggunakan fitur tersebut dan berikan alasan mengapa fitur tersebut diperlukan._

_Fitur yang paling tepat untuk digunakan dipilih melalui proses seleksi fitur menggunakan metode ANOVA (Analysis of Variance) dengan skor fclassif. Proses ini memungkinkan pemilihan fitur-fitur yang paling signifikan dalam membedakan pola antara kelas yang berbeda. Fitur-fitur ini dipilih karena keberadaannya secara signifikan mempengaruhi hasil klasifikasi, tercermin dalam nilai-nilai skor fclassif yang tinggi. Fitur-fitur tersebut diperlukan untuk memberikan informasi yang paling relevan dan diskriminatif kepada model klasifikasi dalam membedakan pola yang unik dari setiap individu. Dengan demikian, pemilihan fitur yang tepat memastikan bahwa model yang dibangun dapat mengenali pola dengan akurasi dan keandalan yang tinggi, sambil juga menghindari overfitting dan kompleksitas yang berlebihan dalam model._

## Modeling

_Jelaskan bagaimana kalian melakukan hyperparameter tuning pada model tersebut._

## Evaluation
 
_Jelaskan bagaimana peningkatan performa model dari metrics yang kalian gunakan pada berbagai percobaan yang telah kalian lakukan._

_Catatan:_

- _Tutorial mengenai penggunaan Markdown dapat dibaca [di sini](https://guides.github.com/features/mastering-markdown/)_
- _Kalian dapat melakukan copy untuk file `percobaan_n.ipynb` (ganti `n` dengan nomor percobaan) untuk setiap percobaan yang kalian lakukan._