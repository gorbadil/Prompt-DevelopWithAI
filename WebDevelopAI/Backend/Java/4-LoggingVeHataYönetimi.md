# Logging ve Hata Yönetimi

**Örnek:**
"Bir global hata yönetimi mekanizması ekleyin."

**Kod:**

```java
@ControllerAdvice
public class GlobalExceptionHandler {

    @ExceptionHandler(Exception.class)
    public ResponseEntity<String> handleException(Exception ex) {
        return ResponseEntity.status(HttpStatus.INTERNAL_SERVER_ERROR)
                .body("Error: " + ex.getMessage());
    }
}
```

AI'den isteyin:

```
"Bu hata yönetimini daha açıklayıcı mesajlar eklemek için genişlet."
```

**Çıktı:**

```java
public ResponseEntity<String> handleException(Exception ex) {
    return ResponseEntity.status(HttpStatus.INTERNAL_SERVER_ERROR)
            .body("An error occurred: " + ex.getMessage());
}
```
