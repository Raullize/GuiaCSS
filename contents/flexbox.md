<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=header"/>

# 📐 Flexbox 🔄
Modelo de layout flexível ideal para alinhamento e distribuição de espaço entre itens.

## 🧩 Propriedades do Container
```css
.container {
    display: flex; /* ou inline-flex */
    flex-direction: row | row-reverse | column | column-reverse;
    flex-wrap: nowrap | wrap | wrap-reverse;
    justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
    align-items: stretch | flex-start | flex-end | center | baseline;
    align-content: flex-start | flex-end | center | space-between | space-around | stretch;
    gap: 10px; /* espaçamento entre itens */
}
```

## 📦 Propriedades dos Itens
```css
.item {
    order: 0; /* ordem de exibição do item */
    flex-grow: 0; /* capacidade de crescer */
    flex-shrink: 1; /* capacidade de encolher */
    flex-basis: auto; /* tamanho inicial */
    align-self: auto | flex-start | flex-end | center | baseline | stretch;
}
```

## ✨ Exemplo Prático
```css
.gallery {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 16px;
}

.gallery-item {
    flex: 1 0 300px; /* shorthand para grow, shrink e basis */
}
```

---

[🔙 Voltar ao índice principal](../README.md)

<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=footer"/>