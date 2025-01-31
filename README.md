## console.
<table>
<thead>
<tr>
<th>Comando</th>
<th>Descrição</th>
<th>Exemplo</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>assert(expression, message)</code></td>
<td>Envia uma mensagem quando <code>expression</code> é avaliado como <strong>falso</strong>.</td>
<td><code>console.assert((x == 1), &quot;assert message: x != 1&quot;);</code></td>
</tr>
<tr>
<td><code>clear()</code></td>
<td>Limpa as mensagens da janela do console, incluindo mensagens de erro de script, e limpa também o script exibido na janela do console. Não limpa o script inserido no prompt de entrada do console.</td>
<td><code>console.clear();</code></td>
</tr>
<tr>
<td><code>count(title)</code></td>
<td>Envia o número de vezes que o comando count foi chamado para a janela do console. Cada chamada do comando count é identificada exclusivamente pelo <code>title</code>opcional.<br><br> A entrada existente na janela do console é identificada pelo parâmetro <code>title</code> (se presente) e atualizada pelo comando count. Não é criada uma nova entrada.</td>
<td><code>console.count();</code><br><br> <code>console.count(&quot;inner loop&quot;);</code></td>
</tr>
<tr>
<td><code>debug(message)</code></td>
<td>Envia <code>message</code> para a janela do console.<br><br> Esse comando é idêntico a console.log.<br><br> Os objetos transmitidos usando o comando são convertidos em um valor de cadeia de caracteres.</td>
<td><code>console.debug(&quot;logging message&quot;);</code></td>
</tr>
<tr>
<td><code>dir(object)</code></td>
<td>Envia o objeto especificado para a janela do console e o exibe em um visualizador de objetos. Você pode usar o visualizador para inspecionar propriedades na janela do console.</td>
<td><code>console.dir(obj);</code></td>
</tr>
<tr>
<td><code>dirxml(object)</code></td>
<td>Envia o nó XML <code>object</code> especificado para a janela do console e o exibe como uma árvore de nós XML.</td>
<td><code>console.dirxaml(xmlNode);</code></td>
</tr>
<tr>
<td><code>error(message)</code></td>
<td>Envia <code>message</code> para a janela do console. O texto da mensagem está em vermelho e antecedido por um símbolo de erro.<br><br> Os objetos transmitidos usando o comando são convertidos em um valor de cadeia de caracteres.</td>
<td><code>console.error(&quot;error message&quot;);</code></td>
</tr>
<tr>
<td><code>group(title)</code></td>
<td>Inicia um agrupamento das mensagens enviadas à janela do console e envia o <code>title</code> opcional como um rótulo de grupo. Os grupos podem ser aninhados e aparecer em um modo de exibição de árvore na janela do console.<br><br> Os comandos group* podem facilitar a exibição da saída da janela do console em alguns cenários, como quando um modelo de componente está em uso.</td>
<td><code>console.group(&quot;Level 2 Header&quot;);</code> <br> <code>console.log(&quot;Level 2&quot;);</code> <br> <code>console.group();</code> <br> <code>console.log(&quot;Level 3&quot;);</code> <br> <code>console.warn(&quot;More of level 3&quot;);</code> <br> <code>console.groupEnd();</code> <br> <code>console.log(&quot;Back to level 2&quot;);</code> <br> <code>console.groupEnd();</code> <br> <code>console.debug(&quot;Back to the outer level&quot;);</code></td>
</tr>
<tr>
<td><code>groupCollapsed(title)</code></td>
<td>Inicia um agrupamento das mensagens enviadas à janela do console e envia o <code>title</code> opcional como um rótulo de grupo. Os grupos enviados usando <code>groupCollapsed</code> aparecem em uma exibição recolhida por padrão. Os grupos podem ser aninhados e aparecer em um modo de exibição de árvore na janela do console.</td>
<td>O uso é o mesmo do comando <code>group</code>.<br><br> Consulte o exemplo do comando <code>group</code>.</td>
</tr>
<tr>
<td><code>groupEnd()</code></td>
<td>Encerra o grupo atual.<br><br> Requisitos:<br><br> Visual Studio 2013</td>
<td>Consulte o exemplo do comando <code>group</code>.</td>
</tr>
<tr>
<td><code>info(message)</code></td>
<td>Envia <code>message</code> para a janela do console. A mensagem é prefaciada por um símbolo de informação.</td>
<td><code>console.info(&quot;info message&quot;);</code><br><br> Para obter mais exemplos, confira <a href="#ConsoleLog" data-linktype="self-bookmark">Formatando a saída do console.log</a> mais adiante neste tópico.</td>
</tr>
<tr>
<td><code>log(message)</code></td>
<td>Envia <code>message</code> para a janela do console.<br><br> Se você transmitir um objeto, este comando o enviará para a janela do console e o exibirá num visualizador de objeto. Você pode usar o visualizador para inspecionar propriedades na janela do console.</td>
<td><code>console.log(&quot;logging message&quot;);</code></td>
</tr>
<tr>
<td><code>msIsIndependentlyComposed(element)</code></td>
<td>Usado em aplicativos da Web. Sem suporte em aplicativos UWP usando JavaScript.</td>
<td>Não há suporte.</td>
</tr>
<tr>
<td><code>profile(reportName)</code></td>
<td>Usado em aplicativos da Web. Sem suporte em aplicativos UWP usando JavaScript.</td>
<td>Não há suporte.</td>
</tr>
<tr>
<td><code>profileEnd()</code></td>
<td>Usado em aplicativos da Web. Sem suporte em aplicativos UWP usando JavaScript.</td>
<td>Não há suporte.</td>
</tr>
<tr>
<td><code>select(element)</code></td>
<td>Seleciona o HTML especificado <code>element</code> no <a href="quickstart-debug-html-and-css?view=vs-2017" data-linktype="relative-path">Explorador do DOM</a>.</td>
<td>console.select(element);</td>
</tr>
<tr>
<td><code>time (name)</code></td>
<td>Inicia um temporizador que é identificado pelo parâmetro <code>name</code> opcional. Quando usado com <code>console.timeEnd</code>, calcula o tempo decorrido entre <code>time</code> e <code>timeEnd</code> e envia o resultado (medido em ms) ao console usando a cadeia de caracteres <code>name</code> como prefixo. Usado para habilitar a instrumentação de código do aplicativo para medir o desempenho.</td>
<td><code>console.time(&quot;app start&quot;);  app.start();  console.timeEnd(&quot;app start&quot;);</code></td>
</tr>
<tr>
<td><code>timeEnd(name)</code></td>
<td>Interrompe um temporizador que é identificado pelo parâmetro <code>name</code> opcional. Consulte o comando <code>time</code> do console.</td>
<td><code>console.time(&quot;app start&quot;); app.start(); console.timeEnd(&quot;app start&quot;);</code></td>
</tr>
<tr>
<td><code>trace()</code></td>
<td>Envia um rastreamento de pilha à janela do console. O rastreamento inclui a pilha de chamadas completa e informações como o nome do arquivo, o número da linha e o número da coluna.</td>
<td><code>console.trace();</code></td>
</tr>
<tr>
<td><code>warn(message)</code></td>
<td>Envia <code>message</code> para a janela do console, prefaciada por um símbolo de aviso.<br><br> Os objetos transmitidos usando o comando são convertidos em um valor de cadeia de caracteres.</td>
<td><code>console.warn(&quot;warning message&quot;);</code></td>
</tr>
</tbody>
</table>
<h2 id="miscellaneous-commands">Comandos variados</h2>
<p>Esses comandos também estão disponíveis na janela do Console do JavaScript (não estão disponíveis no código).</p>
<table>
<thead>
<tr>
<th>Comando</th>
<th>Descrição</th>
<th>Exemplo</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>$0</code>, <code>$1</code>, <code>$2</code>, <code>$3</code>, <code>$4</code></td>
<td>Retorna o elemento especificado para a janela do console. <code>$0</code> retorna o elemento selecionado atualmente no Explorador do DOM, <code>$1</code> retorna o elemento selecionado anteriormente no Explorador do DOM e assim por diante, até o quarto elemento selecionado anteriormente.</td>
<td>U$3</td>
</tr>
<tr>
<td><code>$(id)</code></td>
<td>Retorna um elemento por ID. Este é um comando de atalho para <code>document.getElementById(id)</code>, em que <code>id</code> é uma cadeia de caracteres que representa a ID do elemento.</td>
<td><code>$(&quot;contenthost&quot;)</code></td>
</tr>
<tr>
<td><code>$$(selector)</code></td>
<td>Retorna uma matriz de elementos que correspondem ao seletor especificado usando a sintaxe do seletor de CSS. Este é um comando de atalho para <code>document.querySelectorAll()</code>.</td>
<td><code>$$(&quot;.itemlist&quot;)</code></td>
</tr>
<tr>
<td><code>cd()</code><br><br> <code>cd(window)</code></td>
<td>Permite que você altere o contexto de avaliação da expressão, da janela de nível superior padrão da página para a janela do quadro especificado. Chamar <code>cd()</code> sem parâmetros reverte o contexto para a janela de nível superior.</td>
<td><code>cd();</code><br><br> <code>cd(myframe);</code></td>
</tr>
<tr>
<td><code>select(element)</code></td>
<td>Seleciona o elemento especificado no <a href="quickstart-debug-html-and-css?view=vs-2017" data-linktype="relative-path">Explorador do DOM</a>.</td>
<td><code>select(document.getElementById(&quot;element&quot;));</code><br><br> <code>select($(&quot;element&quot;));</code><br><br> <code>select($1);</code></td>
</tr>
<tr>
<td><code>dir(object)</code></td>
<td>Retorna um visualizador para o objeto especificado. Você pode usar o visualizador para inspecionar propriedades na janela do console.</td>
<td><code>dir(obj);</code></td>
</tr>
</tbody>
</table>

## JavaScript Básico

- VARIÁVEIS
   - Responsáveis por guardar dados na memória.
   - Inicia com a palavra var, let ou const
```js
var nome = 'André';
let idade = 28;
const possuiFaculdade = true;
COPIAR
EVITAM REPETIÇÕES
DRY (Don't repeat yourself)

var preco = 20;
var totalComprado = 5;
var precoTotal = preco * totalComprado;
```

- SINTAXE
   - Palavra chave var seguida do nome, sinal de igual e o valor.
```js
var nome = 'André';
var idade = 28;
var possuiFaculdade = true;
```

- VÍRGULA
   - Utilizei a vírgula para criar mais de uma variável, sem repetir a palavra chave var.
```js
var nome = 'André',
    idade = 28,
    possuiFaculdade = true;
```

- SEM VALOR
   - Pode declarar ela e não atribuir valor inicialmente.
```js
var precoAplicativo;
// retorna undefined
```

- NOME
   - Os nomes podem iniciar com $, _, ou letras.
   - Podem conter números mas não iniciar com eles
   - Case sensitive
      - nome é diferente de Nome
   - Não utilizar palavras reservadas
   - https://www.w3schools.com/js/js_reserved.asp
   - Camel case
      - É comum nomearmos assim: abrirModal
```js
NOME
// Inválido
var §nome;
var function;
var 1possuiFaculdade;

// Válido
var $selecionar;
var _nome;
var possuiFaculdadeNoExterior;
```

- DECLARAR
   - Erro ao tentar utilizar uma variável que não foi declarada.
```js
console.log(nome);
// retorna nome is not defined
```

- HOISTING
   - São movidas para cima do código, porém o valor atribuído não é movido.
```js
console.log(nome);
var nome = 'André';
// Retorna undefined

var profissao = 'Designer';
console.log(profissao);
// Retornar Designer
```

- MUDAR O VALOR ATRIBUÍDO
   - É possível mudar os valores atribuídos a variáveis declaradas com var e let. Porém não é possível modificar valores das declaradas com const
```js
var idade = 28;
idade = 29;

let preco = 50;
preco = 25;

const possuiFaculdade = true;
possuiFaculdade = false;
// Retorna um erro
```

- 7 TIPOS DE DADOS
   - Todos são primitivos exceto os objetos.
```js
var nome = 'André'; // String
var idade = 28; // Number
var possuiFaculdade = true; // Boolean
var time; // Undefined
var comida = null; // Null
var simbolo = Symbol() // Symbol
var novoObjeto = {} // Object
```

- Primitivos são dados imutáveis.
```js
VERIFICAR TIPO DE DADO
var nome = 'André';
console.log(typeof nome);
// retorna string
```

- typeof null retorna object

- STRING
   - Você pode somar uma string e assim concatenar as palavras.
```js
var nome = 'André';
var sobrenome = 'Rafael';
var nomeCompleto = nome + ' ' + sobrenome;
```

- STRING
   - Você pode somar números com strings, o resultado final é sempre uma string.
```js
var gols = 1000;
var frase = 'Romário fez ' + gols + ' gols';
COPIAR
ASPAS DUPLAS, SIMPLES E TEMPLATE STRING
'JavaScript é "super" fácil';
"JavaScript é 'super' fácil";
"JavaScript é \"super\" fácil";
`JavaScript é "super" fácil"`;
"JavaScript é "super" fácil"; // Inválido
```
   - Não necessariamente precisamos atribuir valores a uma variável


- TEMPLATE STRING
```js
var gols = 1000;
var frase1 = 'Romário fez ' + gols + ' gols';
var frase2 = `Romário fez ${gols} gols`; // Utilizando Template String
```
   - Você deve passar expressões / variáveis dentro de ${}


## JavaScript Assíncrono

- SÍNCRONO VS ASSÍNCRONO
   - Síncrono
      - Espera a tarefa acabar para continuar com a próxima.
   - Assíncrono
      - Move para a próximo tarefa antes da anterior terminar. O trabalho será executado no 'fundo' e quando terminado, será colocado na fila (Task Queue).
      - Exemplos
         - setTimeout, Ajax, Promises, Fetch, Async.

- NEW PROMISE()
   - Promise é uma função construtora de promessas. 
   - Existem dois resultados possíveis de uma promessa, ela pode ser resolvida, com a execução do primeiro argumento, ou rejeitada se o segundo argumento for ativado.

```js
const promessa = new Promise(function(resolve, reject) {
  let condicao = true;
  if(condicao) {
    resolve();
  } else {
    reject();
  }
});

console.log(promessa); // Promise {<resolved>: undefined}
```

- RESOLVE()
   - Podemos passar um argumento na função resolve(), este será enviado junto com a resolução da Promise.

```js
const promessa = new Promise(function(resolve, reject) {
  let condicao = true;
  if(condicao) {
    resolve('Estou pronto!');
  } else {
    reject();
  }
});

console.log(promessa); // Promise {<resolved>: "Estou pronto!"}
```

- REJECT()
   - Quando a condição de resolução da promise não é atingida, ativamos a função reject para rejeitar a mesma. 
   - Podemos indicar no console um erro, informando que a promise foi rejeitada.
```js
const promessa = new Promise(function(resolve, reject) {
  let condicao = false;
  if(condicao) {
    resolve('Estou pronto!');
  } else {
    reject(Error('Um erro ocorreu.'));
  }
});

console.log(promessa); // Promise {<rejected>: Error:...}
```

- THEN()
   - O poder das Promises está no método then() do seu protótipo.
   - O Callback deste método só será ativado quando a promise for resolvida. 
   - O argumento do callback será o valor passado na função resolve.
```js
const promessa = new Promise(function(resolve, reject) {
  let condicao = true;
  if(condicao) {
    resolve('Estou pronto!');
  } else {
    reject(Error('Um erro ocorreu.'));
  }
});

promessa.then(function(resolucao) {
  console.log(resolucao); // 'Estou pronto!'
});
```

- ASSÍNCRONO
   - As promises não fazem sentido quando o código executado dentro da mesma é apenas código síncrono. 
   - O poder está na execução de código assíncrono que executará o resolve() ao final dele.
```js
const promessa = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Resolvida');
  }, 1000);
});

promessa.then(resolucao => {
  console.log(resolucao); // 'Resolvida' após 1s
});
```

- THEN().THEN()
   - O método then() retorna outra Promise. Podemos colocar then() após then() e fazer um encadeamento de promessas. 
   - O valor do primeiro argumento de cada then, será o valor do retorno anterior.
```js
const promessa = new Promise((resolve, reject) => {
  resolve('Etapa 1');
});

promessa.then(resolucao => {
  console.log(resolucao); // 'Etapa 1';
  return 'Etapa 2';
}).then(resolucao => {
  console.log(resolucao) // 'Etapa 2';
  return 'Etapa 3';
}).then(r => r + 4)
.then(r => {
  console.log(r); // Etapa 34
});
```

- CATCH()
   - O método catch(), do protótipo de Promises, adiciona um callback a promise que será ativado caso a mesma seja rejeitada.
```js
const promessa = new Promise((resolve, reject) => {
  let condicao = false;
  if(condicao) {
    resolve('Estou pronto!');
  } else {
    reject(Error('Um erro ocorreu.'));
  }
});

promessa.then(resolucao => {
  console.log(resolucao);
}).catch(reject => {
  console.log(reject);
});
```

- THEN(RESOLVE, REJECT)
   - Podemos passar a função que será ativada caso a promise seja rejeitada, direto no método then, como segundo argumento.
```js
const promessa = new Promise((resolve, reject) => {
  let condicao = false;
  if(condicao) {
    resolve('Estou pronto!');
  } else {
    reject(Error('Um erro ocorreu.'));
  }
});

promessa.then(resolucao => {
  console.log(resolucao);
}, reject => {
  console.log(reject);
});
```

- FINALLY()
   - finally() executará a função anônima assim que a promessa acabar.
   - A diferença do finally é que ele será executado independente do resultado, se for resolvida ou rejeitada.
```js
const promessa = new Promise((resolve, reject) => {
  let condicao = false;
  if(condicao) {
    resolve('Estou pronto!');
  } else {
    reject(Error('Um erro ocorreu.'));
  }
});

promessa.then(resolucao => {
  console.log(resolucao);
}, reject => {
  console.log(reject);
}).finally(() => {
  console.log('Acabou'); // 'Acabou'
});
```

- PROMISE.ALL()
   - Retornará uma nova promise assim que todas as promises dentro dela forem resolvidas ou pelo menos uma rejeitada. 
   - A reposta é uma array com as respostas de cada promise.
```js
const login = new Promise(resolve => {
  setTimeout(() => {
    resolve('Login Efetuado');
  }, 1000);
});
const dados = new Promise(resolve => {
  setTimeout(() => {
    resolve('Dados Carregados');
  }, 1500);
});

const tudoCarregado = Promise.all([login, dados]);

tudoCarregado.then(respostas => {
  console.log(respostas); // Array com ambas respostas
});
```

- PROMISE.RACE()
   - Retornará uma nova promise assim que a primeira promise for resolvida ou rejeitada. Essa nova promise terá a resposta da primeira resolvida.
```js
const login = new Promise(resolve => {
  setTimeout(() => {
    resolve('Login Efetuado');
  }, 1000);
});
const dados = new Promise(resolve => {
  setTimeout(() => {
    resolve('Dados Carregados');
  }, 1500);
});

const carregouPrimeiro = Promise.race([login, dados]);

carregouPrimeiro.then(resposta => {
  console.log(resposta); // Login Efetuado
});
```

- FETCH API
   - Permite fazermos requisições HTTP através do método fetch(). Este método retorna a resolução de uma Promise. Podemos então utilizar o then para interagirmos com a resposta, que é um objeto do tipo Response.
```js
fetch('./arquivo.txt').then(function(response) {
  console.log(response); // Response HTTP (Objeto)
});
```

- RESPONSE
   - O objeto Response, possui um corpo com o conteúdo da resposta. Esse corpo pode ser transformado utilizando métodos do protótipo do objeto Response. Estes retornam outras promises.
```js
fetch('./arquivo.txt').then(function(response) {
  return response.text();
}).then(function(corpo) {
  console.log(corpo);
});
```

- SERVIDOR LOCAL
   - O fetch faz uma requisição HTTP/HTTPS. Se você iniciar um site local diretamente pelo index.html, sem um servidor local, o fetch não irá funcionar.
```js
fetch('c:/files/arquivo.txt')
.then((response) => {
  return response.text();
})
.then((corpo) => {
  console.log(corpo);
}); // erro
```

   - Se dermos um espaço após o objeto ou pularmos linha, o método continua funcionando.

- .JSON()
   - Um tipo de formato de dados muito utilizado com JavaScript é o JSON (JavaScript Object Notation), pelo fato dele possuir basicamente a mesma sintaxe que a de um objeto js. .json() transforma um corpo em json em um objeto JavaScript.
```js
fetch('https://viacep.com.br/ws/01001000/json/')
.then(response => response.json())
.then(cep => {
  console.log(cep.bairro, cep.logradouro);
});
```

- .TEXT()
   - Podemos utilizar o .text() para diferentes formatos como txt, json, html, css, js e mais.

```js
const styleElement = document.createElement('style');

fetch('./style.css')
.then(response => response.text())
.then(style => {
  styleElement.innerHTML = style;
  document.body.appendChild(styleElement);
});
```

- HTML E .TEXT()
   - Podemos pegar um arquivo inteiro em HTML, transformar o corpo em texto e inserir em uma div com o innerHTML. A partir dai podemos manipular esses dados como um DOM qualquer.
```js
const div = document.createElement('div');

fetch('./sobre.html')
.then(response => response.text())
.then(htmlBody => {
  div.innerHTML = htmlBody;
  const titulo = div.querySelector('h1');
  document.querySelector('h1').innerText = titulo.innerText;
});
```

- .BLOB()
   - Um blob é um tipo de objeto utilizado para representação de dados de um arquivo. O blob pode ser utilizado para transformarmos requisições de imagens por exemplo. O blob gera um URL único.
```js
const div = document.createElement('div');

fetch('./imagem.png')
.then(response => response.blob())
.then(imgBlob => {
  const blobUrl = URL.createObjectURL(imgBlob);
  console.log(blobUrl);
});
```

- .CLONE()
   - Ao utilizarmos os métodos acima, text, json e blob, a resposta é modificada. Por isso existe o método clone, caso você necessite transformar uma resposta em diferentes valores.
```js
const div = document.createElement('div');

fetch('https://viacep.com.br/ws/01001000/json/')
.then(response => {
  const cloneResponse = response.clone();
  response.json().then(json => {
    console.log(json)
  });
  cloneResponse.text().then(text => {
    console.log(text)
  });
});
```

- .HEADERS
   - É uma propriedade que possui os cabeçalhos da requisição. É um tipo de dado iterável então podemos utilizar o forEach para vermos cada um deles.
```js
const div = document.createElement('div');

fetch('https://viacep.com.br/ws/01001000/json/')
.then(response => {
  response.headers.forEach(console.log);
});
```

- .STATUS E .OK
   - Retorna o status da requisição. Se foi 404, 200, 202 e mais. ok retorna um valor booleano sendo true para uma requisição de sucesso e false para uma sem sucesso.
```js
const div = document.createElement('div');

fetch('https://viacep.com.br/ws/01001000/json/')
.then(response => {
  console.log(response.status, response.ok);
  if(response.status === 404) {
    console.log('Página não encontrada')
  }
});
```

- .URL E .TYPE
   - .url retorna o url da requisição. .type retorna o tipo da reposta.
```js
const div = document.createElement('div');

fetch('https://viacep.com.br/ws/01001000/json/')
.then(response => {
  console.log(response.type, response.url);
});

//types
// basic: feito na mesma origem
// cors: feito em url body pode estar disponível
// error: erro de conexão
// opaque: no-cors, não permite acesso de outros sites
```

- JSON
   - JavaScript Object Notation (JSON) é um formato de organização de dados, compostos por um conjunto de chave e valor. As aspas duplas são obrigatórias, tanto na chave quanto no valor quando este for uma string.
```json
{
  "id": 1,
  "nome": "Andre",
  "email": "andre@origamid.com"
}
```

- VALORES
   - Os valores podem ser números, strings, boolean, arrays, objetos e null.
```json
{
  "id": 1,
  "faculdade": true,
  "pertences": [
    "lapis",
    "caneta",
    "caderno"
  ],
  "endereco": {
    "cidade": "Rio de Janeiro",
    "pais": "Brasil"
  },
  "casado": null
}
```

- ARRAYS E OBJETOS
   - É comum possuirmos array's com objetos em cada valor da array. Cuidado para não colocar vírgula no último item do objeto ou array.
```json
[
  {
    "id": 1,
    "aula": "JavaScript",
    "tempo": "25min"
  },
  {
    "id": 2,
    "aula": "HTML",
    "tempo": "15min"
  },
  {
    "id": 3,
    "aula": "CSS",
    "tempo": "10min"
  }
]
```

- JSON.PARSE() E JSON.STRINGIFY()
   - JSON.parse() irá transformar um texto JSON em um objeto JavaScript. JSON.stringify() irá transformar um objeto JavaScript em uma string no formato JSON.

```js
const textoJSON = '{"id": 1, "titulo": "JavaScript", "tempo": "25min"}';
const textoOBJ = JSON.parse(textoJSON);

const enderecoOBJ = {
  cidade: "Rio de Janeiro",
  rua: "Ali Perto",
  pais: "Brasil",
  numero: 50,
}
const enderecoJSON = JSON.stringfy(enderecoOBJ);
```

- EXEMPLO REAL
   - Podemos guardar por exemplo no localStorage, uma string como valor de uma propriedade. 
   - E retornar essa string como um objeto.
```js
const configuracoes = {
  player: "Google API",
  tempo: 25.5,
  aula: "2-1 JavaScript",
  vitalicio: true,
}

localStorage.configuracoes = JSON.stringify(configuracoes);
const pegarConfiguracoes = JSON.parse(localStorage.configuracoes);
```

## APIs

- Um servidor, aplicativo, objeto JavaScript ou qualquer outra coisa que você interaja através de comandos. Ao digitar uma URL, estamos utilizando a API do browser para se comunicar com a API do servidor.
- Programação, isso significa que um comando irá encadear uma cadeia de eventos pré-definidos. O resultado esperado é geralmente o mesmo.
- A interface são os comandos criados para permitir a interação com a aplicação. Ex: 'VIOLAO'.toLowerCase() é um método que faz parte da interface do objeto String. A interação com a interface retorna um efeito / resposta.

- EXEMPLOS DE API'S
   - https://api.github.com/users/origamid
   - https://api.github.com/users/origamid/followers
   - Array / Element
   - [].map();
   - [].filter();
   - Element.classList;
   - Element.attributes;
   - Tempo
      - https://www.metaweather.com/api/location/455825/
      - https://github.com/toddmotto/public-apis

- HTTP
   - Hypertext Transfer Protocol é o protocolo utilizando para enviarmos/recebermos arquivos e dados na Web.
```js
fetch('https://pokeapi.co/api/v2/pokemon/')
.then(r => r.json())
.then(pokemon => {
  console.log(pokemon);
});
```

- URL E METHOD
   - Uma requisição HTTP é feita através de uma URL. O método padrão é o GET, mas existem outros como POST, UPDATE, DELETE, HEADER.
```js
const url = 'https://jsonplaceholder.typicode.com/posts/';
const options = {
  method: 'POST',
  headers: {
    "Content-Type": "application/json; charset=utf-8",
  },
  body: '"aula": "JavaScript"';
}

fetch(url, options);
.then(response => response.json())
.then(json => {
  console.log(json);
});
```

- METHOD
   - GET
      - Puxa informação, utilizado para pegar posts, usuários e etc.
   - POST
      - Utilizado para criar posts, usuários e etc.
   - PUT
      - Geralmente utilizado para atualizar informações.
   - DELETE
      - Deleta uma informação.
   - HEAD
      - Puxa apenas os headers.

- GET
   - GET irá puxar as informações da URL. Não é necessário informar que o método é GET, pois este é o padrão.
```js
const url = 'https://jsonplaceholder.typicode.com/posts/';
fetch(url, {
  method: 'GET'
})
.then(r => r.json())
.then(r => console.log(r))
```

- POST
   - POST irá criar uma nova postagem, utilizando o tipo de conteúdo especificado no headers e utilizando o conteúdo do body.
```js
const url = 'https://jsonplaceholder.typicode.com/posts/';

fetch(url, {
  method: 'POST',
  headers: {
    "Content-Type": "application/json; charset=utf-8",
  },
  body: '{"titulo": "JavaScript"}'
})
.then(r => r.json())
.then(r => console.log(r))
```

- PUT
   - PUT irá atualizar o conteúdo do URL com o que for informado no conteúdo do body.
```js
const url = 'https://jsonplaceholder.typicode.com/posts/1/';

fetch(url, {
  method: 'PUT',
  headers: {
    "Content-Type": "application/json; charset=utf-8",
  },
  body: '{"titulo": "JavaScript"}'
})
.then(r => r.json())
.then(r => console.log(r))
```

- HEAD
    - HEAD puxa apenas os headers. É uma requisição mais leve pois não puxa o body.
```js
const url = 'https://jsonplaceholder.typicode.com/posts/1/';

fetch(url, {
  method: 'HEAD',
})
.then(response => {
  response.headers.forEach(console.log);
  console.log(response.headers.get('Content-Type'));
});
```

- HEADERS
   - Cache-Control
       - Tempo que o arquivo deve ficar em cache em segundos. Ex: public, max-age=3600
   - Content-Type
       - Tipo de conteúdo. Ex: text/html; charset=utf-8. Indicar o tipo de arquivo principalmente em métodos POST e PUT.
   - Lista de Headers
       - https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers

- CORS
   - Cross-Origin Resource Sharing, gerencia como deve ser o compartilhamento de recursos entre diferente origens.
   - É definido no servidor se é permitido ou não o acesso dos recursos através de scripts por outros sites.
   - Utilizando o Access-Control-Allow-Origin.
   - Se o servidor não permitir o acesso, este será bloqueado.
   - É possível passar por cima do bloqueio utilizando um proxy.
   - CORS é um acordo entre browser / servidor ou servidor / servidor. 
   - Ele serve para dar certa proteção ao browser, mas não é inviolável.
```js
const url = 'https://cors-anywhere.herokuapp.com/https://www.google.com/';
const div = document.createElement('div');

fetch(url)
.then(r => r.text())
.then(r => {
  div.innerHTML = r;
  console.log(div);
});
```

- ASYNC / AWAIT
   - A palavra chave async indica que a função possui partes assíncronas e que você pretende esperar a resolução da mesma antes de continuar. O await irá indicar a promise que devemos esperar. Faz parte do ES8.
```js
async function puxarDados() {
  const dadosResponse = await fetch('./dados.json');
  const dadosJSON = await dadosResponse.json();
  
  document.body.innerText = dadosJSON.titulo;
}

puxarDados();
```

- THEN / ASYNC
   - A diferença é uma sintaxe mais limpa.
```js
function iniciarFetch() {
  fetch('./dados.json')
  .then(dadosResponse => dadosResponse.json())
  .then(dadosJSON => {
    document.body.innerText = dadosJSON.titulo;
  })
}
iniciarFetch();

async function iniciarAsync() {
  const dadosResponse = await fetch('./dados.json');
  const dadosJSON = await dadosResponse.json();
  document.body.innerText = dadosJSON.titulo;
}
iniciarAsync();
```

- TRY / CATCH
   - Para lidarmos com erros nas promises, podemos utilizar o try e o catch na função.
```js
async function puxarDados() {
  try {
    const dadosResponse = await fetch('./dados.json');
    const dadosJSON = await dadosResponse.json();
    document.body.innerText = dadosJSON.titulo;
  }
  catch(erro) {
    console.log(erro);
  }
}
puxarDados();
```

- INICIAR FETCH AO MESMO TEMPO
   - Não precisamos esperar um fetch para começarmos outro. Porém precisamos esperar a resposta resolvida do fetch para transformarmos a response em json.
```
async function iniciarAsync() {
  const dadosResponse = fetch('./dados.json');
  const clientesResponse = fetch('./clientes.json');

  // ele espera o que está dentro da expressão () ocorrer primeiro
  const dadosJSON = await (await dadosResponse).json();
  const clientesJSON = await (await clientesResponse).json();
}
iniciarAsync();
```

- PROMISE
   - O resultado da expressão à frente de await tem que ser uma promise.  
   -E o retorno do await será sempre o resultado desta promise.
```js
async function asyncSemPromise() {
  // Console não irá esperar.
  await setTimeout(() => console.log('Depois de 1s'), 1000);
  console.log('acabou');
}
asyncSemPromise();

async function iniciarAsync() {
  await new Promise(resolve => {
    setTimeout(() => resolve(), 1000)
  });
  console.log('Depois de 1s');
}
iniciarAsync();
```

- HISTORY
   - É possível acessarmos o histórico de acesso do browser em uma sessão específica através do window.history. O objeto history possui diferentes métodos e propriedades.

```js
window.history;
window.history.back(); // vai para a anterior
window.history.forward(); // vai para a próxima
```

- PUSHSTATE()
   - A parte interessante de manipularmos o history é que podemos modificar o histórico e adicionar um novo item. 
``js
window.history.pushState(obj, title, url).

// Em obj podemos enviar um objeto com dados
// mas o seu uso é restrito por isso geralmente utilizamos
// null. O title ainda é ignorado por alguns browsers, também
// utilizamos null nele. O url que é parte importante.

window.history.pushState(null, null, 'sobre.html');
``

- POPSTATE
   - O evento popstate pode ser adicionado ao objeto window. Assim podemos executar uma função toda vez que o usuário clicar no botão de voltar ou próximo.
``js
window.addEventListener('popstate', () => {
  fetchPage(window.location.pathname);
});
``

- FETCH E HISTORY
   - Ao puxarmos dados via fetch api, o url da página continua o mesmo. Ao combinar fetch com a history api conseguimos simular uma navegação real entre páginas, sem a necessidade de recarregamento da mesma.
``js
async function fetchPage(url) {
  const pageReponse = await fetch(url);
  const pageText = await pageReponse.text();
  window.history.pushState(null, null, url);
}
``

## Classes e Objetos

- CONSTRUCTOR FUNCTION
   - Funções responsáveis pela criação de objetos. O conceito de uma função construtora de objetos é implementado em outras linguagens como Classes.
```js
function Button(text, background) {
  this.text = text;
  this.background = background;
}

Button.prototype.element = function() {
  const buttonElement = document.createElement('button');
  buttonElement.innerText = this.text;
  buttonElement.style.background = this.background;
  return buttonElement;
}

const blueButton = new Button('Comprar', 'blue');
```

- CLASS
   - O ES6 trouxe uma nova sintaxe para implementarmos funções construtoras. Agora podemos utilizar a palavra chave class. É considerada syntactical sugar, pois por baixo dos panos continua utilizado o sistema de protótipos de uma função construtora para criar a classe.
```js
class Button {
  constructor(text, background) {
    this.text = text;
    this.background = background;
  }
  element() {
    const buttonElement = document.createElement('button');
    buttonElement.innerText = this.text;
    buttonElement.style.background = this.background;
    return buttonElement;
  }
}

const blueButton = new Button('Comprar', 'blue');
```

- CLASS VS CONSTRUCTOR FUNCTION
```js
class Button {
  constructor(propriedade) {
    this.propriedade = propriedade;
  }
  metodo1() {}
  metodo2() {}
}

function Button(propriedade) {
  this.propriedade = propriedade;
}
Button.prototype.metodo1 = function() {}
Button.prototype.metodo1 = function() {}
```

- CONSTRUCTOR
   - O método constructor(args) {} é um método especial de uma classe. Nele você irá definir todas as propriedades do objeto que será criado. Os argumentos passados em new, vão direto para o constructor.
```js
class Button {
  constructor(text, background, color) {
    this.text = text;
    this.background = background;
    this.color = color;
  }
}

const blueButton = new Button('Clique', 'blue', 'white');
// Button {text: 'Clique', background: 'blue', color: 'white'}
```

- CONSTRUCTOR RETURN
   - Por padrão a classe retorna this. Ou seja, this é o objeto criado com o new Class. Podemos modificar isso alterando o return do constructor, o problema é que perderá toda a referência do objeto.
```js
class Button {
  constructor(text) {
    this.text = text;
    return this.element(); // não fazer
  }
  element() {
    document.createElement('button').innerText = this.text;
  }
}

const btn = new Button('Clique');
// <button>Clique</button>
```

- THIS
   - Assim como em uma função construtora, this faz referência ao objeto criado com new. Você pode acessar as propriedades e métodos da classe utilizando o this.
```js
class Button {
  constructor(text) {
    this.text = text;
  }
  element() {
    const buttonElement = document.createElement('button')
    buttonElement.innerText = this.text;
    return buttonElement;
  }
  appendElementTo(target) {
    const targetElement = document.querySelector(target);
    targetElement.appendChild(this.element());
  }
}

const blueButton = new Button('Clique');
blueButton.appendElementTo('body');
```

- PROPRIEDADES
   - Podemos passar qualquer valor dentro de uma propriedade.
```js
class Button {
  constructor(options) {
    this.options = options;
  }
}

const blueOptions = {
  backgroundColor: 'blue',
  color: 'white',
  text: 'Clique',
  borderRadius: '4px',
}

const blueButton = new Button(blueOptions);
blueButton.options;
```

- STATIC VS PROTOTYPE
   - Por padrão todos os métodos criados dentro da classe irão para o protótipo da mesma. Porém podemos criar métodos diretamente na classe utilizando a palavra chave static. Assim como [].map() é um método de uma array e Array.from() é um método do construtor Array.
```js
class Button {
  constructor(text) {
    this.text = text;
  }
  static create(background) {
    const elementButton = document.createElement('button');
    elementButton.style.background = background;
    elementButton.innerText = 'Clique';
    return elementButton;
  }
}

const blueButton = Button.create('blue');
```

- STATIC
   - Você pode utilizar um método static para retornar a própria classe com propriedades já pré definidas.
```js
class Button {
  constructor(text, background) {
    this.text = text;
    this.background = background;
  }
  element() {
    const elementButton = document.createElement('button');
    elementButton.innerText = this.text;
    elementButton.style.background = this.background;
    return elementButton
  }
  static createBlue(text) {
    return new Button(text, 'blue');
  }
}

const blueButton = Button.createBlue('Comprar');
```

- GET E SET
   - Podemos definir comportamentos diferentes de get e set para um método.
```js
const button = {
  get element() {
    return this._element;
  }
  set element(tipo) {
    this._element = document.createElement(tipo);
  }
}

button.element = 'button'; // set
button.element; // get (<button></button>);
```

- VALOR ESTÁTICO
   - Se definirmos apenas o get de um método, teremos então um valor estático que não será possível mudarmos.
```js
const matematica = {
  get PI() {
    return 3.14;
  }
}

matematica.PI; // get (3.14)
matematica.PI = 20; // nada acontece
```

- SET
   - Eu posso ter um método com set apenas, que modifique outras propriedades do meu objeto.
```js
const frutas = {
  lista: [],
  set nova(fruta) {
    this.lista.push(fruta);
  }
}

frutas.nova = 'Banana';
frutas.nova = 'Morango';
frutas.lista; // ['Banana', Morango];
```

- CLASS
   - Assim como em um objeto, as classes podem ter métodos de get e set também.
```js
class Button {
  constructor(text, color) {
    this.text = text;
    this.color = color;
  }
  get element() {
    const buttonElement = document.createElement('button');
    buttonElement.innerText = this.text;
    buttonElement.style.color = this.color;
    return buttonElement;
  }
}

const blueButton = new Button('Comprar', 'blue');
blueButton.element; // retorna o elemento
```

- CLASS
   - Assim como em um objeto, as classes podem ter métodos de get e set também.
```js
class Button {
  constructor(text, color) {
    this.text = text;
    this.color = color;
  }
  get element() {
    const buttonElement = document.createElement('button');
    buttonElement.innerText = this.text;
    buttonElement.style.color = this.color;
    return buttonElement;
  }
}

const blueButton = new Button('Comprar', 'blue');
blueButton.element; // retorna o elemento
```

- SET E CLASS
   - Com o set podemos modificar apenas parte do elemento de get. É comum definirmos variáveis privadas, utilizando o underscore _privada.
```js
class Button {
  constructor(text) {
    this.text = text;
  }
  get element() {
    const elementType = this._elementType || 'button';
    const buttonElement = document.createElement(elementType);
    buttonElement.innerText = this.text;
    return buttonElement;
  }
  set element(type) {
    this._elementType = type;
  }
}

const blueButton = new Button('Comprar');
blueButton.element; // retorna o elemento
```

- SUBCLASSES
   - É possível criarmos uma subclasse, esta irá ter acesso aos métodos da classe à qual ela estendeu através do seu protótipo.
```js
class Veiculo {
  constructor(rodas) {
    this.rodas = rodas;
  }
  acelerar() {
    console.log('Acelerou');
  }
}

class Moto extends Veiculo {
  empinar() {
    console.log('Empinou com ' + this.rodas + ' rodas');
  }
}

const honda = new Moto(2);
honda.empinar();
```

- MÉTODOS
   - Podemos escrever por cima de um método herdado.
```js
class Veiculo {
  constructor(rodas) {
    this.rodas = rodas;
  }
  acelerar() {
    console.log('Acelerou');
  }
}

class Moto extends Veiculo {
  acelerar() {
    console.log('Acelerou muito');
  }
}

const honda = new Moto(2);
honda.acelerar();
```

- SUPER
   - É possível utilizar a palavra chave super para falarmos com a classe que pai e acessarmos os seus métodos e propriedades.
```js
class Veiculo {
  constructor(rodas) {
    this.rodas = rodas;
  }
  acelerar() {
    console.log('Acelerou');
  }
}

class Moto extends Veiculo {
  acelerar() {
    super.acelerar();
    console.log('Muito');
  }
}

const honda = new Moto(2);
honda.acelerar();
```

- SUPER E CONSTRUCTOR
   - Podemos utilizar o super para estendermos o método constructor.
```js
class Veiculo {
  constructor(rodas, combustivel) {
    this.rodas = rodas;
    this.combustivel = combustivel;
  }
}

class Moto extends Veiculo {
  constructor(rodas, combustivel, capacete) {
    super(rodas, combustivel);
    this.capacete = capacete;
  }
}

const honda = new Moto(4, 'Gasolina', true);
```

- FUNCTION DECLARATION
   - São duas as formas mais comuns de declararmos uma função. A que utilizamos até o momento é chamado de Function Declaration.
```js
function somar(a,b) {
  return a + b;
}

somar(4,2); // 6
```js

- FUNCTION EXPRESSION
   - É criada a partir da declaração de uma variável, na qual assinalamos uma função. Esta função pode ser anônima ou nomeada. A mesma poderá ser ativada através da variável assinalada.
```js
const somar = function(a,b) {
  return a + b;
}

somar(4,2); // 6
```

- HOISTING
   - Function Declarations são completamente definidas no momento do hoisting, já function expressions apenas serão definidas no momento da execução. Por isso a ordem da declaração de uma FE possui importância.
```js
somar(4,2); // 6
dividir(4,2); // Erro

function somar(a,b) {
  return a + b;
}
const dividir = function(a,b) {
  return a / b;
}
```

- ARROW FUNCTION
   - Podemos criar utilizando arrow functions.
```js
const somar = (a, b) => a + b;
somar(4,2); // 6

const quadrado = a => a * a;
quadrado(4); // 16
```

- ESTRUTURA / PREFERÊNCIA
   - Geralmente o uso entre expression / declaration é uma questão de preferência. Function Expression força a criação da mesma antes de sua ativação, o que pode contribuir para um código mais estruturado.
```js
// Declarada como método de window
// vaza o escopo de bloco, como se
// fosse criada utilizando var
function somar(a,b) {
  return a + b;
}
const dividir = (a,b) => a / b;

somar(4,2);
dividir(4,2);
```

- IIFE - IMMEDIATELY INVOKED FUNCTION EXPRESSION
   - Antes da introdução de modules e da implementação do escopo de bloco, a forma mais comum utilizada para isolarmos o escopo de um código JavaScript era através das chamadas IIFE's.
```js
var instrumento = 'Violão';

(function() {
  // código isolado do escopo global
  var instrumento = 'Guitarra';
  console.log(instrumento); // Guitarra
})();

console.log(instrumento); // Violão
```

- IIFE - ARROW FUNCTION
   - Compiladores ainda transformam modules em IIFE's para manter a compatibilidade com browsers antigos.
```js
const instrumento = 'Violão';

(() => {
  const instrumento = 'Guitarra';
  console.log(instrumento); // Guitarra
})();

console.log(instrumento); // Violão
```

- EXERCÍCIOS
```js
// Remova o erro
priceNumber('R$ 99,99');
const priceNumber = n => +n.replace('R$', '').replace(',', '.');

// Crie uma IIFE e isole o escopo
// de qualquer código JS.

// Como podemos utilizar
// a função abaixo.
const active = callback => callback();
```

- FACTORY FUNCTION
   - São funções que retornam um objeto sem a necessidade de utilizarmos a palavra chave new. Possuem basicamente a mesma função que constructor functions / classes.
```js
function createButton(text) {
  function element() {
    const buttonElement = document.createElement('button');
    buttonElement.innerText = text;
    return buttonElement;
  }
  return {
    element: element,
    text: text,
  }
}

const comprarBtn = createButton('Comprar');
```

- MÉTODOS / VARIÁVEIS PRIVADAS
   - Uma das vantagens é a possibilidade de criarmos métodos / variáveis privadas.
```js
function criarPessoa(nome, sobrenome) {
  const nomeCompleto = `${nome} ${sobrenome}`;

  function andar() {
    return `${nomeCompleto} andou`;
  }
  function nadar() {
    return `${nomeCompleto} nadou`;
  }
  return {
    nome,
    sobrenome,
    andar,
    nadar,
  }
}

const designer = criarPessoa('André', 'Rafael');
```

- ICE FACTORY
   - Podemos impedir que os métodos e propriedades sejam modificados com Object.freeze(). Ideia inicial de Douglas Crockford.
```js
'use strict';

function criarPessoa(nome, sobrenome) {
  const nomeCompleto = `${nome} ${sobrenome}`;
  function andar() {
    return `${nomeCompleto} andou`;
  }
  return Object.freeze({
    nome,
    sobrenome,
    andar,
  });
}

const designer = criarPessoa('André', 'Rafael');
```

- CONSTRUCTOR FUNCTION / FACTORY FUNCTION
   - Uma das vantagens da Factory Function é a possibilidade de iniciarmos a mesma sem a utilização da palavra chave new. Também é possível fazer isso com uma Constructor Function.
```js
function Pessoa(nome) {
  if (!(this instanceof Pessoa)) // ou (!new.target)
    return new Pessoa(nome);
  this.nome = nome;
}

Pessoa.prototype.andar = function() {
  return `${this.nome} andou`;
}

const designer = Pessoa('André');
```

- EXEMPLO REAL
```js
function $$(selectedElements) {
  const elements = document.querySelectorAll(selectedElements);

  function on(onEvent, callback) {
    elements.forEach(element => {
      element.addEventListener(onEvent, callback);
    });
    return this; // retornar this irá funcionar da mesma forma
  }

  function hide() {
    elements.forEach(element => {
      element.style.display = 'none';
    });
    return this;
  }

  function show() {
    elements.forEach(element => {
      element.style.display = 'initial';
    });
    return this;
  }

  function addClass(className) {
    elements.forEach(element => {
      element.classList.add(className);
    });
    return this;
  }

  function removeClass(className) {
    elements.forEach(element => {
      element.classList.add(className);
    });
    return this;
  }
  
  return Object.freeze({
    elements,
    on,
    hide,
    show,
    addClass,
    removeClass,
  });
}

const buttons = $$('button');
buttons.hide().show().addClass('ativo').removeClass('ativo');
```

## Clojures e Debugging

- ESCOPO
   - Quando criamos uma função, a mesma possui acesso à todas as variáveis criadas em seu escopo e também ao escopo pai. A mesma coisa acontece para funções dentro de funções.
```js
let item1 = 1;
function funcao1() {
  let item2 = 2;
  function funcao2() {
    let item3 = 3;
  }
}

// func1, possui acesso à
// item1 e item2

// func2, possui acesso à
// item1, item2 e item3
```

- CLOJURES
   - A funcao2 possui 4 escopos. O primeiro escopo é o Local, com acesso ao item3. O segundo escopo dá acesso ao item2, esse escopo é chamado de Clojure (funcao1) (escopo de função dentro de função). O terceiro escopo é o Script com acesso ao item1 e o quarto escopo é o Global/Window.
```js
let item1 = 1;
function funcao1() {
  let item2 = 2;
  function funcao2() {
    let item3 = 3;
    console.log(item1);
    console.log(item2);
    console.log(item3);
  }
  funcao2();
}
```

- DEBUGGING
   - É possível "debugarmos" um código JavaScript utilizando ferramentas do browser ou através do próprio Visual Studio Code. Se o código possuir qualquer Web API, o processo deve ser feito no Browser. Plugins podem interferir no debug dentro do browser.
```js
debugger; // adicione a palavra debugger
let item1 = 1;
function funcao1() {
  let item2 = 2;
  function funcao2() {
    let item3 = 3;
    console.log(item1);
    console.log(item2);
    console.log(item3);
  }
  funcao2();
}
```

- CASO CLÁSSICO
   - Um dos casos mais clássicos para a demonstração de Clojures é através da criação de uma função de incremento. É como se a função incrementar carregasse uma mochila chamada contagem, onde uma referência para as suas variáveis estão contidas na mesma.
```js
function contagem() {
  let total = 0;
  return function incrementar() {
    total++;
    console.log(total);
  }
}

const ativarIncrementar = contagem();
ativarIncrementar(); // 1
ativarIncrementar(); // 2
ativarIncrementar(); // 3
```

- CLOJURES NA REAL
   - Todas as funções internas da Factory Function possuem uma closure de $$. As mesmas contém uma referência à variável elements declarada dentro do escopo da função.
```js
function $$(selectedElements) {
  const elements = document.querySelectorAll(selectedElements);

  function hide() { ... }
  function show() { ... }
  function on() { ... }
  function addClass() { ... }
  function removeClass() { ... }

  return { hide, show, on, addClass, removeClass }
}
```

- DESTRUCTURING
   - Permite a desestruturação de Arrays e Objetos. Atribuindo suas propriedades à novas variáveis.
```js
const carro = {
  marca: 'Fiat',
  ano: 2018,
  portas: 4,
}

const {marca, ano} = carro;

console.log(marca); // Fiat
console.log(ano); // 2018
```

- DESTRUCTURING OBJECTS
   - A desestruturação irá facilitar a manipulação de dados. Principalmente quando temos uma grande profundidade de objetos.
```js
const cliente = {
  nome: 'Andre',
  compras: {
    digitais: {
      livros: ['Livro 1', 'Livro 2'],
      videos: ['Video JS', 'Video HTML']
    },
    fisicas: {
      cadernos: ['Caderno 1']
    }
  }
}

console.log(cliente.compras.digitais.livros);
console.log(cliente.compras.digitais.videos);

const {livros, videos} = cliente.compras.digitais;

console.log(livros);
console.log(videos);
```

- NESTING
   - É possível aninhar uma desestruturação dentro de outra.
```js
const cliente = {
  nome: 'Andre',
  compras: {
    digitais: {
      livros: ['Livro 1', 'Livro 2'],
      videos: ['Video JS', 'Video HTML']
    },
    fisicas: {
      cadernos: ['Caderno 1']
    }
  }
}

const {fisicas, digitais, digitais: {livros, videos}} = cliente.compras;

console.log(fisicas);
console.log(livros);
console.log(videos);
console.log(digitais);
```

- NOME DAS VARIÁVEIS
   - É necessário indicar o nome da propriedade que você deseja desestruturar de um objeto. É possível mudar o nome da variável final com:
```js
const cliente = {
  nome: 'Andre',
  compras: 10,
}

const {nome, compras} = cliente;
// ou
const {nome: nomeCliente, compras: comprasCliente} = cliente;
```

- VALOR INICIAL
   - Caso a propriedade não exista o valor padrão dela será undefined. É possível modificar este valor no momento da desestruturação.
```js
const cliente = {
  nome: 'Andre',
  compras: 10,
}

const {nome, compras, email = 'email@gmail.com', cpf} = cliente;
console.log(email) // email@gmail.com
console.log(cpf) // undefined
```

- DESTRUCTURING ARRAYS
   - Para desestruturar array's você deve colocar as variáveis entre [] colchetes.
```js
const frutas = ['Banana', 'Uva', 'Morango'];

const primeiraFruta = frutas[0];
const segundaFruta = frutas[1];
const terceiraFruta = frutas[2];

// Com destructuring
const [primeira, segunda, terceira] = frutas;
```

- DECLARAÇÃO DE VARIÁVEIS
   - A desestruturação pode servir para declararmos uma sequência de variáveis.
```js
const primeiro = 'Item 1';
const segundo = 'Item 2';
const terceiro = 'Item 3';
// ou
const [primeiro, segundo, terceiro] = ['Item 1', 'Item 2', 'Item 3']; 
```

- ARGUMENTO DESESTRUTURADO
   - Se uma função espera receber como argumento um objeto, podemos desestruturar ele no momento da declaração.
```js
function handleKeyboard(event) {
  console.log(event.key);
}
// Com Destructuring
function handleKeyboard({key}) {
  console.log(key);
}

document.addEventListener('keyup', handleKeyboard);
```

- EXERCÍCIOS
```js
// Extraia o backgroundColor, color e margin do btn
const btn = document.querySelector('button');
const btnStyles = getComputedStyle(btn);


// Troque os valores das variáveis abaixo
let cursoAtivo = 'JavaScript';
let cursoInativo = 'HTML';

// Corrija o erro abaixo
const cachorro = {
  nome: 'Bob',
  raca: 'Labrador',
  cor: 'Amarelo'
}

const {bobCor: cor} = cachorro;
```

- Rest e Spread
- PARÂMETROS
   - Nem todos os parâmetros que definimos são utilizados quando uma função é executada, devido a falta de argumentos. Por isso é importante nos prepararmos para caso estes argumentos não sejam declarados.
```js
function perimetroForma(lado, totalLados) {
  return lado * totalLados;
}

perimetroForma(10, 4); // 40
perimetroForma(10); // NaN
```

- PARÂMETRO PADRÃO (DEFAULT) ES5
   - Antes do ES6 a forma de definirmos um valor padrão para um parâmetro, era através de uma expressão.
```js
function perimetroForma(lado, totalLados) {
  totalLados = totalLados || 4; // se não for definido, será igual à 4
  return lado * totalLados;
}

perimetroForma(10, 3); // 30
perimetroForma(10); // 40
```

- PARÂMETRO PADRÃO (DEFAULT) ES6+
   - Com o ES6 é possível definirmos o valor de um parâmetro direto na declaração do mesmo, caso o argumento não seja passado no momento da execução.
```js
function perimetroForma(lado, totalLados = 4) {
  return lado * totalLados;
}

perimetroForma(10, 5); // 50
perimetroForma(10); // 40
```

- ARGUMENTS
   - A palavra chave arguments é um objeto Array-like criado dentro da função. Esse objeto contém os valores dos argumentos.
```js
function perimetroForma(lado, totalLados = 4) {
  console.log(arguments)
  return lado * totalLados;
}

perimetroForma(10);
perimetroForma(10, 4, 20);
```

- PARÂMETRO REST
   - É possível declararmos uma parâmetro utilizando ... na frente do mesmo. Assim todos os argumentos que passarmos na ativação da função, ficarão dentro do parâmetro.
```js
function anunciarGanhadores(...ganhadores) {
  ganhadores.forEach(ganhador => {
    console.log(ganhador + ' ganhou.')
  });
}

anunciarGanhadores('Pedro', 'Marta', 'Maria');
```

- ÚNICO REST
   - Só é possível ter um único parâmetro rest e ele deve ser o último.
```js
function anunciarGanhadores(premio, ...ganhadores) {
  ganhadores.forEach(ganhador => {
    console.log(ganhador + ' ganhou um ' + premio)
  });
}

anunciarGanhadores('Carro', 'Pedro', 'Marta', 'Maria');
```

- REST VS ARGUMENTS
   - Apesar de parecidos o parâmetro rest e a palavra arguments possuem grandes diferenças. Sendo rest uma array real e arguments um objeto Array-like.
```js
function anunciarGanhadores(premio, ...ganhadores) {
  console.log(ganhadores);
  console.log(arguments);
}

anunciarGanhadores('Carro', 'Pedro', 'Marta', 'Maria');
```

- OPERADOR SPREAD
   - Assim como o rest, o operador Spread também utiliza os ... para ser ativado. O spread irá distribuir um item iterável, um por um.
```js
const frutas = ['Banana', 'Uva', 'Morango'];
const legumes = ['Cenoura', 'Batata'];

const comidas = [...frutas, 'Pizza', ...legumes];
```

- SPREAD ARGUMENT
   - O Spread pode ser muito útil para funções que recebem uma lista de argumentos ao invés de uma array.
```js
const numeroMaximo = Math.max(4,5,20,10,30,2,33,5); // 33

const listaNumeros = [1,13,21,12,55,2,3,43];
const numeroMaximoSpread = Math.max(...listaNumeros);
```

- TRANSFORMAR EM ARRAY
   - É possível transformar itens iteráveis em uma array real com o spread.
```js
const btns = document.querySelectorAll('button');
const btnsArray = [...btns];

const frase = 'Isso é JavaScript';
const fraseArray = [...frase];
```

- EXERCÍCIOS
```js
// Reescreva a função utilizando
// valores iniciais de parâmetros com ES6
function createButton(background, color) {
  background = background || 'blue';
  if(color === undefined) {
    color = 'red';
  }
  const buttonElement = document.createElement('button');
  buttonElement.style.background = background;
  return buttonElement;
} 

const redButton = createButton();

// Utilize o método push para inserir as frutas ao final de comidas.
const frutas = ['Banana', 'Uva', 'Morango'];
const comidas = ['Pizza', 'Batata'];
```

- ITERABLE
   - São objetos que possuem o método [Symbol.iterator], geralmente no protótipo, é dentro dele que a função que lida com a iteração será definida. Ex: Array, String, NodeList, boa parte das Array-Like e outros.
```js
const frutas = ['Banana', 'Morango', 'Uva'];
const frase = 'Isso é JavaScript';

fetch('https://pokeapi.co/api/v2/pokemon/')
.then(({headers}) => console.log(headers));
```

- FOR...OF
   - É possível fazemos um loop por cada iteração do objeto iterável utilizando o for...of. Além deste loop podemos também utilizar o Spread Operator nos mesmos.
```js
const frutas = ['Banana', 'Morango', 'Uva'];
const frase = 'Isso é JavaScript';

for(const fruta of frutas) {
  console.log(fruta);
}

for(const char of frase) {
  console.log(char);
}
```

- SPREAD E FOR...OF
   - Com o for loop podemos manipular cada um dos elementos do objeto iterável.
```js
const buttons = document.querySelectorAll('button');

for(const btn of buttons) {
  btn.style.background = 'blue';
}

console.log(...buttons);
```

- APENAS ITERÁVEIS
   - O for...of não irá funcionar em um objeto comum que não seja iterável.
```js
const carro = {
  marca: 'Honda',
  ano: 2018,
}

// Erro, não é Iterável
for(const propriedade of carro) {
  console.log(propriedade);
}
```

- FOR...IN
   - Este loop irá retornar a chave (key) de todas as propriedades enumeráveis (que não sejam símbolos) de um objeto.
```js
const carro = {
  marca: 'Honda',
  ano: 2018,
}

for(const propriedade in carro) {
  console.log(propriedade);
}
```

- ARRAYS E FOR...IN
   - Uma Array é um objeto, porém a chave de cada valor é igual ao seu index.
```js
const frutas = ['Banana', 'Morango', 'Uva'];

for(const index in frutas) {
  console.log(index);
}

for(const index in frutas) {
  console.log(frutas[index]);
}
```

- CHAVE E VALOR
   - Utilizando o for...in podemos retornar todas as chaves e valores de propriedades enumeráveis.
```js
const btn = document.querySelector('button');
const btnStyles = getComputedStyle(btn);

for(const style in btnStyles) {
  console.log(`${style}: ${btnStyles[style]}`);
}
```

- DO / WHILE
   - Outro tipo de loop é o Do / While. Não é muito utilizado.
```js
let i = 0;
do {
  console.log(i++)
} while (i <= 5);
```

- REGULAR EXPRESSION
   - Regexp ou Regex são expressões utilizadas para realizarmos buscas / substituições de padrões em strings. Os padrões devem ser colocados entre //. Geralmente vamos utilizá-las nos métodos .replace() e .split().
```js
// Procura: a
const padraoRegexp = /a/;

const texto = 'JavaScript';
const novoTexto = texto.replace(padraoRegexp, 'B');
// BavaScript
```
- Praticamente todas as linguagens possuem uma implementação de regexp

- LITERAL
   - Utilizar um caracter literal irá realizar uma busca específica deste caracter.
```js
// Procura: J seguido de a, v e a
const regexp = /Java/;

'JavaScript'.replace(regexp, 'Type');
// TypeScript
```

- FLAG: G
   - As flags irão modificar como a expressão é interpretada. Uma das mais utilizadas é a g, que significa global, ou seja, retorne todos os resultados que estiverem dentro do padrão e não apenas o primeiro. A flag deve ser colocada no final da expressão.
```js
// Procura: Todo a
const regexp = /a/g;

'JavaScript'.replace(regexp, 'i');
// JiviScript
```

- FLAG: I
   - Com o i informamos que devem ser ignoradas as diferenças entre maiúsculas e minúsculas. Isso significa que /a/ irá buscar por a e A.
```js
// Procura: Todo PE, Pe, pE e pe
const regexp = /Pe/gi;

'Perdeu perdido'.replace(regexp, 'Ba');
// Bardeu Bardido
```

- CHARACTER CLASS
   - Se colocarmos os caracteres entre colchetes, estamos definindo uma classe. /[ab]/ irá procurar por a ou por b.
```js
// Procura: Todo a, A, i, I
const regexp = /[ai]/gi;

'JavaScript'.replace(regexp, 'u');
// JuvuScrupt
```

- CHARACTER CLASS E ESPECIAIS
   - Podemos utilizar caracteres que não são alfanuméricos dentro da classe. Mas fique atento, pois existem diversos casos especiais para os mesmos.
```js
// Procura: - ou .
const regexp = /[-.]/g;

'111.222-333-44'.replace(regexp, '');
// 11122233344
```

- UM OU OUTRO
   - Combine caracteres literais com uma classe para buscarmos variações: Ju[nl]ho busca Julho ou Junho.
```js
// Procura: B, seguido de r, a
// seguido de s ou z, seguido de i, l
const regexp = /Bra[sz]il/g;

'Brasil é com z: Brazil'.replace(regexp, 'Prazer');
// Prazer é com z: Prazer
```

- DE A À Z
   - O traço - dentro de [] pode servir para definirmos um alcance. [A-Z] irá buscar os caracteres de A à Z. [0-9] busca de 0 à 9. A tabela UNICODE é utilizada como referência para definir os caracteres dentro do alcance.
```js
// Busca por itens de a à z
const regexp = /[a-z]/g;

'JavaScript é a linguagem.'.replace(regexp, '0');
// J000S00000 é 0 000000000.

// Busca por itens de a à z e A à Z
const regexp = /[a-zA-Z]/g;

'JavaScript é a linguagem.'.replace(regexp, '1');
// 1111111111 é 1 111111111.

// Busca por números de 0 à 9
const regexpNumero = /[0-9]/g;

'123.333.333-33'.replace(regexpNumero, 'X');
// XXX.XXX.XXX-XX
```
- https://unicode-table.com/en/

- NEGAR
   - Utilizando o acento circunflexo podemos negar caracteres. Ou seja, pegue tudo que não seja [^a]
```js
// Procura: tudo que não estiver entre a e z
const regexp = /[^a-z]/g;

'Brasil é com z: Brazil'.replace(regexp, ' ');
// rasil   com z   razil 
```

- PONTO
   - O ponto . irá selecionar qualquer caracter, menos quebras de linha.
```js
// Procura: todos os caracteres menos quebra de linha
const regexp = /./g;

'JavaScript é a linguagem.'.replace(regexp, '0');
// 0000000000000000000000000
```

- ESCAPAR ESPECIAIS
   - Caracteres especiais como o ponto ., podem ser escapados utilizando a barra \, assim este não terá mais a sua função especial e será tratado como literal. Lista de caracteres especiais: +*?^$\.[]{}()|/
```js
// Procura: todos os pontos
const regexp = /\./g;
const regexpAlternativa = /[.]/g;

'999.222.222.11'.replace(regexp, '-');
// 999-222-222-11
```

- WORD
   - O \w irá selecionar qualquer caracter alfanumérico e o underline. É a mesma coisa que [A-Za-z0-9_].
```js
// Procura: todos os alfanuméricos
const regexp = /\w/g;

'Guarda-chuva R$ 23,00.'.replace(regexp, '-');
// ------------ -$ --,--.
```

- NOT WORD
   - O \W irá selecionar tudo o que não for caracter alfanumérico e o underline. É a mesma coisa que [^A-Za-z0-9_].
```js
// Procura: o que não for caracter alfanuméricos
const regexp = /\W/g;

'Guarda-chuva R$ 23,00.'.replace(regexp, '-');
// Guarda-chuva-R--23-00-
```

- DIGIT
   - O \d irá selecionar qualquer dígito. É a mesma coisa que [0-9].
```js
// Procura: todos os dígitos
const regexp = /\d/g;

'+55 (21) 2222-2222'.replace(regexp, 'X');
// +XX (XX) XXXX-XXXX.
```

- NOT DIGIT
   - O \D irá selecionar tudo que não for dígito. É a mesma coisa que [^0-9].
```js
// Procura: o que não for dígito
const regexp = /\D/g;

'+55 (21) 2222-2222'.replace(regexp, '');
// 552122222222
```

- WHITESPACE
   -O \s irá selecionar qualquer espaço em branco, isso inclui espaços, tabs, quebra de linhas.
```js
// Procura: espaços em branco
const regexp = /\s/g;

'+55 (21) 2222-  2222  '.replace(regexp, '');
// +55(21)2222-2222
```

- NOT WHITESPACE
   - O \S irá selecionar qualquer caracter que não for espaço em branco.
```js
// Procura: o que não for espaço em branco
const regexp = /\S/g;

'+55 (21) 2222-  2222  '.replace(regexp, '');
// XXX XXXX XXXXX  XXXX  
```
=/[\s\S]/g irá selecionar tudo.

- QUANTIFICADOR
   - É possível selecionar caracteres seguidos, como /bbb/g irá selecionar apenas bbb. Com as chaves podemos indicar a repetição /b{3}/g. Agora ele está fazendo uma seleção completa e não caracter por caracter.
```js
// Procura: 4 a's seguidos
const regexp = /aaaa/g;
const regexpAlt = /a{4}/g;

'Vaaaai ali por favor.'.replace(regexp, 'a');
// Vai ali por favor.  
```

- QUANTIFICADOR MIN E MAX
   - Podemos informar o min e max do quantificador /a{2,4}/ vai selecionar quando aparecer a duas vezes ou até 4 vezes. /a{2,}/ irá selecionar quando se repetir duas ou mais vezes.

```js
// Procura: dígitos seguidos de 2 à 3
const regexp = /\d{2,3}/g;

'222.333.222.42'.replace(regexp, 'X');
// X.X.X.X

// Procura: letras seguidos com 1 caracter ou mais
const regexpLetras = /\w{1,}/g;

'A melhor linguagem é JavaScript'.replace(regexpLetras, 'X');
// X X X é X
```

- MAIS +
   - O sinal de + significa que devemos selecionar quando existir pelo menos uma ou mais ocorrências.
```js
// Procura: dígitos em ocorrência de um ou mais
const regexp = /\d+/g;

'222.333.222.42'.replace(regexp, 'X');
// X.X.X.X

// Procura: Começa com d, seguido por uma ou mais letras.
const regexpLetras = /d\w+/g;

'Dígitos, dados, desenhos, Dito, d'.replace(regexpLetras, 'X');
// Dígitos, X, X, Dito, d
```

- ASTERISCO *
   - O sinal * significa que devemos selecionar quando existir 0 ou mais ocorrências.
```js
// Procura: Começa com d, seguido por zero ou mais letras.
const regexp = /d\w*/g;

'Dígitos, dados, desenhos, Dito, d'.replace(regexp, 'X');
// Dígitos, X, X, Dito, X
```

- OPCIONAL ?
   - O sinal ? significa que o caracter é opcional, pode ou não existir.
```js
// Procura: Por regex com p opcional
const regexp = /regexp?/g;

'Qual é o certo, regexp ou regex?'.replace(regex, 'Regular Expression');
// Qual é o certo, Regular Expression ou Regular Expression?
```

- ALTERNADO |
   - O sinal | irá selecionar um ou outro. java|php
```js
// Procura: java ou php (case insensitive)
const regexp = /java|php/gi;

'PHP e Java são linguagens diferentes'.replace(regexp, 'X');
// X e X são linguagens diferente
```

- WORD BOUNDARY \B
   - O sinal \b irá indicar que pretendemos fazer uma seleção que deve ter início e fim de não caracteres \w.
```js
// Procura: java (case insensitive)
const regexp = /java/gi;
'Java não é JavaScript.'.replace(regexp, 'X');
// X não é XScript.

// Procura: java (case insensitive)
const regexpBoundary = /\bjava\b/gi;
'Java não é JavaScript.'.replace(regexpBoundary, 'X');
// X não é JavaScript.

// Procura: Dígitos em sequência, que estejam isolados
const regexpDigito = /\b\d+\b/gi;
'O Restaurante25 na Rua 3, custa R$ 32,00'.replace(regexDigito, 'X');
// O Restaurante25 na Rua X, custa R$ X,X

'11_22 33-44 55é66 77e88'.replace(regexpDigito, 'X');
// 11_22 X-X XéX 77e88
```

- NOT WORD BOUNDARY \B
   - É o contrário do \b.
```js
const regexpDigito = /\B\d+\B/gi;

'11_22 33-44 55é66 77e88'.replace(regexpDigito, 'X');
// 1X_X2 33-44 55é66 7XeX8
```

- ANCHOR BEGINNING
   - Com o ^ é possível informar que a busca deve ser iniciada no início da linha.
```js
// Procura: sequência de alfanuméricos
// no início da linha.
const regexp = /^\w+/g;

`andre@origamid.com
contato@origamid.com`.replace(regexp, 'X');
// X@origamid.com
// contato@origamid.com
```

- ANCHOR END
   - Com o $ é possível informar que a busca deve ser iniciada no final da linha.
```js
// Procura: sequência de alfanuméricos
// no final da linha.
const regexp = /\w+$/g;

`andre@origamid.com
contato@origamid.com`.replace(regexp, 'X');
// andre@origamid.com
// contato@origamid.X
```

- FLAG: M
   - Com a flag m de multiline, podemos informar que a busca de início ^ e final $ de linha devem ocorrer em todas as linhas disponíveis.
```js
// Procura: sequência de alfanuméricos
// no final da linha.
const regexp = /\w+$/gm;

`andre@origamid.com
contato@origamid.com`.replace(regexp, 'X');
// andre@origamid.X
// contato@origamid.X

// Procura: sequência de alfanuméricos
// no início da linha.
const regexp = /^\w+/gm;

`andre@origamid.com
contato@origamid.com`.replace(regexp, 'X');
// X@origamid.com
// X@origamid.com
```

- LINE FEED \N
   - O \n irá selecionar o final de uma linha, quando criamos uma nova.
```js
const regexp = /\n/g;

`andre@origamid.com\ncontato@origamid.com`.replace(regexp, '---');
// andre@origamid.com---contato@origamid.com

`andre@origamid.com
contato@origamid.com`.replace(regexp, 'X');
// andre@origamid.com---contato@origamid.com
\t seleciona tabs
```

- UNICODE \U
   - O \u irá selecionar o respectivo caracter unicode, de acordo com o código passado em \uXXXX. Ex: \u0040 seleciona o @.
```js
// Procura: @ ou ©
const regexp = /\u0040|\u00A9/g;

'andre@origamid.com ©'.replace(regexp, '---');
// andre---origamid.com ---
```

- REFERÊNCIA DA SELEÇÃO
   - É possível utilizarmos o $& durante o momento da substituição para fazermos uma referência à seleção.
```js
// Procura: Java
const regexp = /Java/g;

'PHP e Java são linguagens diferentes'.replace(regexp, '--$&Script');
// PHP e --JavaScript são linguagens diferentes
// $& será igual à Java
```

- GRUPO DE CAPTURA
   - É possível definirmos diferentes grupos de captura, que poderão ser referenciados durante a substituição. Basta envolvermos um grupo entre () parênteses. A referência se cada grupo será feita com $n, sendo o primeiro $1.
```js
// Procura: sequência alfanumérica, seguida
// de @, seguido de alfanumérico ou .
const regexp = /(\w+)@[\w.]+/g;

'andre@email.com.br'.replace(regexp, '$1@gmail.com');
// andre@gmail.com
```
- Não use este regexp para emails, ele falha em alguns casos.

- MAIS DE UM GRUPO
   - Podemos definir quantos grupos de captura quisermos.
```js
// Procura: sequência alfanumérica, seguida
// de , seguido espaço de sequência alfanumérica.
const regexp = /(\w+),\s(\w+)/g;

'Rafael, Andre'.replace(regexp, '$2 $1');
// Andre Rafael
```

- MAIS DO QUE CAPTURA APENAS
   - Um grupo também serve para agruparmos uma sequência de caracteres que queremos em repetição.
```js
// Procura: qualquer sequência de ta
const regexp = /(ta)+/gi;

'Tatata, tata, ta'.replace(regexp, 'Pá');
// Pá, Pá, Pá
```

- IGNORAR CAPTURA
   - Utilize o (?:) para ignorar a captura.
```js
// Procura: qualquer sequência de ta
const regexp = /(?:ta)+/gi;

'Tatata, tata, ta'.replace(regexp, 'Pá');
// Pá, Pá, Pá
```

- POSITIVE LOOKAHEAD
   - Faz a seleção dos itens que possuírem o padrão dentro de (?=) à sua frente. Apesar de utilizar () parênteses o positive lookahead não captura grupo.
```js
// Procura: dígitos em sequência, que
// possuírem px, sem selecionar o px.
const regexp = /\d(?=px)/g;

'2em, 4px, 5%, 2px, 1px'.replace(regexp, 'X');
// 2em, Xpx, 5%, Xpx, Xpx
```

- NEGATIVE LOOKAHEAD
   - Faz a seleção dos itens não possuírem o padrão dentro de (?!) à sua frente.
```js
// Procura: dígitos que não possuírem px
// sem selecionar o restante.
const regexp = /\d(?!px)/g;

'2em, 4px, 5%, 5px, 1px'.replace(regexp, 'X');
// Xem, 4px, X%, 5px, 1px
```

- POSITIVE LOOKBEHIND
   - Faz a seleção dos itens que possuírem o padrão dentro de (?<=) atrás dos mesmos.
```js
// Procura: dígitos que possuírem R$
// na frente dos mesmos
const regexp = /(?<=R\$)[\d]+/g;

'R$99, 100, 200, R$20'.replace(regexp, 'X');
// R$X, 100, 200, R$X
```

- CEP
```js
const regexpCEP = /\d{5}[-\s]?\d{3}/g;

const ceps = [
  '00000-000',
  '00000 000',
  '00000000'
];

for(cep of ceps) {
  console.log(cep, cep.match(regexpCEP));
}
```

- CPF
```js
const regexpCPF = /(?:\d{3}[-.]?){3}\d{2}/g;

const cpfs = [
  '000.000.000-00',
  '000-000-000-00',
  '000.000.000.00',
  '000000000-00',
  '00000000000'
];

for(cpf of cpfs) {
  console.log(cpf, cpf.match(regexpCPF));
}
```

- CNPJ
```js
const regexpCNPJ = /\d{2}[-.]?(?:\d{3}[-.]?){2}[-\/]?\d{4}[-.]?\d{2}/g;

const cnpjs = [
  '00.000.000/0000-00',
  '00000000000000',
  '00-000-000-0000-00',
  '00.000.000/000000',
  '00.000.000.000000',
  '00.000.000.0000.00',
];

for(cnpj of cnpjs) {
  console.log(cnpj, cnpj.match(regexpCNPJ));
}
```

- TELEFONE
```js
const regexpTELEFONE = /(?:\+?55\s?)?(?:\(?\d{2}\)?[-\s]?)?\d{4,5}[-\s]?\d{4}/g;

const telefones = [
  '+55 11 98888-8888',
  '+55 11 98888 8888',
  '+55 11 988888888',
  '+55 11988888888',
  '+5511988888888',
  '5511988888888',
  '11 98888-8888',
  '11 98888 8888',
  '(11) 98888 8888',
  '(11) 98888-8888',
  '11-98888-8888',
  '11 98888 8888',
  '11988888888',
  '11988888888',
  '988888888',
  '(11)988888888',
  '98888 8888',
  '8888 8888'
];

for(telefone of telefones) {
  console.log(telefone, telefone.match(regexpTELEFONE));
}
```

- EMAIL
```js
const regexpEMAIL = /[\w.-]+@[\w-]+\.[\w-.]+/gi;

const emails = [
  'email@email.com',
  'email@email.com.org',
  'email-email@email.com',
  'email_email@email.com',
  'email.email23@email.com.br',
  'email.email23@empresa-sua.com.br',
  'c@contato.cc',
];

for(email of emails) {
  console.log(email, email.match(regexpEMAIL));
}
```
- http://emailregex.com/


- TAG
```js
const regexpTAG = /<\/?[\w\s="']+\/?>/gi;
const tags = [
  '<div>Isso é uma div</div>',
  '<div class="ativa">Essa está ativa</div>',
  '<img src="imagem" />',
  '<img src="imagem">',
  '<ul class="ativa">',
  '<li>Essa está ativa</li>',
  '</ul>'
];

for(tag of tags) {
  console.log(tag, tag.match(regexpTAG));
}
```

- TAG APENAS O NOME
```js
const regexpTAG = /(?<=<\/?)[\w]+/gi;
const tags = [
  '<div>Isso é uma div</div>',
  '<div class="ativa">Essa está ativa</div>',
  '<img src="imagem" />',
  '<img src="imagem">',
  '<ul class="ativa">',
  '<li>Essa está ativa</li>',
  '</ul>'
];

for(tag of tags) {
  console.log(tag, tag.match(regexpTAG));
}
```
- Positive Lookbehind (?<=) não está disponível em todos os browsers.


- REGEXP CONSTRUCTOR
   - Toda regexp é criada com o constructor RegExp() e herda as suas propriedades e métodos. Existem diferenças na sintaxe de uma Regexp criada diretamente em uma variável e de uma passada como argumento de RegExp.
```js
const regexp = /\w+/gi;

// Se passarmos uma string, não precisamos dos //
// e devemos utilizar \\ para meta characters, pois é necessário
// escapar a \ especial. As Flags são o segundo argumento
const regexpObj1 = new RegExp('\\w+', 'gi');
const regexpObj2 = new RegExp(/\w+/, 'gi');

'JavaScript Linguagem 101'.replace(regexpObj1, 'X');
// X X X

// Exemplo complexo:
const regexpTELEFONE1 = /(?:\+?55\s?)?(?:\(?\d{2}\)?[-\s]?)?\d{4,5}[-\s]?\d{4}/g;
const regexpTELEFONE2 = new RegExp('(?:\\+?55\\s?)?(?:\\(?\\d{2}\\)?[-\\s]?)?\\d{4,5}[-\\s]?\\d{4}', 'g');
```

- PROPRIEDADES
   - Uma regexp possui propriedades com informações sobre as flags e o conteúdo da mesma.
```js
const regexp = /\w+/gi;

regexp.flags; // 'gi'
regexp.global; // true
regexp.ignoreCase; // true
regexp.multiline; // false
regexp.source; // '\w+'
```

- REGEXP.TEST()
   - O método test() verifica se existe ou não uma ocorrência da busca. Se existir ele retorna true. A próxima vez que chamarmos o mesmo, ele irá começar do index em que parou no último true.
```js
const regexp = /Java/g;
const frase = 'JavaScript e Java';

regexp.lastIndex; // 0
regexp.test(frase); // true
regexp.lastIndex; // 4
regexp.test(frase); // true
regexp.lastIndex; // 17
regexp.test(frase); // false
regexp.lastIndex; // 0
regexp.test(frase); // true (Reinicia
regexp.lastIndex;  // 4
```

- TEST() EM LOOP
   - Podemos utilizar o while loop, para mostrar enquanto a condição for verdadeira. Assim retornamos a quantidade de match's.
```js
const regexp = /Script/g;
const frase = 'JavaScript, TypeScript e CoffeeScript';

let i = 1;
while(regexp.test(frase)) {
  console.log(i++, regexp.lastIndex);
}
// 1 10
// 2 22
// 3 37
```

- REGEXP.EXEC()
   - O exec() diferente do test(), irá retornar uma Array com mais informações do que apenas um valor booleano.
```js
const regexp = /\w{2,}/g;
const frase = 'JavaScript, TypeScript e CoffeeScript';

regexp.exec(frase);
// ["JavaScript", index: 0, input: "JavaScript,
// TypeScript e CoffeeScript", groups: undefined] 
regexp.exec(frase);
// ["TypeScript", index: 12, input: "JavaScript,
// TypeScript e CoffeeScript", groups: undefined] 
regexp.exec(frase);
// ["CoffeeScript", index: 25, input: "JavaScript,
// TypeScript e CoffeeScript", groups: undefined] 
regexp.exec(frase);
// null
regexp.exec(frase); // Reinicia
// ["JavaScript", index: 0, input: "JavaScript,
// TypeScript e CoffeeScript", groups: undefined] 
```

- LOOP COM EXEC()
   - Podemos fazer um loop com exec e parar o mesmo no momento que encontre o null.
```js
const regexp = /\w{2,}/g;
const frase = 'JavaScript, TypeScript e CoffeeScript';
let regexpResult;

while((regexpResult = regexp.exec(frase)) !== null) {
  console.log(regexpResult[0]);
}
```

- STR.MATCH()
   - O match() é um método de strings que pode receber como argumento uma Regexp. Existe uma diferença de resultado quando utilizamos a flag g ou não.
```js
const regexp = /\w{2,}/g;
const regexpSemG = /\w{2,}/;
const frase = 'JavaScript, TypeScript e CoffeeScript';

frase.match(regexp);
// ['JavaScript', 'TypeScript', 'CoffeeScript']

frase.match(regexpSemG);
// ["JavaScript", index: 0, input: "JavaScript,
// TypeScript e CoffeeScript", groups: undefined]
```
- Se não tiver match retorna null

- STR.SPLIT()
   - O split serve para distribuirmos uma string em uma array, quebrando a string no argumento que for passado. Este método irá remover o match da array final.
```js
const frase = 'JavaScript, TypeScript, CoffeeScript';

frase.split(', ');
// ["JavaScript", "TypeScript", "CoffeeScript"]
frase.split(/Script/g);
// ["Java", ", Type", ", Coffee", ""]

const tags = `
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
`;

tags.split(/(?<=<\/?)\w+/g).join('div');
// <div>
//   <div>Item 1</div>
//   <div>Item 2</div>
// <div>
```

- STR.REPLACE()
   - O método replace() é o mais interessante por permitir a utilização de funções de callback para cada match que ele der com a Regexp.
```js
const tags = `
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
`;

tags.replace(/(?<=<\/?)\w+/g, 'div');
// <div>
//   <div>Item 1</div>
//   <div>Item 2</div>
// <div>
```

- CAPTURA
   - É possível fazer uma referência ao grupo de captura dentro do argumento do replace. Então podemos utilizar $&, $1 e mais.
```js
const tags = `
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
`;

tags.replace(/<li/g, '$& class="ativo"');
// <ul>
//   <li class="ativo">Item 1</li>
//   <li class="ativo">Item 2</li>
// </ul>
```

- GRUPOS DE CAPTURA
   - É possível definirmos quantos grupos de captura quisermos.
```js
const emails = `
empresa@email.com
contato@email.com
suporte@email.com
`;

emails.replace(/(\w+@)[\w.]+/g, '$1gmail.com');
// empresa@gmail.com
// contato@gmail.com
// suporte@gmail.com
```

- CALLBACK
   - Para substituições mais complexas, podemos utilizar um callback como segundo argumento do replace. O valor do return será o que irá substituir cada match.
```js
const regexp = /(\w+)(@[\w]+)/g;
const emails = `joao@homail.com.br
marta@ggmail.com.br
bruna@oulook.com.br`

emails.replace(regexp, function(...args) {
  console.log(args);
  if(args[2] === '@homail') {
    return `${args[1]}@hotmail`;
  } else if(args[2] === '@ggmail') {
    return `${args[1]}@gmail`;
  } else if(args[2] === '@oulook') {
    return `${args[1]}@outlook`;
  } else {
    return 'x';
  }
});

// joao@hotmail.com.br
// marta@gmail.com.br
// bruna@outlook.com.br
```
