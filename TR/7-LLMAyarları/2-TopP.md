# Top P Örnekleme

Top P, “çekirdek örnekleme” olarak da bilinir, bir modelin ürettiği çıktının rastgeleliğini kontrol etmek için daha dinamik bir yöntem sağlar. Metin üretiminde kalite ve çeşitlilik arasındaki dengeyi iyileştirir.

## Top P Nasıl Çalışır?

Top K örneklemede olduğu gibi en yüksek olasılığa sahip K token'ı seçmek yerine, Top P örnekleme, toplam olasılığı verilen P değerine eklenen bir dizi token seçer. P, 0 ile 1 arasında bir olasılık kütlesidir. Bu, seçilen token sayısının değişeceği ve dağılıma daha ayrıntılı bir şekilde uyum sağlayacağı anlamına gelir.

## Top P'nin Avantajları

**Daha çeşitli ve tutarlı çıktılar:** Top P örnekleme, aşırı muhafazakar ve yüksek derecede rastgele metin arasında bir denge kurar. Bu, Top K örneklemeye kıyasla daha çeşitli ve tutarlı çıktılar oluşturur.

**Uyarlanabilir eşik:** Top P örneklemenin dinamik doğası, K'nın manuel ayarlanmasını gerektiren Top K örneklemenin aksine, token olasılık dağılımına uyum sağlamasına olanak tanır.

**OOV token'larını önler:** Top P örnekleme, kümülatif olasılık eşiğine dayalı olarak token'ları toplayarak, kelime dağarcığı dışı (OOV) token'ların seçilmesini etkili bir şekilde önler.

## Top P Değerini Ayarlama

**Düşük değerler:** P değerini düşürmek, çeşitlilik pahasına daha odaklanmış çıktılarla sonuçlanacaktır.

**Yüksek değerler:** P değerini artırmak, modelin daha çeşitli yanıtlar keşfetmesini teşvik eder, ancak bu tutarlılık pahasına olabilir.

Pratikte, yaygın olarak kullanılan bir Top P değeri 0.9'dur, ancak belirli kullanım durumunuza ve çeşitlilik ile tutarlılık arasındaki istediğiniz dengeye bağlı olarak farklı P değerlerini denemelisiniz.
