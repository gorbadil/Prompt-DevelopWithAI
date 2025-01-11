# Unit Test Yazımı

**Örnek:**
"Bir UserController için birim testi yazın."

**Kod:**

```java
@WebMvcTest(UserController.class)
public class UserControllerTest {

    @Autowired
    private MockMvc mockMvc;

    @Test
    public void shouldReturnAllUsers() throws Exception {
        mockMvc.perform(get("/users"))
                .andExpect(status().isOk())
                .andExpect(content().contentType(MediaType.APPLICATION_JSON))
                .andExpect(jsonPath("$.length()").value(2));
    }
}
```

AI'den isteyin:

```
"Bu teste POST ve PUT işlemlerini test eden senaryolar ekle."
```

**Çıktı:**

```java
@Test
public void shouldAddUser() throws Exception {
    mockMvc.perform(post("/users")
            .contentType(MediaType.APPLICATION_JSON)
            .content("{\"id\":3,\"name\":\"Charlie\"}"))
            .andExpect(status().isOk())
            .andExpect(jsonPath("$.id").value(3))
            .andExpect(jsonPath("$.name").value("Charlie"));
}

@Test
public void shouldUpdateUser() throws Exception {
    mockMvc.perform(put("/users/3")
            .contentType(MediaType.APPLICATION_JSON)
            .content("{\"id\":3,\"name\":\"David\"}"))
            .andExpect(status().isOk())
            .andExpect(jsonPath("$.id").value(3))
            .andExpect(jsonPath("$.name").value("David"));
}
```
