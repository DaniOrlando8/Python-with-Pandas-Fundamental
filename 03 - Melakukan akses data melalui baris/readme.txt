Melakukan akses data melalui baris

Selain melakukan akses data melalui kolom, dengan menggunakan pandas juga bisa melakukan akses dengan menggunakan baris.
Berbeda dengan akses melalui kolom, fungsi untuk menampilkan data dari suatu baris adalah fungsi .iloc[i] dimana [i] 
menunjukan urutan baris yang akan ditampilkan yang dimana indexnya diawali dari 0. 

Coba ketikan code di bawah ini untuk mempermudah :

import pandas as pd

csv_data = pd.read_csv("https://storage.googleapis.com/dqlab-dataset/shopping_data.csv")

print(csv_data.iloc[5])

Hasil pada panel console akan keluar seperti berikut :
CustomerID                     6
Genre                     Female
Age                           22
Annual Income (k$)            17
Spending Score (1-100)        76
Name: 5, dtype: object