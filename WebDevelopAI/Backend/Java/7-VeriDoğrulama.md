# Veri Doğrulama

**Örnek:**
"Kullanıcı doğrulama için bir Validator sınıfı oluşturun."

**Kod:**

```java
@Component
public class UserValidator {

    public boolean isValidEmail(String email) {
        return email != null && email.contains("@");
    }

    public boolean isValidPassword(String password) {
        return password != null && password.length() >= 8;
    }
}
```

AI'den isteyin:

```
"Bu sınıfa kullanıcı adı doğrulama fonksiyonu ekle."
```

**Çıktı:**

```java
public boolean isValidUsername(String username) {
    return username != null && username.length() >= 5;
}
```

```java
@Component
public class UserValidator {

    public boolean isValidEmail(String email) {
        return email != null && email.contains("@");
    }

    public boolean isValidPassword(String password) {
        return password != null && password.length() >= 8;
    }

    public boolean isValidUsername(String username) {
        return username != null && username.length() >= 5;
    }
}
```
