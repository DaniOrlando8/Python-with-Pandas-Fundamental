Menampilkan suatu data dari baris dan kolom tertentu

Tidak hanya dengan menentukan dari kolom dan baris, dengan menggunakan pandas kita juga bisa memanggil suatu data dari 
suatu baris dan kolom tertentu dalam satu waktu. 

Perhatikan dan coba kode di bawah ini:

import pandas as pd

csv_data = pd.read_csv("https://storage.googleapis.com/dqlab-dataset/shopping_data.csv")

print(csv_data['Age'].iloc[1])

print("Cuplikan Dataset:")

print(csv_data.head())

Hasil pada panel console akan keluar seperti berikut :

21
Cuplikan Dataset:
   CustomerID   Genre  Age  Annual Income (k$)  Spending Score (1-100)
0           1    Male   19                  15                      39
1           2    Male   21                  15                      81
2           3  Female   20                  16                       6
3           4  Female   23                  16                      77
4           5  Female   31                  17                      40