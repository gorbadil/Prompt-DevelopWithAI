# Backend Geliştirme ve AI: Java Spring Boot Pratik Örnekler

## Basit Bir REST API Oluşturma

**Örnek:**  
"AI'den basit bir `User` API'si oluşturmasını isteyin."

**Kod:**

```java
@RestController
@RequestMapping("/users")
public class UserController {

    private List<User> users = new ArrayList<>(List.of(
            new User(1, "Alice"),
            new User(2, "Bob")
    ));

    @GetMapping
    public List<User> getAllUsers() {
        return users;
    }

    @PostMapping
    public User addUser(@RequestBody User user) {
        users.add(user);
        return user;
    }
}
```

AI'den isteyin:

```
"Bu API'ye bir PUT metodu ekleyerek kullanıcıları güncelleme işlemi yap."
```

**Çıktı:**

```java
@PutMapping("/{id}")
public User updateUser(@PathVariable int id, @RequestBody User user) {
    User existingUser = users.stream()
            .filter(u -> u.getId() == id)
            .findFirst()
            .orElseThrow(() -> new RuntimeException("User not found"));
    existingUser.setName(user.getName());
    return existingUser;
}
```
