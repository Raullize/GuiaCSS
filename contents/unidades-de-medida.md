<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=header"/>

# �� Unidades de Medida 📐

## 📌 Unidades Absolutas
Mantêm seu tamanho independente do dispositivo ou configuração:
- `px` (pixels): 1px = 1/96 de 1 polegada 🖥️
- `pt` (pontos): 1pt = 1/72 de 1 polegada 📄
- `pc` (picas): 1pc = 12pt 📝
- `cm` (centímetros): 1cm = ~38px 📏
- `mm` (milímetros): 1mm = ~4px 📊
- `in` (polegadas): 1in = 96px 📐

## 🔄 Unidades Relativas
Ajustam-se dinamicamente em relação a outros elementos:
- `em`: Relativo ao tamanho da fonte do elemento pai 🔤
- `rem`: Relativo ao tamanho da fonte do elemento raiz (html) 🌱
- `%`: Relativo ao elemento pai 💯
- `vw`: 1% da largura da viewport (janela do navegador) 🖥️
- `vh`: 1% da altura da viewport 🔍
- `vmin`: 1% da menor dimensão da viewport (largura ou altura) 🔽
- `vmax`: 1% da maior dimensão da viewport (largura ou altura) 🔼
- `fr`: Fração do espaço disponível (somente em Grid) 🧩
- `ch`: Largura do caractere "0" da fonte atual ⌨️

## 🤔 Quando Usar Cada Uma
- **Absolutas**: Quando o tamanho precisa ser exato independente do dispositivo (impressão, bordas finas) 🖨️
- **Relativas**: Para layouts responsivos e adaptáveis a diferentes dispositivos 📱💻🖥️

## 💡 Exemplos Práticos
```css
/* Layout responsivo */
.container {
    width: 90%; /* 90% da largura do elemento pai */
    max-width: 1200px; /* limite máximo absoluto */
    margin: 0 auto; /* centralizado */
}

/* Tipografia flexível */
html {
    font-size: 16px; /* tamanho base para cálculo de rem */
}

h1 {
    font-size: 2.5rem; /* 40px se o tamanho base for 16px */
}

p {
    font-size: 1rem; /* igual ao tamanho base */
    line-height: 1.5; /* 1.5x o tamanho da fonte */
}

/* Layout adaptativo */
.hero {
    height: 50vh; /* 50% da altura da viewport */
    padding: 2em; /* relativo ao tamanho da fonte do próprio elemento */
}

/* Componente dimensionado pela fonte */
.icon {
    width: 1.5ch; /* baseado na largura do caractere '0' */
    height: 1.5em; /* baseado na altura da fonte */
}
```

---

[🔙 Voltar ao índice principal](../README.md)

<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=footer"/>