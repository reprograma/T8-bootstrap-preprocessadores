# T8-bootstrap-sass

[AULA 01 - 07/10](#aula-1---0710) | 
[AULA 02 - 08/10](#aula-2---0810) |
[AULA 03 - 09/10](#aula-3---0910) |
[AULA 04 - 10/10](#aula-4---1010) |

# Bootstrap
## Documentação 
[Documentação do Bootstrap PT/BR](https://getbootstrap.com.br/docs/4.1/getting-started/introduction/)

---

## Instalação
### Instalação por CDN
- O que é CDN?

    **CDN (Content Delivery Network, ou Rede de Entrega de Conteúdo)** é uma rede de distribuição de informação, cujo objetivo é entregar conteúdo Web de forma mais rápida a usuários geograficamente dispersos.

    A **CDN** é composta de servidores espalhados geograficamente pelo globo terrestre, com o conteúdo a ser acessado sendo replicado e distribuído por todas essas máquinas. O usuário é então conduzido ao servidor que contém aquele conteúdo e tem condições de respondê-lo mais rapidamente. Ou seja, o servidor mais próximo. O conteúdo sai do servidor original e cópias suas são disponibilizadas em outros servidores ao redor do mundo, conforme haja demanda o acesso é feito a partir do servidor mais próximo do cliente, economizando tempo e dinheiro.

    Existem várias redes **CDN**, e qualquer empresa pode contratar o serviço de uma para seu sistema, essa decisão normalmente é tomada levando em conta vários aspectos como ganhos de performance, segurança e custos.

- Como instalar o Bootstrap via CDN no seu projeto?

    A instalação por **CDN** é a maneira mais rápida de instalar o Bootstrap no seu projeto, sem a necessidade de baixar os arquivos e adicioná-los no seu diretório. 

    **Copie e cole o arquivo de estilo abaixo, dentro da sua `<head>` antes de todos os outros arquivos de estilo para carregar o CSS.**

    ```
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css"  integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
    ```

    **Muitos dos componentes do Bootstrap precisam de JavaScript para funcionar. Mais especificamente, eles precisam do jQuery, Popper.js e de seus próprios plugins JavaScript. Coloque os `<script>`s abaixo, perto do final da sua página, logo antes do fechamento da tag `</body>`. O `<script>` jQuery tem que vir antes, depois o Popper.js e só depois os plugins de JavaScript do Bootstrap.**

    ```
    <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js" integrity="sha384-ZMP7rVo3mIykV+2+9J3UJ46jBk0WLaUAdn689aCwoqbBJiSnjAK/l8WvCWPIPm49" crossorigin="anonymous"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js" integrity="sha384-ChfqqxuZUCnJSK3+MXmPNIyE6ZbWh2IMqE241rYiqJxyMiZ6OW/JmZQ5stwEULTy" crossorigin="anonymous"></script>
    ```

### Instalação por download
[Link para download dos arquivos](https://getbootstrap.com.br/docs/4.1/getting-started/download/)

1. Faça o download do diretório zipado no endereço acima
2. Entre em `./css` copie o arquivo de nome `bootstrap.min.css` e cole dentro da pasta `./style` do projeto
3. Entre em `./js` copie o arquivo de nome `bootstrap.min.js` e cole dentro da pasta `./js` do projeto
4. Vamos fazer o download do arquivo `jquery-3.4.1.min.js` no site do [jQuery](https://jquery.com/download/) na versão **"minificada"** (ou __minified__) [aqui](https://code.jquery.com/jquery-3.4.1.min.js) e salvá-lo dentro na pasta `./js` do projeto

![salvar-como-jquery](/imagens/salvar-como-jquery.jpg)

5. Agora vamos linkar o arquivo `jquery-3.4.1.min.js` no `<html>` do projeto, perto do final da sua página, logo antes do fechamento da tag `</body>`
6. Agora vamos linkar os arquivo do Bootstrap no `<html>` do projeto: o arquivo `bootstrap.min.css` deve ser colocado antes de qualquer outro arquivo de estilo e o `bootstrap.min.js` deve vir depois do arquivo `jquery-3.4.1.min.js`

### Instalação via npm (extra!)

---

## Conteúdo que vamos abordar :)

- [ ] [Navbar](https://getbootstrap.com.br/docs/4.1/components/navbar/)
- [ ] [Carousel](https://getbootstrap.com.br/docs/4.1/components/carousel/) 
- [ ] [Flex](https://getbootstrap.com.br/docs/4.1/utilities/flex/)
- [ ] [Texto](https://getbootstrap.com.br/docs/4.1/utilities/text/)
- [ ] [Alinhamento](https://getbootstrap.com.br/docs/4.1/utilities/vertical-align/)
- [ ] [Cores](https://getbootstrap.com.br/docs/4.1/utilities/colors/)
- [ ] [Espeçamento](https://getbootstrap.com.br/docs/4.1/utilities/spacing/)
- [ ] [Cards](https://getbootstrap.com.br/docs/4.1/components/card/)
- [ ] [Grid](https://getbootstrap.com.br/docs/4.1/layout/grid/)
- [ ] [Modal](https://getbootstrap.com.br/docs/4.1/components/carousel/)

---

## Aula 1 - 07/10
- O que é Bootstrap?

    O Bootstrap é um [framework](https://tableless.github.io/iniciantes/manual/js/o-que-framework.html) front-End intuitivo, para o desenvolvimento web mais rápido e eficaz. O Bootstrap foi desenvolvido por Mark Otto e Jacob Thornton no Twitter. Foi lançado como um produto de seu código aberto em agosto de 2011 no GitHub.

- Prós e contras 

    Prós | Contras
    --------- | ------
    Conjunto de componentes extenso | Visual Padrão
    Funcionamento | 
    Responsividade | 
    Experiência do Usuário | 
    Acessibilidade com uso de classes | 

- **data-toggle** e **data-target**

    O **data-toggle** é um atributo de dados do HTML5 que liga automaticamente o elemento ao tipo correspondente.

    ```html
    <div class="dropdown">
    <a class="dropdown-toggle" data-toggle="dropdown" href="#">Dropdown trigger</a>
    <ul class="dropdown-menu" role="menu" aria-labelledby="dLabel">
        <li><a href="#">Item</a></li>
    </ul>
    </div>

    Alguns outros elementos que são mais comumente usados:

    data-toggle="modal"
    data-toggle="collapse"
    data-toggle="dropdown"
    data-toggle="tab"

    ```

    O **data-target** geralmente utilizado no Bootstrap. Pelo próprio nome, subentende-se que irá fazer referência ao seu alvo, objetivo. Este atributo deve conter um seletor CSS que aponte para o elemento HTML que irá participar do evento.

    ```html
    <button type="button" class="btn btn-primary btn-lg" data-toggle="modal" data-target="#myModal">
    Launch demo modal
    </button>

    <!-- Modal -->
    <div class="modal fade" id="myModal" tabindex="-1" role="dialog" aria-labelledby="myModalLabel">
    <div class="modal-dialog" role="document">
        <div class="modal-content">
        <div class="modal-header">
            <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
            <h4 class="modal-title" id="myModalLabel">Modal title</h4>
        </div>
        <div class="modal-body">
            ...
        </div>
        <div class="modal-footer">
            <button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
            <button type="button" class="btn btn-primary">Save changes</button>
        </div>
        </div>
    </div>
    </div>

    ```

    Entenda mais sobre os atributos **data-*** no artigo abaixo:
    - [Tudo que você precisa saber sobre o atributo Data do HTML5](https://webdesign.tutsplus.com/pt/tutorials/all-you-need-to-know-about-the-html5-data-attribute--webdesign-9642)

- Display **grid**

    Entenda mais sobre o display **grid** no guia abaixo:
    - [Guia CSS Grid Layout](https://www.origamid.com/projetos/css-grid-layout-guia-completo/)

---

## Aula 2 - 08/10

### Começando o nosso projeto 
1. Faça o download deste repositório [reprograma/T8-bootstrap-preprocessadores](https://github.com/reprograma/T8-bootstrap-preprocessadores)
2. Crie um novo repositório no seu Github seguindo esse modelo de nome: **seu-nome.github.io**
2. Copie a pasta clonada `./portfolio-nome`
4. Renomeie com o seu nome
5. Entre no diretório `./portfolio-nome`
6. [Instale](#instalação) o Bootstrap no arquivo `<html>` do projeto
7. Abra a [documentação](#documentação) do Bootstrap no seu navegador
8. #boracomeçar!

### Portfólio ♡  
- Quais componentes vamos construir?
    - [ ] Navbar
    - [ ] Carousel
    - [ ] Seção - Habilidade e Sobre
    - [ ] Seção - Meus projetos
    - [ ] Footer

- Como ele vai ficar?

![portfolio-nome](/imagens/portfolio-nome.png)

---

# Sass
## Documentação 
[Documentação do Sass](http://www.sass-lang.com/documentation)

---

## Instalação
### Instalação via npm

Para instalarmos o **Sass** via **npm**, precisamos verificar se a nossa máquina possui o **node.js** instalado, é só rodar no seu terminal o comando `node -v`, se ele não apresentar a versão assim `v10.15.3` é só baixar ele [aqui!](https://nodejs.org/en/)

[O que é npm? - Introdução básica para iniciantes](https://www.hostinger.com.br/tutoriais/o-que-e-npm)

### Instalando o Sass

1. No terminal, entre no diretório do seu projeto e rode o comando `npm init` responda ao comando, logo após será gerado um arquivo `package.json`

    ![instalando-sass-npm-init](/imagens/instalando-sass-npm-init.jpg)

2. Ainda no terminal instale o sass através do comando `npm install sass --save-dev`, será gerado um arquivo `package-lock.json` e uma pasta `./node_modules`

    ![instalando-sass-npm-install](/imagens/instalando-sass-npm-install.jpg)

3. Crie um arquivo `.gitignore` junto aos arquivos `.json` com a seguinte linha de texto dentro:

    ![instalando-sass-gitignore](/imagens/instalando-sass-gitignore.jpg)

4. Agora vamos estruturar as pastas da seguinte maneira: 

    ![instalando-sass-estrutura-pastas](/imagens/instalando-sass-estrutura-pastas.jpg)

5. Vamos fazer um teste, dentro do arquivo `_base` adicionameremos uma propriedade `background-color: black` ao `<html>` e em seguida iremos importá-lo no arquivo `style.scss` assim: 

    ![instalando-sass-import](/imagens/instalando-sass-import.jpg)

6. Vamos adicionar o script `"sass styles/style.scss styles/style.css"` no arquivo `package.json`

    ![instalando-sass-script](/imagens/instalando-sass-script.jpg)

7. Agora é só rodar no terminal o comando `npm run sass` e ele irá compilar o arquivo gerando um arquivo `style.css`

    ![instalando-sass-compiler](/imagens/instalando-sass-compiler.jpg)

8. Caso queira que o arquivo seja compilado de modo automático é só rodar o seguinte comando `sass --watch styles/style.scss styles/style.css`

--- 

## Conteúdo que vamos abordar :)

- [ ] Imports
- [ ] Partials
- [ ] Aninhamento
- [ ] Variáveis
- [ ] Mixins e includes - com parâmetro
- [ ] Mixins e includes - sem parâmetro
- [ ] Placeholders e extends
- [ ] Funções

## Aula 3 - 09/10

- Quais as vantagens de usar o Sass?

    * Evitar duplicação de código
    * Código Limpo
    * Funcionalidades que o css não possui
    * Manutenção

### Começando a configurar o nosso ambiente!

1. Faça o download deste repositório [reprograma/T8-bootstrap-preprocessadores](https://github.com/reprograma/T8-bnomeootstrap-preprocessadores)
5. Entre no diretório `./pasta-do-projeto`, utilize o seu terminal através do comando `cd pasta-do-projeto`
3. **Tenha a certeza de estar dentro da pasta** `./pasta-do-projeto`
6. Agora vamos [instalar](#instalando) o Sass 

## Aula 4 - 10/10

- Partials

Para modularizar nosso código e deixar mais fácil de configurar, conseguimos separar em arquivos chamados **partials**, que são pedaços de css separados em arquivos e que recebem um **_** no começo do nome, para que o Sass entenda que não deve gerar o código no css, só quando chamarmos por **@import**.

![sass-partials](/imagens/sass-partials.PNG)

- Imports

Para fazer com que os nossos partials sejam gerados no css é necessário importá-los no arquivo **.scss** principal.

**Lembrando que a ordem que a gente chama os @imports é a ordem que será gerado no css.**

![imports-sass](/imagens/imports-sass.PNG)

- Aninhamento

`.scss`

![navegacao--scss](/imagens/navegacao--scss.PNG)

`.css`

![navegacao--css](/imagens/navegacao--css.PNG)

- Variáveis

`.scss`

![vars--example](/imagens/vars--example.PNG)

`.css`

![vars--example-css](/imagens/vars--example--css.PNG)

- Mixins | @include

    * sem parâmetros:

    ![mixin--sem-parametros](/imagens/mixin--sem-parametros.PNG)

    * com parâmetros: 

    ![mixin--com-parametros-sem-valor-padrao](/imagens/mixin--com-parametros-sem-valor-padrao.PNG)

    * com parâmetros e valor padrão: 

    ![mixin--com-parametros-com-valor-padrao](/imagens/mixin--com-parametros-com-valor-padrao.PNG) 

- Placeholders | @extends

    ![placeholder-height-display](/imagens/placeholder-height-display.PNG)

    ![placeholdercall-height-display](/imagens/placeholdercall-height-display.PNG)

- Mixin vs. Placeholders

    Assim como o **mixin**, os **placeholders** também são trechos de código que podemos reutilizar, mas se ele faz a mesma coisa que o mixin, por que utilizarmos?

    ![mixin-height-display](/imagens/mixin-height-display.PNG)

    ![mixincall-height-display](/imagens/mixincall-height-display.PNG)

    * Resultado Mixin

    ![banner-destination-css](/imagens/banner-destination-css.PNG)

    * Resultado Placeholder

    ![ideal-css](/imagens/ideal-css.PNG)

    **Não podemos criar placeholders com parâmetros, como fazemos com os mixins.**

- Funções de cores

    * `darken($color, $amount)` > `darken(black, 20%)`
    * `lighten($color, $amount)` > `darken(#829dad, 70%)`
    
- Funções com números

    Funções, diferente dos mixins, retornam valores, e não trechos de código.

    ![mixin-adapta](/imagens/mixin-adapta.PNG)

    Quando chamado no `.scss` >

    `@include adapta-tamanho(2);`

    Resultado no `.css` >

    `height: 32px;`

    ![funcao-adapta](/imagens/funcao-adapta.PNG)

    Quando chamada no `.scss` >

    `margin-top: adapta-tamanho(2);`

    Resultado no `.css` >

    `margin-top: 32px;`