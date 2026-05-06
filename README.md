# CheatSheet: Desenvolvimento Web (HTML, CSS, e JavaScript)

**Nome:** Robert William Dettenborn

### Estrutura Básica Padrão
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8"> <! Suporte a caracteres especiais (ascentos, etc.) >
    <title>Título da página</title> <! Título na aba do navegador >
    <meta name="description" content="descrição legal da minha página"> <! Responsividade >
    <meta name="author" content="Robert"> <! Responsividade >
    <meta name="keywords" content="html, css, js"> <! Responsividade >

    <link rel="stylesheet" href="style.css"> <! Usado para ascessar/vincular outro arquivos do programa>
    <link rel="manifest" href="manifest.json"> <! Usado para ascessar/vincular outro arquivos do programa>
</head>
<body>
    <! O conteúdo visível da página vai aqui >
</body>
</html>
```
###Tags mais usadas
```html
<h1> a <h6>: <h1> Título </h1> ... <h6> </h6> <! Usados para Títulos, sendo h1 o mais importante >
<p>: <p> Texto </p> <! Usando para Parágrafos de texto >
<a>: <a href="https://google.com" target="_blank">Google</a> <! Usado para Links >
<img>: <img src="caminho.jpg" alt="Descrição acessível"> <! usado para idicionar uma imagem no programa (pode ser feita por um arquivo local ou um link web)>
<div>: <div id=""></div> <! Um conteiner genérico para agrupar elementos>
<span>: <p>O botão de emergência é <span style="color: red; font-weight: bold;">vermelho</span> e não deve ser apertado.</p> <! Um conteiner para textos pequenos (inline)>
<form>: <form action="/processar-login" method="POST"> </form> <! Usada para criar um formulário interativo >


```
