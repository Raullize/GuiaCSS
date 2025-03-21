<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=header"/>

# 📊 Grid Layout 🏗️
Sistema CSS Grid para criar layouts em duas dimensões com linhas e colunas.

## 🔲 Propriedades do Container
```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr) | 200px auto 1fr;
    grid-template-rows: 100px 200px | repeat(2, minmax(100px, auto));
    grid-template-areas: "header header" "sidebar content" "footer footer";
    grid-column-gap: 10px; /* espaço entre colunas */
    grid-row-gap: 15px; /* espaço entre linhas */
    gap: 10px 15px; /* shorthand para row-gap e column-gap */
    justify-items: start | end | center | stretch;
    align-items: start | end | center | stretch;
    justify-content: start | end | center | stretch | space-around | space-between | space-evenly;
    align-content: start | end | center | stretch | space-around | space-between | space-evenly;
}
```

## 🧩 Propriedades dos Itens
```css
.item {
    grid-column: 1 / 3; /* início / fim */
    grid-row: 2 / 4;
    grid-area: header; /* nome definido no grid-template-areas */
    justify-self: start | end | center | stretch;
    align-self: start | end | center | stretch;
}
```

## 🖥️ Exemplo Prático: Layout de Página
```css
.page-layout {
    display: grid;
    grid-template-columns: 1fr 3fr;
    grid-template-rows: auto 1fr auto;
    grid-template-areas: 
        "header header"
        "sidebar content"
        "footer footer";
    gap: 16px;
    min-height: 100vh;
}

.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.content { grid-area: content; }
.footer { grid-area: footer; }
```

---

[🔙 Voltar ao índice principal](../README.md)

<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=footer"/>