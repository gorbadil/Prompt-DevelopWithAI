# Performans Optimizasyonu ve Refactoring

**Örnek:**
"Bir React uygulamasında gereksiz renderları azaltın."

**Kod:**

```javascript
import React, { memo } from "react";

const TodoItem = memo(({ text }) => {
  console.log("Rendered:", text);
  return <li>{text}</li>;
});

export default TodoItem;
```

Cursor AI'den isteyin:

```
"Memo kullanılmadan önce ve sonra kodun performans farklarını açıkla."
```

**Çözüm:**

```javascript
import React from "react";

const TodoItem = ({ text }) => {
  console.log("Rendered:", text);
  return <li>{text}</li>;
};

export default TodoItem;
```

**Açıklama:**

`React.memo` kullanımı, komponentin sadece gerekli durumlarda yeniden render edilmesini sağlar. Bu örnekte `TodoItem` komponenti, `React.memo` ile sarmalanmıştır. Bu sayede `TodoItem` komponenti, `text` prop'unun değişmediği durumlarda yeniden render edilmez. `React.memo` kullanımı, performansı artırırken gereksiz renderları azaltır.
