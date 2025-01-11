# React Router ile Çalışma

**Örnek:**
"Bir blog uygulaması için dinamik rotalar oluşturun."

**Kod:**

```javascript
import { BrowserRouter as Router, Routes, Route } from "react-router-dom";

function App() {
  return (
    <Router>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/blog/:id" element={<BlogPost />} />
      </Routes>
    </Router>
  );
}
```

Cursor AI'den isteyin:

```
"BlogPost komponentinde useParams kullanarak id parametresini yakala ve bir yazı başlığı göster."
```

**Çözüm:**

```javascript
import { useParams } from "react-router-dom";

function BlogPost() {
  const { id } = useParams();
  return <h1>Yazı #{id}</h1>;

  // Diğer içerikler...
}
```
