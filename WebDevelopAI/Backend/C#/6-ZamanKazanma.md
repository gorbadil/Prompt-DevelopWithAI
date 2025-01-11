# AI ile Zaman Kazanma

**Örnek:**
"Projede sık kullanılan bir veri doğrulama şablonu oluşturun."

**Kod:**

```csharp
public class UserValidator
{
public bool ValidateEmail(string email) =>
!string.IsNullOrWhiteSpace(email) && email.Contains("@");

    public bool ValidatePassword(string password) =>
        !string.IsNullOrWhiteSpace(password) && password.Length >= 8;

}
```

AI'den isteyin:

```
"Bu sınıfa kullanıcı adını kontrol eden bir metot ekle."
```

**Çıktı:**

```csharp
public class UserValidator
{
    public bool ValidateEmail(string email) =>
        !string.IsNullOrWhiteSpace(email) && email.Contains("@");

    public bool ValidatePassword(string password) =>
        !string.IsNullOrWhiteSpace(password) && password.Length >= 8;

    public bool ValidateUsername(string username) =>
        !string.IsNullOrWhiteSpace(username) && username.Length >= 3;
}
```

**Açıklama:**

AI, sınıfa yeni bir metot eklemek için gerekli kodu oluşturdu. Bu, geliştiricinin zaman kazanmasına yardımcı olur ve hızlı bir şekilde işlevselliği genişletebilir.
