# AI ile Frontend Projelerinde Zaman Kazanma

**Örnek:**
"Bir form doğrulama şablonu oluşturun."

**Kod:**

```javascript
function LoginForm() {
  const [formData, setFormData] = useState({ email: "", password: "" });

  const handleChange = (e) => {
    setFormData({ ...formData, [e.target.name]: e.target.value });
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    console.log("Submitted:", formData);
  };

  return (
    <form onSubmit={handleSubmit}>
      <input type="email" name="email" onChange={handleChange} />
      <input type="password" name="password" onChange={handleChange} />
      <button type="submit">Giriş Yap</button>
    </form>
  );
}
```

AI'den isteyin:

```
"Bu formda e-posta doğrulaması ekle ve şifre en az 8 karakter uzunluğunda olmalı."
```

**Çözüm:**

```javascript
function LoginForm() {
  const [formData, setFormData] = useState({ email: "", password: "" });

  const handleChange = (e) => {
    setFormData({ ...formData, [e.target.name]: e.target.value });
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    console.log("Submitted:", formData);
  };

  const validateEmail = (email) => {
    const re = /\S+@\S+\.\S+/;
    return re.test(email);
  };

  const validatePassword = (password) => {
    return password.length >= 8;
  };

  return (
    <form onSubmit={handleSubmit}>
      <input
        type="email"
        name="email"
        onChange={handleChange}
        required
        pattern="\S+@\S+\.\S+"
      />
      <input
        type="password"
        name="password"
        onChange={handleChange}
        required
        minLength="8"
      />
      <button
        type="submit"
        disabled={
          !validateEmail(formData.email) || !validatePassword(formData.password)
        }
      >
        Giriş Yap
      </button>
    </form>
  );
}
```

**Açıklama:**

Bu örnekte, form doğrulama işlemleri için `validateEmail` ve `validatePassword` fonksiyonları oluşturulmuştur. E-posta doğrulaması için `pattern` özelliği kullanılmış ve şifre doğrulaması için `minLength` özelliği eklenmiştir. Giriş butonu, e-posta ve şifre doğrulamaları geçmediği sürece devre dışı bırakılmıştır. Bu sayede kullanıcıya form doğrulama hataları hakkında geri bildirim sağlanmıştır.
