Prediksi saat menembak cewek

## Overview
Prediksi jawaban “Kita temenan aja ya!” atau “Aku mau kok jadi pacar kamu” dari gebetan dengan Machine Learning dan algoritma Logistic Regresion.

Pada topik kali ini saya akan membuat artikel yang sedikit nyeleneh hha. mengapa topik ini dibuat? karena pada keadaan ini (nembak cewe) adalah suatu keadaan dimana seorang cowok akan dihadapkan pada 2 pilihan dimana diterima atau tidak dan ini sangat bergaris lurus dengan algoritma Logistic Regression dimana algoritma ini hanya memberi nilai keluar 0 atau 1, ya atau tidak, menang atau kalah, lulus atau gagal dan sebagainya.

Algoritma Logistic Regression

Pada ilmu statistika algoritma ini sama dengan Logit Regression atau Logit Model. algoritma ini hanya mengeluarkan output 2 nilai yaitu “0” atau “1”. pada kehidupan dapat direpresintasikan seperti ya/tidak, menang/kalah dan sebagainya. untuk regresi yang menginginkan lebih dari 2 value outcomes yaitu multinomial logistic regression.
Di kehidupan nyata algoritma ini dapat di aplikasikan pada ilmu kedokteran seperti menentukan apakah pasien memiliki penyakit diabetes berdasarkan properti seperti umur, jenis kelamin, berat badan, hasil test darah, dan sebagainya atau kecenderungan masyarakat indonesia mengidolakan Raisya atau Zaskia Gotik berdasarkan umur, jenis kelamin, pekerjaan, dan tempat tinggal.
Pada penerapannya pada artikel ini penulis akan membuat suatu machine learning sederhana untuk memprediksi apakah kita akan diterima atatu tidak sebagai Pacar pada saat nembak doi. untuk properti penulis akan membuat properti dengan data dummy yang berelasi pada keadaan ini.
Properti:
1. Jarak rumah.
2. Level bau ketek.
3. Jenis kendaraan.
4. Pengeluaran saat PDKT.
5. Jumlah ketemuan dalam seminggu.

oke langsung saja pada pengaplikasiannya pada machine learning. seperti biasa untuk instalasi adalah seperti berikut.
Hal-hal yang di butuhkan adalah
1. Python
2. Scikit Learn
3. Numpy
4. Scipy
untuk instalasi hal-hal diatas bisa menggunakan package manager seperti pip.
Penerapan pada aplikasi.

```python
# import algoritma logistic regression pada scikit learn
from sklearn.linear_model import LogisticRegression
# membuat variable classifier dengan algoritma logistic regression
clf = LogisticRegression()
# properti yang dibutuhkan pada aplikasi ini mempunyai sebuah array dengan value sebagai berikut
# index 0 : Jarak rumah dalam KM
# index 1 : Level bau ketek (1 - 10)
# index 2 : Jenis kendaraan denga properti 0 = angkot, 1 = motor, 2 = mobil
# index 3 : Pengeluaran saat PDKT
# index 4 : Jumlah ketemuan dalam seminggu [dalam puluh ribu]
data = [[5, 1, 0, 5, 1], [35, 6, 2, 8, 4], [1, 4, 0, 11, 1], [23, 3, 1, 3, 3], [54, 1, 0, 80, 5], 
        [16, 3, 1, 6, 3], [7, 3, 2, 10, 2], [4, 7, 1, 12, 2], [10, 2, 1, 5, 2], [8, 2, 0, 40, 3], 
        [3, 5, 0, 7, 2], [18, 2, 1, 150, 3], [6, 4, 1, 2, 4], [23, 1, 2, 6, 1], [17, 1, 1, 20, 2]]
# target berdasarkan data diatas adalah sebagai berikut
# value 0 : diterima
# value 1 : ditolak
target = [0, 1, 0, 0, 1, 0, 1, 0, 0, 1, 1, 0, 0, 1, 0]
# target value
target_value = ["Kita temenan aja ya!", "Aku mau kok jadi pacar kamu"]
# mentrain data berdasarkan properti diatas
clf.fit(data, target)
# membuat prediksi dari cowok kere
prediction = clf.predict([[0, 0, 0, 0, 0]])
# memperint dari prediksi
print target_value[int(prediction)]
# maka akan mempunyai hasil sebagai berikut
# Kita temenan aja ya!
```

Sekian machine learning sederhana yang menentukan apakah kita diterima atau tidak saat nembak Doi.
Selamat Mencoba


## Contact 
email : meilyasahsan@gmail.com
