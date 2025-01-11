# Giriş - Prompting

Prompting, bir modelin belirli bir görevi yerine getirmesi için bir "prompt" veya talimat verme işlemidir. Örneğin, İngilizce metni Fransıza çevirmek istiyorsanız, aşağıdaki talimatı verebilirsiniz:

```
Translate the text delimited by triple quotes from English to Turkish:

"""Hello, how are you?"""
```

Model, ardından aşağıdaki çıktıyı üretecektir:

```
Merhaba, nasılsınız?
```

Bu örnekte, modeli bir görevi yerine getirmesi için talimatlarla birlikte bir prompt ile donattık. Fark ederseniz, promptumuzu yazarken özel bir yol izledik. Basitçe aşağıdaki promptı verebilirdik ve yine de çalışırdı:

```
Translate the following to Turkish:
```

```
Hello, how are you?
```

Ancak, promptımızı daha açık ve talimatları içerikten ayırmak için ayraçlar kullanmak en iyi uygulamalardan biridir. Bu konuda daha fazla bilgi, yol haritasının "Öneriler" bölümünde öğreneceksiniz.
