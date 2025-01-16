# Guia CSS 🌈

Bem-vindo ao **GuiaCSS**! Este guia tem como objetivo oferecer uma introdução abrangente ao CSS para iniciantes e até mesmo para aqueles que já possuem experiência intermediária e desejam relembrar conceitos fundamentais. Aqui você encontrará conceitos, exemplos práticos e dicas úteis. Vamos lá! 🚀

---

## O que é CSS? 🤔
O **CSS (Cascading Style Sheets)** é uma linguagem utilizada para estilizar páginas HTML, permitindo definir cores, espaçamentos, fontes, layouts e muito mais. Ele trabalha em conjunto com o HTML para criar interfaces visuais atraentes.

---

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

---

## Conceitos Iniciais 🌟

### 1. Cores 🎨
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

### 2. Background e Border 🖼️
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
### 3. Comentários 📝
Os comentários em CSS são úteis para organizar e documentar o código, facilitando a leitura e manutenção. Eles são ignorados pelo navegador durante a execução.

- Para adicionar um comentário, use /* no início e */ no final.
- Comentários podem ser usados para explicar regras, marcar seções ou desativar partes do código temporariamente.

Exemplo:
```css
/* Este é um comentário explicativo */
body {
    background-color: #f0f0f0; /* Define a cor de fundo da página */
}

/* Desativando temporariamente uma regra */
/* h1 {
    color: red;
} */
```

### 4. Box Model 📦
O CSS utiliza o **box model** para determinar como os elementos são exibidos na tela. Ele é composto por:
- **Content**: O conteúdo real.
- **Padding**: Espaço interno entre o conteúdo e a borda.
- **Border**: A borda do elemento.
- **Margin**: Espaço externo entre o elemento e outros.

Exemplo:
```css
div {
    width: 200px;
    padding: 10px;
    border: 5px solid black;
    margin: 20px;
}
```

### 5. Display 🖥️
Controla como os elementos são exibidos:
- `none`: Oculta o elemento.
- `block`: O elemento ocupa toda a largura disponível.
- `inline`: O elemento ocupa apenas o espaço do seu conteúdo.
- `inline-block`: Comporta-se como `inline`, mas permite aplicar propriedades de largura e altura.

Exemplo:
```css
div {
    display: inline-block;
    width: 100px;
    height: 100px;
    background-color: coral;
}
```

### 6. Seletores Básicos 🎯
- **Universal**: `*` seleciona todos os elementos.
- **Tag**: `p` seleciona todas as tags `<p>`.
- **Classe**: `.minha-classe` seleciona elementos com essa classe.
- **ID**: `#meu-id` seleciona o elemento com esse ID.

Exemplo:
```css
p {
    color: green;
}

.minha-classe {
    font-size: 16px;
}

#meu-id {
    text-align: center;
}
```

---

## Tópicos Intermediários 🚀

### 7. Textos e Fontes ✍️
Controle estilos como:
- **Fonte**: `font-family`
- **Tamanho**: `font-size`
- **Estilo**: `font-style`
- **Peso**: `font-weight`
- **Alinhamento**: `text-align`

Exemplo:
```css
h1 {
    font-family: 'Arial', sans-serif;
    font-size: 24px;
    font-weight: bold;
    text-align: center;
}
```

### 8. Unidades de Medida 📏
- **Relativas**: `em`, `rem`, `%`.
- **Fixas**: `px`, `cm`, `mm`.

Exemplo:
```css
p {
    font-size: 1.2em;
    margin: 10px;
}
```

### 9. Herança 📚
Algumas propriedades, como `color` e `font`, são herdadas automaticamente de elementos ancestrais. Isso significa que elementos filhos adotam essas propriedades caso elas não sejam definidas explicitamente. No entanto, nem todas as propriedades são herdadas por padrão.

Exemplo:
```css
body {
    color: black; /* Essa cor é herdada pelos elementos filhos */
}

h1 {
    font-size: 24px; /* Não herdado, pois font-size não é uma propriedade herdável */
}
```
Se você quiser que uma propriedade não herdável seja aplicada a todos os elementos filhos, é possível usar `inherit`:

```css
p {
    font-size: inherit; /* Herda o tamanho de fonte do elemento pai */
}
```

### 10. Especificidade 📊
A especificidade determina qual regra CSS será aplicada quando há conflitos entre seletores. As regras seguem a seguinte prioridade:
1. Estilos inline (atributo `style` no HTML)
2. IDs (`#id`)
3. Classes, pseudo-classes e atributos (`.classe`, `:hover`, `[atributo]`)
4. Elementos e pseudo-elementos (`div`, `h1`, `::before`)

Exemplo:
```css
body {
    color: black;
}

h1 {
    color: blue; /* Sobrescreve o color herdado do body */
}

#titulo {
    color: red; /* Sobrescreve o color definido pelo seletor h1 */
}
```
> **Dica**: Evite usar IDs para estilização sempre que possível, pois eles têm alta especificidade e podem dificultar a manutenção do código.

### 11. Seletores Avançados 🔍
Os seletores avançados permitem que você aplique estilos com maior precisão. Aqui estão alguns exemplos comuns:

#### Filho Direto (`>`)
Aplica estilos apenas aos elementos que são filhos diretos de outro elemento.
```css
ul > li {
    color: red; /* Apenas os li que são filhos diretos de ul serão afetados */
}
```

#### Irmão Adjacente (`+`)
Aplica estilos ao elemento que é imediatamente seguinte a outro elemento.
```css
h1 + p {
    font-style: italic; /* Aplica apenas ao primeiro parágrafo após h1 */
}
```

#### Irmão Geral (`~`)
Aplica estilos a todos os elementos que são irmãos posteriores de outro elemento.
```css
h1 ~ p {
    color: gray; /* Aplica a todos os parágrafos após h1 */
}
```

> **Nota**: Combine seletores para criar regras ainda mais específicas e poderosas. Por exemplo: `ul > li:first-child` estiliza apenas o primeiro item de uma lista.

### 12. Variáveis 🎛️
Defina valores reutilizáveis com `var`:
```css
:root {
    --primary-color: #3498db;
    --font-size: 16px;
}

h1 {
    color: var(--primary-color);
    font-size: var(--font-size);
}
```

### 13. Básico de Responsividade 📱
Use media queries para adaptar o layout a diferentes tamanhos de tela:
```css
@media (max-width: 600px) {
    body {
        font-size: 14px;
    }
}
```

## Links úteis 🔗
- [MDN Web Docs - CSS](https://developer.mozilla.org/pt-BR/docs/Web/CSS)
- [CSS Tricks](https://css-tricks.com/)
- [Can I Use](https://caniuse.com/)

---

Esperamos que este guia tenha sido útil para você! 😄 Continuaremos expandindo com mais dicas e exemplos.

🎯 Contribuições são bem-vindas! Caso queira adicionar algo, faça um pull request no repositório.

