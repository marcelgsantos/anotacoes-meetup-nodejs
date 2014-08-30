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
* O primeiro contato com o Node.js pode ser feito através do REPL digitando `node` no terminal.
* Pode-se utilizar CoffeeScript digitando `coffee` no terminal.
* Não existe padrão estabelecido para módulos em JavaScript. No NodeJS utiliza-se o **CommonJS**.
* Utiliza-se `module.exports` para declarar e consumir módulos.

```
module.exports = {
    soma: function (a,b) { return a + b; }
}
```
* O Node.js possui **módulos nativos** e escrito em JavaScript. Os módulossão síncronos.
* alguns exemplos de módulos são Console, HTTP, Streams, Eventos, OS, etc.
* Utiliza-se **pacotes** para a **distribuição de módulos** através no NPM. 
* Um pacote é uma reunião de vários módulos.
* Para o **versionamento** dos módulos utiliza-se o Semantic Versioning.
* O registro de módulos é **aberto** e todos podem **registrar** e **instalar** módulos.
* Nas aplicações recomenda-se utilizar **pacotes locais**.
* Os **pacotes globais** ficam instalados num diretório específico.
* Utiliza-se **pacotes globais** somente ferramentas como `coffee`, `grunt`, `gulp`, `mocha`.
* Utiliza-se o arquivo `package.json` para a definição de um módulo.
* No `package.json` informa-se nome, versão, repositório, dependências, autor, licença.
* O sistema de **pacotes locais** permite diferentes versões para um mesmo pacote.

```
/app
    /node_module
        /dep_a
            /dep_z (0.5)
        /dep_b
            /dep_z (0.9)
```
* Para iniciar um módulo ou projeto utiliza-se o comando `npm init`.
* Instalar todas as dependências do projeto utiliza-se o comando `npm install`.
* Para instalar um módulo utiliza-se o comando `npm install <module>` ou `npm install <module> --save` .
* Utiliza-se `NodeJS` para criar **tarefas automatizadas** que anteriormente poderia ser escritas em **shell script**.
* Para rodar uma aplicação em Node.js basta iniciar o servidor. Após cada alteração do arquivo é necessário reiniciar a aplicação.
* Para automatizar este processo utiliza-se o nodemon que pode ser instalado através do comando `npm install nodemon -g`.
* O Node.js possui um **debugger** nativo acessível via linha de comando. Ele é um pouco complexo e quase ninguém usa.
* É recomendável delegar o processo de debugger a uma ferramenta terceira.
* A **natureza assíncrona** do JavaScript torna alguns testes mais difíceis de escrever.
* Usa-se **callback** e **promises** para resolver o problema.
* Existem várias ferramentas de **testes** para Node.js. Atualmente a mais utilizada é o **Mocha**.
* Existem ferramentas para testes de **unidade**, **integrados** ou de **aceitação**.
* Existem várias IDEs e **editores** para desenvolver em Node.js ou JavaScript como WebStorm, VIM, Sublime Text e fluxo de trabalho envolve algumas janelas de **terminais** abertas.
* Recomenda-se utilizar um **automatizador de tarefas** para tarefas que são executadas com frequência como build, deploy, testes, compilação entre outros.
* As principais ferramentas de automatização de tarefas são o Grunt (mais conhecido e utilizado) e o Gulp (mais novo e com versões inovadoras).
* Recomenda-se não versionar o diretório `node_modules` ou dependências.
* Se precisar saber exatamente o que rodar utiliza-se o comando `npm shinkwrap`.
* Recomenda-se não versionar **pacotes de front-end**, este tarefa deve ser delegada ao Bower.
* Recomenda-se também não versionar o JavaScript gerado por *transpilers*.
* Para rodar o Node.js em produção é necessário levar em consideração:
    * o Node.js não é multi-thread então deve-se utilizar várias instâncias
    * o gerenciamento é um pouco complexo e utiliza-se ferramentas para o gerenciamento
    * Ele é independente do servidor web
* Alguns mitos de como o Node.js **não escala** é refutado observando sua utilização nas empresas.
* Recomenda-se não fazer coisas que dependam de alto uso de CPU. 
* Pode-se utilizar várias linguagens CoffeeScript, TypeScript e Clojure.
* O NodeJS utiliza **threads** não-bloqueantes e isso é muito bom para o **desempenho** como em aplicações realtime, por exemplo.

## Node.js para frontenders por [Paulo Pires](https://twitter.com/paulo_hp)

* O NodeJS é uma ferramenta interessante pois permite executar JS no servidor, hardware ou desktop.
* É importante conhecer a diferença entre o JavaScript executado no servidor e no navegador.
* É bastante utilizado em ferramentas de front-end como Grunt, Gulp e Bower.
* No Node.js não existe métodos e eventos de navegadores como `onload`, `getElementById` entre outros. 
* Utiliza-se o comando `npm publish` para publicar um pacote do Node.js.
* É muito fácil publicar e utilizar um módulo em NodeJS.

## Why frameworks por [Guilherme de Souza](https://twitter.com/_Gui_Souza)

* No começo era difícil encontrar referências sobre Node.js.
* Problemas iniciais e insegurança com servidores web, conexão com banco de dados, servir arquivos estáticos.
* **Frozen spots** são pedaços de códigos que não devem ser alteradas.
* **Hot spots** são pedaços de códigos que devem ser alterados.
* Benefícios de utilizar um **framework** para desenvolvimento:
    * possui uma **organização** pré-definida
    * utiliza a arquitetura MVC
    * facilita a conexão com o banco de dados, criar modelos e rotas
* **Code Activism**
* **Expose Yourself** e publique seu código no GitHub.
* **Ordine** é uma biblioteca para enfileiramento de callbacks.

##  Linha de comando por [Marcos Bergamo](https://twitter.com/mvbergamo)

* Para utilizar o Node.js em linha de comando basta adicionar o `#!/usr/bin/env node`.
* O Node.js fornece os objetos como `process` por padrão para utilização.
* Utilizar o Node.js no terminal é uma tarefa bem fácil e possui diversos módulos que facilitam estas tarefas.

## Testando com Node.js por [Ciro Costa](https://twitter.com/cirowrc)

* É **importante** testar as aplicações.
* Ao corrigir um bug, cinco outros nascem.
* O JavaScript é dinâmica, fracamente tipada e bastante aberta. Neste, liberdade pode levar a problemas.
* Esforços para melhorar com padrões, bibliotecas e testes.
* O teste compara o **estado** e **comportamento** do produto contra oráculos.
* Para quê testar?
    * Feedback rápido
        * ao alterar alguma coisa, saber se tudo **continua** funcionando da maneira esperada
    * Incerteza
        * **diminui a incerteza** com os testes, pois dados os parâmetros testa-se os resultados
        * ao encontrar algum erro não coberto, adiciona-se nos testes e realiza a implementação
    * Design de código
        * Ao começar testando, promove-se a melhor **arquitetura do código**
    * Regressão
        * Evitar **regressão** do código ao consertar um problema e aparecer cinco outros 
    * Documentação
        * Os testes funcionam como **documentação** pois eles sempre estarão atualizados pois fazem parte do *workflow* de desenvolvimento
* O **Mocha** é o test runner e o **Chai** é a biblioteca das asserções.
* **Asserções** são afirmações para verificar um verdade.
* O `describe()` é o agrupamento dos testes.
* O `it()` coloca-se as **especificações**, ou seja, onde são verificadas as asserções.
* Coloca-se a quantidade de **espectativas** necessárias para organização dos seus testes.
* Em Node.js o primeiro argumento dos callbacks são **sempre erros** e os restantes são os valores retornados.
* O Mocha parte do princípio que seus callbacks **não** devem **demorar** mais que um período de tempo definido.
* Para navegadores utiliza-se o Jasmine e QUnit.
* Pode-se utilizar o Mocha e Chai no **navegador** e realiza as configurações para informar o "sabor" dos testes que está realizando.
* O Mocha realiza vários tipos de **verificações** vazamento de memória, variáveis globais entre outros.
* O **Karma** é utilizado para realizar testes com navegadores como Chrome, Firefox e PhantomJS.
* Utiliza-se o SinonJS e espiões para fazer testes com Ajax.
* O método `beforeEach()` é um método de setup para o SinonJS preparar os testes.
* Pode-se utilizar o **Protractor** para testes de interface com AngularJS.
* Todo código é **testável** e pode ser automatizado com o Grunt ou Gulp.

## Introdução ao MongoDB e Node.js [Jean Carlo Nascimento](twitter.com/osuissa)

* MongoDB é um banco de dados NoSQL.
* É feito em C++ e usa o V8 como engine de JavaScript.
* Não possui um esquema (**schemaless**) e é delegado para a aplicação.
* Não possui junções em MongoDB.
* Possui sharding, réplicas e GridFS.
* Ele pode ser instalado com o **binário** ou através de **gerenciador de pacotes**.
* Utiliza-se o comando `mongo` para acessar a linha de comando do MongoDB.
* Cria-se a **base de dados** e pode-se adicionar **coleções**.
* O JavaScript é case sensitive e necessita de **expressão regular** para consultas.
* Recomenda-se utilizar o Mongoose como middleware entre o MongoDB e o NodeJS.
* Para instalar o Mongoose utiliza-se o comando `npm install mongoose --save`. 
* Pode-se utilizar um ouvinte da conexão do Mongoose para `connected`, `disconnected`, `open`, `error` entre outras.

```javascript
mongoose.connection.on("connected", function(){
    console.log("Conectado!");
});
```
* Para criar o esquema no Mongoose.

```javascript
    var Schema = mongoose.Schema;
    var BeerSchema = new Schema({
        name: {type: String, default: ''},
        description: {type: String, default: ''},
        abv: {type: Number, min: 0},
        created_at: {type: Date, default: Date.now}
    });
```
* Para criar um modelo no Mongoose.

```javascript
var BeerModel = mongoose.model('Beer', BeerSchema);

var dados = {};
var beer = new BeerModel(dados);
beer.save(function(error, data){
    // ...
});

BeerModel.find({}, function(err, data) {
    // ...
});

BeerModel.remove({_id: a1sasdhjb34b23jhb432});
```