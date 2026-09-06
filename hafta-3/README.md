# Deney Notları: Bigram Dil Modeli (makemore)

## Ne Yaptım?

- Önce verilen `names.txt` dosyasıyla verileri tanıdım.
- Bigram counting (ikili karakter sayımı) ile başladım.
- Ardından tensor counting (PyTorch tensörleriyle sayım) ile tanıştım.
- Daha iyi bir sezgisel anlayış için verileri görselleştirdim, ardından olasılık matrisini hesaplayıp 5 tane yeni örnek isim ürettim.
- Sonra loss'u, yani negative log-likelihood'u (negatif log-olabilirlik) hesapladım.
- Son olarak basit, tek katmanlı bir sinir ağı kurdum ve gradient descent ile optimize ettim.

## Nerede Zorlandım?

- Optimizasyon kısmında zorlandım.
- Daha spesifik olarak softmax'in implementasyonunda zorlandım.
- Softmax'in ne yaptığını biliyordum ama sıfırdan nasıl inşa edildiğine dikkatlice bakmam gerekti.

## Negatif log-likelihood neden bu işin loss'u?

Hedef, gerçek veriye yüksek olasılık verdirmek; bu da likelihood'u maksimize etmekle eşdeğer. Ancak optimizasyon kütüphaneleri minimize etmek üzere tasarlandığı için, işareti çevirip negative log-likelihood'u minimize ederiz.

**Neden negatif?** Log, 0-1 aralığında hep negatif değer verir (olasılık 1'e yaklaştıkça log 0'a yaklaşır); negatif almak bunu minimize edilebilir bir loss'a çevirir.
