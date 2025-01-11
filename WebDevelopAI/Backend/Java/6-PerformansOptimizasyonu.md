# Performans Optimizasyonu

**Örnek:**
"Bir sorguyu optimize etmek için caching kullanın."

**Kod:**

```java
@Service
public class ProductService {

    private final ProductRepository productRepository;

    public ProductService(ProductRepository productRepository) {
        this.productRepository = productRepository;
    }

    @Cacheable("products")
    public List<Product> getAllProducts() {
        return productRepository.findAll();
    }
}
```

AI'den isteyin:

```
"Cache'yi ürün adıyla filtreleme özelliği ekleyecek şekilde genişlet."
```

**Çıktı:**

```java
@Cacheable(value = "products", key = "#name")
public List<Product> getProductsByName(String name) {
    return productRepository.findByName(name);
}
```
