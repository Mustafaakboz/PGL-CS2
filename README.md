# PGL-CS2

PGL CS2 Major Copenhagen 2024 oyuncu verileri üzerinde yapılmış veri analizi ve makine öğrenmesi projesi.

## Proje Hakkında

Bu projede PGL CS2 Major Copenhagen 2024 turnuvasına ait oyuncu istatistikleri analiz edilmiştir. [file:170]
Amaç, oyuncuların performans metriklerini incelemek ve hangi oyuncuların **Top Performer** olarak sınıflandırılabileceğini tahmin etmektir. [file:170]

Notebook içinde veri yükleme, keşifsel veri analizi, korelasyon incelemesi, özellik seçimi, model eğitimi ve model değerlendirme adımları uçtan uca uygulanmıştır. [file:170]

## Kullanılan Veri Seti

Projede Kaggle üzerindeki **PGL CS2 Major Copenhagen 2024 Data** veri seti kullanılmıştır. [web:194]
Notebook, veri klasörü içinden `PlayerKills.csv` ve `weaponsdata.csv` dosyalarını otomatik olarak tespit etmektedir. [file:170]
Ana analiz oyuncu bazlı istatistikleri içeren `PlayerKills.csv` üzerinden yapılmıştır ve bu tabloda 80 oyuncu ile 39 özellik yer almaktadır. [file:170]

## Problem Tanımı

Projede ikili sınıflandırma problemi kurulmuştur. [file:170]
`topperformer` değişkeni, oyuncunun ADR değerinin veri seti medyanının üzerinde olup olmamasına göre oluşturulmuştur. [file:170]
Buna göre:
- `1` = Top Performer [file:170]
- `0` = Ortalama Oyuncu [file:170]

## Kullanılan Özellikler

Model eğitiminde şu değişkenler kullanılmıştır: `killcount`, `assistcount`, `deathcount`, `headshotpercentage`, `kast`, `score`, `mvp`, `firstkillcount`, `damagehealth`, `damagearmor`, `bombplantedcount`, `bombdefusedcount`, `k1`, `k2`, `k3`, `k4`, `k5`. [file:170]

Bu değişkenler oyuncunun genel savaş performansını, skor katkısını, hasar üretimini ve round içi etkisini temsil etmektedir. [file:170]

## Yapılan Analizler

Projede aşağıdaki adımlar gerçekleştirilmiştir:

1. Veri dosyalarının otomatik bulunması ve yüklenmesi. [file:170]
2. Oyuncu istatistiklerinin incelenmesi. [file:170]
3. ADR medyanına göre hedef değişken üretilmesi. [file:170]
4. EDA grafikleri ile dağılım analizleri yapılması. [file:170]
5. ADR’ye göre en iyi 10 oyuncunun çıkarılması. [file:170]
6. Sayısal değişkenler için korelasyon matrisi oluşturulması. [file:170]
7. Verilerin train-test olarak ayrılması ve ölçeklenmesi. [file:170]
8. Random Forest ve Gradient Boosting modellerinin eğitilmesi. [file:170]
9. Confusion matrix ve classification report ile performans ölçümü yapılması. [file:170]
10. Leave-One-Out Cross Validation ile ek doğrulama yapılması. [file:170]

## Kullanılan Modeller

Bu projede iki farklı sınıflandırma modeli kullanılmıştır:

- Random Forest Classifier. [file:170]
- Gradient Boosting Classifier. [file:170]

Veri, model öncesinde `StandardScaler` ile ölçeklenmiştir. [file:170]

## Sonuçlar

Notebook çıktısında hem **Random Forest** hem de **Gradient Boosting** modeli için test doğruluğu `%100.0` olarak raporlanmıştır. [file:170]
Ek olarak Leave-One-Out Cross Validation sonucunda ortalama doğruluk `%91.2`, standart sapma ise `%28.3` olarak verilmiştir. [file:170]
Notebook sonunda en iyi model **Random Forest** olarak seçilmiştir. [file:170]

## Üretilen Görseller

Notebook toplam 5 görsel üretip kaydetmektedir. [file:170]
Kaydedilen çıktılar şunlardır: `playerstatseda.png`, `top10players.png`, `correlationmatrix.png`, `modelcomparison.png`, `featureimportance.png`. [file:170]

## Kullanılan Teknolojiler

- Python [file:170]
- pandas [file:170]
- NumPy [file:170]
- Matplotlib [file:170]
- Seaborn [file:170]
- scikit-learn [file:170]

## Kaggle Notebook

Aşağıdaki Kaggle notebook bu projenin kaynak çalışmasını içermektedir:

[https://www.kaggle.com/code/mustafaakboz/pgl-major-tahmin](https://www.kaggle.com/code/mustafaakboz/pgl-major-tahmin)

## Repository

GitHub repository bağlantısı:

[https://github.com/Mustafaakboz/PGL-CS2](https://github.com/Mustafaakboz/PGL-CS2)

## Genel Değerlendirme

Bu proje, esports verileri üzerinde veri analizi ve makine öğrenmesi uygulamak için iyi bir örnektir. [file:170]
Hem istatistiksel görselleştirme hem de sınıflandırma yaklaşımı kullanılarak oyuncu performansını açıklamaya ve tahmin etmeye yönelik bütünlüklü bir çalışma sunmaktadır. [file:170]

## Lisans

Veri seti Kaggle üzerinde **CC BY-NC-SA 4.0** lisansı ile paylaşılmaktadır. [web:194]
