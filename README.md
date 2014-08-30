# Meetup de NodeJS - NodeBR

## Apresentando o Node.js por [Giovanni Bassi](https://twitter.com/giovannibassi)

* O NodeJS tem somente **5 anos** e foi criado em 2009 por Ryal Dahl.
* A instalação do Node.js é bastante simples em praticamente todos os sistemas operacionais.
    * Linux
        * Utilizar o gerenciador de pacotes padrão de sua distribuição como **apt-get** ou **yum**. 
        * Utilizar o Node Version Manager ou **NVM** para ** gerenciar as versões ** do NodeJS.
    * Mac
        * Utilizar o gerenciador de pacotes como o `brew`
        * Utilizar o **NVM** 
        * Utilizar o instalador
    * Windows
        * Utilizar o instalador
* Utilizar o NVM é muito **prático** e **útil** para manter diferentes versões.
* As versões **pares** são as **estáveis** (0.8 e 0.10) e **ímpares** são **instáveis** (0.11).
* Na versão 0.11 já existe algumas novidades do ECMAScript 6.
* Primeiro contato é feito com o REPL digitando `node` no terminal.
* Pode-se utilizar CoffeeScript digitando `coffee` no terminal.
* Não existe padrão para módulos em JavaScript e no NodeJS utiliza-se o CommonJS.
* Usar `module.exports` para declarar e consumir módulos.

```
module.exports = {
    soma: function (a,b) { return a + b; }
}

```
* O Node possui módulos nativos e escrito em JavaScript e são síncronos
* Path, Console, HTTP, Streams, Eventos, OS, etc.
* Utiliza-se pacotes para a distribuição de módulos através no NPM. Ou seja, um pacote é uma reunião de vários módulos.
* Utiliza-se o SemVer.
* O registro é aberto e todos podem instalar e registrar modulos.
* Os pacotes são sempre locais
* Os pacotes globais ficam instalados num diretório específico.
* Não recomenda-se instalar pacotes globais para o desenvolvimento de aplicações. E pacotes globais são uma péssima idéia.
* Globais somente ferramentas como `coffee`, `grunt`, `gulp`, `mocha`.
* O arquivo `package.json` é usado para definir um móulo
* Informa nome, versão, repositoório do Github, as dependências, autor, licença.
* O sistema de pacotes locais permite diferentes versoes e dependencias e subdependencias.

```
    /app
        /node_modules
            /dep_a
                /dep_z (v1)
            /dep_b
                /dep_z (v2)
```
* Para iniciar um módulo ou projeto utiliza-se o comando `npm init`.
* Instalar todas as dependências do projeto utiliza-se o comando `npm install`.
* Para instalar um módulo utiliza-se o comando `npm install <module>` ou `npm install <module> --save` .
* Utiliza-se `NodeJS` para criar **tarefas automatizadas** que anteriormente poderia ser escritas em **Shell Script**.
* Utilizar o #/hashbang para crs
* Iniciar o servidor com node <arquivo.js>, altera o arquivo e reiniciar a aplicacao.
* Isso pode ficar chato, apara isso iso use o nodemon `npm install nodemon -g`.
* Existe um debugger natico, acessivel via linha de comando.
* `node debug script.js`.
* Complexo de usar, quase ninguém usa.
* Melhor delegar a uma ferramenta terceira.
* A natureza assincrona do JavaScrpt torna os testes mais dificeis de escrever
    * Usa-se callback e promisses para resolver o problema
* Uma série de frameworks existem e atualmente o mais utilizado é o Mocha.
* Desde testes de unidade simples,ate testes integrados ou de front-end
* ´xiste bastante IDEs WebStorm ou VIM, Sublime Text2 e fluxo de trabalho envolve alguns terminais abertos e editor de texto
* Utilizar automatizador de tarefas para tarefas que são executadas com frequência como build, deploy, tests, compilacao.
* As principais ferramentas são o Grunt (mais conhecido e utilizado) e o Gulp (mais novo e com versões inovadoras).
* Não versione dependências ou nao versione o diretorio node_moduls.
* Se precisar saber exatamente o que rodar utiliza o `npm shinkwrap`.
* Não versione pacotes de front-end também (deixe o trabalho para o Bower)
* Se tiver usando um transpilars nao versione o JS.
* Rodando em producao
    * NodeJS nao é multi-thread entao deve-se utilizar varias instanacias
    * para gerenciar isso, é complexo
    * Se cair ele nao sobe sozinho
    * Ele é independente do APache
* Mitos
    * node nao escala -> muitas empresas utilizam bastante.
    * nao fazer coisas que dependam de alto uso de CPU. 
    * Pode-se utilizar CoffeeScript, TypeScript e Clojure.
    * 
* O NodeJS utilza threads não-bloqueantes e isso é muito bom para o desempenho favorecendo aplicações realtime, por exemplo.

## Node.js para frontenders por [Paulo Pires](https://twitter.com/paulo_hp)

* O NodeJS é uma ferramenta interessante pois permite executar JS no servidor, hardware ou desktop.
* É importante conhecer a diferença entre o JavaScript executado no servidor e no navegador.
* O 
* Como renderizar pagina estatica
* Ferramentas de FE
* No node nao existe onload, getElementElement, 
* Cria-se um arquivo `script.js` e para publicar `npm publish`.
* É muito fácil publicar e utilizar um módulo em NodeJS.
* 

## Why frameworks por [Guilherme de Souza](https://twitter.com/_Gui_Souza)

## Dúvidas

* 