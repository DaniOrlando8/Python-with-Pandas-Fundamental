Menampilkan informasi statistik dengan Numpy

Mengetahui informasi statistik pada suatu data sangat penting. 
Mulai dari distribusi data, nilai max atau min, hingga standar deviasi dari suatu dataset. 
Jika datanya berjumlah dibawah 10 mungkin masih dikerjakan secara manual. 
Namun, bayangkan jika datanya sudah mencapai ratusan bahkan ribuan. Tidak mungkin pastinya untuk dilakukan secara manual.
Maka dari itu pentingnya fungsi describe() pada pandas. Fungsi describe() ini memungkinkan untuk mengetahui informasi 
statistik dari suatu dataset secara cepat. Coba untuk ketikkan kode di bawah ini :

import pandas as pd

csv_data = pd.read_csv("https://storage.googleapis.com/dqlab-dataset/shopping_data.csv")

print(csv_data.describe(include='all'))

Hasil pada panel console akan keluar seperti berikut :

CustomerID   Genre         Age  Annual Income (k$)  \
count   200.000000     200  200.000000          200.000000
unique         NaN       2         NaN                 NaN
top            NaN  Female         NaN                 NaN
freq           NaN     112         NaN                 NaN
mean    100.500000     NaN   38.850000           60.560000
std      57.879185     NaN   13.969007           26.264721
min       1.000000     NaN   18.000000           15.000000
25%      50.750000     NaN   28.750000           41.500000
50%     100.500000     NaN   36.000000           61.500000
75%     150.250000     NaN   49.000000           78.000000
max     200.000000     NaN   70.000000          137.000000

        Spending Score (1-100)
count               200.000000
unique                     NaN
top                        NaN
freq                       NaN
mean                 50.200000
std                  25.823522
min                   1.000000
25%                  34.750000
50%                  50.000000
75%                  73.000000
max                  99.000000

Note : Banyak nilai NaN yang tampil. Hal itu karena pada dataset ada format data string yang akhirnya memunculkan format NaN.

Untuk meminimalisir hal tersebut dan memfilter hanya data numerical saja, digunakan  exclude=[‘O’], dimana fungsi itu akan
mengabaikan data yang non-numerical untuk diproses. Coba implementasikan code di bawah ini:

import pandas as pd

csv_data = pd.read_csv("https://storage.googleapis.com/dqlab-dataset/shopping_data.csv")

print(csv_data.describe(exclude=['O']))

Hasil pada panel console akan keluar seperti berikut :

CustomerID         Age  Annual Income (k$)  Spending Score (1-100)
count  200.000000  200.000000          200.000000              200.000000
mean   100.500000   38.850000           60.560000               50.200000
std     57.879185   13.969007           26.264721               25.823522
min      1.000000   18.000000           15.000000                1.000000
25%     50.750000   28.750000           41.500000               34.750000
50%    100.500000   36.000000           61.500000               50.000000
75%    150.250000   49.000000           78.000000               73.000000
max    200.000000   70.000000          137.000000               99.000000