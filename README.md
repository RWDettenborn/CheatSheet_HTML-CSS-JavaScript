# CheatSheet: Desenvolvimento Web (HTML, CSS, e JavaScript)

---

**Nome:** Robert William Dettenborn

**Objetivo:** Guia de referência rápida com os principais conceitos de HTML, CSS, JavaScript e fundamentos da Web.

---

## HTML (HyperText Markup Language)

### Estrutura Básica

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

---

### Tags Mais Usadas

| Tag | Descrição | Exemplo de Uso |
|:---:|---|---|
| `<h1>` a `<h6>` | Títulos (Headings), sendo h1 o mais importante. | `<h1>Título Principal</h1>` |
| `<p>` | Parágrafo de texto. | `<p>Este é um texto.</p>` |
| `<a>` | Link (Hyperlink). O atributo `href` define o destino. | `<a href="https://github.com">GitHub</a>` |
| `<img>` | Imagem. Requer `src` (caminho) e `alt` (texto alternativo). | `<img src="foto.jpg" alt="Minha foto">` |
| `<div>` | Contêiner genérico para agrupar elementos (block-level). | `<div class="container">...</div>` |
| `<span>` | Contêiner genérico em linha (inline). | `<span>Texto destacado</span>` |
| `<ul>` / `<ol>`| Listas não-ordenadas (com marcadores) e ordenadas (números). | `<ul><li>Item 1</li></ul>` |

---

## Formulários e Inputs Básicos
```html
<!-- Formulário básico com método e ação -->
<form action="/enviar-dados" method="POST">
    <!-- Rótulo para o campo de texto -->
    <label for="nome">Nome:</label>
    <input type="text" id="nome" name="nome" placeholder="Digite seu nome" required>
    
    <label for="senha">Senha:</label>
    <input type="password" id="senha" name="senha" required>

    <!-- Botão de submissão -->
    <button type="submit">Enviar</button>
</form>
```
### Boas Práticas em HTML
*   **Semântica:** Use tags como `<header>`, `<nav>`, `<main>`, `<article>`, `<section>` e `<footer>` em vez de usar `<div>` para tudo. Isso melhora o SEO e a acessibilidade.
*   **Acessibilidade (a11y):** Sempre inclua o atributo `alt` nas imagens.
*   **Indentação:** Mantenha o código bem indentado para facilitar a leitura.
---

## CSS (Cascading Style Sheets)
### Seletores Principais

| *Seletor*    | *Sintaxe*            | *O que seleciona*                       |
| :----------: | ------------------ | ------------------------------------- |
| `Tag`        | p { }              | Todos os elementos <p>                |
| `Classe`     | .minha-classe { }  | Elementos com class="minha-classe"    |
| `ID`         | #meu-id { }        | O elemento único com id="meu-id"      |
| `Universal`  | * { }              | Todos os elementos da página          |

---

### Propriedades Essenciais e Box Model

```css
/* Reseta margens e define o modelo de caixa padrão */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box; /* O padding e a borda não aumentam o tamanho total do elemento */
}

body {
    background-color: #f4f4f4; /* Cor de fundo */
    color: #333; /* Cor do texto */
    font-family: Arial, sans-serif; /* Tipografia */
    font-size: 16px; /* Tamanho da fonte */
}

.caixa {
    width: 100%; /* Largura */
    max-width: 1200px; /* Largura máxima */
    margin: 20px auto; /* Margem: 20px em cima/baixo, centralizado nas laterais */
    padding: 15px; /* Espaçamento interno (entre a borda e o conteúdo) */
    border: 1px solid #ccc; /* Borda: espessura, estilo, cor */
}
```

---

### Layout: Flexbox vs Grid

**Flexbox (Unidimensional - Linhas ou Colunas):**
Ideal para alinhar itens dentro de um contêiner.

```css
.flex-container {
    display: flex; /* Ativa o flexbox */
    flex-direction: row; /* Alinha em linha (padrão). Use 'column' para empilhar */
    justify-content: center; /* Alinhamento no eixo principal (horizontal, neste caso) */
    align-items: center; /* Alinhamento no eixo transversal (vertical) */
    gap: 10px; /* Espaçamento entre os itens (Flex gap) */
}
```

---

**CSS Grid (Bidimensional - Linhas e Colunas):**
Ideal para a estrutura geral da página.

```css
.grid-container {
    display: grid; /* Ativa o grid */
    grid-template-columns: repeat(3, 1fr); /* Cria 3 colunas de tamanhos iguais */
    grid-template-rows: auto; /* A altura da linha se adapta ao conteúdo */
    gap: 20px; /* Espaçamento entre colunas e linhas */
}
```

---

### Boas Práticas (CSS)

*   **Mobile First:** Escreva o CSS base para telas pequenas e use `@media queries` para adaptar para telas maiores.
*   **Evite `!important`:** Tente resolver conflitos de estilo através da especificidade dos seletores, não forçando com `!important`.
*   **Organização:** Agrupe estilos relacionados e mantenha um padrão de nomenclatura (ex: BEM - *Block, Element, Modifier*).

---

## JavaScript (Interatividade, lógica e dinamismo para a página)

### Variáveis e Tipos de Dados

```javascript
// 'const' para valores que não mudam (Constantes)
const nome = "Robert"; 

// 'let' para valores que podem ser reatribuídos
let idade = 25; 

// Tipos comuns
const ehProgramador = true; // Boolean
const habilidades = ["HTML", "CSS", "JS"]; // Array
const usuario = { nome: "Robert", role: "Dev" }; // Objeto
```

---

### Funções

```javascript
// Função tradicional
function somar(a, b) {
    return a + b;
}

// Arrow Function (Sintaxe mais moderna e concisa)
const multiplicar = (a, b) => {
    return a * b;
};

// Arrow Function com retorno implícito (uma linha)
const subtrair = (a, b) => a - b;
```

---

### Manipulação do DOM e Eventos

```html
<!-- HTML de exemplo para manipulação -->
<button id="meu-botao">Clique Aqui</button>
<p id="mensagem"></p>
```

```javascript
// 1. Selecionando elementos do HTML (DOM)
const botao = document.querySelector("#meu-botao");
const texto = document.getElementById("mensagem");

// 2. Adicionando um "Ouvinte de Evento" (Event Listener)
botao.addEventListener("click", () => {
    // 3. Modificando o conteúdo e o estilo do elemento
    texto.innerHTML = "<strong>Botão clicado!</strong> Olá, mundo!";
    texto.style.color = "green";
    
    // 4. Manipulando classes CSS
    texto.classList.add("destaque"); // Adiciona uma classe ao parágrafo
});
```
---

### Boas Práticas (JavaScript)
*   **Uso de `let` e `const`:** Abandone o uso de `var` para evitar problemas de escopo global e içamento (*hoisting*).
*   **Nomenclatura:** Use *camelCase* para variáveis e funções (ex: `minhaVariavel`, `calcularTotal`).
*   **Console limpo:** Remova os `console.log()` do código de produção.

---

## Outros Conceitos (PWA, Cache, Web)
### Como a Internet Funciona (Básico)
*   **Cliente:** O navegador do usuário (Chrome, Firefox) que faz a requisição.
*   **Servidor:** O computador remoto onde os arquivos do site estão hospedados.
*   **HTTP/HTTPS:** O protocolo de comunicação. O *HTTPS* garante que os dados enviados entre cliente e servidor sejam criptografados.

---

### Armazenamento no Navegador (Web Storage)
Permite salvar dados diretamente no navegador do usuário, sem precisar de um banco de dados no servidor para informações simples.

```javascript
// 1. LocalStorage (Os dados não expiram, mesmo fechando a aba)
localStorage.setItem("tema", "dark");
const temaAtual = localStorage.getItem("tema");

// 2. SessionStorage (Os dados são apagados quando a aba/janela é fechada)
sessionStorage.setItem("token", "12345xyz");
```

---

### PWA (Progressive Web Apps)
São aplicações web que utilizam tecnologias modernas para oferecer uma experiência de aplicativo nativo no navegador (podem ser instaladas no celular/PC e funcionar offline).
*   **Web App Manifest:** Um arquivo JSON (`manifest.json`) que informa ao navegador sobre a aplicação (nome, ícones, cor de fundo), permitindo a instalação.
*   **Service Workers:** Scripts em JavaScript que rodam em segundo plano no navegador. São eles que interceptam requisições de rede, permitindo fazer cache de arquivos para **funcionamento Offline** e o envio de notificações Push.

---

### Exemplo básico de registro de um Service Worker
```javascript
if ('serviceWorker' in navigator) {
  window.addEventListener('load', () => {
    navigator.serviceWorker.register('/sw.js')
      .then(registration => console.log('SW registrado com sucesso!'))
      .catch(err => console.log('Falha ao registrar SW', err));
  });
}
```

---
