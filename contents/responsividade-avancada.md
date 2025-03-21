<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=header"/>

# 📱 Responsividade Avançada 📲
Técnicas avançadas para criar layouts web que se adaptam perfeitamente a qualquer dispositivo.

## 📋 Media Queries
A base da responsividade, permitindo aplicar estilos específicos com base nas características do dispositivo:

```css
/* Estilos para dispositivos móveis (até 767px) */
@media (max-width: 767px) {
    .container {
        padding: 1rem;
    }
}

/* Tablets e dispositivos médios (768px - 1023px) */
@media (min-width: 768px) and (max-width: 1023px) {
    .container {
        padding: 2rem;
    }
}

/* Desktops (1024px e acima) */
@media (min-width: 1024px) {
    .container {
        padding: 3rem;
    }
}
```

### 🔍 Media Queries Avançadas
Além do tamanho da tela, você pode verificar outras características:

```css
/* Modo escuro */
@media (prefers-color-scheme: dark) {
    body {
        background-color: #121212;
        color: #f1f1f1;
    }
}

/* Dispositivos com tela de alta resolução (retina) */
@media (min-resolution: 2dppx) {
    .imagem {
        background-image: url('imagem@2x.png');
    }
}

/* Orientação do dispositivo */
@media (orientation: portrait) {
    .galeria {
        flex-direction: column;
    }
}
```

## ✨ Funções CSS Modernas

### 📊 Funções de Contenção: clamp(), min() e max()
```css
.texto-responsivo {
    /* clamp(mínimo, preferencial, máximo) */
    font-size: clamp(1rem, 4vw, 2.5rem);
    
    /* Define o valor mínimo entre as opções */
    width: min(90%, 1200px);
    
    /* Define o valor máximo entre as opções */
    margin-bottom: max(20px, 5vh);
}

.botao {
    /* Garante que o botão seja largo o suficiente para o texto, 
       mas não muito largo em telas grandes */
    width: clamp(150px, 50%, 300px);
    padding: clamp(0.5rem, 2vw, 1.5rem);
}
```

## 🧩 Container Queries
A evolução das media queries, permitindo que os elementos respondam ao tamanho do seu container, não da viewport:

```css
/* Define um contexto de consulta para o container */
.card-container {
    container-type: inline-size;
    container-name: card;
}

/* Estilos que respondem ao tamanho do container */
@container card (max-width: 400px) {
    .card-title {
        font-size: 1.2rem;
    }
    
    .card-details {
        display: none;
    }
}
```

## 🖼️ Imagens Responsivas

### 📸 Picture e srcset
```html
<picture>
    <source media="(max-width: 600px)" srcset="imagem-pequena.jpg">
    <source media="(max-width: 1200px)" srcset="imagem-media.jpg">
    <img src="imagem-grande.jpg" alt="Descrição da imagem">
</picture>
```

### 🎭 CSS para Imagens Responsivas
```css
.imagem-capa {
    width: 100%;
    height: 50vh;
    object-fit: cover;
    object-position: center;
}

.imagem-bg {
    background-image: url('imagem-desktop.jpg');
    
    @media (max-width: 768px) {
        background-image: url('imagem-mobile.jpg');
    }
}
```

## 🏗️ Layout Responsivo com Grid Areas
```css
.page-layout {
    display: grid;
    gap: 20px;
    grid-template-columns: 1fr 3fr 1fr;
    grid-template-areas: 
        "header header header"
        "sidebar content aside"
        "footer footer footer";
}

@media (max-width: 768px) {
    .page-layout {
        grid-template-columns: 1fr;
        grid-template-areas: 
            "header"
            "content"
            "sidebar"
            "aside"
            "footer";
    }
}
```

## 🔠 Tipografia Fluida
```css
h1 {
    /* Escala de 1.5rem (24px) para 3.5rem (56px) */
    font-size: clamp(1.5rem, 1rem + 4vw, 3.5rem);
    /* Espaçamento de linha proporcional */
    line-height: 1.1;
}

p {
    font-size: clamp(1rem, 0.8rem + 0.5vw, 1.25rem);
    line-height: 1.5;
}
```

## 💡 Boas Práticas

1. 📱 **Mobile-First**: Comece com estilos para dispositivos móveis e adicione complexidade para telas maiores
2. 🧪 **Teste em Dispositivos Reais**: Não confie apenas em emuladores ou redimensionamento do navegador
3. 📏 **Evite Breakpoints Fixos**: Deixe o conteúdo determinar onde os breakpoints devem estar
4. 📊 **Use Unidades Relativas**: Prefira `rem`, `em`, `%`, `vh`, `vw` em vez de pixels
5. 🔄 **Flexível, não Fluido**: Nem tudo precisa ser 100% fluido; às vezes limites (min/max) são melhores
6. ♿ **Considere a Acessibilidade**: Tamanhos de texto muito pequenos ou controles difíceis de tocar prejudicam a experiência

---

[🔙 Voltar ao índice principal](../README.md)

<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=footer"/>