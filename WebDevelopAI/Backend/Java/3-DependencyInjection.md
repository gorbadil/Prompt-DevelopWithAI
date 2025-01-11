# Dependency Injection (DI) Kullanımı

**Örnek:**
"Bir e-posta servisinin Dependency Injection ile projeye dahil edilmesini sağlayın."

**Kod:**

```java
@Service
public class EmailService {
    public void sendEmail(String to, String subject, String body) {
        System.out.println("Email sent to " + to + ": " + subject);
    }
}

@RestController
@RequestMapping("/notifications")
public class NotificationController {

    private final EmailService emailService;

    public NotificationController(EmailService emailService) {
        this.emailService = emailService;
    }

    @PostMapping
    public String notify(@RequestParam String to) {
        emailService.sendEmail(to, "Welcome!", "Thanks for joining us.");
        return "Notification sent to " + to;
    }
}
```

AI'den isteyin:

```
"Bu serviste birden fazla alıcıya e-posta göndermek için bir metod ekle."
```

**Çıktı:**

```java
public void sendEmails(List<String> toList, String subject, String body) {
    toList.forEach(to -> sendEmail(to, subject, body));
}
```
