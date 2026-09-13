# Hafta 4

## experiment_part2.ipynb

- Türkçe isim veri setiyle çalıştım (isimler.txt, 30.000 isim), vocab'ı Türkçe karakterleri (ç, ö, ü, ğ, ı, ş, â) kapsayacak şekilde genişlettim.
- Modele Batch Normalization ekledim.
- Ağırlık başlatmasını iyileştirdim (W1, W2, b2 için).
- 100.000 adım eğittim, loss 3.45'ten ~1.0-1.2 bandına düştü.
- Train/val loss'u ayrı ölçtüm: 1.64 / 1.69
- Modelden yeni Türkçe isimler ürettim (bazıları başarılı: yusuf, kadır, aydın).
