#### Unoesc Chapecó
#### Pós-graduação em Desenvolvimento Web, Cloud e dispositivos móveis - WebMob
#### Disciplina: HTML5+CSS3
#### Professor: Jean Carlo Nascimento
#### Acadêmico(a): Evandro Diego Erlo
### Artigo de revisão de CSS3

<h1>Funcionalidades CSS3 </h1>
<h2>border-image</h2>
##### Funcionalidade: border-image
##### O que é?
Esta propriedade é utilizada para adicionar uma imagem de borda em elementos da página.
##### Onde usar:
Em qualquer elemento que disponibilize o atributo border-image.
##### Como usar:
São 3 propriedades definidas para a imagem de borda:
- 1 - URL / Caminho da imagem.
- 2 - O tamanho que a imagem ficará na borda em relação a seu tamanho original.
- 3 - Específica se a imagem vai se repetir na borda ou será esticada para o tamanho total da borda.
```css
.minha_div{
        border: xy;
        border-image: url(<source>) <size>  <type>;
}
```
##### Exemplo de uso
A sintaxe para aplicar a `border-image` completa seria da seguinte forma:

```css
.minha_div{
        border: 10px; // definimos o tamanho da borda
        border-image: url(image.jpg) 10% stretch; // definimos que a image.jpg irá ser usada 10% do seu tamanho original e será esticada para preencher os espaçõs da borda do elemento.
}

```
### Referência:
[W3C - border-image](http://www.w3schools.com/css/css3_border_images.asp)


<h2>text-shadow</h2>
##### Funcionalidade: text-shadow
##### O que é?
Esta propriedade é utilizada para adicionar sombras a textos.
##### Onde usar:
Em elementos que contenham texto.
##### Como usar:
São 4 propriedades definidas para a text-shadow:
- 1 - Posição horizontal da sombra.
- 2 - Posição vertical da sombra.
- 3 - Tamanho da nevoa da sombra em relação ao tamanho original do texto.
- 4 - Cor da sombra.
```css
.minha_div h1{
       text-shadow: <x> <y> <z> <color>;
}
```
##### Exemplo de uso
A sintaxe para aplicar o `text-shadow` completo seria da seguinte forma:

```css
.minha_div h1{
        text-shadow: 10px 10px 80px red;
}

```
### Referência:
[W3C - text-shadow](http://www.w3schools.com/css/css3_shadows.asp)

<h2>box-shadow</h2>
##### Funcionalidade: box-shadow
##### O que é?
Esta propriedade é utilizada para adicionar sombras a elmentos.
##### Onde usar:
Em qualquer elemento que possua a propriedade box-shadow.
##### Como usar:
São 4 propriedades definidas para a box-shadow:
- 1 - Posição horizontal da sombra.
- 2 - Posição vertical da sombra.
- 3 - Tamanho da nevoa da sombra em relação ao tamanho original do box.
- 4 - Cor da sombra.

Não necessariamente se utiliza as 4 propriedades.

```css
.minha_div{
       box-shadow: <x> <y> <z> <color>;
}
```
##### Exemplo de uso
A sintaxe para aplicar o `box-shadow` completo seria da seguinte forma:

```css
.minha_div{
        box-shadow: 10px 10px 5px green;
}

```
### Referência:
[W3C - box-shadow](http://www.w3schools.com/css/css3_shadows.asp)

<h2>font-face</h2>
##### Funcionalidade: @font-face
##### O que é?
Utilizada para incorporar fontes externas ao seu projeto
##### Onde usar:
Deve ser declarada preferêncialmente no início do css.
##### Como usar:
São 2 propriedades principais definidas.
- 1 - `Font-family` onde você difine um nome para a fonte.
- 2 - `src` onde você define o arquivo que será importado para gerar a fonte.

```css
@font-face{
        font-family: <nomedafonte>;
        src: url(<source>);
}
.minha_div{
      font-family: <nomedafonte>;
}
```
##### Exemplo de uso
A sintaxe para aplicar o `@font-face` completo seria da seguinte forma:

```css
@font-face{
        font-family: olamundofonte;
        src: url(open_sans.otf);
}
.minha_div{
      font-family: olamundofonte;
}
```
### Referência:
[W3C - @font-face](http://www.w3schools.com/css/css3_fonts.asp)




<h2>Transforms - 2D</h2>
##### Funcionalidade: Transforms
##### O que é?
Transforms permitem trabalhar com os elementos, alterando sua escala, rotacionar, mudar posição, mudar tamanho entre outras funcionalidades, trablhar tambem com efeitos 3D e 2D.
##### Onde usar:
Pode ser usada para criar de animações simples até animações mais complexas utilizando de elementos de seu projeto.
##### Como usar:
O Transform possui várias opções, irei abordar as que considero mais válidas incialmente para serem utilizadas.
- translate() - Opção utilizada para mover o elementeo conforme coordenadas com base de sua origem.
- rodate() - Rotaciona um elemento em um determinado grau com base no seu ponto central.
- scale() - Altera a escala do elemento com base no seu tamanho inicial.
- skewX() - Distorce o elemento com base no seu eixo X.
- skewY() - Distorce o elemento com base no seu eixo Y.
- skew() - Distorce o elemento com base no eixo X e Y.
- matrix() - Combinação de todas as transformações 2D.

O Transform também pode ser usado com a propriedade `transform-origin` que move o elemento transformado com base na posição inicial, esta propriedade deve ser usada logo em sequencia a `transform`. Estas seriam as principais opções de transformar objetos em 2D.
```css
.minha_div{ 
      transform: <method>(<value>); 
}

```
##### Exemplo de uso
A sintaxe para aplicar o `transform` completo seria da seguinte forma:

```css
.minha_div{ 
      transform: rotate(25deg);  // sendo assim rotacionei meu elemento em 25 graus com base no centro dele.
}
```
Utilizando o `transform-origin`:
```css
.minha_div{ 
      transform: rotate(25deg);  // sendo assim rotacionei meu elemento em 25 graus com base no centro dele.
      transform-origin: 10% 5%; // após transformar o elemento foi movido 10% em X e 5% em Y com base no seu estado inicial.
}
```

### Referência:
[W3C - transform](http://www.w3schools.com/css/css3_2dtransforms.asp)



<h2>Transforms - 3D</h2>
##### Funcionalidade: Transforms
##### O que é?
Semelhante ao transforms falado anteriormente, mas este em especifico será utilizado para funcionalidades 3D.
##### Onde usar:
Pode ser usada para criar de animações simples até animações mais complexas utilizando de elementos de seu projeto.
##### Como usar:
O Transform possui várias opções, irei abordar as que considero mais válidas incialmente para serem utilizadas com efeitos 3D.
- rotateX() - Opção utilizada para rotacionar elemento com base em seu eixo X.
- rotateY() - Opção utilizada para rotacionar elemento com base em seu eixo Y.
- rotateZ() - Opção utilizada para rotacionar elemento com base em seu eixo Z.

O Transform também pode ser usado com várias outras propriedades:
- `transform-style` - é o estilo em que o efeito de rotação 3D será aplicado no elemento.
- `perspective` - define a distancia que ficará o elemento na frente, em relação a sua base.
- `perspective-origin` - define a distacia referente a origem que o elemento será movido em X e Y.
- `backface-visibility` - define se o elemento ao girar, será possivel ver a parte de trás do elemento.

##### Exemplo de uso
A sintaxe para aplicar o `transform` completo seria da seguinte forma:

```css
.minha_div{ 
      transform: rotateX(25deg);  // sendo assim rotacionei meu elemento em 25 graus com base no centro dele no eixo X.
}
```
Utilizando as propriedades disponíveis:

```css
.minha_div{ 
      transform: rotateX(25deg);
      perspective: 400px // definido que o elemento ficará 400px a frente de sua base.
      perspective-origin: 5% 10%; //difinido que o elemento moverá 5% em X e 10% em Y referente a sua posição original.
}
```
Outros metodos podem ser utilizados para rotação 3D:
 - `matrix3d(n,n,n,n,n)` , `translate3d(x,y,z)` , `translateX(x)` , `translateY(y)` , `translateZ(z)`, `scale3d(x,y,z)`, `scaleX(x)`, `scaleY(y)`, `scaleZ(z)`, `rotate3d(x,y,z,angle)`, `rotateX(angle)`, `rotateY(angle)`, `rotateZ(angle)`, `perspective(x)`.

### Referência:
[MAUJOR - Tutoriais CSS](http://www.maujor.com/tutorial/css3-modulo-transition.php)


<h2>transition</h2>
##### Funcionalidade: transition
##### O que é?
Transition simplesmente fantástico, utilizado para gerar transições de propriedades de elementos.
##### Onde usar:
Pode ser usado para o mais diversos efeitos de animação, por exemplo, alterar o tamanho e cor de um botão quando o mouse passar por ele.
##### Como usar:
O Transform possui as seguintes opções: 
- transition - Opção utilizada para definir principalmente o tempo de uma transição de propriedades, declarando cada propriedade o tempo que ela demora para alterar.
- transition-delay - Opção que determina o tempo que demora para iniciar o efeito apos a ação do transition ser solicitada.

Separando o `transition` em propriedades especificas:
- transition-property - Determina qual propriedade será alterada.
- transition-duration - Determina o tempo que levará para o efeito completar.
- transition-timing-function: - Determina o método de retorno do elemento ao seu estado inicial, podendo ser: `ease`, que é o metodo default, onde o elemento inicia lento, depois rápido, depois lentamente para finalizar. O metodo `liner` onde o efeito se mante na mesma velocidade para todas as etapas. O metodo `ease-in` onde o efeito é feito lentamente durante todo o processo. O metodo `ease-out` onde o efeito finaliza lentamente. O metodo `ease-in-out` onde o efeito é lento no início e ao final da transição.  

```css
.minha_div {
    background: <cor>;
    transition: background <time>;
}

.minha_div:hover {
    background: <corefeito>;
}

```
##### Exemplo de uso
A sintaxe para aplicar o `transform` completo seria da seguinte forma:

```css
.minha_div {
    background: red; // Determinado a cor inicial de fundo do meu elemento
    transition: background 2s; // Determinado que levará 2 segundos para o efeito completo
}

.minha_div:hover {
    background: green; // Determinado a cor final de fundo do meu elemento após o efeito estar completado.
}
```

### Referência:
[W3C - transition](http://www.w3schools.com/css/css3_transitions.asp)


<h2>@keyframes </h2>
##### Funcionalidade: @keyframes 
##### O que é?
Utilizado para se criar regras de efeito para serem usados em qualquer elemento compativel sem precisar recriar para cada elemento o efeito.
##### Onde usar:
Pode ser usado para o mais diversos efeitos de animação, por exemplo, alterar o tamanho e cor de um botão quando o mouse passar por ele e utilizar o keyframe em outro elemento que realizará a mesma animação sem precisar recriar o efeito.
##### Como usar:
Primeiramente se declara o `@keyframes` da seguinte maneira: 

```css
@keyframes artigo_css { // defino a keyframe com um nome qualquer
    from {width: 800px;} //defino o estado inicial do efeito
    to {width: 1000px;} // defino o estado final do efeito
}

.minha_div { // crio um elemento qualquer
    width: 800px; // determino tamanho de largura
    height: 900px; // determino tamanho de altura
    animation-name: artigo_css; // digo qual animaçãp eu vou utilizar
    animation-duration: 4s; // digo quanto tempo ela vai durar.
}
```
Tambem posso determinar cada % do meio efeito, e outras propriedades interessantes, por exemplo: 

```css
@keyframes artigo_css_tempo { // defino a keyframe com um nome qualquer
    0%{width: 800px;}
    50%{width: 2000px;}
    100%{width: 1000px;}
}

.minha_div { // crio um elemento qualquer
    width: 800px; // determino tamanho de largura
    height: 900px; // determino tamanho de altura
    animation-name: artigo_css; // digo qual animaçãp eu vou utilizar
    animation-duration: 4s; // digo quanto tempo ela vai durar.
    animation-delay: 1s; // aqui adicionei um pequeno tempo de espera antes de iniciar o efeito.
    animation-iteration-count: 2; // aqui defino que o efeito será realizado duas vezes, podendo ser setado `infinite`.
    animation-direction: reverse; // defino que o efeito será de traz para frente, podento ser `alternate` que a cada vez que o efeito inicia ele será de sentido diferente.
}
```
Com o metodo `animation` podemos criar inúmeros efeitos diferentes, deixando seu projeto até mesmo mais atrativo.


### Referência:
[W3C - css3_animations](http://www.w3schools.com/css/css3_animations.asp)


<h2>Multi-column  </h2>
##### Funcionalidade: Multi-column  
##### O que é?
Utilizado para se criar colunas de texto dentro de elementos .
##### Onde usar:
Pode ser utilizado para se divider conteúdo de texto em colunas para se facilitar a leitura.
##### Como usar:
A utilização é meramente simples, veja o exemplo: 

```css
@keyframes artigo_css { // defino a keyframe com um nome qualquer
    from {width: 800px;} //defino o estado inicial do efeito
    to {width: 1000px;} // defino o estado final do efeito
}

.minha_div { // crio um elemento qualquer
    width: 800px; // determino tamanho de largura
    height: 900px; // determino tamanho de altura
    animation-name: artigo_css; // digo qual animaçãp eu vou utilizar
    animation-duration: 4s; // digo quanto tempo ela vai durar.
}
```
Tambem posso determinar cada % do meio efeito, e outras propriedades interessantes, por exemplo: 

```css

.minha_div { // crio um elemento qualquer
   column-count: 3; //defino que o texto deste elemento será dividido em 3 colunas verticais.
   column-fill: auto; // definido que as colunas serão geradas com seu conteudo possivelmente com tamanhos diferentes, podendo ser usado, `balance`, aonde as colunas são mantidas semelhantes em seu tamanho, `initial`, `inherit`.
   column-gap: 80px; // determina o espaço entra cada coluna
   column-rule-color: red; // determina que as colunas serão vermelhas
   column-rule-style: solid; // determina que as colunas terão o formato solido, partindo do princípio de borda.
   column-rule-width: 10px; // determina que a borda da coluna possui 10px de largura
   column-width: 40px; // detrmina que a coluna terá 40px de largura cada
}
.minha_div h1{
     column-span: all; // determino que meu elemento `h1` detro da `.minha_div` não obedecerá as regras de colunas.
}

```
Ainda não é muito utilizado esta opção por ter suporte fraco para navegadores mais antigos.

### Referência:
[W3C - multi-column ](http://www.w3schools.com/css/css3_multiple_columns.asp)
------ FIM do artigo ------ 