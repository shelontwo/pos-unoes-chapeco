#### Unoesc Chapecó
#### Pós-graduação em Desenvolvimento Web, Cloud e dispositivos móveis - WebMob
#### Disciplina: HTML5+CSS3
#### Professor: Jean Carlo Nascimento
#### Acadêmico(a): Evandro Diego Erlo
### Artigo de revisão de CSS3

<h1>Funcionalidades CSS3 </h1>

##### Funcionalidade: border-image
##### O que é?
Esta propriedade é utilizada para adicionar uma imagem de borda em elementos da página.
##### Onde usar:
Em qualquer elemento que disponibilize o atributo border-image.
##### Como usar:
São 3 propriedades definidas para a imagem de borda:
1 - URL / Caminho da imagem.
2 - O tamanho que a imagem ficará na borda em relação a seu tamanho original.
3 - Específica se a imagem vai se repetir na borda ou será esticada para o tamanho total da borda.
```css
.minha_div{
        border: xy;
        border-image: url(<source>) <size>  <type>;
}
```
##### Exemplo de uso
A sintaxe para aplicar a <code>border-image</code> completa seria da seguinte forma:

```css
.minha_div{
        border: 10px; // definimos o tamanho da borda
        border-image: url(image.jpg) 10% stretch; // definimos que a <code>image.jpg</code> irá ser usada 10% do seu tamanho original e será esticada para preencher os espaçõs da borda do elemento.
}

```
### Referencia:
[http://www.w3schools.com/css/css3_border_images.asp](W3C - border-image)



------ FIM do artigo ------