# 🎬 Film ve Dizi Veri Analizi ve Görselleştirme (EDA)

Python, Pandas, NumPy, Matplotlib ve Seaborn kullanarak sentetik olarak oluşturulan film ve dizi veri seti üzerinde keşifsel veri analizi (EDA), özellik mühendisliği ve görselleştirme gerçekleştiren veri bilimi projesi.

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge&logo=python&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

---

## 🎯 Projenin Amacı ve Çözdüğü Problem

Dijital içerik kataloglarında yapım türü, yayın yılı, ülke, izleyici oyları ve puanlar arasındaki ilişkileri hızlıca anlamlandırmak; ham tablo verisinden anlamlı içgörüler üretmek için temel bir keşifsel veri analizi (EDA) iş akışı gerektirir.

Bu proje, harici bir veri dosyasına bağımlı kalmadan `NumPy` ve `Pandas` ile yapılandırılmış sentetik bir film/dizi veri seti oluşturmayı, veriyi kategorize ederek zenginleştirmeyi (feature engineering) ve istatistiksel dağılımları 6 farklı grafik türüyle görselleştirerek uçtan uca bir analiz pratiği sunmayı amaçlar.

---

## ✨ Öne Çıkan Özellikler ve Proje Bulguları

### Yapılan İşlemler
- **Sentetik Veri Seti Üretimi:** 100 farklı yapım için 8 temel sütun (`Title`, `Type`, `Genre`, `ReleaseYear`, `Rating`, `Duration`, `Country`, `Votes`) rastgele üretilir.
- **Veri Kontrolü ve Özet İstatistikler:** Yapım türü sayıları, benzersiz tür adedi, genel puan ortalaması ve eksik değer kontrolü yapılır.
- **Sıralama ve Gruplama Analizleri:** En yüksek puanlı 10 yapım, en fazla oy alan 10 yapım, türlere göre ortalama puanlar, ülkelere ve yıllara göre film sayıları hesaplanır.
- **Özellik Mühendisliği (Feature Engineering):**
  - `RatingCategory`: Puanlara göre yapımlar **Düşük** (`≤ 5.0`), **Orta** (`≤ 7.0`), **İyi** (`≤ 8.5`) ve **Çok İyi** (`> 8.5`) şeklinde sınıflandırılır.
  - `Period`: Yayın yıllarına göre yapımlar **Before 2000**, **2000-2010**, **2010-2020** ve **2020+** dönemlerine ayrılır.
- **Karşılaştırmalı İstatistikler:** `Movie` ve `TV Show` grupları için ortalama (`mean`), medyan (`median`) ve standart sapma (`std`) değerleri hesaplanır.
- **Veri Görselleştirme:** Histogram (KDE eğrili), çubuk grafik (barplot), zaman serisi çizgi grafiği (lineplot), kutu grafiği (boxplot), dağılım grafiği (scatterplot) ve regresyon trend çizgili dağılım grafiği (lmplot) oluşturulur.

### Mevcut Çalıştırma Çıktılarından Öne Çıkan Bulgular
> **Not:** Veri seti kod içinde sabit bir rastgelelik tohumu (`random seed`) tanımlanmadan üretildiği için notebook yeniden çalıştırıldığında sayısal değerler değişiklik gösterecektir. Aşağıdaki veriler, paylaşılan çalıştırma çıktısına aittir.

- **Veri Bütünlüğü:** 100 yapım kaydında tüm sütunlarda `0` eksik değer bulunmaktadır.
- **Yapım Dağılımı:** Toplam **55 Dizi (`TV Show`)** ve **45 Film (`Movie`)**; 6 farklı tür (`Action`, `Comedy`, `Drama`, `Horror`, `Romance`, `Sci-Fi`).
- **Genel Puan Ortalaması:** Tüm yapımlar için ortalama puan **5.58** olarak hesaplanmıştır.
- **Film vs. Dizi Puan İstatistikleri:**

| Yapım Türü (`Type`) | Ortalama (`mean`) | Medyan (`median`) | Standart Sapma (`std`) |
| :--- | :---: | :---: | :---: |
| **Movie** | 5.81 | 6.00 | 2.42 |
| **TV Show** | 5.39 | 5.20 | 2.65 |

- **Türlere Göre Ortalama Puan:** En yüksek puan ortalaması **Romance (6.65)** türünde, ardından **Drama (5.64)** ve **Sci-Fi (5.54)** türlerinde görülmüş; en düşük ortalama **Comedy (5.30)** türünde elde edilmiştir.
- **Ülkelere Göre Film (`Movie`) Sayısı:** En fazla film **South Korea (14)**, **USA (9)** ve **France (8)** ülkelerine aittir; bunları **Japan (7)**, **UK (4)** ve **Turkey (3)** takip etmektedir.
- **Öne Çıkan Yapımlar:**
  - En yüksek puanlı yapım: **Yapım 86** (`Movie`, Drama, 2024, France — **9.9** puan, 319.869 oy)
  - En fazla oy alan yapım: **Yapım 7** (`TV Show`, Action, 2013, France — **1.991.575** oy, 3.6 puan)

---

## 🛠️ Kullanılan Teknolojiler ve Araçlar

- **Dil:** Python 3
- **Veri İşleme ve Sayısal Hesaplama:** `pandas`, `numpy`
- **Veri Görselleştirme:** `matplotlib`, `seaborn`
- **Geliştirme Ortamı:** Jupyter Notebook

---

## ⚙️ Kurulum ve Çalıştırma

Projeyi kendi bilgisayarında çalıştırmak için aşağıdaki adımları takip edebilirsin:

1. **Depoyu (repository) klonla:**
   ```bash
   git clone https://github.com/esmanuryavuz908/film-dizi-veri-analizi-eda.git
   cd film-dizi-veri-analizi-eda
   ```

2. **(Önerilen) Sanal ortam oluştur ve etkinleştir:**
   ```bash
   python -m venv venv
   # Windows için:
   venv\Scripts\activate
   # macOS / Linux için:
   source venv/bin/activate
   ```

3. **Gerekli kütüphaneleri yükle:**
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```

4. **Jupyter Notebook'u başlat ve dosyayı çalıştır:**
   ```bash
   jupyter notebook
   ```
   Açılan tarayıcı penceresinden `film_dizi_eda.ipynb` dosyasını seçip tüm hücreleri sırayla (`Run All`) çalıştırabilirsin.

---
