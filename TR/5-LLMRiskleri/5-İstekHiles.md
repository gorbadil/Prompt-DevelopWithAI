# İstek Hilesi

## Açıklama

Size bir istek ve bu istek temelinde metin üreten bir model verilir. Modelin istenen metni üretmesini sağlamak için isteği istediğiniz şekilde değiştirebilirsiniz. Amaç, isteği mümkün olduğunca az değişiklikle istenen metni üretmesini sağlamaktır.

## Talimatlar

- **Amaç**: İsteği mümkün olduğunca az değişiklikle istenen metni üretmesini sağlamak.
- **Girdi**:
  - İstek: Bir metin isteği.
  - İstenen Metin: Modelin üretmesini istediğiniz metin.
  - Model: Metin üretmek için kullanacağınız model.
- **Çıktı**: - İstek: Değiştirilmiş istek. - Üretilen Metin: Modelin değiştirilmiş istek kullanarak ürettiği metin. - Değişiklikler: İstek üzerinde yapılan değişiklikler.
- **Örnek**: - İstek: "Bir varmış bir yokmuş," - İstenen Metin: "orada - Model: GPT-3 - İstek (Değiştirilmiş): "Bir varmış bir yokmuş, orada" - Üretilen Metin: "Bir varmış bir yokmuş, orada küçük bir - Değişiklikler: "küçük bir" eklendi

## Ek Notlar

- İstenen metni elde etmek için isteğin herhangi bir kısmını ekleyebilir, çıkarabilir veya değiştirebilirsiniz.
- İsteği istenen metni elde etmek için nasıl değiştireceğiniz konusunda yaratıcı olun.
- Ne kadar az değişiklik yaparsanız o kadar iyi.

## Örnekler

### Örnek 1

- İstek: "Bir varmış bir yokmuş,"
- İstenen Metin: "orada küçük bir
- Model: GPT-3

---

- İstek (Değiştirilmiş): "Bir varmış bir yokmuş, orada"
- Üretilen Metin: "Bir varmış bir yokmuş, orada küçük bir
- Değişiklikler: "küçük bir" eklendi

---

### Örnek 2

- İstek: "Uzak, çok uzak bir galakside,"
- İstenen Metin: "bir kahraman kötü imparatorluğa karşı savaştı."
- Model: GPT-3

---

- İstek (Değiştirilmiş): "Uzak, çok uzak bir galakside, bir kahraman kötü imparatorluğa karşı savaştı."
- Üretilen Metin: "Uzak, çok uzak bir galakside, bir kahraman kötü imparatorluğa karşı savaştı."
- Değişiklikler: Değişiklik gerekmedi.
