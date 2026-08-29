# Deney Notları: Sıfırdan Autograd

## Ne Yaptım?

- Autograd'ı sıfırdan kurdum.
- İleri geçiş: hem hesap yapıyor hem de bir DAG (grafik) kuruyor. Örneğin `a + b * c` yazınca, sonuç hesaplanıyor ve aynı zamanda bu DAG oluşuyor.
- Geriye yayılım (backpropagation): zincir kuralını bu DAG üzerinden otomatik uyguluyor.

## Nerede Zorlandım?

Öğrendiklerimi büyük resme oturtmakta zorlandım. Nöronlar konusuna geçilince kafam karıştı. Tek bir nöron kodlanmaya başlayınca resim netleşti.

## backward() Nasıl Çalışır?

1. **Topolojik sıralama:** Düğümleri, önce çocukları işlenmiş olacak şekilde sıraya diz.
2. **Başlangıç:** Çıktının gradyanını 1 yap (çünkü `doutput/doutput = 1`).
3. **Tersten gez:** Sıralamayı ters çevirip çıktıdan girdiye doğru ilerle.
4. **backward'ı çağır:** Her düğümün `_backward` fonksiyonunu çalıştırıp gradyanı çocuklarına aktar.

Bu sırayla zincir kuralı tüm grafik boyunca otomatik uygulanmış olur.
