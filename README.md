CSS Responsivo

# CSS Responsivo

Em poucas palavras, "Responsividade" é a habilidade de uma página web adaptar sua aparência e _layout_ para promover uma experiência de usuário agradável independente do tamanho da tela do dispositivo. Desenvolver com esse conceito é chamado (RWD) Web Design Responsivo e visa atender os diversos tamanhos e resoluções encontrados nas telas de dispositívos.

## O que vamos aprender?

* A importância de construir páginas web responsivas.

* Como construir páginas web modernas e responsivas usando HTML e CSS.

* Configurar corretamente o _viewport_.

* Criar regras CSS que são aplicadas dependendo do tamanho da tela do dispositivo.

* A diferença entre responsividade e adaptabilidade.

## Por que isso é importante?

No início da _internet_, as pessoas acessavam a rede com seu computador pessoal, conhecido como PC. Mas no final dos anos 2000 com o surgimento dos *smartphones* teve início uma nova era para a internet. 

Pode ser que você deixe de lado seu computador pessoal pela praticidade do seu *smartphone*. 

Pode ser que você prefira acessar a internet através do seu _smartphone_ ao invés de usar um computador de mesa ou _notebook_. A praticidade que os _smartphones_ trouxeram causou muitas mudanças. Em muitos *sites* se têm percebido um aumento no acesso através de aparelhos portáteis na mesma proporção que se têm notado a diminuição do acesso através de PCs.

![Mission: Impossible | Paramount Pictures](./mission_impossible_-pc.jpg)

**Mission: Impossible | Paramount Pictures**

------

Imagine você tirando seu _smartphone_ do bolso para navegar na internet. Então você acessa uma página que foi desenhada para aparecer na tela do computador.

Clicar em um botão numa tela pequena acaba se tornando uma tarefa impossível.

![Mission: Impossible | Paramount Pictures](./Tom-Cruise-in-Mission-Impossible.jpg)

**Mission: Impossible | Paramount Pictures**

Ainda pior: clicar mais de uma vez no elemento errado pode fazer você desistir de usar a página. O que você pode fazer é dar _zoom_ na página e deslizar em todas as direções até encontrar o que procura. Uma tarefa nada fácil, muitas vezes demorada e cansativa. 

Fica claro que uma experiência de usuário agradável é importante independente o dispositivo.

# Conteúdos

Antes de você começar a fazer uma página web responsiva é importante entender alguns conceitos.

## Viewport  - janela de exibição

O primeiro conceito é o viewport: a área visível de uma página web.  
Normalmente uma página de internet com uma largura fixa se torna muito 
larga para caber no viewport numa tela uma pequena assim como a 
de um dispositivo móvel, como um tablet por exemplo. Para contornar isso 
navegadores de dispositivos móveis reduzem a escala da página inteira até 
ela caber na tela. Esse é o motívo de uma página que não é responsiva parecer ter o _zoom_ reduzido quando acessada por um dispositivo móvel.

A notícia boa é que você pode controlar o comportamento do viewport em HTML5 usando a _tag_ `<meta>`. Para isso você pode simplesmente incluir essa linha de código no conteúdo da sua `<head></head> `

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Primeiro você configura a largura do _viewport_ para ser a mesma largura da tela do dispositivo com: `width=device-width`
Então você configura o nível de _zoom_ inicial para `1.0` ou seja nenhum _zoom_ com: `initial-scale=1.0`

Apesar de você poder utilizar os valores que desejar, é recomendável usar esses valores como um padrão.

## Media Queries  - consultas de mídia

As _media queries_ permitem a você especificar um determinado estilo CSS para uma determinada largura de _viewport_ por exemplo, fazendo sua página responsiva.  Na realidade você pode aplicar estilos com base no resultado de uma ou mais consultas de mídia, que testam o tipo, as caracterísitcas específicas e o ambiente de um dispositivo.

O exemplo a seguir mostra como você pode definir uma _media query_ usando a regra `@media` dentro da sua folha de estilos.

```css
@media screen and (max-width: 768px) {
    body {
    background-color: red;
    }
}
```

*Entendendo o código:* A regra `@media` é seguida pelo tipo de mídia que vamos consultar, `screen` nesse caso (a tela do dispositivo) então temos o operador lógico `and` e por fim a condição para a aplicação da regra, no caso `max-width: 768px` para então definirmos a regra que desejamos aplicar.

Além disso podemos definir múltiplas condições por exemplo máximo e mínimo largura do *viewport*.

```css
@media screen and (min-width: 480px) and (max-width: 800px) {
   body {
     background-color: green;
  }
}  
```

Agora o estilo vai ser aplicado em telas com tamanho entre 480 e 800 pixels.  


Você também pode definir diversas medias Queries para uma única página. Outra possibilidade interessante é definir uma folha de estilos baseado no tipo de mídia:

```css
<!-- Folha de estilo dependente do tipo de mídia  -->
<link rel="stylesheet" media="screen and (min-width: 1024px)" href="widescreen-styles.css" />
```

Nesse exemplo uma folha de estilo `widescreen-styles.css` inteira é usada apenas quando a condição `media="screen and (min-width: 1024px)"` for verdadeira.

> Revisar o conteúdo a seguir:




## Unidades Relativas

A parte importante do nosso layout a não utilizar unidades fixas para nossas larguras.  
Nós usamos por valores percentuais que fazem os elementos expandir hein de forma relativa a largura dos elementos superiores.  

Dessa forma permitimos mais liberdade aos elementos o que é essencial quando juntamos tudo em um design responsivo.  

#### A unidade 'em'

CSS permite definir unidades relativas ao tamanho da fonte font-size  
Por exemplo se o corpo da sua página tem um tamanho de fonte de 16 pixels usando 1.5em é o mesmo que 24 pixels (16*1.5)  

Isso é útil porque quando você tem que mudar o tamanho da fonte você precisa
 alterar isso somente no elemento raiz. Os elementos filhos vão herdar o
 tamanho relativo se estes usarem unidades em.  

Contudo quando 
você definir todos os tamanhos usando em você pode acabar tendo um 
efeito em cascata. Nessa situação você tem muitos elementos aninhados 
usando tamanhos de fonte relativa para os seus correspondentes paz o que
 resulta em unidades de tamanho difíceis de controlar.  

#### A unidade 'rem'

Outra unidade relativa é o rem. Elementos com unidade observam apenas o tamanho da fonte do elemento raiz que é o elemento html.  
Isso torna muito mais fácil de usar que em.  
Configuramos o tamanho da fonte para o elemento html e todos tamanhos de fonte usando rem.  
Tamanhos relativos também pode ser usados para margin e paddings.

## Vamos praticar!

## Recursos Adicionais

## Gabarito (separar do arquivo)
