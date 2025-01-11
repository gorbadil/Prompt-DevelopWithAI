# CSS ve UI Geliştirmede AI

**Örnek:**
"Bir düğme animasyonu tasarlayın."

**Kod:**

```css
.button {
  background-color: #007bff;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  transition: transform 0.2s ease-in-out;
}

.button:hover {
  transform: scale(1.1);
}
```

AI'den isteyin:

```
"Bu CSS'i React'te styled-components ile yeniden yaz."
```

**Çözüm:**

```javascript
import styled from "styled-components";

const Button = styled.button`
  background-color: #007bff;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  transition: transform 0.2s ease-in-out;

  &:hover {
    transform: scale(1.1);
  }
`;
```
