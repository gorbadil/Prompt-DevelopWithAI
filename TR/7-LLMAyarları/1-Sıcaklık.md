# Sıcaklık

Sıcaklık, Dil Modelleri (LM'ler) için özellikle ince ayar sürecinde önemli bir ayardır. Dil modelinin softmax fonksiyonundaki “sıcaklık” parametresini ifade eder. Sıcaklığı ayarlamak, modelin çıktısının rastgeleliğini veya tutuculuğunu etkileyebilir.

## Sıcaklığın Rolü

Sıcaklık, modelin metin üretirken ne kadar yaratıcı ve cesur olacağını kontrol eder. Daha düşük sıcaklık değeri, modelin daha tutucu olmasını sağlar ve eğitim verilerinden öğrendiği kalıplara sıkı sıkıya bağlı kalır. Daha yüksek sıcaklık değerleri, modelin daha az olası kelimeleri daha olası hale getirerek daha riskli çözümler keşfetmesini teşvik eder.

## Pratik Kullanımlar

Bir LM'yi ince ayar yaparken, sıcaklığı ayarlayarak modelin davranışını düzenleyebilirsiniz:

**Daha düşük sıcaklık değerleri (örneğin, 0.2 veya 0.5):** Model, eğitim verilerinden öğrendiği ifadeler ve kelime dizilerine daha fazla odaklanacaktır. Çıktı daha az çeşitli olacak, ancak yenilik veya yaratıcılık eksikliği olabilir. Metin özetleme veya çeviri gibi tutuculuğun önemli olduğu görevler için uygundur.

**Daha yüksek sıcaklık değerleri (örneğin, 1.0 veya 2.0):** Model, yenilikçi kelime kombinasyonları ile daha yaratıcı çıktılar üretecektir. Ancak, daha az tutarlı veya bağlamsal olarak uygunsuz metinler üretebilir. Yaratıcı yazma veya beyin fırtınası gibi keşif ve farklılığın gerekli olduğu görevler için kullanışlıdır.

Çeşitli sıcaklık değerleriyle denemeler yapmak, belirli bir görev ve istenen çıktı doğrultusunda yaratıcılık ve tutarlılık arasında optimal dengeyi bulmaya yol açabilir.
