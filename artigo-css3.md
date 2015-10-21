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
### Referencia:
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
### Referencia:
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
### Referencia:
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
### Referencia:
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

### Referencia:
[W3C - transform](http://www.w3schools.com/css/css3_2dtransforms.asp)



------ FIM do artigo ------