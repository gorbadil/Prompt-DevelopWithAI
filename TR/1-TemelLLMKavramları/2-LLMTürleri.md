# LLM Türleri

Doğal Dil İşleme (NLP) alanındaki büyük gelişmeler, büyük dil modellerinin (LLM) yükselişine yol açmıştır. LLM'ler, büyük miktarda metin verisi üzerinde eğitilmiş derin öğrenme modelleridir ve doğal dil işleme görevlerini gerçekleştirmek için kullanılırlar. LLM'ler, metin verilerini anlamak, dil modelleri oluşturmak, metin oluşturmak ve metin sınıflandırmak gibi birçok görevde kullanılabilirler.

### Temel LLM

Temel LLM'ler, eğitim verilerine dayanarak bir sonraki kelimeyi tahmin etmek için tasarlanmış LLM'lerdir. Soruları yanıtlamak, konuşmalar yapmak veya sorunları çözmeye yardımcı olmak gibi görevler için tasarlanmamışlardır. Örneğin, bir temel LLM'ye "LLM'ler hakkında bu kitapta, tartışacağız" cümlesini verirseniz, bu cümleyi tamamlayabilir ve size "LLM'ler hakkında bu kitapta, LLM'lerin ne olduğunu, nasıl çalıştıklarını ve uygulamalarınızda nasıl kullanabileceğinizi tartışacağız." verebilir. Veya "Neler bazı ünlü sosyal ağlar?" verirseniz, yanıt vermek yerine "Neden insanlar sosyal ağları kullanıyor?" veya "Sosyal ağların bazı faydaları nelerdir?" geri verebilir. Görebileceğiniz gibi, bize ilgili metin veriyor ancak soruyu yanıtlamıyor. İşte burada Talimat Ayarlı LLM'ler devreye giriyor.

### Talimat Ayarlı LLM'ler

Talimat Ayarlı LLM'ler, metinlerinizi otomatik olarak tamamlamak yerine, verilen talimatları takip etmeye çalışır. Örneğin, "LLM'ler hakkında neler?" cümlesini girdiğinizde, eğitildiği verileri kullanarak soruyu yanıtlamaya çalışır. Benzer şekilde, "Neler bazı ünlü sosyal ağlar?" cümlesini girdiğinizde, soruyu yanıtlamaya çalışır.

Talimat Ayarlı LLM'ler, Temel LLM'lerin üzerine inşa edilmiştir:

```
Talimat Ayarlı LLM'ler = Temel LLM'ler + Daha Fazla Ayarlama + RLHF
```

Talimat Ayarlı LLM'ler oluşturmak için, bir Temel LLM alınır ve örnek "Talimatları" ve bu talimatların sonucunda modelin nasıl performans göstermesi gerektiğini kapsayan büyük bir veri kümesini kullanarak daha fazla eğitilir. Model daha sonra, insan geri bildirimi kullanarak öğrenmesine ve zamanla performansını iyileştirmesine olanak tanıyan "İnsan Geri Bildirimi ile Pekiştirmeli Öğrenme" (RLHF) adlı bir teknik kullanılarak daha fazla ayarlanır.

## Sonuç

LLM'ler, geniş bir dil işleme görevlerini çözmek için kullanılabilen güçlü bir araçtır. Sağlık, finans, eğitim vb. gibi çeşitli endüstrilerde kullanılmakta ve süreçleri otomatikleştirmek ve verimliliği artırmak için kullanılmaktadır. LLM'ler, bilgisayarlarla etkileşim şeklimizi devrimleştirmek ve hayatımızı kolaylaştırmak için potansiyele sahiptir.
