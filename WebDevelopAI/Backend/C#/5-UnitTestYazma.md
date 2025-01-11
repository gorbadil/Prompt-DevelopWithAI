# Unit Test Yazma

**Örnek:**
"Bir repository için basit bir birim testi yazın."

**Kod:**

```csharp
[TestClass]
public class ProductRepositoryTests
{
    [TestMethod]
    public void AddProduct_ShouldAddProductToList()
    {
        // Arrange
        var repository = new ProductRepository();
        var product = new Product { Id = 1, Name = "Test Product" };

        // Act
        repository.AddProduct(product);

        // Assert
        var result = repository.GetProductById(1);
        Assert.IsNotNull(result);
        Assert.AreEqual("Test Product", result.Name);
    }
}
```

AI'den isteyin:

```
"Bu teste daha fazla senaryo ekleyerek kapsamını genişlet."
```

**Çıktı:**

```csharp
[TestClass]
public class ProductRepositoryTests
{
    [TestMethod]
    public void AddProduct_ShouldAddProductToList()
    {
        // Arrange
        var repository = new ProductRepository();
        var product = new Product { Id = 1, Name = "Test Product" };

        // Act
        repository.AddProduct(product);

        // Assert
        var result = repository.GetProductById(1);
        Assert.IsNotNull(result);
        Assert.AreEqual("Test Product", result.Name);
    }

    [TestMethod]

    public void AddProduct_ShouldNotAddProductWithSameId()
    {
        // Arrange
        var repository = new ProductRepository();
        var product = new Product { Id = 1, Name = "Test Product" };
        repository.AddProduct(product);

        // Act
        var newProduct = new Product { Id = 1, Name = "New Product" };
        repository.AddProduct(newProduct);

        // Assert
        var result = repository.GetProductById(1);

        Assert.IsNotNull(result);
        Assert.AreEqual("Test Product", result.Name);
    }
}
```

**Açıklama:**

Bu test, ProductRepository sınıfının AddProduct metodu için bir birim testtir. Test, bir ürün eklenip eklenmediğini doğrular. Test, Arrange, Act ve Assert bölümlerinden oluşur. Arrange bölümünde, ProductRepository sınıfı ve bir ürün örneği oluşturulur. Act bölümünde, AddProduct metodu çağrılır ve bir ürün eklenir. Assert bölümünde, eklenen ürünün doğru eklenip eklenmediği doğrulanır.
