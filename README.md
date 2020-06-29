# Curso HTML e CSS

## Seção 1 -

### 4.
 * Hipertexto -> Textos onde a leitura nn é linear, o leitor pode escolher qual direção quer seguir.
 * HTTP -> Protocolo de transferência de hipertexto
 * Página -> Um arquivo `.html`
 * Site -> Conjunto de páginas `.html`

### 6.
 * A tag `<h1>` serve para hierarquizar as informações, nn para deixar o texto maior.
 * `<em></em>`*(itálico semântico)*: Serve **para dar ênfase**. Visualmente aparece como itálico, mas o propósito é para  dar ênfase.
 * `<strong></strong>`*(negrito semântico)*: Visualmente é igual a tag `<b></b>`, mas carrega uma carga semântica de que aqle trecho tem uma importância para o contexto.

### 9.
 * Doctype -> É uma maneira de eu informar para o browser que tipo de documento eu estou escrevendo.
   * `<!doctype html>`
 * Meta tag -> descrevem o conteúdo do seu site para os buscadores.
 * `<meta chaset="">` -> é uma meta tag que indica o tipo de codificação de caractere que está sendo usada no arquivo.
 * `<link>` -> Serve para  linkar outros arquivos.
   * Atributos *(os dois são usados juntos)*
     * `href=""`: nome do arq q quer linkar.
     * `rel=""`: especifica o tipo do arquivo.
#### Estrutura Básica HTML
```html
<!doctype html>
<!-- doctype informa ao agente de usuario a versão do html que deve ser renderizada-->
<html lang="pt-br">
    <head>
        <title> pagina de exemplo estrutura basica </title>
        <meta charset="utf-8">
        <meta name="author" content="Gustavo">
        <meta name="description" content="descrição bacanuda">
        <meta name="keywords" content="html5, tecnologia">
    </head>
    <body>

    </body>
</html>
```

## Seção 2 -

### 13.
#### Propriedades `Font`
```css
p {
    font-family: Arial, Helvetica, sans-serif;
    font-size: 40px;
    font-style: italic; /*Ou é itálico ou é normal*/
    font-variant: small-caps; /*Normal ou small-caps, que é as letras minúsculas com formatação de maiúsculas*/
}
```

#### Propriedades `Text`
```css
p {
    text-align: center; /*left:padrão; Ai tem right, center e justify*/
    text-decoration: line-through; /*Serve para colocar sublindado, para riscar aqle elemento(line-through)*/
    text-indent: 15px; /*Tamanho da identação*/
    text-transform: uppercase; /*Tudo em maiúsculo ou minúsculo*/
}
```

### 18.
#### Pseudo-classes para `<a>`
  * `a:visited{}`: Alguma formatação para o estado padrão do link, sem ser *visited*, *active*, etc.
  * `a:visited{}`: Alguma formatação diferente para quando o link ja foi visitado.
  * `a:hover{}`: Alguma formatação diferente para qnd o mouse estiver sobre o link.
  * `a:active{}`: Alguma formatação para qnd o user estiver clicando no link.

### 19.
#### Propriedades `<li></li>`

```css
li {
    list-style-type: circle; /*Muda o tipo de formatação. Tem diversas possibilidades tanto pra ul quanto pra ol.*/
    list-style-position: inside; /*Pode ser outside(padrão) ou inside, que deixa como se estivesse identado*/
    list-style: none;/*Tira as bolhinhas para um menu*/
}
```
---
> `margin: auto;`: *gambiarra* para centralizar. Ele pega o total das margin horizontal e divide em cada lado.

## Seção 3 -

###  23.
#### Trabalhando cm Imagens
```html
<img src="" alt="">
```
```css
background-image: url(...);
```

### 24.
```css
  line-height: 2; /*Aumenta o espaçamento entre as linhas. Pode colocar um valor em px
  ou um numero normar, por exemplo '2' que vai ter o dobro do espaçamento padrão*/


  .img-html{
    float: left; /*A img flutua para a esquerda e o texto vai se encaixando ao lado dela*/
  }

  body{
    background-image: url(imagens/bg.jpg);
    background-repeat: no-repeat; /*Opções: repeat(padrão), repeat-x, repeat-y e no-repeat. Neste exemplo, caso a img q for usada de fundo for menor que o tamanho do body, ela se repetirá até ocupar todo o espaço. Utilizando o no-repeat ela nn se repete.*/

    background-attachment: fixed;
    /*Opções: scroll(padrão) e fixed(que fixa a img de fundo, ela nn scrolla jnt)*/

    background-size: value-width value-height;/*Pode ser em px ou em %. Duas palavrinhas mágicas: contain, ele vai ocupar a área inteira privilegiando o conteúdo da img, msm que a imagem se repita. Cover, ele vai ocupar a área inteira msm que esconda um pedaço da img*/

    background-position: right bottom; /*imagem sempre alinhada a direta e pra baixo. Assim prioriza esse pedaço da img e se precisar esconder, irá esconder o resto. Options: right, left, bottom, top and center*/
  }
```

### 25.
#### Tags Semânticas
  * header
  * nav
  * main
  * footer
  * section
  * article
    * Onde mora o conteúdo central da pag
  * aside
    * Vai incluir nela qualque conteúdo a parte do seu site. Propragandas, etc.

#### Tags nn Semânticas
  * Div:
    * Para criar blocos e ajudar nas questões visuais.
  * Span:
    * Parecida cm a `div`, mas utilizada dentro de textos.
    * Display: inline, entt se comporta como elemento linha

### 27.

```css
  h1{
    text-shadow: 3px 3px 2px #333;
    /*text-shadow: deslocX deslocY esfumaçamento color;*/
  }
```

### 29.
  * Elementos de Bloco:
    * **Ocupa** por padrão a **área toda disponível**(de um container etc) e **gera uma quebra de linha**
    * Logo um sempre fica debaixo do outro
    * Exemplos:
      * `<p></p> ; <h1>...</h6> ; <div></div> ; <ul></ul> ; <ol></ol> ; <li></li> ; <footer></footer>`
    * É possível aplicar todas as propriedades do box-model
  * Elemento de Linha:
    * Funciona como se fosse uma única linha.
    * Não gera quebra de linha, logo fica um ao lado do outro
    * Não ocupa 100% da largura disponível, ocupa somente o espaço para que aqle elemento exista
    * Exemplos:
      * `<a></a> ; <strong></strong> ; <i></i> ; <spam></spam> ; <img> ; <input> ; <label></label>`
```css
/*Para mudar o diplay usa tendo 3 possibilidades: block, inline, inline-block e none*/
  display: inline-block;
  /*inline-block é um elemento de linha que é passivel de receber as propriedades do box-model sem perder as caracteristícas do elemento de linha, por exemplo nn quebrar a linha etc.*/
  /*o displau: none; nn mostra o elemento na tela(como se apagasse, como se nn existisse no html, perde seu espaço na tela)*/

  visibility: hidden;
  /*ele tbm esconde o elemento, mas nn é como se apagasse, o espaço do elemento ainda fica reservado na tela, ele só ta invisível*/
```

### 30.

```css
letter-spacing: 2px; /*Espaçamento entre as letras*/

/*rgba(red, green, blue, transparencia)*/
  /*Sendo a transparencia variando de 0 - 1*/
background-color: rgba(0, 0, 0, 0.3);
```

### 31.
#### Box-sizing
```css
/*O padrão do box-sizing é o content-box*/
  div{
    /*Por padrão se eu fixar a altura e largura de um elemento bloco e add um padding, a altura e largura total ultrapassa oq eu fixei.*/
    /*Neste Ex largura total é 200px e a altura 150px.*/
    width: 150px;
    height: 100px;
    padding: 25x;
  }

  /*Para deixar a altura e largura que eu fixei absoluta, entt usa box-sizing: border-box*/
  div{
    width: 150px;
    height: 100px;
    padding: 25x;
    box-sizing: border-box;
    /*Deste modo o elemento dentro da div se ajusta para ter os 25px de padding e ainda manter os valores absolutos de altura e largura*/
  }
```

### 32.
#### Float
  * Propriedade q mais tem efeito colateral
  * Assistir o video 32 e 33 se for usar

## Seção 4 -

### 35.
#### Position
  * Por padrão `position: static;`
  * Só faz sentido o uso se trabalhar junto com outras propriedades
    * top
    * bottom
    * left
    * right
##### Relative
O relative é relativo a ele mesmo. Nesse caso a `div3` olha pra posição original dela e se distancia 15px do top e do left. A posição original é preservada, os outros elementos acham que essa div está na sua posição original.
```css
#container div{
  width: 350px;
  position: static;
}

#container .div3{
  position relative;
  top: 15px;
  left: 15px;
}
```

##### Absolute
O elemento que estiver como `abosolute` sempre vai se referenciar pelo último elemento acima dele(hierárquia) que tenha a propriedade `position` diferente de `static`. Se o `#container` nn fosse `position: relative`, ele ia se referenciar pelo body ou html.
O elemento tbm sai do fluxo normal do elemento, assim nn sendo enxergado pelas outras divs de `#container`.
```html
<body>
<div id="container">
  <div></div>
  <div class=div2></div>
  <div></div>
</div>
</body>

<style>

  #container{
    width: 550px;
    position: relative;
  }

  #container div{
  width: 350px;
  position: static;
}

  #container .div2{
    position: absolute;
    top: 10px;
    right: 10px;
  }


</style>
```
##### Fixed
Ele vai sempre se referenciar à janela do browser. O elemento tbm sai do fluxo normal do elemento, assim nn sendo enxergado pelas outras divs de `#container`.
```css
#container div{
  width: 350px;
  position: static;
}

#container .div3{
  position fixed;
  top: 15px;
  left: 15px;
}
```

> `z-index: 4;` -> indica a prioridade de aparecer na frente da tela(nn ficar em baixo de outros elementos). Maior índice maior prioridade.

### 38.
  * `<address></address>` : Representa a forma de contato com o dono da página ou o dono do article
    * Serve para deixar mais semântico

### 40.
#### Transition

```css
a{
  color: black;
  transition: color .3s linear;
/*Recebe 3 parâmetros:*/
  /*1- Propriedade que vai ser animada */ /*Caso ela receba somente o valor `all`, ela animará qualquer propriedade que for alterada no `hover` ou outra coisa*/
  /*2- Tempo que vai durar*/
  /*3- aceleração ou desaceleração(vai ser explicado dps)*/

}

a:hover{
  color: white;
}
```


## Seção 5 -

### 41.
#### Listas Aninhadas
  * Literalmente lista dentro de lista
 ```html
  <ul>
    <li>abc</li>
    <li>
      <ol>
        <li>asdad</li>
        <li>adasd</li>
      </ol>
    </li>
    <li>asdasd</li>
  </ul>
```

#### Listas de Definição
  * Usada qnd se tem um ou vários termos com uma ou várias definições.
  * `dl`: definition list
  * `dt`: definition term
  * `dd`: definition description

```html
  <dl>
    <dt></dt>
    <dd></dd>
    <dt></dt>
    <dd></dd>
  </dl>

  ou

  <dl>
    <dt></dt>
    <dt></dt>
    <dt></dt>
    <dd></dd>
  </dl>

  ou

  <dl>
    <dt></dt>
    <dd></dd>
    <dd></dd>
    <dd></dd>
  </dl>

  e por ai vai
```

### 42.
> No final do video tem um exemplo daora de passar o mouse e mostrar o conteudo escondido.

### 43.
#### Overflow
  * Serve para tratar o conteúdo que excede a determinado elemento.
  * Valores Possíveis:
    * `visible`(padrão)
    * `hidden`
      * Esconde o texto que excedeu o tamanho
    * `scroll`
      * Coloca uma barra de rolagem para acessar o conteúdo que excedeu o tamanho.
      * Mesmo se nenhum conteúdo tenha excedido o tamanho a barra de scroll vertical e horizontal continuará lá.
    * `auto`
      * Se precisar de bara de rolagem ele coloca, se nn precisar ele nn coloca.

### 44.
#### Tabelas
  * Tags padrões
    * `<table>`
    * `<tr></tr>`(linha)
    * `<td></td>`(coluna)
    * `<th></th>`(table header)
    * `<thead></thead>`
    * `<tfoot></tfoot>`(tem q ser nessa ordem, tfoot antes do tbody)(Pra colocar uma legenda, essas coisas)
    * `<tbody></tbody>`
    * `<caption></caption>`(Título da tabela)(Bom acessibilidade)

  * Para mesclar linhas ou colunas, tem que escrever toda a estrutura e utilizar os atributos **Sempre nas tags td**:
    * `colspan`
    * `rowspan`
  * CSS
    * `border-collapse`:
      `separate`(padrão)(com espaços entre as células)
      `collapse`(as células ficam grudadas)(nn muda msm se colocar margin etc)

      <table>
          <tr>
            <td colspan="2">1A</td>
            <!-- Vai ocupar 2 colunas -->
          </tr>
          <tr>
            <td>2A</td> <td>2B</td>
          </tr>
          <tr>
            <td>3A</td> <td>3B</td>
          </tr>
      </table>

      ```html
        <table>
          <tr>
            <td colspan="2">1A</td>
            <!-- Vai ocupar 2 colunas -->
          </tr>
          <tr>
            <td>2A</td> <td>2B</td>
          </tr>
          <tr>
            <td>3A</td> <td>3B</td>
          </tr>
        </table>

          ou

        <table>
          <tr>
            <td rowspan="2">1A</td>
            <!-- Essa célula vai ocupar 2 linhas -->
            <td>1B</td>
          </tr>
          <tr>
            <td>2B</td>
          </tr>
          <tr>
            <td>3A</td> <td>3B</td>
          </tr>
        </table>
      ```

## Seção 6 -

### 47.
#### Exemplo de Formulário
<form action="#" method="post">
  <fieldset>
    <legend>Login</legend>
    <label for="log">User:</label>
    <input type="text" name="txt" id="log" autofocus>
    <label for="pass">Password:</label>
    <input type="password" name="pass" id="pass">
  </fieldset>
  <input type="submit" value="Login">
</form>

```html
<form action="pagina.php" method="post">
  <fieldset><!-- Login é a legenda do fieldset -->
    <legend>Login</legend>
    <label for="log">User:</label>
    <input type="text" name="txt" id="log" autofocus>
    <!-- Esse autofocus faz q qnd a pag é carregada o foco ja vai pra esse input -->
    <label for="pass">Password:</label>
    <input type="password" name="pass" id="pass">
  </fieldset>
  <input type="submit" value="Login">
</form>
```

### 48.
```css
  /* #user é um input */
  /* qnd eu clicar dentro do input ele muda o background*/
  #user:focus{
    background-color: #ccc;
  }
```

### 49.
#### Tipos de Inputs
  * email
  * tel
  * url
  * number
    * min e max
  * date
    * min e max (no formato americano de data)
  * radio (Só pode escolher uma opção dos radio)
    * Coloca um label pra cada
    * Para funcionas, cada `input type="radio"` tem que ter o msm nome
    * Tem que ter o atributo value para o navegador saber que dado enviar, assim vai enviar oq ta dentro do value
  * reset (limpa o form)
  * submit
  * button
  * range
  * color(se o navegador tiver suporte aparece um pedaço pra escolher uma cor)
  * time (é possivel selecionar uma hora)

#### Alguns Atributos dos Inputs
  * autofocus
  * checked
  * required
  * maxlength
  * multiple
    * é usada junto cm o `<select></select>` para poder selecionar mais de uma opção(se usar o *ctrl*)
  * placeholder
  * min
  * max
  * cols
  * rows
  * size
  * step

### 50.
#### Select
  <label for="estado">Estado</label>
  <select id="estado" name="estado">
    <option value="0">Selecione</option>
    <option value="SP">São Paulo</option>
    <option value="RJ">Rio de Janeiro</option>
    <option value="MG">Minas Gerais</option>
  </select>
  ```html
    <label>Estado</label>
    <select name="estado">
      <option value="0">Selecione</option>
      <option value="SP">São Paulo</option>
      <option value="RJ">Rio de Janeiro</option>
      <option value="MG">Minas Gerais</option>
    </select>
  ```

#### CheckBox
  <label>
    <input type="checkbox" name="html" value="html">
    HTML
  </label>

  <input type="checkbox" name="css" value="css" id="css">
  <label for="css">CSS</label>

  <input type="checkbox" name="js" value="js" id="js">
  <label for="js">JavaScript</label>

  ```html
    <label>
      <input type="checkbox" name="html" value="html">
      HTML
    </label>


    <input type="checkbox" name="css" value="css" id="css">
    <label for="css">CSS</label>

    <input type="checkbox" name="js" value="js" id="js">
    <label for="js">JavaScript</label>
  ```

#### TextArea
<textarea name="msg"></textarea>

> É possível definir a qntd de linhas e colunas cm os atributos ` rows="" cols=""` inline msm, mas é preferível que faça no css
> no css a propriedade `resize: none` tira do canto inferior direito a possibilidade de alterar o tamanho. Ficando, assim, fixo no tamanho que vc definir.

---
> Se um campo é obrigatório, coloque o atributo required para indicar isso. `<input type="email" required >`

#### Range

<input type="range" min="0" max="10" step="2">

```html
<input type="range" min="0" max="10" step="2">
<!-- o step fala quanto ele tem q pular, nesse caso ele permite escolher de 2 em 2-->
```

## Seção 7 -

### 53.
#### Border-Radius
* 1 Parâmetro
  * Aplica o valor em todos on cantos tanto na horizontal quanto na vertical
* Mais de 1 parâmetro
  * `border-radius: cs-esq cs-direito ci-direito ci-esq ;`
  * > cs = canto superior
  * > ci = canto inferior
* Se utilizar da `/`, tudo que vier **antes** dela são valores na **horizontal**. Tudo que vier **dps** são valores na **vertical**
  * `border-radius: cs-esq cs-direito ci-direito ci-esq  / cs-esq cs-direito ci-direito ci-esq;`
> Como se nn utilizássemos a `/` estariamos pensando em um *raio* de um circulo.

> Utilizando a `/` é como se pensássemos em um *raio* de uma elipse

##### Exemplo
Esfera Perfeita
<div style="width:30px;height:30px;background-color:#525c9e;border-radius:50%;"></div>
<br>

```css
  div{
    width: 30px;
    height: 30px;
    background-color: #525c9e;
    border-radius: 50%;
  }
```

Usando a `/`
<div style="width:50px;height:50px;background-color:#525c9e;border-radius:12.5px 25px / 25px 12.5px;"></div>
<br>

```css
  div{
    width: 50px;
    height: 50px;
    background-color: #525c9e;
    border-radius: 12.5px 25px / 25px 12.5px;;
  }
```

### 54.
#### Box-Shadow
> É como se criasse uma clone do elemento e vc modificasse ele

Parâmetros:
  * `box-shadow: qntd-direita qntd-esq esfumaçamento tamanho-sombra(opcional) cor`
> Valores negativos vão para o lado oposto ou diminuem no caso do *tamanho-sombra*

> É possível add mais de uma sombra em um elemento, é só acrescentar uma `,` e passar os valores.

Exemplo
<div style="width:40px;height:40px;background-color:#a2515e;border-radius:50%;box-shadow: 5px 0 1px #51a295, 0 -5px 0 #6baf5e, 6px -6px 5px 5px #a25eaf;"></div>
<br>

```css
  div{
    width:40px;
    height:40px;
    background-color:#a2515e;
    border-radius:50%;
    box-shadow: 5px 0 1px #51a295, 0 -5px 0 #6baf5e, 6px -6px 0 5px #a25eaf
  }
```
### 55.
#### Text-Shadow
Mesma coisa do *box-shadow*, com exceção de que nn é possivel mudar o tamanho da sombra.

### 56.
#### Gradiente Linear
* Sempre vai funcionar como um backgroun-image
* Precisa da **cor inicial** e a **cor final**(mas pode ter cores intermediárias) e tbm é possível declarar a direção dele. Caso nn seja declarada a direção, o padrão é `to bottom`.
* É possível utilizar junto com imagens e outros gradientes
  * `background-image:linear-gradient(...), url(...), linear-gradient(...);`
* Padrão
  * `background-image: linear-gradient(to bottom, #fff03a, #8e3aff)`:


<div style="width:60px;height:60px;border:1px solid black;margin-left:50px;background-image:linear-gradient(#fff03a, #8e3aff);"></div>
<br>

* Com cores intermediárias diagonal
  * `background-image:linear-gradient(to top right,#ff3a49, #fff03a, #3afff0, #3a49ff);`
  * Tbm é possível colocar valores em graus
    * `background-image:linear-gradient(45deg,#ff3a49, #fff03a, #3afff0, #3a49ff);`

<div style="width:60px;height:60px;border:1px solid black;margin-left:50px;background-image:linear-gradient(to top right,#ff3a49, #fff03a, #3afff0, #3a49ff);"></div>
<br>

* Determinando tamanhos
  * `background-image:linear-gradient(200deg,#3aacff 30% , #ff3a49, #3aff8e 70%);`

<div style="width:60px;height:60px;border:1px solid black;margin-left:50px;background-image:linear-gradient(200deg,#3aacff 30% , #ff3a49, #3aff8e 70%);"></div>
<br>

### 57.
```css
  @font-face{
    font-family: 'nadia';/*Apelido pra minha fonte*/
    src: url(fonts/nadia/nadia-serif.eot);
    src: url(fonts/nadia/nadia-serif.woff) format('woff'),
         url(fonts/nadia/nadia-serif.ttf format('truetype')
         url(fonts/nadia/nadia-serif.svg) format('svg');
    /* O format() serve para o navegador identificar o tipo do arquivo antes de fazer dowload */
  }
```

### 58.
#### Transition
* Precisa fazer que haja algum efeito que dispare uma animação. Ex: `:hover`
* `transition-property:;`- Propriedade do elemento que vai ser animada
* `transition-duration:;`- Tempo que dura a animação
* `transition-time-function:;`- Para modificar a velocidade e aceleração da animação.
  * Valores:
    * *linear* (padrão)
    * *ease*
    * *ease-in*
    * *ease-out*
    * *ease-in-out*
    * ou algm valor *cubic-bezier()*
    * Verificar a diferança de cada um em https://cubic-bezier.com/#.17,.67,.83,.67
* `transition-delay:;`- Se quiser esperar algum tempo antes de começar a animação.

##### Exemplo
<style>
  #Dtransition{
    width:60px;height:60px;border:1px solid black;margin-left:50px;background-color:#7d1186;transition-property:width, border;transition-duration:1s,1.5s;transition-time-function:cubic-bezier(.67, -.38, .5,1.5), ease;
  }
  #Dtransition:hover{
    width: 100px;
    border: 4px solid #11867d;
  }
</style>
<div id="Dtransition">
</div>
<br>

```css
  #transition{
    transition-property:width, border;transition-duration:1s,1.5s;transition-time-function:cubic-bezier(.67, -.38, .5,1.5), ease;
  }
  #transition:hover{
    width: 100px;
    border: 4px solid #11867d;
  }
```

## Seção 8 -
### 62.
<h4>4 . 10<sup>2</sup></h4>

* `<h4>4 . 10<sup>2</sup></h4>`

ou
<h4>C<sub>6</sub>H<sub>12</sub>C<sub>6</sub></h4>

* `<h4>C<sub>6</sub>H<sub>12</sub>C<sub>6</sub></h4>`

* Tags:
  * `<code></code>`
    * Se precisar colocar um pedaço de código como demonstração
  * `<blockquote></blockquote>`
    * Para representar uma citação
    * Normalmente citações grandes
    * atributo `cite="" para o link da citação`
  * `<q></q>`
    * igual o *blockquote* só que para citações pequenas
    * atributo `cite="" para o link da citação`
  * Icon como fonte
    * https://fontawesome.com/

### 68.
* Valor `inherit` no CSS
  * Representa que aquele elemento vai **herda**r o valor da **mesma propriedade** do elemento **pai**
  * Deste modo, nn é preciso definir em dois lugares diferente, logo se alterar, só é preciso modificar em um lugar.
* > Caso eu não defina a cor da borda, ela pega a cor da font
  * <a style="color:#11867d;border-bottom:3px dotted;">Teste</a>


 ```css
  a{
    color:#11867d;
    border-bottom:3px dotted;
  }
```

### 69.
* Unidade de medida **`em`**
  * refere-se ao tamanho do font-size daquele elemento/bloco

<style>.teste{margin:0 0 1em;} </style>
<h1 class="teste">Teste</h1>
<h2 class="teste">Teste</h2>
<h3 class="teste">Teste</h3>

```css
  h1, h2, h3{
    margin: 0, 0, 1em;
    /*Nesse caso, a margin-bottom dos títulos vai
    depender do tamanho da fonte, sendo maior no h1 e menor no h3*/
  }
```

### 70.
* pseudo-classe **`:last-child`**
  * Pega o último filho/elemento daquele identificado
* pseudo-classe **`:first-child`**
  * Pega o primerio filho/elemento daquele identificado
* pseudo-classe **`:nth-child()`**
  * Pega o filho que você identificar
    * Podendo passar o número do filho, (3) ou (7)
    * Ou pode passar as palavras *odd*(ímpar) ou *even*(par)
  * > Caso eu tenha, por exemplo: `article:nth-child(2)`
    * > Ele nn seleciona o segundo que **é** *article*, Ele vai selecionar o segundo filho **se** ele for um *article*

<ul class="ul-alternate"><li>item1</li><li>item2</li><li>item3</li></ul><br>
<style>
  .ul-alternate{list-style:none;}
  .ul-alternate li{border-bottom:2px solid #666;}
  .ul-alternate li:last-child{border:0;}
  .ul-alternate li:nth-child(odd){color: red;}
  .ul-alternate li:nth-child(2){background:yellow;}
</style>

```css
  ul{list-style:none;}
  ul li{border-bottom:2px solid #666;}
  ul li:last-child{border:0;}
  ul-alternate li:nth-child(odd){
    color: red;
  }
  .ul-alternate li:nth-child(2) {
    background:yellow;
  }
```

### 74.
#### Selecionar no CSS por atributo
* Usa o `[atributo=""]`
##### Exemplo
```css
input[type="checkbox"], input[type="radio"]{
  width: 50px;
}
```

### 75.
* Propriedade `max-width`/`max-height`
  * Qnd usado em img, ele pode variar o tamanho até o valor max da img.
    * Se a imagem original tem 150px de width, na pag ela só vai poder ter valores até 150px(150px <=)

### 76.
> Se eu estiver fazendo `margin-bottom:2%;, mesmo sendo aplicada na vertical, o 2% é sempre relativo ao tamanho do eixo horizontal`

#### nth-child() com múltiplos ou fórmulas
* `xn` representa os múltiplos de x
  * `nth-child(2n)` ; `nth-child(3n)` e ai vai...
*  Caso eu queria pegar os filhos 2,5 e 8
   *  `nth-child(3n - 1)`
* E assim vai

## Seção 9 -
### 82.
#### Seletores Compostos
* `>` : *Filho Direto*
  * `article p > a{}`
    * Seleciona todo **`a`** que é filho direto de **`p`**
* `+` : *Imediatamente Após*
  * `h3 + p{}`
    * Seleciona todo o **`p`** que vem **imediatamente** após um **`h3`**
* `~` : *Irmãos Próximos*
  * `h3 ~ p{}`
    * Seleciona todos os **`p`** que vem após um **`h3`**

#### Seletores de Atributos
* [atributo] : *Padrão*
  * `a[title]{}`
    * Seleciona todo o **`a`** que tenha o atributo *Title*
* [atributo="..."] : *Com Valor*
  * `img[alt="..."]`
    * Seleciona todo a **`img`** que tenha o atributo *alt* com o valor que vc definir
* [atributo^="..."] : *Inicía Com Tal Valor*
  * `a[href^="http"]`
    * Seleciona todo o **`a`** que tenha o atributo *href* que começe com "*http*"
* [atributo$="..."] : *Termina Com Tal Valor*
  * `img[src$=".png"]`
    * Seleciona toda **`img`** que contenha o atributo *src* e ele termine com "*.png*"

#### Seletor `:not`
* **É uma negação padrão**
* `p:not(.destaque){}`
  * Seleciona todo `p` que **não pertença** à classe *.destaque*
* `img:not([alt])`
  * Seleciona toda a `img` que **não tenha** o atributo *alt*

### 84.
#### Add Conteúdo dinamicamente com css
* Pseudo-Elementos: *::Before* e *::After*
  * ***INDICADO PARA SER USADO SOMENTE PARA QUESTÕES VISUAIS***
* Sempre que usar esses dois pseudo-elementos é necessário utilizar, obrigatóriamente, o `content:"";`. **Mesmo** se o conteúdo for **vazio**
  * O *Content* é por padrão um elemento de linha
* Ele coloca um conteúdo(antes ou depois) do conteúdo principal.
* O texto add com CSS **nn é selecionável**, nn é possível copiar

### 86.
> Para **forçar** algum elemento poder receber o focus(*qnd navegar pelo tab vai ser possivel ver o elemento*), usa o *tabindex-""*. `<div tabindex="4"></div>`, o valor passado é um número pra identificar a ordem da navegação que ele ta

### 88.
* `::first-letter`: Pega a primeira letra
* `::first-line`: pega a primeira linha
* `::selection`: Pra formatar a seleção(tentar copiar ; clicar e arrastar o mouse) que o usuário tentar fazer em algum texto
* **caniuse.com** para ver se determinado atributo/pseudo-elemento/pseudo-classes/ etc tem **suporte** nos *navegadores*

### 89.
#### Propriedade Transform
* Serve para **transformar** elementos
* É possível colocar vário valores tipo
  * `transform: rotate(45deg) translateX(50%)`
  * A **ordem importa**
* ##### Valores
  * **`transform: translate(valorX, valorY)`**
    * Para **transladar** o elemento
    * Valores **negativos** vão pra *esquerda* ou pra *cima*
    * Os eixos são referentes ao do próprio elemento.
      * Entt se o elemento estiver rotacionado, isso altera os seus eixos.
    * Movimenta o elemento e tbm **mantém** a posição original dele, **não quebrando** o fluxo do código
    * A *diferença* dele pro `position: relative;` é que quando for utilizado **porcentagem**, o translate é sempre **relativo ao seu proprio tamanho**. Entt quando eu coloco *`translateX(100%)`* ele vai andar o seu próprio tamanho no eixo x
  * **`transform: rotate()`**
    * recebe graus como parâmetro
    * Ele rotaciona a partir no centro do elemento.
    * Para mudar o eixo de rotação, utiliza-se o `transform-origin:;` com valores como: *left* *top* *right* *bottom*
  * **`transform: skew()`**
    * Ele deforma o elemento
    * Pega as extremidades e movimenta em sentido opostos
    * Recebe graus como parâmetro
      * Primeiro o valor do X dps do Y
    * <style>
        #skew{
        width:60px;height:60px;border:1px solid black;margin-left:50px;background-color:#3cd37d;
        transform: skew(15deg, 5deg);
        }
      </style>
      <div id="skew">
      </div>

    * ```css
          div{
            width:60px;
            height:60px;
            border:1px solid black;margin-left:50px;background-color:#3cd37d;
            transform: skew(15deg, 5deg);
          }
        ```
  * **`transform: scale()`**
    * Recebe os valores de x e y em números inteiros
    * ou um número só para os dois eixos
    * Aumenta a escala em relação ao seu próprio tamanho
    * Se eu passo `scale(2)` ele dobra a escala, e por ai vai
    * <br><style>
        #scale{
        width:60px;height:60px;border:1px solid black;margin-left:50px;background-color:#db0d0d;
        transform: scale(2, 1.4);
        }
      </style>
      <div id="scale">
      </div>
      <br>
    * ```css
          div{
            width:60px;
            height:60px;
            border:1px solid black;margin-left:50px;background-color:#db0d0d;
            transform: scale(2, 1.4);
          }
        ```
    * <br><style>
        #scaleTransition{
        width:60px;height:60px;border:1px solid black;margin-left:50px;background-color:#db0d0d;
        transition: transform .5s;
        }
        #scaleTransition:hover{
          transform: scale(2)
        }
      </style>
      <div id="scaleTransition">
      </div><br><br>
    * ```css
        div{
        width:60px;
        height:60px;
        border:1px solid black;background-color:#db0d0d;
        transition: transform .5s;
        }
        #scaleTransition:hover{
          transform: scale(2)
        }
      ```

## Seção 10 -
* `<meta name="viewport" content="width=device-width,initial-scale=1.0"`
  * Essa meta tag equaliza o tamanho da resolução em px do aparelho fisíco
    * Se o aparelho mede 480px, a resolução que o css tem q levar em conta é de 480px
* `calc()`: faz uma conta
  * Ex: `calc(50% - 30px)`