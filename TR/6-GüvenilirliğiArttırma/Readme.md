# Güvenilirliği Artırma

Belirli bir ölçüde, daha önce ele alınan tekniklerin çoğu, özellikle öz-tutarlılık açısından, tamamlamaların doğruluğunu ve dolayısıyla güvenilirliği artırmakla ilgilidir. Ancak, temel istem stratejilerinin ötesinde güvenilirliği artırmak için kullanılabilecek başka teknikler de vardır.

LLM'lerin, yanlış yazılmış, kötü ifade edilmiş veya hatta aktif olarak yanıltıcı istemlere yanıt verirken bir istemin ne söylemeye çalıştığını yorumlama konusunda beklediğimizden daha güvenilir olduğu bulunmuştur. Bu yeteneğe rağmen, halüsinasyonlar, CoT yöntemleriyle hatalı açıklamalar ve çoğunluk etiketi yanlılığı, yakınlık yanlılığı ve yaygın token yanlılığı dahil olmak üzere çeşitli sorunlar sergilemeye devam ederler. Ayrıca, sıfır atış CoT, hassas konularla ilgilenirken özellikle önyargılı olabilir.

Bu sorunların bazılarına yaygın çözümler arasında, önceden var olan önyargıları kaldırmak için kalibratörler ve tamamlamaları puanlamak için doğrulayıcılar ile tamamlamalarda çeşitliliği teşvik etmek yer alır.
