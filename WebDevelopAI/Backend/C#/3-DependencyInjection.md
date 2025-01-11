# Dependency Injection ile Çalışma

**Örnek:**
"Bir servis katmanını Dependency Injection (DI) ile projeye ekleyin."

**Kod:**

```csharp
public interface IEmailService
{
    void SendEmail(string to, string subject, string body);
}

public class EmailService : IEmailService
{
    public void SendEmail(string to, string subject, string body)
    {
        Console.WriteLine($"Email sent to {to}: {subject} - {body}");
    }
}
```

AI'den isteyin:

```
"Bu servisi DI ile Startup.cs dosyasına ekleyin ve bir kontrolörde kullanın."
```

**Çıktı:**

```csharp
public void ConfigureServices(IServiceCollection services)
{
    services.AddSingleton<IEmailService, EmailService>();
}

[ApiController]
[Route("api/[controller]")]
public class EmailController : ControllerBase
{
    private readonly IEmailService _emailService;

    public EmailController(IEmailService emailService)
    {
        _emailService = emailService;
    }

    [HttpPost]
    public void SendEmail([FromBody] Email email)
    {
        _emailService.SendEmail(email.To, email.Subject, email.Body);
    }
}
```

Bu örnekte, `EmailService` sınıfı, `IEmailService` arayüzünü uygular ve e-posta gönderme işlemlerini gerçekleştirir. `EmailController` sınıfı, `IEmailService` arayüzüne bağımlıdır ve bu arayüzü kullanarak e-posta gönderme işlemlerini gerçekleştirir.
