<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=header"/>

# 📂 Como criar e usar um arquivo CSS
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

[🔙 Voltar ao índice principal](../README.md)

<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=2965F1&height=120&section=footer"/>