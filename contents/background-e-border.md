<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=header"/>

# 🖼️ Background e Border 🧩
Propriedades essenciais para decorar e delimitar elementos HTML.

## 🎨 Backgrounds

### 🎭 Background Color
```css
.elemento {
    background-color: #3498db;
    background-color: rgb(52, 152, 219);
    background-color: rgba(52, 152, 219, 0.5); /* Com transparência */
}
```

### 🌄 Background Image
```css
.elemento {
    /* Imagem simples */
    background-image: url('imagem.jpg');
    
    /* Múltiplas imagens (em camadas, da mais próxima para a mais distante) */
    background-image: 
        url('foreground.png'),
        url('middle.png'),
        url('background.jpg');
    
    /* Gradientes */
    background-image: linear-gradient(to right, #3498db, #2ecc71);
    background-image: radial-gradient(circle, #3498db, #2ecc71);
}
```

### 🎛️ Controle de Background
```css
.elemento {
    /* Tamanho do background */
    background-size: cover; /* Cobre todo o elemento */
    background-size: contain; /* Contido no elemento */
    background-size: 200px 100px; /* Largura e altura específicas */
    background-size: 50% auto; /* 50% da largura, altura proporcional */
    
    /* Posição do background */
    background-position: center;
    background-position: top right;
    background-position: 25% 75%;
    
    /* Repetição do background */
    background-repeat: no-repeat;
    background-repeat: repeat-x; /* Repete apenas horizontalmente */
    background-repeat: space; /* Repete sem cortar as imagens */
    
    /* Fixar durante a rolagem */
    background-attachment: fixed;
    background-attachment: scroll; /* padrão */
    background-attachment: local; /* rola com o conteúdo */
    
    /* Área de pintura do background */
    background-clip: border-box; /* padrão, inclui a borda */
    background-clip: padding-box; /* exclui a borda */
    background-clip: content-box; /* apenas o conteúdo */
    background-clip: text; /* apenas o texto (requer color: transparent) */
    
    /* Origem do posicionamento */
    background-origin: border-box;
    background-origin: padding-box; /* padrão */
    background-origin: content-box;
}
```

### 🧰 Shorthand de Background
```css
.elemento {
    /* cor | imagem | posição / tamanho | repetição | attachment | origin | clip */
    background: #3498db url('imagem.jpg') center / cover no-repeat fixed;
}
```

## 📏 Borders

### 📐 Propriedades de Border
```css
.elemento {
    /* Espessura */
    border-width: 2px;
    border-width: thin | medium | thick;
    border-width: 2px 5px 1px 3px; /* topo | direita | baixo | esquerda */
    
    /* Estilo */
    border-style: solid;
    border-style: dotted | dashed | double | groove | ridge | inset | outset | none | hidden;
    border-style: solid dashed dotted double; /* topo | direita | baixo | esquerda */
    
    /* Cor */
    border-color: black;
    border-color: #000;
    border-color: rgb(0, 0, 0);
    border-color: red blue green yellow; /* topo | direita | baixo | esquerda */
}
```

### 🔄 Shorthand de Border
```css
.elemento {
    /* largura | estilo | cor */
    border: 2px solid black;
    
    /* Lados específicos */
    border-top: 3px dashed blue;
    border-right: 2px solid red;
    border-bottom: 4px double green;
    border-left: 1px dotted orange;
}
```

### 🌀 Border Radius
Cria cantos arredondados:
```css
.elemento {
    /* Igual para todos os cantos */
    border-radius: 10px;
    
    /* Cantos específicos (superior-esquerdo | superior-direito | inferior-direito | inferior-esquerdo) */
    border-radius: 10px 20px 30px 40px;
    
    /* Elíptico (horizontal / vertical) para cada canto */
    border-radius: 10px / 20px;
    border-radius: 10px 20px 30px 40px / 5px 10px 15px 20px;
    
    /* Círculo perfeito */
    border-radius: 50%;
}
```

### 🖼️ Border Image
```css
.elemento {
    border-image-source: url('borda.png');
    border-image-slice: 27 27 27 27;
    border-image-width: 20px;
    border-image-outset: 10px;
    border-image-repeat: stretch | repeat | round | space;
    
    /* Shorthand */
    border-image: url('borda.png') 27 / 20px / 10px round;
}
```

## ✨ Efeitos Avançados

### 🌟 Box Shadow
```css
.elemento {
    /* deslocamento-x | deslocamento-y | desfoque | expansão | cor */
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.2);
    
    /* Múltiplas sombras */
    box-shadow: 
        0 0 10px rgba(0, 0, 0, 0.1),
        0 0 20px rgba(0, 0, 0, 0.1),
        0 0 30px rgba(0, 0, 0, 0.1);
    
    /* Sombra interna */
    box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.5);
}
```

### 📌 Outline
Similar à borda, mas não afeta o layout:
```css
.elemento {
    outline: 2px solid red;
    outline-offset: 5px; /* Espaço entre o elemento e o outline */
}
```

### 🎁 Combinando Efeitos
```css
.cartao {
    background: #fff;
    border: 1px solid rgba(0, 0, 0, 0.1);
    border-radius: 8px;
    box-shadow: 
        0 2px 4px rgba(0, 0, 0, 0.05),
        0 8px 16px rgba(0, 0, 0, 0.1);
}

.cartao:hover {
    transform: translateY(-5px);
    box-shadow: 
        0 10px 20px rgba(0, 0, 0, 0.15),
        0 15px 30px rgba(0, 0, 0, 0.2);
    border-color: rgba(0, 0, 0, 0.15);
}
```

---

[🔙 Voltar ao índice principal](../README.md)

<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=footer"/>