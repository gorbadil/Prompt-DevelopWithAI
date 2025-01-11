# Frontend Geliştirme ve Cursor AI: Pratik Örnekler

## React Projelerinde Cursor AI Kullanımı

**Örnek:**  
"Bir `TodoList` komponenti oluşturun ve Cursor AI'ye bir `TodoItem` alt komponenti eklemesini isteyin."

**Kod:**

```javascript
function TodoList() {
  const todos = ["React öğren", "Cursor AI'yi dene", "Proje tamamla"];
  return (
    <ul>
      {todos.map((todo, index) => (
        <TodoItem key={index} text={todo} />
      ))}
    </ul>
  );
}
```

**Prompt:**

```
Bu kodda eksik olan bir şey var. Cursor AI'den yardım alarak `TodoItem` komponentini oluşturun.
```

**Çözüm:**

```javascript
function TodoItem({ text }) {
  return <li>{text}</li>;
}
```
