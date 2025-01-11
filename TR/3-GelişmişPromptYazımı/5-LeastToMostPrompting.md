# En Azdan Çoğa Doğru Yönlendirme

En azdan çoğa doğru yönlendirme, bir problemi alt problemlere ayırarak her birini çözmeyi içeren bir tekniktir. Bu teknik, çocuklar için gerçek dünya eğitim stratejilerinden esinlenmiştir.

## Problem

GPT-3, bazen karmaşık soruları doğru bir şekilde yanıtlamakta zorlanabilir. Bu durumda, en azdan çoğa doğru yönlendirme, sorunu alt problemlere ayırarak çözmeyi amaçlar. İlk adımda, bu alt problemler birbirlerine dayanan bir dizi alt probleme ayrılır. İkinci adımda, bu alt problemler birer birer çözülür. Çözülen önceki alt problemlerin çözümü, bir sonraki problemi çözmeye çalışan yönlendirmeye beslenir.

## Çözüm

1. Soruyu alt problemlere ayırın.
2. Her bir alt problemin çözümünü sırayla çözün.
3. Çözülen alt problemlerin çözümleri, bir sonraki alt problemin çözümüne yönlendirme olarak beslenir.

## Örnek

Gelin, biraz karmaşık bir müşteri hizmetleri sorusu soralım:

```
MÜŞTERİ SORUSU:
1 Mart'ta Arnold koleksiyonundan bir tişört satın aldım.
300 TL 'lık bir tişört satın aldım ve% 40 indirimli olduğunu gördüm.
Şimdi tüm tişörtlerde% 50 indirim olduğunu gördüm.
Tişörtü iade edebilir ve iki tişört satın alacak kadar mağaza kredim olup olmadığını merak ediyorum?

TALİMATLAR:
Müşteri sorularına nazikçe yanıt vermekle görevli bir müşteri hizmetleri temsilcisisiniz.
İadeler 30 gün içinde yapılabilir.
Bugünün tarihi 29 Mart'tır.
Şu anda tüm tişörtlerde% 50 indirim var. Mağazanızda tişört fiyatları 180-1000 TL arasında değişmektedir.
İndirim politikaları hakkında herhangi bir bilgi uydurmayın.
```

Modelden gelen çıktı şu şekilde olacaktır:

```
Teşekkürler sorunuz için. Maalesef, tişörtü 1 Mart'ta satın aldığınızdan, 30 günlük iade politikamızın dışındadır.
Ancak, şu anda tüm tişörtlerde% 50 indirim var, bu yüzden aynı miktarda mağaza kredisi ile iki tişört satın alabilirsiniz.
Tişörtlerim için fiyatlar 18-100 TL arasında değişmektedir. Başka sorunuz varsa lütfen bize bildirin.
```

Bu soruyu çözmek için, modelin alt problemleri çözmesi gerekmektedir. İlk olarak, müşterinin 30 günlük iade penceresi içinde olup olmadığını belirlemesi gerekmektedir. Eğer model hemen bir yanıt vermezse, bir sonraki alt probleme geçilir ve bu şekilde devam edilir.

```
MÜŞTERİ SORUSU:
1 Mart'ta Arnold koleksiyonundan bir tişört satın aldım.
300 TL 'lık bir tişört satın aldım ve% 40 indirimli olduğunu gördüm.
Şimdi tüm tişörtlerde% 50 indirim olduğunu gördüm.
Tişörtü iade edebilir ve iki tişört satın alacak kadar mağaza kredim olup olmadığını merak ediyorum?

TALIMATLAR:
Müşteri sorularına nazikçe yanıt vermekle görevli bir müşteri hizmetleri temsilcisisiniz.
İadeler 30 gün içinde yapılabilir.
Bugünün tarihi 29 Mart'tır.
Şu anda tüm tişörtlerde% 50 indirim var. Mağazanızda tişört fiyatları 180-1000 TL arasında değişmektedir.
İndirim politikaları hakkında herhangi bir bilgi uydurmayın.
30 günlük iade penceresi içinde olup olmadığını belirleyin.
Adım adım ilerleyelim.
```

Modelden gelen çıktı şu şekilde olacaktır:

```
Evet, müşteri 30 günlük iade penceresi içindedir.
Müşteri tişörtü 1 Mart'ta satın aldı ve bugünün tarihi 29 Mart'tır, bu da 30 günlük iade penceresi içindedir.
Müşteri, tişörtü iade edebilir ve satın alım için mağaza kredisi alabilir.
Müşteri, mağaza kredisini kullanarak şu anda% 50 indirimli iki tişört satın alabilir.
```

İlk alt problemin çözümüyle, tüm sorunu çözmüş olduk. Eğer GPT-3 hemen bir yanıt vermezse, bir sonraki alt probleme geçilir ve bu şekilde devam edilir. Dikkat edilmesi gereken bir nokta, Adım adım ilerleyelim.. Bu ifadenin eklenmesi her zaman gerekli değildir, ancak bu örnekte yardımcı olur.

```
MÜŞTERİ SORUSU:
1 Mart'ta Arnold koleksiyonundan bir tişört satın aldım.
300 TL 'lık bir tişört satın aldım ve% 40 indirimli olduğunu gördüm.
Şimdi tüm tişörtlerde% 50 indirim olduğunu gördüm.
Tişörtü iade edebilir ve iki tişört satın alacak kadar mağaza kredim olup olmadığını merak ediyorum?

TALIMATLAR:
Müşteri sorularına nazikçe yanıt vermekle görevli bir müşteri hizmetleri temsilcisisiniz.
İadeler 30 gün içinde yapılabilir.
Bugünün tarihi 29 Mart'tır.
Şu anda tüm tişörtlerde %50 indirim var. Mağazanızda tişört fiyatları 180-1000 TL arasında değişmektedir.
İndirim politikaları hakkında herhangi bir bilgi uydurmayın.
30 günlük iade penceresi içinde olup olmadığını belirleyin.
Adım adım ilerleyelim.
```

Modelden gelen çıktı şu şekilde olacaktır:

```
Evet, müşteri 30 günlük iade penceresi içindedir.
Müşteri tişörtü 1 Mart'ta satın aldı ve bugünün tarihi 29 Mart'tır, bu da 30 günlük iade penceresi içindedir.
Müşteri, tişörtü iade edebilir ve satın alım için mağaza kredisi alabilir.
Müşteri, mağaza kredisini kullanarak şu anda% 50 indirimli iki tişört satın alabilir.
```

İlk alt problemin çözümüyle, tüm sorunu çözmüş olduk. Eğer GPT-3 hemen bir yanıt vermezse, bir sonraki alt probleme geçilir ve bu şekilde devam edilir. Dikkat edilmesi gereken bir nokta, Adım adım ilerleyelim.. Bu ifadenin eklenmesi her zaman gerekli değildir, ancak bu örnekte yardımcı olur.
