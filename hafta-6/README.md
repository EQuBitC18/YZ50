# Hafta 6: WaveNet

## Ne Yaptım?

- Hafta 4/5'teki MLP + BatchNorm kodunu sınıflara topladım: `Linear`, `BatchNorm1d`, `Tanh`, `Embedding`, `FlattenConsecutive`, `Sequential`.
- Aynı düz modeli önce bağlam 3, sonra bağlam 8 ile eğitip karşılaştırdım.
- Bağlamı tek seferde düzleştirmek yerine, karakterleri ikişer ikişer birleştiren hiyerarşik bir yapı (WaveNet) kurdum.

## BatchNorm Hatası

`BatchNorm1d`, 2 boyutlu girdi (batch, channel) için yazılmıştı. WaveNet'te katmanlar arasında 3 boyutlu tensörler (batch, grup, channel) dolaştığı için ortalama yanlış eksende alınıyor, shape'ler uyuşmuyordu. Ortalamanın hangi eksenlerde alınması gerektiğini bulup düzelttim.

## Karşılaştırma

| Model | Parametre | Train loss | Val loss |
|---|---|---|---|
| Bağlam 3, düz MLP | 18,297 | 2.0422 | 2.0954 |
| Bağlam 8, düz MLP | 33,297 | 1.8677 | 2.0072 |
| Bağlam 8, WaveNet | 76,963 | 1.7647 | 1.9896 |

Bağlamı büyütmek tek başına en büyük kazancı verdi. Aynı bağlamda hiyerarşik birleştirmeye geçmek (WaveNet) ek bir kazanç sağladı, ama parametre artışına oranla daha mütevazı

## Dosyalar

- `experiment.ipynb` — kendi yazdığım kod
- `makemore_part5_cnn1.ipynb` — Karpathy'nin ders notebook'u (referans)
- `names.txt` — veri seti
