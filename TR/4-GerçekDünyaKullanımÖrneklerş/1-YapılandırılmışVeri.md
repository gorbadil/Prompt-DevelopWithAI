# Yapılandırılmış Veri

Yapılandırılmış veri, bilgileri etkili bir şekilde düzenlemek için güçlü bir araçtır, özellikle e-ticaret, mobil ve arama gibi gerçek dünya uygulamalarında. Kullanıcı girdilerini JSON, Markdown tabloları, HTML ve YAML gibi yapılandırılmış biçimlere dönüştürmeye yardımcı olur, veri yönetimini ve geri alımını geliştirir. Bu alandaki son gelişmeler arasında Google'ın genişletilmiş ürün bilgi türleri, yapılandırılmış veri işlemlerini otomatikleştirmek ve geliştirmek için yapay zekayı kullanma, yapılandırılmış veri biçimi olarak JSON-LD'nin tercih edilmesinin devam etmesi ve zengin medya ve ayrıntılı bilgilerle arama sonuçlarında geliştirilmiş mobil deneyimler yer almaktadır.

## Örnekler

### Örnek: JSON Objesi

Bir kullanıcı, "18 aylık kızım için doğum günü hediyesi" arıyorsa, yapılacak olan yapılandırılmış veri işlemleriyle çeşitli biçimlerde yapılandırılmış veri oluşturabilirsiniz.

JSON Örneği:

```json
JSON formatında, üçlü tırnaklarla sınırlanmış metinden aşağıdaki bilgileri içeren bir JSON nesnesi oluşturun:
- `Cinsiyet` ("erkek", "kadın"),
- `Durum` ("parti", "doğum günü", "yıl dönümü"),
- `Yaş (yıl)` (sayısal değer)
  """18 aylık kızım için doğum günü hediyesi"""
```

Çıktı Model, aşağıdaki JSON nesnesini oluşturacaktır:

```json
{
  "Cinsiyet": "kadın",
  "Durum": "doğum günü",
  "Yaş (yıl)": 1.5
}
```

Yapılandırılmış verilerin başka biçimlere dönüştürülmesini gösteren bir diğer yetenek olan veri formatı değişimini, tek bir kaynak promptundan farklı biçimlere dönüştürme örneğiyle genişleten aşağıdaki örnekler, orijinal JSON promptunu diğer biçimlere dönüştürmektedir.

### Örnek: Markdown Tablosu

JSON'dan Markdown tablosuna

```markdown
| Cinsiyet | Durum      | Yaş (yıl) |
| -------- | ---------- | --------- |
| Kadın    | Doğum Günü | 1.5       |
```

### Örnek: HTML Tablosu

JSON'dan HTML tablosuna

```html
<table>
  <thead>
    <tr>
      <th>Cinsiyet</th>
      <th>Durum</th>
      <th>Yaş (yıl)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Kadın</td>
      <td>Doğum Günü</td>
      <td>1.5</td>
    </tr>
  </tbody>
</table>
```
