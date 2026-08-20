# Genel yapılması gerekilenler
🎯 GitHub kod teslimi
    Karpathy videosu ve ek okuma takip edilir
    Haftanın kod egzersizi tamamlanır
    Deneyler çalıştırılır
    Loss, accuracy, sample quality ve training davranışı not edilir
🎯 Kısa deney notu
🎯 3 slaytlık ilerleme sunumu

# Bu hafta yapılması gereken egzersiz
Python ile tek nöron forward pass yaz
Basit bir loss fonksiyonu oluştur
Parametreyi manuel değiştirerek loss'un nasıl değiştiğini gözlemle

# Kısa Deney Notu

**Kavramlar:** Forward pass, loss fonksiyonu, parametre güncelleme, numerical derivative, gradient descent.

**Forward Pass nedir?**
Öncelikle bir modelin generic forward pass'ini yazdım. Forward pass, girdilerin bir sinir ağının katmanlarından geçirilerek son katmanda bir tahmin üretilmesi sürecidir; her nöronda girdiler ağırlıklarla çarpılır, bias eklenir ve elde edilen sonuç bir aktivasyon fonksiyonundan geçirilir.

**Loss nedir?**
Sonra bir loss fonksiyonu yazdım. Loss fonksiyonu, modelin tahminini gerçek etiketle karşılaştırıp modelin ne kadar "yanlış" olduğunu bir skalar değere dönüştürür.

**Parametre güncellemesi neden önemlidir?**
Loss'un nasıl değiştiğini gözlemledim, parametreleri manuel değiştirerek. Hangi ağırlıkların loss'a ne kadar katkıda bulunduğu belirlendikten sonra, bu ağırlıklar gradient descent gibi bir algoritma ile güncellenir.

**Gradient Descent nedir?**
Gradient Descent'i yakından inceledim. Gradient descent, loss fonksiyonunu minimize etmek için model parametrelerini (ağırlıklar, bias) adım adım güncelleyen iteratif bir optimizasyon algoritmasıdır.

# 3 slaytlık ilerleme sunumu
Ekte







