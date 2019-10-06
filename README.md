# T8-bootstrap-sass

# Bootstrap
## Documentação 
[Documentação do Bootstrap PT/BR](https://getbootstrap.com.br/docs/4.1/getting-started/introduction/)

## Instalação
### Instalação por CDN
- O que é CDN?

    **CDN (Content Delivery Network, ou Rede de Entrega de Conteúdo)** é uma rede de distribuição de informação, cujo objetivo é entregar conteúdo Web de forma mais rápida a usuários geograficamente dispersos.

    A **CDN** é composta de servidores espalhados geograficamente pelo globo terrestre, com o conteúdo a ser acessado sendo replicado e distribuído por todas essas máquinas. O usuário é então conduzido ao servidor que contém aquele conteúdo e tem condições de respondê-lo mais rapidamente. Ou seja, o servidor mais próximo. O conteúdo sai do servidor original e cópias suas são disponibilizadas em outros servidores ao redor do mundo, conforme haja demanda o acesso é feito a partir do servidor mais próximo do cliente, economizando tempo e dinheiro.

    Existem várias redes **CDN**, e qualquer empresa pode contratar o serviço de uma para seu sistema, essa decisão normalmente é tomada levando em conta vários aspectos como ganhos de performance, segurança e custos.

- Como instalar o Bootstrap no seu projeto?

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

- Percorrendo a documentação
- data-toggle e data-target

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

## Aula 2 - 08/10
### Começando o nosso projeto 
1. Clone o repositório
2. Entre no diretório `./portfolio-nome`
3. [Instale](#instalação) o Bootstrap no arquivo `<html>` do projeto
4. Abra a [documentação](#documentação) do Bootstrap no seu navegador
5. #boracomeçar!

### Portfólio ♡  
- Quais componentes vamos construir?
    - [ ] Navbar
    - [ ] Formulário de contato
    - [ ] Carousel de fotos
    - [ ] Seção - Quem sou
    - [ ] Seção - Habilidades
    - [ ] Cards - Meus projetos
    - [ ] Footer

# Sass
## Aula 3 - 09/10
## Aula 4 - 10/10

[link do layout 1](https://dribbble.com/shots/7158635-TheHub-Website-Exploration-01)
[link do layout 2](https://dribbble.com/shots/3937735-Payment-Interaction)