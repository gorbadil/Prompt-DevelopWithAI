# Repository Pattern ile Çalışma

**Örnek:**
"Bir Product repository'si ve servisi oluşturun."

**Kod:**

```java
@Repository
public class ProductRepository {
    private List<Product> products = new ArrayList<>();

    public List<Product> findAll() {
        return products;
    }

    public Product findById(int id) {
        return products.stream()
                .filter(p -> p.getId() == id)
                .findFirst()
                .orElse(null);
    }

    public void save(Product product) {
        products.add(product);
    }
}
```

AI'den isteyin:

```
"Bu repository'yi kullanarak bir ProductService oluştur ve CRUD işlemleri ekle."
```

**Çıktı:**

```java
@Service
public class ProductService {
    private final ProductRepository productRepository;

    public ProductService(ProductRepository productRepository) {
        this.productRepository = productRepository;
    }

    public List<Product> getAllProducts() {
        return productRepository.findAll();
    }

    public Product getProductById(int id) {
        return productRepository.findById(id);
    }

    public void addProduct(Product product) {
        productRepository.save(product);
    }
}
```
