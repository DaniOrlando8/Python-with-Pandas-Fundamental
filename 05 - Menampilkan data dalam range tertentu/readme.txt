Menampilkan data dalam range tertentu

Setelah menampilkan suatu kelompok data, bagaimana jika ingin menampilkan data dari baris ke 5 sampai ke 20 dari suatu 
dataset? Untuk mengantisipasi hal tersebut, pandas juga bisa menampilkan data dalam range tertentu, baik range untuk baris 
saja, kolom saja, dan range untuk baris dan kolom.

Akses range pada suatu kolom dan baris tertentu, untuk mencobanya silahkan ketikkan kode di bawah ini :
import pandas as pd

csv_data = pd.read_csv("https://storage.googleapis.com/dqlab-dataset/shopping_data.csv")

print("Menampilkan data ke 5 sampai kurang dari 10 :")

print(csv_data['Age'].iloc[5:10])

Hasil pada panel console akan keluar seperti berikut :

Menampilkan data ke 5 sampai kurang dari 10 :
5    22
6    35
7    23
8    64
9    30
Name: Age, dtype: int64

Menampilkan suatu range data tertentu pada suatu baris saja. Cobalah ketikan kode di bawah ini :

import pandas as pd

csv_data = pd.read_csv("https://storage.googleapis.com/dqlab-dataset/shopping_data.csv")

print("Menampilkan data ke 5 sampai kurang dari 10 dalam satu baris:")

print(csv_data.iloc[5:10])

Hasil pada panel console akan keluar seperti berikut :

Menampilkan data ke 5 sampai kurang dari 10 dalam satu baris:
  CustomerID   Genre  Age  Annual Income (k$)  Spending Score (1-100)
5           6  Female   22                  17                      76
6           7  Female   35                  18                       6
7           8  Female   23                  18                      94
8           9    Male   64                  19                       3
9          10  Female   30                  19                      72