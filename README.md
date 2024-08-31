# **1. Business Problem Understanding**

---

## **1.1 Context**

Dewasa ini, menjaga pelanggan tetap setia kepada perushaan adalah kunci utama untuk keberlanjutan dan pertumbuhan bisnis. Customer churn, atau hilangnya pelanggan yang beralih ke layanan atau produk lain, merupakan tantangan besar yang dapat memengaruhi profitabilitas perusahaan. Ketika pelanggan memilih untuk berhenti menggunakan platform e-commerce tertentu dan beralih ke kompetitor, perusahaan tidak hanya kehilangan pendapatan, tetapi juga menghadapi biaya tambahan untuk memperoleh pelanggan baru. Biaya untuk menarik pelanggan baru ini bisa mencapai lima kali lebih mahal dibandingkan dengan mempertahankan pelanggan yang sudah ada. Hal ini menunjukkan betapa pentingnya upaya retensi pelanggan dalam strategi bisnis e-commerce.[usetada](https://blog.usetada.com/id/apa-itu-customer-churn-dan-bagaimana-menghentikannya)

E-commerce, yang memungkinkan transaksi jual beli produk dan layanan melalui platform online tanpa interaksi langsung antara penjual dan pembeli, telah menjadi bisnis yang sangat efektif dan populer. Namun, dengan semakin banyaknya platform e-commerce dan ketatnya persaingan, menjaga loyalitas pelanggan menjadi sangat dibutuhkan dalam berbisnis. Platform e-commerce perlu terus berinovasi dan menawarkan promosi menarik untuk mempertahankan pelanggan mereka. Jika tidak, risiko churn meningkat, di mana pelanggan berhenti bertransaksi dan beralih ke platform kompetitor yang menawarkan pengalaman lebih baik atau nilai yang lebih menarik.

Analisis data churn menjadi semakin penting di industri e-commerce karena memberikan informasi tentang perilaku pelanggan dan alasan dibalik churn. Dataset churn umumnya berisi informasi tentang riwayat pembelian pelanggan, termasuk frekuensi pembelian, waktu pembelian terakhir, dan jenis produk yang dibeli. Dengan menganalisis data ini, perusahaan dapat mengidentifikasi pola perilaku pelanggan yang rentan terhadap churn dan mengembangkan strategi retensi yang lebih efektif. Ini dapat mencakup pengembangan program loyalitas, personalisasi penawaran, atau peningkatan kualitas layanan untuk mencegah pelanggan berpindah ke platform lain.

Secara keseluruhan, memahami dan mengelola churn pelanggan sangat penting bagi perusahaan e-commerce untuk mempertahankan basis pelanggan yang kuat dan memaksimalkan profitabilitas. Dengan pendekatan yang tepat, perusahaan dapat mengurangi churn dan meningkatkan kepuasan serta loyalitas pelanggan, yang pada akhirnya mendukung pertumbuhan jangka panjang dan daya saing di pasar yang semakin dinamis ini.


## **1.2 Problem Statement**

Customer churn merupakan tantangan besar bagi bisnis e-commerce karena pelanggan yang datang dan pergi secara terus-menerus dapat berdampak signifikan terhadap pendapatan jangka panjang. Untuk mengurangi kerugian pendapatan, perusahaan e-commerce perlu mengidentifikasi dan memprediksi pelanggan yang berpotensi churn sebelum mereka benar-benar meninggalkan layanan. Dengan demikian, perusahaan dapat mengambil langkah proaktif, seperti memberikan promosi yang tepat sasaran dan lebih relevan untuk mempertahankan pelanggan. Namun, sangat penting untuk memastikan bahwa promosi ini diberikan hanya kepada pelanggan yang diprediksi akan churn, karena kesalahan dalam pemberian promosi dapat menyebabkan kerugian operasional akibat pengeluaran yang tidak perlu. Selain itu, dengan meningkatnya biaya akuisisi pelanggan di tengah persaingan yang semakin ketat, kegagalan dalam mempertahankan pelanggan tidak hanya mengurangi pendapatan, tetapi juga dapat memengaruhi reputasi perusahaan jika pelanggan yang churn berbagi pengalaman negatif mereka. Oleh karena itu, strategi retensi yang efektif dan tepat sasaran sangat diperlukan untuk menjaga stabilitas dan pertumbuhan bisnis e-commerce.

## **1.3 Goals**

Tujuan dari analisis ini adalah untuk mengembangkan model prediksi machine learning yang dapat secara akurat mengidentifikasi pola pelanggan yang berpotensi meninggalkan platform mereka, sehingga dapat mengambil tindakan pemasaran yang tepat dan efisien dalam biaya. Dengan memprediksi pelanggan yang kemungkinan akan churn, perusahaan e-commerce dapat mengoptimalkan strategi promosi mereka dengan memfokuskan penawaran hanya kepada pelanggan yang memiliki probabilitas tinggi untuk churn, sehingga mengurangi kerugian pendapatan yang tidak perlu. Selain itu, dengan memahami faktor atau variabel yang mempengaruhi churn, perusahaan dapat menyusun rencana yang lebih efektif dan personal dalam mempertahankan pelanggan, meningkatkan loyalitas, dan menurunkan tingkat churn secara keseluruhan. Tujuan ini akan membantu perusahaan untuk tidak hanya menghemat biaya akuisisi pelanggan baru, tetapi juga memperkuat hubungan dengan pelanggan yang ada, yang pada akhirnya akan meningkatkan profitabilitas dan daya saing perusahaan di pasar e-commerce yang semakin kompetitif.

## **1.4 Analytic Approach**

Pertama, kami akan menganalisis data pelanggan untuk mengidentifikasi pola yang memisahkan pelanggan yang cenderung churn dari mereka yang tidak. Selanjutnya, kami akan mengembangkan model klasifikasi yang dapat memperkirakan kemungkinan pelanggan akan churn, sehingga perusahaan dapat menerapkan strategi retensi yang lebih tepat sasaran untuk mengurangi tingkat churn dan mempertahankan basis pelanggan mereka.

## **1.5 Metric Evaluation**

Dalam analisis prediksi customer churn untuk e-commerce, penggunaan metrik evaluasi yang tepat sangat penting untuk memahami bagaimana model memprediksi pelanggan yang mungkin churn atau tidak. Berikut adalah definisi metrik dan pertimbangan utama yang relevan untuk kasus ini:

![Confussion Matrix](https://www.nbshare.io/static/snapshots/cm_colored_1-min.png)

- True Positive (TP): Pelanggan diprediksi akan churn dan benar-benar churn.
- False Positive (FP): Pelanggan diprediksi akan churn, tetapi sebenarnya tidak churn. Ini dapat menyebabkan kerugian operasional karena perusahaan mengeluarkan biaya untuk promosi yang tidak diperlukan.
- False Negative (FN): Pelanggan diprediksi tidak akan churn, tetapi sebenarnya churn. Ini dapat menyebabkan kehilangan pendapatan karena pelanggan yang sebenarnya churn tidak dikenali dan tidak diambil tindakan pencegahan.
- True Negative (TN): Pelanggan diprediksi tidak akan churn dan benar-benar tidak churn.


Konsekuensi Kesalahan Prediksi:
- Type 1 Error (False Positive): Menghasilkan kerugian operasional ([*operation loss*](https://www.investopedia.com/terms/o/operating-loss.asp#:~:text=An%20operating%20loss%20occurs%20when,profit%20before%20interest%20and%20taxes.)) karena memberikan promosi kepada pelanggan yang tidak berisiko churn, yang menyebabkan pemborosan biaya tanpa mendapatkan manfaat yang diharapkan.
- Type 2 Error (False Negative): Mengakibatkan kerugian pendapatan (profit loss) karena pelanggan yang benar-benar berisiko churn tidak diidentifikasi, dan perusahaan kehilangan kesempatan untuk melakukan intervensi untuk mempertahankan mereka.


Target:
- 0: Pelanggan tidak churn.
- 1: Pelanggan churn.


Dalam konteks ini, mempertahankan pelanggan sangat penting karena biaya untuk mendapatkan pelanggan baru lebih tinggi daripada biaya untuk mempertahankan yang ada. Kesalahan False Negative (FN) dianggap lebih merugikan karena langsung terkait dengan hilangnya pelanggan dan pendapatan. Namun, kesalahan False Positive (FP) juga perlu diperhatikan karena dapat menyebabkan pemborosan sumber daya dan biaya untuk upaya retensi yang tidak perlu.


[F2](https://docs.h2o.ai/driverless-ai/1-10-lts/docs/userguide/scorers.html#:~:text=The%20F2%20score%20is%20the,to%20recall%20than%20to%20precision) Score dipilih sebagai metrik evaluasi yang tepat karena memberikan lebih banyak bobot pada recall daripada precision. Dalam kasus ini, lebih penting untuk mengurangi False Negative karena setiap pelanggan yang hilang berarti potensi pendapatan yang hilang. Oleh karena itu, F2 Score yang menekankan pada recall sangat cocok untuk mengukur performa model prediksi customer churn ini, dengan tetap mempertimbangkan pengurangan biaya dan efektivitas operasional perusahaan e-commerce.

