# Handling Events with React
---
### JSX vs HTML
1. JSX passes a function, HTML passes a string.

HTML
```html
<button onclick="showResult()">
  Show Result
</button>
```

JSX
```jsx
<button onclick={showResult}>
  Show Result
</button>
```

2. JSX can only use `e.preventDefault()`, HTML can also `return false;` for preventing default behavior.

HTML
```HTML
<a href="#" onclick="console.log("You clicked the link!"); return false">
  CLick me
</a>
```

JSX
```JSX
function LinkThatWantsToBeClicked() {
  function handleClick(e) {
    e.preventDefault();
    console.log("You clicked me!");
  }
  
  return (
    <a href="#" onClick={handleClick}>
      Click me
    <a>
  );
}
```

