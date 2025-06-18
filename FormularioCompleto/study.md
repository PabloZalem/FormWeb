# SOBRE A CRIACAO DO FORMULARIO

## SOBRE O CORPO DO INDEX.HTML

Temos duas formas criar um cabeçalho padrao na criacao do arquivo.html
Primeira forma: Podemos entrar no arquivo.html e dando um ponto de exclamacao(!), onde criará o padrao
Segunda forma: Ao entrar no arquivo.html, escrever html e podemos dar enter e criaremos o cabeçalho padrão do html

Nosso código ira se desenvolver dentro da tag body: Qual a funcao da tag body?
A tag body ela define o **corpo deo documento**. Dentro dela que todo conteúdo visível de uma página web é inserido, como textos, imagens, vídeos, links, tabelas, formulários e outros elementos interativos:

``` Exemplo
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Exemplo de Página</title>
</head>
<body>
  <h1>Bem-vindo!</h1>
  <p>Este é um exemplo de conteúdo dentro da tag body.</p>
</body>
</html>
```

## Sobre o a tag link

A tag <link> no HTML é usada para estabelecer uma conexão entre o documento HTML e recursos externos, como folhas de estilo (CSS), ícones ou fontes. Ela é colocada dentro da seção <head> do documento e não exibe conteúdo diretamente na página.

### Principais funcoes da tag<link>

1. Incorporar folhas de estilo externas:
    - É a função mais comum, permitindo que o HTML utilize arquivos CSS externos para estilizar a página.

    ```Exemplo
    <link rel="stylesheet" href="estilos.css">
    ```

2. Definir ícones da página (favicon):
    - Especifica o ícone que aparece na aba do navegador ou nos favoritos.

    ```Exemplo
    <link rel="icon" href="favicon.ico" type="image/x-icon">
    ```

3. Importar fontes ou outros recursos:
    - Pode ser usada para carregar fontes personalizadas ou outros tipos de arquivos.

    ```Exemplo
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet">
    ```

### Atributos comuns

- rel: Define o tipo de relação entre o documento e o recurso (ex.: stylesheet, icon, preconnect).
- href: Especifica o caminho ou URL do recurso externo.
- type: Define o tipo de arquivo (opcional, como text/css para CSS).

## SOBRE O ARQUIVO.CSS

### O QUE É

Um arquivo CSS (Cascading Style Sheets) é usado para estilizar elementos de uma página web, definindo cores, fontes, espaçamentos, layouts e outros aspectos visuais.
Ele pode ser criado separadamente com a extensão .css e vinculado ao HTML para manter a organização e reutilização do código.

```Exemplo de um arquivo CSS básico:
/* Estilo para o corpo da página */
body {
  font-family: Arial, sans-serif;
  background-color: #f4f4f4;
  margin: 0;
  padding: 0;
}

/* Estilo para títulos */
h1 {
  color: #333;
  text-align: center;
}

/* Estilo para parágrafos */
p {
  color: #666;
  line-height: 1.6;
  margin: 10px 20px;
}

/* Estilo para links */
a {
  color: #007BFF;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}
```

### COMO VINCULAR O CSS AO HTML

```Vincular
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de CSS</title>
  <link rel="stylesheet" href="estilos.css">
</head>
<body>
  <h1>Bem-vindo!</h1>
  <p>Este é um exemplo de página estilizada com CSS.</p>
  <a href="#">Clique aqui</a>
</body>
</html>
```

### O USO DO BOX-SIZING NO CSS

O uso de box-sizing no arquivo CSS é uma prática comum para controlar como o tamanho de elementos é calculado, incluindo ou excluindo o padding e a borda no cálculo total da largura e altura

```Exemplo básico de box-sizing no CSS:
/* Define box-sizing para todos os elementos */
* {
  box-sizing: border-box;
}

/* Exemplo de estilo para um elemento */
.container {
  width: 300px;
  padding: 20px;
  border: 5px solid #333;
  background-color: #f4f4f4;
}
```

### EXPLICAÇÃO

1. box-sizing: border-box;:
    - Inclui o padding e a border no cálculo total da largura e altura do elemento.
    - Isso facilita o controle do layout, evitando que o elemento ultrapasse o tamanho definido.

2. Aplicacao glocal(*)
    - Aplicar box-sizing: border-box, a todos os elementos e uma pratica recomendada para manter consistência no layout

3. Resultado
    - No exemplo acima, a largutra total do .container sera 300px ja que o padding e a border estao incluidos no cálculo.

### MARGIN

a propriedade margin é usada para definir o espaço externo ao redor de um elemento.

1. Definir uma margem uniforme

```Exemplo
div {
  margin: 20px; /* Aplica 20px de margem em todos os lados */
}
```

2. Definir margens específicas para cada lado

```Exemplo
div {
  margin-top: 10px;    /* Margem superior */
  margin-right: 15px;  /* Margem direita */
  margin-bottom: 20px; /* Margem inferior */
  margin-left: 25px;   /* Margem esquerda */
}
```

3. Usar a notação abreviada

```Exemplo
div {
  margin: 10px 15px 20px 25px; /*Ordem: cima, direita, baixo, esquerda*/
}
```

4. Margem automática para centralizar. Se o elemento tiver um valor de largura (width) definido, você pode usar margin: auto para centralizá-lo horizontalmente:

```Exemplo
div {
  width: 50%;       /*Define a largura do elemento */
  margin: 0 auto;   /* Centraliza horizontalmente*/
}
```

5. Remover margens

```Exemplo
div {
  margin: 0; /*Remove todas as margens*/
}
```

### PADDING

No arquivo CSS, a propriedade padding é usada para definir o espaçamento interno de um elemento, ou seja, o espaço entre o conteúdo do elemento e sua borda. Você pode especificar o padding de forma geral ou individualmente para cada lado (superior, direito, inferior, esquerdo). Aqui estão alguns exemplos:

1. Definir o padding para todos os lados

```Exemplo
.elemento {
  padding: 20px; /* Aplica 20px de espaçamento em todos os lados */
}
```

2. Definir o padding para lados específicos

```Exemplo
.elemento {
  padding-top: 10px;    /* Espaçamento superior */
  padding-right: 15px;  /* Espaçamento à direita */
  padding-bottom: 20px; /* Espaçamento inferior */
  padding-left: 25px;   /* Espaçamento à esquerda */
}
```

3. Usar valores abreviados
Você pode usar até quatro valores para o padding:

```Exemplo
.elemento {
  padding: 10px 15px 20px 25px;
  /* Ordem: superior, direita, inferior, esquerda */
}
```

4. Valores abreviados com menos números
Dois valores: O primeiro é para superior/inferior, o segundo para direita/esquerda.

```Exemplo
padding: 10px 20px; /* 10px em cima e embaixo, 20px nos lados */
Três valores: O primeiro é para o topo, o segundo para os lados, o terceiro para a parte inferior.
padding: 10px 20px 30px; /* 10px em cima, 20px nos lados, 30px embaixo */
```

5. Usar unidades diferentes
Você pode usar unidades como px, %, em, rem, etc.:

```Exemplo
.elemento {
  padding: 5%; /* Espaçamento relativo ao tamanho do elemento pai */
}
```

### <div class="container>

O atributo class em HTML é usado para atribuir uma ou mais classes a um elemento, permitindo que ele seja estilizado ou manipulado por CSS e JavaScript. Quando você vê algo como div class="container", significa que a div está sendo identificada com a classe chamada "container".

Explicação:

1. div: É uma tag HTML usada para criar divisões ou seções na página. Ela é um contêiner genérico para agrupar outros elementos.

2. class="container": A classe "container" é um nome arbitrário, geralmente usado para indicar que essa div serve como um contêiner principal para organizar o conteúdo da página.

```Exemplo
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Container</title>
  <style>
    .container {
      width: 80%;
      margin: 0 auto;
      background-color: #f0f0f0;
      padding: 20px;
      border: 1px solid #ccc;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Bem-vindo!</h1>
    <p>Este é um exemplo de um contêiner estilizado com CSS.</p>
  </div>
</body>
</html>
```

### <section class="header>

A expressão <section class="header"> em HTML e CSS refere-se a uma seção de conteúdo que está sendo estilizada ou identificada com a classe header. A tag <section> é usada para agrupar conteúdo relacionado em uma página. Quando você adiciona o atributo class="header", está atribuindo uma classe chamada header a essa seção.

```Exemplo HTML
<section class="header">
  <h1>Bem-vindo ao meu site</h1>
  <p>Esta é a seção de cabeçalho.</p>
</section>
```

Pode usar a classe header para estilizar essa seção. Por exemplo, pode alterar a cor de fundo, o tamanho da fonte, o espaçamento, etc.

```Exemplo CSS
.header {
  background-color: #f4f4f4;
  color: #333;
  padding: 20px;
  text-align: center;
}
```

```Exemplo
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Section Header</title>
  <style>
    .header {
      background-color: #6200ea;
      color: white;
      padding: 20px;
      text-align: center;
    }
  </style>
</head>
<body>
  <section class="header">
    <h1>Minha Página</h1>
    <p>Este é o cabeçalho estilizado com CSS.</p>
  </section>
</body>
</html>
```

### <form id="form" class="form">

1. <form> em HTML: O elemento <form> é usado para criar um formulário em uma página web

```Exemplo
<form action="/enviar-dados" method="post">
  <label for="nome">Nome:</label>
  <input type="text" id="nome" name="nome">
  <button type="submit">Enviar</button>
</form>
```

- action: Define para onde os dados do formulário serão enviados.
- method: Especifica o método HTTP usado para enviar os dados (geralmente GET ou POST).

2. id no formulário: O atributo id é usado para identificar de forma única um elemento HTML, incluindo o <form>.

```Exemplo
<form id="meuFormulario">
  <input type="text" name="email" placeholder="Digite seu e-mail">
</form>
```

3. class formulario: O atributo class é usado para aplicar estilos (CSS) ou agrupar elementos com características semelhantes. Diferente do id, a class pode ser compartilhada por vários elementos.

```Exemplo
<form class="formulario-estilizado">
  <input type="text" name="nome" placeholder="Digite seu nome">
</form>
```

Aplicando o CSS:

```Exemplo
.formulario-estilizado {
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 5px;
}
```