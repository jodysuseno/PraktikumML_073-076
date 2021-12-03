# Klasikikasi Gambar pada Penyakit daun jagung menggunakan CNN

> Anggota Kelompok Kelas Pembelajaran Mesin B :
> - Jody Ririt Krido Suseno - 201810370311073
> - Muhammad Aries Ramadhan - 201810370311076

## Journal
Pada jurnal dataset yang digunakan menggunakan dataset gambar yang berasal dari PlantVillage. 
Pada dataset ini dilakukan preprocessing seperti data augmentation dan spliting data. 
Model yang digunakan pada praktikum ini adalah Model arsitektur yang bernama Alexnet dengan akurasi 93%.
![Example screenshot](assets/alexnetArsitektur.png | width=300)

## Dataset
Dataset yang digunakan adalah Plant LEaf Diseses yang bersumber dari PlantVillage. dalam dataset tersebut memiliki 39 kelas yang berbeda dari daun tanaman dan gambar latar belakang. 
![Example screenshot](assets/corn_leaf.png | width=300)
Namun kita hanya menggunkan 4 kelas untuk klasifikasi penyakit daun jagung. dengan deskripsi seperti berikut:
- Link Dataset : [Dataset : Plant Leaf Diseases](https://data.mendeley.com/datasets/tywbtsjrjv/1)
- Jumlah image pada dataset 3852.
- Jumlah image pada setiap kelas
  - healthy               : 1162
  - Cercospora            : 513
  - common rust           : 1192
  - northern leaf blight  : 958
- Jumlah persentase spliting dataset
  - Data Train            : 80% - 3044
  - Data Validation       : 19% - 772
  - Data Test             : 1%  - 36

## Preprocessing
Preprocesing data menggunakan metode berikut :
- Augmentasi Data
  - rescale = 1./255
  - horizontal flip = True
  - vertical flip = True
  - rotation range = 90
  - height shift range = 0.2
  - width shift range = 0.2
  - zoom range = 0.2
  - validation split = 0.7
  - size = (224, 224)
  - color mode = 'rgb'
  - class mode = 'categorical'
  - shuffle = True
- Spliting Data
  - Data Train            : 80% 
  - Data Validation       : 19% 
  - Data Test             : 1% 

## Model
Model yang digunakan adalah Alexnet Model
- Model 1 (Alexnet)
  - Summary</br>
    ![Example screenshot](assets/alexnetArsitektur.png | width=300)
  - Confution matriks evaluation</br>
    ![Example screenshot](assets/alexnetMatrix.png | width=300)
  - grafik akurasi dan loss</br>
    ![Example screenshot](assets/alexnetAccLoss.png | width=300)
  - Classification Report</br>
    |                      | precision | recall | f1-score | support |
    |----------------------|-----------|--------|----------|---------|
    | Cercospora           | 0.64      | 0.94   | 0.76     | 405     |
    | Common_rust          | 1.00      | 1.00   | 1.00     | 942     |
    | Northern_Leaf_Blight | 0.97      | 0.72   | 0.82     | 779     |
    | Corn_healthy         | 0.98      | 1.00   | 0.99     | 918     |
    |                      |           |        |          |         |
    | macro avg            | 0.90      | 0.91   | 0.89     | 3044    |
    | weighted avg         | 0.94      | 0.92   | 0.92     | 3044    |
    | accuracy             |           |        | 0.92     | 3044    |
- Model 2 (Alexnet Hyper Parameter)
  - Summary</br>
    ![Example screenshot](assets/alexnetArsitektur.png | width=300)
  - matriks evaluation</br>
    ![Example screenshot](assets/alexnetHparamMatrix.png | width=300)
  - grafik akurasi dan loss</br>
    ![Example screenshot](assets/alexnetHparamAccLoss.png | width=300)
  - Classification Report</br>
    |                      | precision | recall | f1-score | support |
    |----------------------|-----------|--------|----------|---------|
    | Cercospora           | 0.86      | 0.78   | 0.82     | 405     |
    | Common_rust          | 1.00      | 0.99   | 1.00     | 942     |
    | Northern_Leaf_Blight | 0.91      | 0.91   | 0.91     | 779     |
    | Corn_healthy         | 0.96      | 1.00   | 0.98     | 918     |
    |                      |           |        |          |         |
    | macro avg            | 0.93      | 0.92   | 0.93     | 3044    |
    | weighted avg         | 0.95      | 0.95   | 0.95     | 3044    |
    | accuracy             |           |        | 0.95     | 3044    |
## Predict pada sample data
On Going

## Sumber Referensi
 - [Dataset : Plant Leaf Diseases](https://data.mendeley.com/datasets/tywbtsjrjv/1)
 - [Artikel rujukan](http://dx.doi.org/10.12928/telkomnika.v18i3.14840)




