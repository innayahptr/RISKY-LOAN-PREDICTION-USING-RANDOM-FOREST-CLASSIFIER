![image](https://github.com/innayahptr/RISKYL-LOAN-PREDICTION-USING-RANDOM-FOREST-CLASSIFIER/assets/113874779/343fd950-ea8d-49e0-88ac-89e5683f8151)# MODELLING FLOW 

## 1. Exploratory Data Analysis
a. Data terdiri dari 75 kolom dan 242.059 baris tanpa nilai duplikat dan 17 kolom kosong sehingga kolom di putuskan untuk di drop sejak awal dan tersisa 58 kolom. <br> 
b. Kolom loan_status merupakan kolom target <br>
c. Risky Loan distribution pada Data kategorikal : <br>
![Screenshot 2024-01-02 165255](https://github.com/innayahptr/RISKYL-LOAN-PREDICTION-USING-RANDOM-FOREST-CLASSIFIER/assets/113874779/f3c72631-9b7d-4878-9bf8-589d76c707e7)
d. Risky Loan distribution pada Data Numerikal : <br>
![Screenshot 2024-01-02 165404](https://github.com/innayahptr/RISKYL-LOAN-PREDICTION-USING-RANDOM-FOREST-CLASSIFIER/assets/113874779/cd470112-1d25-4325-8bc4-cc58bee5d523)

## 2. Pre-Processing
a. Semua kolom terdeteksi memiliki outlier akan tetapi masih dalam kategori normal (mewakili real life case) oleh karena itu diputuskan untuk tidak perlu melakukan handling outlier pada pre-processing <br>
b. Terdapat 1 fitur baru yang merupakan representasi fitur “emp_length” (kurun waktu bekerja) menjadi lingkup yang lebih kecil yaitu alih-alih dikelompokkan tahunan, hasil dari ekstraksi mengelompokkan “emp_length” dengan new, middle dan senior <br>
c. Label encoding dilakukan pada kolom term, grade dan emp_length serta one hot encoding dilakukan pada kolom home_ownership, verification_status, initial_list_status dan application type <br>
d. Train-test split dilakukan dengan pembagian 70% data train dan 30% data test <br>
e. Feature transformation dilakukan Normalisasi beberapa kolom menggunakan Min-Max scaler <br>
f. oversampling dilakukan menggunakan SMOTE

## 3. Modelling
Model yang digunakan adalah Random Forest Classifier dengan Metrix evaluasi F1 score dengan hasil akhir 0.88 untuk data test dan 0.89 untuk data train.

