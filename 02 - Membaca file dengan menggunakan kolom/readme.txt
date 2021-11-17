Melakukan akses data kolom

Dalam suatu analisis data ada kalanya kita hanya butuh melakukan akses beberapa data saja dan tidak perlu harus menampilkan semua data. 
Pada pandas kita bisa melakukan akses dalam berbagai kebutuhan. 
Mulai dari hanya akses kolom tertentu ataupun baris tertentu. Pada sesi kali ini kita akan mencoba untuk melakukan akses beberapa kolom tertentu pada suatu dataset.

Pertama yang harus dilakukan untuk melakukan akses kolom adalah mengetahui nama-nama kolom yang ada. Coba ketikkan kode di bawah ini untuk melihat nama kolom yang ada.

import pandas as pd

csv_data = pd.read_csv("https://storage.googleapis.com/dqlab-dataset/shopping_data.csv")

print(csv_data.columns)

Hasil pada panel console akan keluar seperti berikut :

Index(['CustomerID', 'Genre', 'Age', 'Annual Income (k$)',
       'Spending Score (1-100)'],
      dtype='object')

Note : Pada dataset ini ada 5 kolom termasuk class, dimana 4 kolom  merupakan data numerik dan 1 kolom merupakan data string.
Pada praktek selanjutnya kita akan mencoba mengakses data age. 

Untuk melakukannya coba tuliskan kode di bawah ini :

import pandas as pd

csv_data = pd.read_csv("https://storage.googleapis.com/dqlab-dataset/shopping_data.csv")

print(csv_data['Age'])

Hasil pada panel console akan keluar seperti berikut :

In [1]: import pandas as pd
        
        csv_data = pd.read_csv("http://storage.googleapis.com/dqlab-dataset/shopping_data.csv")
        
        print(csv_data['Age'])

0      19
1      21
2      20
3      23
4      31
5      22
6      35
7      23
8      64
9      30
10     67
11     35
12     58
13     24
14     37
15     22
16     35
17     20
18     52
19     35
20     35
21     25
22     46
23     31
24     54
25     29
26     45
27     35
28     40
29     23
       ..
170    40
171    28
172    36
173    36
174    52
175    30
176    58
177    27
178    59
179    35
180    37
181    32
182    46
183    29
184    41
185    30
186    54
187    28
188    41
189    36
190    34
191    32
192    33
193    38
194    47
195    35
196    45
197    32
198    32
199    30
Name: Age, Length: 200, dtype: int64