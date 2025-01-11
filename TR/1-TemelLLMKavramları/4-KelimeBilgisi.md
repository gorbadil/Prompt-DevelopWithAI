# Kelime Bilgisi

Bu bölümde, LLM'lerle çalışırken karşılaşabileceğiniz birçok yeni terimle karşılaşacaksınız. Bu bölüm, bu terimlerin anlamını ve LLM'ler bağlamında nasıl kullanıldıklarını anlamanıza yardımcı olacaktır.

**AI** — Yapay zeka. Yapay zeka, bilgisayar sistemlerinin insan benzeri zekaya sahip olmasını sağlayan bir bilim dalıdır. Yapay zeka, birçok farklı alt alanı içerir, bunlar arasında makine öğrenimi, doğal dil işleme, görüntü işleme ve daha fazlası yer alır.

**Model** — Bir model, bir yapay zeka algoritması tarafından öğrenilen bir görevi yerine getirmek için kullanılan bir matematiksel yapıdır. Modeller, genellikle büyük miktarda veri üzerinde eğitilir ve ardından yeni verileri analiz etmek, tahmin yapmak veya sınıflandırmak için kullanılır.

**LLM** — Büyük dil modeli. Büyük dil modeli, insan benzeri metni anlayabilen ve üretebilen bir yapay zeka türüdür. Bu modeller, geniş miktarda metin verisi üzerinde eğitilmişlerdir ve soruları yanıtlama, konuşmalar yapma, metin özetleme, dil çevirisi ve çok daha fazlasını yapabilme yeteneğine sahiptir.

**MLM** — Maskelenmiş dil modeli. Maskelenmiş dil modeli, bir metin dizisindeki bir sonraki kelimeyi tahmin etmek için eğitilen bir dil modeli türüdür. Genellikle büyük bir metin veri kümesi üzerinde eğitilir ve makine çevirisi, duygu analizi, özetleme ve daha fazlası gibi çeşitli görevler için kullanılabilir.

**NLP** — Doğal dil işleme. Doğal dil işleme, bilgisayarlar ve insan dilleri arasındaki etkileşimle ilgilenen yapay zeka dalıdır. İnsan dillerini analiz etmek, anlamak ve üretmek için kullanılır.

**Etiket** — Etiketler, verilen bir metnin sınıflandırılması için olası seçeneklerdir. Örneğin, "Seni seviyorum" diyen bir metin varsa, etiketler "olumlu", "olumsuz" veya "tarafsız" olabilir. Model, giriş metne dayanarak hangi etiketin en olası doğru olduğunu tahmin etmeye çalışacaktır.

**Etiket Boşluğu** — Etiket Boşluğu, belirli bir metne atanan tüm olası etiketlerin kümesidir. Örneğin, "Seni seviyorum" diyen bir metin varsa, etiket boşluğu "olumlu", "olumsuz" veya "tarafsız" olabilir.

**Etiket Dağılımı** — Etiket dağılımı, etiket uzayı üzerindeki olasılık dağılımıdır. Örneğin, "Seni seviyorum" diyen bir metin varsa, etiket dağılımı [0.8, 0.1, 0.1] olabilir. Bu, modelin metnin olumlu olma olasılığının %80 olduğunu, olumsuz olma olasılığının %10 olduğunu ve tarafsız olma olasılığının %10 olduğunu düşündüğünü gösterir.

**Metin Sınıflandırma** — Metin sınıflandırma, bir metni belirli bir kategoriye atama işlemidir. Örneğin, bir metnin olumlu, olumsuz veya tarafsız olup olmadığını belirlemek için metin sınıflandırma kullanılabilir.

**Metin Üretme** — Metin üretme, bir dil modelinin belirli bir metin girişi verildiğinde yeni metinler oluşturmasını sağlayan bir işlemdir. Bu, hikaye yazma, şiir oluşturma, makale yazma ve daha fazlası gibi çeşitli uygulamalarda kullanılabilir.

**Metin Özetleme** — Metin özetleme, bir metin girişi verildiğinde, metnin ana fikrini veya önemli noktalarını özetleyen kısa bir metin oluşturma işlemidir. Bu, makalelerin özetlenmesi, kitapların özetlenmesi ve daha fazlası gibi uygulamalarda kullanılabilir.

**Metin Oluşturma** — Metin oluşturma, bir dil modelinin belirli bir metin girişi verildiğinde yeni metinler oluşturmasını sağlayan bir işlemdir. Bu, hikaye yazma, şiir oluşturma, makale yazma ve daha fazlası gibi çeşitli uygulamalarda kullanılabilir.

```
Tweet: "Sıcak cebimdeki pastaları seviyorum"
Bu tweet'in duygusu nedir? 'pos' veya 'neg' deyin.
Burada, sözlendirici, pozitif ve negatif kavramsal etiketlerden pos ve neg tokenlerine eşleştirme yapar.
```

**Pekiştirmeli Öğrenme** — Pekiştirmeli öğrenme, bir modelin bir ortamda belirli bir görevi gerçekleştirmesini öğrenmek için kullanılan bir öğrenme yaklaşımıdır. Model, çevresel geri bildirimlere dayanarak belirli bir eylemi gerçekleştirmeyi öğrenir.
