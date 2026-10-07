# Anotações — Café Aurora

## Estrutura do projeto

O projeto foi organizado desta forma:

```text
cafe-aurora/
├── index.html
├── style.css
├── script.js
├── estudos/
│   └── anotacoes.md
└── assets/
    └── images/
```

- `index.html`: estrutura e conteúdo da página.
- `style.css`: aparência, cores, espaçamentos e responsividade.
- `script.js`: interações da página.
- `assets/images/`: imagens utilizadas no site.
- `estudos/`: anotações pessoais sobre o desenvolvimento.

## HTML

HTML é responsável pela estrutura da página.

### Estrutura básica

```html
<!DOCTYPE html>
<html lang="pt-BR">
```

O `DOCTYPE` informa que estamos utilizando HTML5.

O atributo `lang="pt-BR"` indica que o conteúdo da página está em português do Brasil.

### Head

Dentro do `<head>` ficam informações importantes da página, como:

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Café Aurora</title>
```

O `charset` permite trabalhar corretamente com caracteres especiais.

O `viewport` ajuda a página a funcionar corretamente em celulares.

O `<title>` define o nome exibido na aba do navegador.

### Links internos

Usei links como:

```html
<a href="#cardapio">Cardápio</a>
```

O `#cardapio` faz o navegador levar o usuário até o elemento que possui:

```html
id="cardapio"
```

Isso também foi utilizado para criar a navegação entre as seções da página.

### Imagens

As imagens foram adicionadas utilizando:

```html
<img src="assets/images/cafe-espresso.jpg" alt="Café espresso">
```

O `src` indica o caminho da imagem.

O `alt` descreve a imagem e também ajuda na acessibilidade.

### Classes

Usei classes para identificar elementos que precisam receber estilos no CSS:

```html
<section class="hero">
```

No CSS, essa classe pode ser selecionada utilizando:

```css
.hero {
}
```

## CSS

CSS é responsável pela aparência da página.

### Reset

Usei:

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

Isso ajuda a remover espaçamentos padrão do navegador e facilita o controle dos tamanhos dos elementos.

### Cores

O projeto utiliza uma paleta inspirada em café:

- marrom escuro;
- marrom médio;
- creme;
- bege;
- tons claros para o fundo.

Exemplo:

```css
background-color: #3b2920;
```

### Flexbox

O menu de navegação utiliza Flexbox:

```css
.navbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
}
```

`display: flex` coloca os elementos em um layout flexível.

`justify-content: space-between` distribui os elementos pelo espaço disponível.

`align-items: center` alinha os elementos verticalmente.

### Grid

Os produtos do cardápio utilizam CSS Grid:

```css
.products {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
}
```

Isso permite organizar os produtos em três colunas no desktop.

### Responsividade

Foi utilizado:

```css
@media (max-width: 768px) {
}
```

Esse recurso permite aplicar estilos diferentes quando a tela fica menor.

No celular, os produtos passam de três colunas para uma:

```css
.products {
    grid-template-columns: 1fr;
}
```

## JavaScript

O JavaScript foi utilizado para criar o menu mobile.

Primeiro, os elementos foram selecionados:

```javascript
const menuButton = document.querySelector(".menu-button");
const navLinks = document.querySelector(".nav-links");
```

Depois foi criado um evento para detectar o clique:

```javascript
menuButton.addEventListener("click", () => {
    navLinks.classList.toggle("active");
});
```

Quando o botão é clicado, a classe `active` é adicionada ou removida.

No CSS existe uma regra para mostrar o menu quando essa classe está presente:

```css
.nav-links.active {
    display: flex;
}
```

## Caminho das imagens

As imagens ficam dentro de:

```text
assets/images/
```

Por isso, no HTML o caminho utilizado é:

```html
src="assets/images/nome-da-imagem.jpg"
```

É importante prestar atenção ao nome do arquivo e às pastas, porque um caminho incorreto faz a imagem não aparecer.

## Live Server

Usei o Live Server no VS Code para visualizar o projeto no navegador enquanto desenvolvia.

Isso facilita porque consigo alterar o código e visualizar as mudanças rapidamente no navegador.

## Git

Git é utilizado para controlar as versões do projeto.

Alguns comandos importantes:

```bash
git status
```

Mostra o estado atual dos arquivos.

```bash
git add .
```

Adiciona as alterações para o próximo commit.

```bash
git commit -m "mensagem"
```

Cria uma versão registrada do projeto.

```bash
git push
```

Envia as alterações para o GitHub.

## O que aprendi neste projeto

- Criar a estrutura de uma página utilizando HTML.
- Organizar um projeto em diferentes arquivos.
- Utilizar classes e IDs.
- Criar navegação entre seções.
- Inserir imagens locais.
- Estilizar uma página utilizando CSS.
- Utilizar Flexbox.
- Utilizar CSS Grid.
- Criar uma página responsiva.
- Utilizar Media Queries.
- Criar uma interação simples com JavaScript.
- Utilizar o Live Server no VS Code.
- Organizar imagens dentro do projeto.
- Trabalhar com Git e GitHub.

## Próximos estudos

Depois deste projeto, quero continuar estudando:

- JavaScript;
- manipulação do DOM;
- formulários;
- animações com CSS;
- acessibilidade;
- Git e GitHub;
- consumo de APIs;
- integração entre frontend e backend.