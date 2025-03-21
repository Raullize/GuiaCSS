<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=header"/>

# 🧑‍🔬 Animações e Transições ✨
Adicione movimentos suaves e interativos aos elementos da sua página.

## 🎭 Transições
Transições permitem animar suavemente a mudança de um valor para outro.

### ⚙️ Propriedades 
```css
.elemento {
    transition-property: all | background-color, transform, etc;
    transition-duration: 0.3s;
    transition-timing-function: ease | linear | ease-in | ease-out | ease-in-out | cubic-bezier(n,n,n,n);
    transition-delay: 0s;
    
    /* Shorthand */
    transition: property duration timing-function delay;
}
```

### 🔰 Exemplo Básico
```css
button {
    background-color: blue;
    transition: background-color 0.5s ease;
}

button:hover {
    background-color: coral;
}
```

### 🚀 Exemplo Avançado
```css
.card {
    transform: translateY(0);
    opacity: 0.8;
    box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    transition: 
        transform 0.3s ease-out,
        opacity 0.2s linear,
        box-shadow 0.3s ease-in;
}

.card:hover {
    transform: translateY(-10px);
    opacity: 1;
    box-shadow: 0 10px 20px rgba(0,0,0,0.3);
}
```

## 🎬 Animações
Animações permitem criar sequências mais complexas de mudanças.

### 🎞️ Keyframes e Propriedades
```css
@keyframes nomeAnimacao {
    from { /* propriedades iniciais */ }
    50% { /* propriedades intermediárias */ }
    to { /* propriedades finais */ }
}

.elemento {
    animation-name: nomeAnimacao;
    animation-duration: 2s;
    animation-timing-function: ease-in-out;
    animation-delay: 0s;
    animation-iteration-count: 1 | infinite;
    animation-direction: normal | reverse | alternate | alternate-reverse;
    animation-fill-mode: none | forwards | backwards | both;
    animation-play-state: running | paused;
    
    /* Shorthand */
    animation: name duration timing-function delay iteration-count direction fill-mode;
}
```

### 🔰 Exemplo Básico
```css
@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

.box {
    animation: fadeIn 1s ease-in-out;
}
```

### 🎯 Exemplos Avançados
```css
/* Animação de carregamento */
@keyframes rotate {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}

.loader {
    animation: rotate 1.5s linear infinite;
}

/* Animação de pulsação */
@keyframes pulse {
    0% { transform: scale(1); }
    50% { transform: scale(1.1); }
    100% { transform: scale(1); }
}

.heart {
    animation: pulse 1.5s ease-in-out infinite;
}

/* Múltiplas animações */
.notification {
    animation: 
        fadeIn 0.5s ease-out forwards,
        shake 0.5s ease-in-out 0.5s;
}
```

## ⚡ Dicas de Performance
- 🔄 Priorize animar as propriedades `transform` e `opacity` para melhor desempenho
- ⚠️ Evite animar propriedades que causam reflow (como `width`, `height`, `top`, `left`)
- 🔋 Use `will-change` com moderação para otimizar animações complexas

---

[🔙 Voltar ao índice principal](../README.md)

<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=footer"/>