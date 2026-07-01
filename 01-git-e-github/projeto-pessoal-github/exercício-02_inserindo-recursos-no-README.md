# Exercício 02 - Inserindo recursos no README 

## :link: Um link para um site
Para adicionar links para ir à determinado site, basta colocar o nome do site ou texto em que queira botar o link entre `[]` (colchetes) e o url entre `()` (parênteses), seguindo este método:
```
[Exemplo](https://exemplo.com)
```
Resultado:

[GitHub](https://github.com)

---

## :pushpin: Um link para outro arquivo do projeto
Para adicionar um link para ir à outro arquivo do mesmo projeto, basta copiar e adicionar o endereço do arquivo ao lugar da url:
```
[Texto linkável sobre o arquivo](nome-do-arquivo.md)
```
Exemplo:
```
[Veja como melhorar o visual do seu README no GitHub no Exercício 1](exercício-01_melhorando-o-visual-do-readme.md)
```
Resultado:

[Veja como melhorar o visual do seu README no GitHub no Exercício 1](exercício-01_melhorando-o-visual-do-readme.md)

---

## :framed_picture: Uma imagem

Para inserir uma imagem do projeto dentro do arquivo deve-se adicionar um imagem no mesmo projeto, ir até nele e copiar seu endereço, e adicionar o `!` antes do `[]` (para o markdown entender que se trata de uma imagem e inserí-la no `arquivo.md`) e o endereço dentro dos `()`:

```
[Texto sobre a imagem](imagens/imagem.jpeg)
```

Exemplo:

```
Veja a imagem com todos os ![Comandos Git](../imagens/Comandos_Git_Guia.jpeg).
```
Veja a imagem com todos os Comandos do Git (clique na imagem para ir ao diretótio da imagem):

![Comandos Git](../imagens/Comandos_Git_Guia.jpeg).

Este *Exercício 02* está em `01-git-e-github/projeto-pessoal-github/`, e a imagem está em `01-git-e-github/imagens/Comandos_Git_Guia.jpeg`, logo será nescessário **voltar uma pasta** com o `..` (dois pontos).

Se a imagem estivesse na mesma pasta do *Exercício 02*, seria apenas `[Veja o guia de Comandos Git](Comandos_Git_Guia.jpeg)`.

Se a imagem a ser inserida for externa, basta usar a mesma base, mas usando o endereço da imagem nos `()`:

![GitHub]([https://th.bing.com/th/id/R.d602152f52d405b512e104738a5d3554?rik=pRfd7kygN1ZV9A&pid=ImgRaw&r=0](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/12/gitHub.png))

Caso não queira inserir a imagem em seu `arquivo.md`, basta tirar o `!` no início que o link estará em texto:
```
[Exemplo](url.png)
```
Resultado:

![GitHub]([https://th.bing.com/th/id/R.d602152f52d405b512e104738a5d3554?rik=pRfd7kygN1ZV9A&pid=ImgRaw&r=0](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/12/gitHub.png))

---

## :page_facing_up: Um arquivo PDF;

Basta adicionar o endereço do pdf nos `()`:

```
Veja o [PDF do projeto](../pdf/projeto-pessoal-github.pdf).
```

Resultado:

Veja o [PDF do projeto](../pdf/projeto-pessoal-github.pdf).

---

## :sparkler: Um GIF.
Da mesma forma que se adiciona uma imagem:
```
![Nya Cat](../gif/nyan-cat-animated.gif)
```

Resultado:

![Nya Cat](../gif/nyan-cat-animated.gif)
