<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=180&section=header&text=GuiaCSS&fontSize=30&fontColor=fff&animation=twinkling&fontAlignY=35"/>

# 🎨 GuiaCSS

Bem-vindo ao **GuiaCSS**! Este guia tem como objetivo oferecer uma introdução abrangente ao CSS para iniciantes e até mesmo para aqueles que já possuem experiência intermediária e desejam relembrar conceitos fundamentais. Aqui você encontrará conceitos, exemplos práticos e dicas úteis. Vamos lá! 🚀

## O que é CSS? 🤔
O **CSS (Cascading Style Sheets)** é uma linguagem utilizada para estilizar páginas HTML, permitindo definir cores, espaçamentos, fontes, layouts e muito mais. Ele trabalha em conjunto com o HTML para criar interfaces visuais atraentes.

## Como criar e usar um arquivo CSS 📂
1. **Inline CSS**: Adicione estilos diretamente no elemento HTML.
   ```html
   <p style="color: red; font-size: 20px;">Texto com estilo inline</p>
   ```
2. **CSS Interno**: Adicione um bloco de estilo dentro da tag `<style>` no cabeçalho do HTML.
   ```html
   <style>
       p {
           color: blue;
           font-size: 18px;
       }
   </style>
   ```
3. **CSS Externo**: Crie um arquivo separado (`styles.css`) e linke-o ao HTML usando a tag `<link>`.
   ```html
   <link rel="stylesheet" href="styles.css">
   ```
   Arquivo `styles.css`:
   ```css
   body {
       font-family: Arial, sans-serif;
       background-color: #f0f0f0;
   }
   ```

## Conceitos Iniciais e Intermediários 🌟

### Cores 🎨
Você pode definir cores usando:
- **Nomes de cores**: `red`, `blue`, `green`.
- **Hexadecimal**: `#FF5733`.
- **RGB**: `rgb(255, 87, 51)`.
- **HSL**: `hsl(10, 100%, 50%)`.

Exemplo:
```css
h1 {
    color: #FF5733;
    background-color: rgb(240, 240, 240);
}
```

### Background e Border 🖼️
- **Background** define a cor ou imagem de fundo de um elemento.
- **Border** adiciona bordas ao redor do elemento.

Exemplo:
```css
div {
    background-color: lightblue;
    border: 2px solid black;
    border-radius: 5px;
}
```

### Comentários 📝
Os comentários em CSS são úteis para organizar e documentar o código, facilitando a leitura e manutenção. Eles são ignorados pelo navegador durante a execução.

Exemplo:
```css
/* Este é um comentário explicativo */
body {
    background-color: #f0f0f0; /* Define a cor de fundo da página */
}
```

### 📐 Unidades de Medida
- **Absolutas**: `px`, `cm`, `mm`, `in` (não se ajustam ao tamanho da tela).
- **Relativas**: `em`, `rem`, `%`, `vw`, `vh`, `vmin`, `vmax` (se ajustam dinamicamente).

Exemplo:
```css
.container {
    width: 80vw; /* 80% da largura da tela */
    font-size: 1.5rem; /* 1.5 vezes o tamanho da fonte raiz */
}
```

### 📐 Flexbox
Modelo de layout flexível ideal para alinhamento e distribuição de espaço.

Exemplo básico:
```css
.container {
    display: flex;
    justify-content: center; /* Alinha no eixo principal */
    align-items: center; /* Alinha no eixo cruzado */
}
```

### 📊 Grid Layout
Sistema CSS Grid para criar layouts em duas dimensões.

Exemplo básico:
```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
}
```

### 🧑‍🔬 Animações e Transições
Adicione movimentos suaves aos elementos.

Exemplo de transição:
```css
button {
    transition: background-color 0.5s ease;
}

button:hover {
    background-color: coral;
}
```

Exemplo de animação:
```css
@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

.box {
    animation: fadeIn 1s ease-in-out;
}
```

### 📱 Responsividade Avançada
Técnicas como `clamp()`, `min()`, `max()` para adaptar elementos ao tamanho da tela.

Exemplo com `clamp()`:
```css
h1 {
    font-size: clamp(1rem, 2.5vw, 3rem);
}
```

## Links úteis 🔗
- [MDN Web Docs - CSS](https://developer.mozilla.org/pt-BR/docs/Web/CSS)
- [CSS Tricks](https://css-tricks.com/)
- [Can I Use](https://caniuse.com/)

---

Esperamos que este guia tenha sido útil para você! 😄 Continuaremos expandindo com mais dicas e exemplos.

🎯 Contribuições são bem-vindas! Caso queira adicionar algo, faça um pull request no repositório.

<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=footer"/>
