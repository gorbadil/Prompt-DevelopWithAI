# Veri Katmanı (Repository Pattern)

**Örnek:**
"Bir ürün veritabanı için repository pattern'ı kullanın."

**Kod:**

```csharp
public interface IProductRepository
{
    IEnumerable<Product> GetAllProducts();
    Product GetProductById(int id);
    void AddProduct(Product product);
}

public class ProductRepository : IProductRepository
{
    private readonly List<Product> _products = new List<Product>();

    public IEnumerable<Product> GetAllProducts() => _products;

    public Product GetProductById(int id) => _products.FirstOrDefault(p => p.Id == id);

    public void AddProduct(Product product) => _products.Add(product);
}
```

AI'den isteyin:

```
"Bu repository'yi kullanarak bir ProductController oluştur."
```

**Çıktı:**

```csharp
[ApiController]
[Route("api/[controller]")]
public class ProductController : ControllerBase
{
    private readonly IProductRepository _productRepository;

    public ProductController(IProductRepository productRepository)
    {
        _productRepository = productRepository;
    }

    [HttpGet]
    public IEnumerable<Product> Get() => _productRepository.GetAllProducts();

    [HttpGet("{id}")]
    public Product Get(int id) => _productRepository.GetProductById(id);

    [HttpPost]
    public void Post([FromBody] Product product) => _productRepository.AddProduct(product);
}
```

Bu örnekte, `ProductRepository` sınıfı, `IProductRepository` arayüzünü uygular ve ürün veritabanı işlemlerini gerçekleştirir. `ProductController` sınıfı, `IProductRepository` arayüzüne bağımlıdır ve bu arayüzü kullanarak ürün veritabanı işlemlerini gerçekleştirir.
