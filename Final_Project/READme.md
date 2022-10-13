# 4 ward Final Project
> Repository ini dibuat untuk project akhir Rakamin Data Scientist Batch 24. Group 4 ward beranggotakan Baladzuri Hafizh Fathoni, Bernadine Hendrietta, Junilia, Nabilah Sarah A, dan Rheza Paleva Uyanto. Silakan klik Data set yang kami gunakan : [_HR Analytics: Job Change of Data Scientist_](https://www.kaggle.com/datasets/arashnic/hr-analytics-job-change-of-data-scientists?taskId=3015). <!-- If you have the project hosted somewhere, include the link here. -->

## Problem Statement
- Big Data & Data Science Company kesulitan mendapatkan kandidat data scientist
- Perusahaan akan memberikan pelatihan data science kepada karyawan
- Perusahaan ingin memprediksi karyawan mana saja yang serius ingin berkarir sebagai data scientist

## Goals
- Mendapatkan karyawan yang serius ingin bekerja di perusahaan setelah training selesai (tidak mencari pekerjaan lain/tidak pindah).

## Objective
- Identify : Identifikasi faktor pengaruh karyawan mencari pekerjaan lain
- Modelling : Membuat model untuk memprediksi karyawan pindah/tidak
- Recommendation : Memberi rekomendasi untuk memaksimalkan kegiatan training

## Overview Data set : 
- Dataset terdiri dari 19.158 baris dan 14 kolom
- Terdapat 4 data numerik dan 10 data kategorikal
- Terdapat beberapa kolom yang masih memiliki null / missing values

## Target Feature : 
- 0 : not looking for a job change (tidak pindah)(false)
- 1 : looking for a job change (pindah) (true)

## Data Preprocessing :
- Handling Missing Value : Diisi dengan nilai Modus dan dinormalisasi dengan nilai lainnya untuk nilai spesial karakter
- Handling Duplicate Data : Tidak ada duplikasi data
- Handling Outlier : Sudah dilakukan handling outlier dengan Z-score
- Feature Selection : Beberapa fitur didrop
- Feature Encoding : Ordinal Encoding dan One-Hot Encoding
- Scaling : Standardization

## Machine Learning Preparation : 
- Split Data Train & Test (70 : 30): Data Train : 13325, Data Test : 5711
- Handling Class Imbalance : SMOTE hanya untuk data train
- Machine Learning Model : 9 model
- Machine Learning Evaluation : Accuracy, Precision, Recall, F1 Score, AUC, Train Score dan Test Score
- Feature Importance : Re run Machine Learning dengan Feature Importance
- Hypertuning

## Result Machine Learning :
- Model XGBOOST dipilih karena menunjukkan nilai precision yang besar daripada model lain yakni 0,49.
- Dengan nilai precision, kita fokus mencari yang benar-benar berminat, yang berarti yang pindah, Precision digunakan untuk mengurangi kejadian false positive. Dengan mengecilkan false positive, nilai precision menjadi meningkat.
- Fitur Importance : Company_size_map, city_development_index, enrolled_university_Full time course, education_level_map, dan relevent_experience_map, 
- Setelah di hyperparameter tuning, dann memilih fitur importance. Dilakukan kembali running machine preparation : nilai precision meningkat menjadi 0,51.

## Business Simulation
- Misalkan ada 100 orang yang apply : Sebanyak 51 orang sudah sesuai antara yang kita prediksi dan aktualnya.



