## Gabarito

1. Complete o seguinte código com a `tag` usada para determinar o *viewport* e adicione ao seu arquivo `index.html`
   
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

2. Complete o código com o seletor que define o tamanho da unidade relativa `rem` dentro do arquivo `styles.css`
   
   ```css
   html {
       font-size: 24px;
   }
   ```

3. Complete o código com uma *media query* que aplique a regra de estilo em **telas** com **largura de até** `768px`
   
   ```css
   @media screen and (max-width : 768px) {
       p {
           font-size: 16px
       }
   }
   ```

4. Complete o código para fazer as classes `left` e `right` ocuparem `100%` da largura em telas **maiores** que `639px` de largura e **menores** que `801px` de largura.
   
   ```css
   @media screen and (min-width: 640px) and (max-width: 800px) {
    .left, .right {
      width: 100%;
    }
   }
   ```

5. **BÔNUS** - Crie uma regra que torne o `background-color` de todos os elementos branco somente quando o conteúdo for para impressão.
   
   ```css
   @media print {
       * {
           background-color: white;
       }
   }
   ```

___
