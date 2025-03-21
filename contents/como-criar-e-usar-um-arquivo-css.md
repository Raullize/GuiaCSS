<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=header"/>

# 📂 Como criar e usar um arquivo CSS 📝

## 🔄 Métodos de Inclusão CSS

### 1️⃣ CSS Inline
Adicionado diretamente ao elemento HTML usando o atributo `style`:
```html
<p style="color: red; font-size: 20px; font-weight: bold;">
    Este texto tem estilo inline.
</p>
```
**✅ Vantagens**: Aplicação imediata; prioridade alta.  
**⚠️ Desvantagens**: Difícil manutenção; mistura conteúdo com estilo; não reutilizável.

### 2️⃣ CSS Interno (Internal)
Definido no cabeçalho do documento HTML usando a tag `<style>`:
```html
<head>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
        }
        
        h1 {
            color: navy;
            text-align: center;
        }
        
        p {
            color: #555;
            line-height: 1.6;
        }
    </style>
</head>
```
**✅ Vantagens**: Não precisa de arquivo externo; carrega com a página.  
**⚠️ Desvantagens**: Aumenta o tamanho do HTML; não é reutilizável em outras páginas; dificulta a manutenção em projetos grandes.

### 3️⃣ CSS Externo (External)
Criado em um arquivo separado com extensão `.css` e vinculado ao HTML:

#### 📄 Criando o arquivo CSS (styles.css):
```css
/* Reset básico */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Estilo geral */
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: #333;
    background-color: #fff;
}

/* Tipografia */
h1, h2, h3 {
    margin-bottom: 20px;
    color: #2965F1;
}

p {
    margin-bottom: 15px;
}

/* Layout */
.container {
    width: 80%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 15px;
}
```

#### 🔗 Vinculando o CSS ao HTML:
```html
<head>
    <!-- Método padrão -->
    <link rel="stylesheet" href="styles.css">
    
    <!-- Com atributos adicionais -->
    <link rel="stylesheet" href="print.css" media="print">
    
    <!-- Carregamento alternativo -->
    <link rel="stylesheet" href="styles.css" media="all" crossorigin="anonymous">
    
    <!-- Importação via @import (dentro de um elemento style) -->
    <style>
        @import url('styles.css');
    </style>
    
    <!-- Usar defer para não bloquear renderização (moderno) -->
    <link rel="stylesheet" href="styles.css" media="print" onload="this.media='all'">
</head>
```
**✅ Vantagens**: Melhor manutenção; cacheável; reusável em várias páginas; separação de responsabilidades.  
**⚠️ Desvantagens**: Requisição HTTP adicional (mitigada com HTTP/2).

## 📁 Organização e Estrutura de Arquivos CSS

### 📋 Estrutura Básica
```
projeto/
├── index.html
├── css/
│   ├── styles.css
│   ├── reset.css
│   └── typography.css
├── js/
└── img/
```

### 🧩 Divisão por Funcionalidade
```
projeto/
├── css/
│   ├── main.css           # Importa todos os demais arquivos
│   ├── reset.css          # Normalização entre navegadores
│   ├── typography.css     # Regras de texto e fontes
│   ├── layout.css         # Estrutura, grid, containers
│   ├── components.css     # Componentes reutilizáveis
│   └── utilities.css      # Classes utilitárias
```

### 🏗️ Divisão por Metodologia (BEM, SMACSS, ITCSS, etc)
```
projeto/
├── css/
│   ├── settings/          # Variáveis, configurações
│   ├── tools/             # Mixins, funções
│   ├── generic/           # Reset, normalizações
│   ├── elements/          # HTML base, sem classes
│   ├── objects/           # Estruturas layout sem estilo
│   ├── components/        # UI identificável (botões, cards)
│   └── utilities/         # Classes com alta especificidade
```

## 📚 Metodologias de Organização CSS

### 🧱 BEM (Block, Element, Modifier)
```css
/* Bloco */
.card { }

/* Elemento (componente do bloco) */
.card__title { }
.card__image { }

/* Modificador (variações do bloco ou elemento) */
.card--featured { }
.card__title--large { }
```

### 🔄 SMACSS (Scalable and Modular Architecture for CSS)
Divide CSS em cinco categorias:
1. 🌱 **Base** - Elementos HTML padrão
2. 🏗️ **Layout** - Estruturas principais da página
3. 🧩 **Module** - Componentes reutilizáveis
4. 🔄 **State** - Estados dos elementos (ativo, hover, etc)
5. 🎨 **Theme** - Alterações visuais (cores, fontes)

### 🔺 ITCSS (Inverted Triangle CSS)
Organiza CSS em camadas de especificidade crescente:
1. ⚙️ **Settings** - Variáveis
2. 🛠️ **Tools** - Mixins, funções
3. 🧹 **Generic** - Resets
4. 📝 **Elements** - HTML base
5. 📦 **Objects** - Classes não cosmétcas
6. 🧩 **Components** - Componentes designados
7. 🔧 **Utilities** - Helper classes

## 📋 Ordem de Importação
Para evitar conflitos, mantenha uma ordem lógica:
```html
<head>
    <!-- 1. Reset/Normalize (zera estilos nativos) -->
    <link rel="stylesheet" href="css/normalize.css">
    
    <!-- 2. Bibliotecas de terceiros (frameworks) -->
    <link rel="stylesheet" href="css/bootstrap.min.css">
    
    <!-- 3. Estilos globais da aplicação -->
    <link rel="stylesheet" href="css/global.css">
    
    <!-- 4. Estilos específicos de componentes -->
    <link rel="stylesheet" href="css/components.css">
    
    <!-- 5. Estilos específicos de páginas -->
    <link rel="stylesheet" href="css/home.css">
</head>
```

## 💡 Boas Práticas

1. 📤 **Prefira CSS Externo** para melhor manutenção e reutilização
2. 📦 **Minimize o número de arquivos** em produção (use bundlers)
3. 🔄 **Utilize pré-processadores** como SASS/SCSS para projetos maiores
4. 📚 **Adote uma metodologia** de organização consistente
5. 🎨 **Use variáveis CSS** para cores, fontes e valores reutilizáveis
6. ⚠️ **Evite especificidade excessiva** que dificulta sobrescrever regras
7. 📝 **Comente seu código** para facilitar a manutenção
8. ⚡ **Otimize para produção** minificando o CSS

---

[🔙 Voltar ao índice principal](../README.md)

<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=footer"/>