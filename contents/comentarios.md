<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=header"/>

# 📝 Comentários 💬
Os comentários em CSS são úteis para organizar e documentar o código, facilitando a leitura e manutenção. Eles são ignorados pelo navegador durante a execução.

## 📋 Sintaxe de Comentários
```css
/* Este é um comentário simples em uma linha */

/*
 * Este é um comentário
 * em múltiplas linhas
 * com formatação padronizada
 */
```

## 🔍 Casos de Uso

### 📑 Documentação de Seções
```css
/* ========== CABEÇALHO ========== */
header {
    padding: 20px;
    background-color: #333;
}

/* ========== CONTEÚDO PRINCIPAL ========== */
main {
    min-height: 500px;
}

/* ========== RODAPÉ ========== */
footer {
    padding: 10px;
    background-color: #222;
}
```

### 🔍 Explicação de Propriedades
```css
.card {
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1); /* Sombra suave para elevação */
    transition: transform 0.3s ease; /* Animação ao passar o mouse */
    will-change: transform; /* Otimiza para animações */
}
```

### 👨‍💻 Anotações de Autor e Versionamento
```css
/**
 * Componente: Botão Principal
 * Autor: João Silva
 * Data: 15/04/2023
 * Versão: 1.2
 */
.btn-primary {
    /* ... */
}
```

### 🚫 Desabilitando Código Temporariamente
```css
.elemento {
    color: black;
    /* font-weight: bold; */
    /* 
    padding: 10px;
    margin: 20px;
    background-color: yellow;
    */
}
```

### 📌 TODOs e Fixmes
```css
/* TODO: Revisar estas cores para acessibilidade */
.botao {
    background-color: blue;
    color: white;
}

/* FIXME: Resolver problema no Safari */
.galeria {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
}
```

### 🌐 Compatibilidade com Navegadores
```css
.flexbox-container {
    display: -webkit-box; /* Safari antigo */
    display: -ms-flexbox; /* IE10 */
    display: flex; /* Navegadores modernos */
}
```

## 💡 Melhores Práticas

### ✅ Comentários Significativos
```css
/* BOM: Descreve o propósito */
.visually-hidden {
    position: absolute;
    width: 1px;
    height: 1px;
    overflow: hidden;
    clip: rect(0, 0, 0, 0);
    /* Esconde visualmente o elemento mas mantém acessível para leitores de tela */
}

/* EVITAR: Comentário óbvio demais */
.texto-vermelho {
    color: red; /* Define a cor como vermelho */
}
```

### 📋 Comentários para Organização de Código
```css
/* 1. RESET E BASE */
/* ... */

/* 2. TIPOGRAFIA */
/* ... */

/* 3. LAYOUT */
/* ... */

/* 4. COMPONENTES */
/* ... */

/* 5. UTILITÁRIOS */
/* ... */
```

### 👥 Documentação para Colaboração
```css
/* NOTA: A classe .container possui largura máxima de 1200px para manter consistência
 * Se você precisar de um container com largura total, use .container-fluid
 */
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 15px;
}
```

---

[🔙 Voltar ao índice principal](../README.md)

<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=footer"/>