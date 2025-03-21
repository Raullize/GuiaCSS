<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=header"/>

# 🎨 Cores 🌈
As cores são fundamentais para o design de qualquer interface. O CSS oferece várias maneiras de definir cores.

## 🎭 Formatos de Cores

### 📝 Nomes de Cores
CSS suporta [148 nomes de cores pré-definidos](https://developer.mozilla.org/pt-BR/docs/Web/CSS/color_value):
```css
.elemento {
    color: red;
    background-color: skyblue;
    border: 1px solid black;
}
```

### 📊 Hexadecimal (#RRGGBB)
Cores em formato hexadecimal, com 6 dígitos (ou 3 como abreviação):
```css
.elemento {
    color: #FF0000; /* vermelho */
    background-color: #00F; /* azul (abreviado de #0000FF) */
    border-color: #333; /* cinza escuro */
}
```

### 🖌️ RGB e RGBA
Valores Red, Green, Blue (0-255) e Alpha (0-1):
```css
.elemento {
    color: rgb(255, 0, 0); /* vermelho */
    background-color: rgba(0, 0, 255, 0.5); /* azul com 50% de transparência */
}
```

### 🔄 HSL e HSLA
Hue (0-360), Saturation (0-100%), Lightness (0-100%) e Alpha (0-1):
```css
.elemento {
    color: hsl(0, 100%, 50%); /* vermelho */
    background-color: hsla(240, 100%, 50%, 0.5); /* azul com 50% de transparência */
}
```

### ✨ Modern Syntax (CSS Color Module Level 4)
Sintaxe moderna de cores com canais alfa:
```css
.elemento {
    color: rgb(255 0 0); /* sem vírgulas */
    background-color: rgb(0 0 255 / 50%); /* alfa com notação de barra */
}
```

## 🧩 Variáveis de Cores (Custom Properties)
Use variáveis CSS para criar um sistema de cores consistente:
```css
:root {
    --cor-primaria: #2965F1;
    --cor-secundaria: #FFC700;
    --cor-texto: #333;
    --cor-background: #f9f9f9;
    --cor-acento: #FF5733;
}

.botao-primario {
    background-color: var(--cor-primaria);
    color: white;
}

.botao-secundario {
    background-color: var(--cor-secundaria);
    color: var(--cor-texto);
}
```

## 🔮 Funções de Cores
CSS oferece funções para manipular cores:
```css
.elemento {
    /* Clarear uma cor em 15% */
    background-color: color-mix(in srgb, var(--cor-primaria), white 15%);
    
    /* Escurecer uma cor em 10% */
    border-color: color-mix(in srgb, var(--cor-primaria), black 10%);
    
    /* Inversão de cores */
    filter: invert(100%);
    
    /* Transparência */
    background-color: color-mix(in srgb, var(--cor-primaria) 80%, transparent);
}
```

## 🌊 Gradientes
Crie transições suaves entre cores:
```css
.gradiente-linear {
    background: linear-gradient(to right, #2965F1, #FFC700);
}

.gradiente-radial {
    background: radial-gradient(circle, #2965F1, transparent);
}

.gradiente-conico {
    background: conic-gradient(from 45deg, #2965F1, #FFC700, #FF5733, #2965F1);
}

.gradiente-multi-step {
    background: linear-gradient(to bottom, 
        #2965F1 0%, 
        #83A4E8 30%, 
        #FFC700 70%, 
        #FF5733 100%);
}
```

## 🎯 Esquemas de Cores
Algumas estratégias comuns para criar esquemas de cores harmonizados:
- 🔵 **Monocromático**: Várias tonalidades da mesma cor
- 🔶 **Análogo**: Cores adjacentes na roda de cores
- 🔄 **Complementar**: Cores opostas na roda de cores
- 🔻 **Triádico**: Três cores equidistantes na roda de cores

---

[🔙 Voltar ao índice principal](../README.md)

<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=footer"/>