# Recycling learning with JavaScript

## Criação: 22 de Fevereiro de 2020
## Prática : @reluviari

## Ferramentas : 
![Javascript](/images/logo-javascript.png)
![VSCode](/images/logo-VSCode.png)
![Git](/images/logo-git.png)
![Github](/images/logo-github.png)
![Rocketseat](/images/logo-rocketseat.png)

### Introdução à Javascript 

#### 1. Introdução 
- Interpretar scripts na interface do navegador no ambiente do cliente.

#### 2. Configuração Ambiente 
- Visual Studio Code
- Console de Desenvolvedor - Google Chrome

#### 3. Variáveis e Dados
- string, inteiro, decimal, boolean, vetor, objeto
- console.log

````javascript
	var nome = "Danilo";//string
	var idade = 35;//inteiro
	var peso = 105.5;//decimal
	var humano = true;//boolean
	var alunos = ['Danilo', 'Roberto', 'Lucas'];//vetor
	var aluno = {//objeto
	    nome: 'Danilo',
	    idade: 29,
	    peso: 84.5,
	    humano: true
	};
	console.log(alunos[1]);
	console.log(aluno.peso);
````

#### 4. Operações Matemáticas

````javascript
	var x = 9, y = 3;
	console.log(x + y);
````

#### 5. Funções

````javascript
	function soma(numero1, numero2){
	    var resultado = numero1 + numero2;
	    return resultado;
	}
	var resultadosoma = soma(1, 2);
	console.log(resultadosoma);
````

#### 6. Condicionais

- if
````javascript
	function qualSexo(sexo){//M ou F
	    if(sexo == 'M'){
	        return 'Masculino';
	    } else if( sexo == 'F') {
	        return 'Feminino'; 
	    } else {
	        return 'Outro';
	    }
	}
	var resultadoSexo = qualSexo('M');
	console.log(resultadoSexo);
````

- switch case
````javascript
	function qualSexo(sexo){//M ou F
	    switch (sexo) {
	        case 'M':
	            return 'Masculino';
	        case 'F':
	            return 'Feminino';
	        default:
	            return 'Outro';
	    }
	}
	var resultadoSexo = qualSexo('F');
	console.log(resultadoSexo);
````

#### 7. Operadores Lógicos

- and
````javascript        
	var sexo = 'M', idade = 35;
	if(sexo === 'M' && idade >=18){
	    console.log('OK');
	}
````
- or
````javascript       
	var sexo = 'M', idade = 15;
	if(sexo === 'M' || idade >=18){
	    console.log('OK');
	}
````
- not : verificar a desigualdade
```` javascript       
	var sexo = 'F';
	if(sexo !== 'M'){
	    console.log('OK');
	}
````

#### 8. Condicional Ternária

- estrutura tradicional if else
````javascript
	var sexo = 'M';
	if (sexo === 'M'){
	    return 'Masculino';
	} else {
	    return 'Feminino';
	}
````
- estrutura ternária

````javascript
	var sexo = 'F';
	var retorno = (sexo === 'M') ? 'Masculino' : 'Feminino';
	console.log(retorno);
````

#### 9. Estruturas de Repetição

- for : exibir no console de 0 a 99 
````javascript
	for (var i = 0; i < 100; i++){
	    console.log(i);
	}
````
- while - quando não há conhecimento de quantas interações serão realizadas
````javascript
	var j = 0;
	while (j<100){
	    console.log(j);
	    j++;
	}
````

#### 10. Intervalo e Timeout

- Intervalo : executa repetidas vezes no intervalo de tempo informado como parâmetro
````javascript
	function exibirAlgo(){
	    console.log('@relviari');
	}
	setInterval(exibirAlgo, 1000);
````
- Timeout : executa uma vez após o intervalo de tempo informado como parâmetro
````javascript	
	function exibirAlgo(){
		console.log('@reluviari');
	}
	setTimeout(exibirAlgo, 6000);
````

#### Desafio
- arquivo pdf : desafio1-introducao.pdf

- consultas :
1. https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf
2. https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/for...of
3. https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/join
- Tarefa 1
````javascript
	<script>  
		var endereco = {
		    rua: "Rua dos pinheiros",
		    numero: 1293,
		    bairro: "Centro",
		    cidade: "São Paulo",
		    uf: "SP"
		};
		function montarEndereco(){

		    return 'O usuário mora em ' + endereco.cidade + '/' + endereco.uf 
		            + ', no bairro ' + endereco.bairro + ', na rua ' + endereco.rua 
		            + ' com nº ' + endereco.numero + '.'
		}

		console.log(montarEndereco());

	</script>
````
- Tarefa 2
````javascript
	function exibirPares(x, y){
		for(var i = x; i <= y; i++){
		    if(i%2 === 0){
		        console.log(i);
		    } 
		}
	}
	console.log(exibirPares(32,321));
````
- Tarefa 3
````javascript
	function temHabilidade(skills, possuiEssaSkill){
	    return skills.indexOf(possuiEssaSkill);
	}

	var skills = [ "Html", "Javascript", "ReactJS", "React  Native"];
	var possuiEssaSkill = "Javascript";

	if(temHabilidade(skills, possuiEssaSkill) != -1){
	    console.log('Possui a habilidade ' + possuiEssaSkill + '.');
	} else {
	    console.log('Não Possui a habilidade ' + possuiEssaSkill + '.');
	}
````
- Tarefa 4 
````javascript
	function experiencia(anos) {
	    if(anos > 0 && anos <= 1 ){
	        return anos + ' anos de estudo. Você é um programador Iniciante';
	    }
	    if(anos > 1 && anos <= 3 ){
	        return anos + ' anos de estudo. Você é um programador Intermediário';
	    }
	    if(anos > 3 && anos <= 6 ){
	        return anos + ' anos de estudo. Você é um programador Avançado';
	    }
	    if(anos > 6 ){
	        return anos + ' anos de estudo. Você é um programador Jedi Master';
	    }
	    else {
	        return ' Você quer ser programador ?';
	    }
	}
	var anosEstudo = 5;
	console.log(experiencia(anosEstudo));
````

- Tarefa 5
````javascript
	var usuarios = [
		{
		    nome: "Diego",
		    habilidades: ["Javascript", "ReactJS", "Redux"]
		},
		{
		    nome: "Danilo",
		    habilidades: ["JQuery", "Ruby on Rails", "Elixir"]
		}
	];

	function leitura(usuarios){
		for(let usuario of usuarios){
		    console.log('O '+ usuario.nome +' possui as habilidades ' + usuario.habilidades + '.');
		}
	}

	leitura(usuarios);
````
### Manipulando a DOM

#### 1. Eventos inline 
- eventos : onclick, onmouseover, onkeypress, entre outros.
````html
	<body>
		<h4> @reluviari </h4>
		<h5> Manipulando DOM</h5>
		<div id="app">
			<button onmouseover ="mostraAlerta()">Pressione</button>
		</div>
		<script>
			function mostraAlerta(){
				alert('Botão foi clicado.');
			}
		</script>
	</body>
````

#### 2. Trabalhando com a DOM 
- Objetivo é buscar as informações nos elementos da DOM
- getElementsByTagName
- getElementsByClassName
- getElementsById 
- Manipulando elementos da nossa DOM
````html
	<div id="app">
		<input type="text" name="nome"/>
		<button class="botao">Adicionar</button>
	</div>
	<script>
		var btnElement = document.querySelector('button.botao');
		var inputElement = document.querySelector('input[name=nome]');
		btnElement.onclick = function(){
			var text = inputElement.value;
			alert(text);
		}
	</script>
````
- Criando e removendo
````html
	<div id="app">
		<input id="nome"/>
	</div>
	<script>
		var linkElement = document.createElement('a');
		linkElement.setAttribute('href','http://rocketseat.com.br');

		var textElement = document.createTextNode('Acessar site da rocketseat.');
		linkElement.appendChild(textElement);

		var containerElement = document.querySelector('#app');
		containerElement.appendChild(linkElement);

		var inputElement = document.querySelector('#nome');
		containerElement.removeChild(inputElement);

	</script>
````
#### 3. Lidando com elementos
- Criando elementos HTML com JS.
````html
<body>
	<div id = "app">

	</div>
	<script>
		var linkElement = document.createElement('a');//criando a tag <a>
		linkElement.setAttribute('href', 'http://rocketseat.com.br');
		var textElement = document.createTextNode('Acessar site da Rocketseat.');
		linkElement.appendChild(textElement);
		var containerElement = document.querySelector('#app');
		containerElement.appendChild(linkElement);
	</script>
</body>
````
#### 4. Alterando Estilos 
- Controlar estilização css
````html
	<div id="app">
		<div class="box"></div>
	</div>
	<script>
		var boxElement = document.querySelector('.box');

		boxElement.style.width = 100;
		boxElement.style.height = 100;
		boxElement.style.backgroundColor = '#f00';            
	</script>
```` 

#### Desafio
- arquivo pdf : desafio2-manipulandoDOM.pdf 
- Tarefa 1
````html
	<button class='botao' id='btnCriar' onClick="gerarQuadrado()">Gerar Quadrado Vermelho</button>
	<body>
	</body>
	<script>        
		function gerarQuadrado() {

			let boxElement = document.createElement("div");

			boxElement.style.width = '100px';
			boxElement.style.height = '100px';
			boxElement.style.margin = '10px';
			boxElement.style.backgroundColor = '#f00';

			//adiciona a classe .box na div criada
			boxElement.classList.add('box');

			document.body.appendChild(boxElement);
		}
	</script>
````
- Tarefa 2
````html
	<button class='botao' id='btnCriar' onClick="gerarQuadrado()" >Gerar Quadrado Vermelho</button>
	<body>
	</body>
	<script>        

		function gerarQuadrado() {

			let boxElement = document.createElement("div");

			boxElement.style.width = '100px';
			boxElement.style.height = '100px';
			boxElement.style.margin = '10px';
			boxElement.style.backgroundColor = '#f00';

			//cria evento mouseover
			boxElement.addEventListener("mouseover", () => {
				let newColor = getRandomColor();
				boxElement.style.backgroundColor = newColor;
			});

			document.body.appendChild(boxElement);
		}

		function getRandomColor() {
			var letters = "0123456789ABCDEF";
			var color = "#";
			for (var i = 0; i < 6; i++) {
				color += letters[Math.floor(Math.random() * 16)];
			}
			return color;
		}
		
	</script>
````
- Tarefa 3 
````html
	<body></body>
    <script>
		var nomes = ["Danilo", "Lucas", "Gabriel", "Marcelo"];

		var element = document.body;

		var newUl = document.createElement('ul');
		
		for(var i = 0 ; i < nomes.length ; i++){
			var newLi = document.createElement('li');
			var itemLi = document.createTextNode(nomes[i]);
			newLi.appendChild(itemLi);
			newUl.appendChild(newLi);
			element.appendChild(newUl); 
		}
	</script>
````
- Tarefa 4
````html
	<input type="text" name="nome">
	<button class="botao" onClick="adicionar()">Adicionar</button>
	<script>
		var nomes = ["Diego", "Lucas", "Gabriel", "Lucas"];
		var element = document.body;
		var newUl = document.createElement('ul');
		for(var i = 0 ; i < nomes.length ; i++){
			var newLi = document.createElement('li');
			var itemLi = document.createTextNode(nomes[i]);
			newLi.appendChild(itemLi);
			newUl.appendChild(newLi);
			element.appendChild(newUl); 
		}
		function adicionar(){
			var inputElement = document.querySelector('input[name=nome]');
			var newLi = document.createElement('li');
			var itemLi = document.createTextNode(inputElement.value);
			newLi.appendChild(itemLi);
			newUl.appendChild(newLi);
			element.appendChild(newUl); 
		}
	</script>
````

### App de Todos

#### 1. Estrutura do App
- `index.html`
- `todos.js`
- Referenciar os elementos html no javascript

#### 2. Iniciando aplicação
- Array de todos

#### 3. Renderizando Todos
- Renderizar via javascript

#### 4. Criando Todos
- Criando via javascript

#### 5. Excluindo Todos
- Excluindo via javascript

#### 6. Salvando no Storage
- Storage via javascript

**Projeto AppTodos**
- `index.html`
````html
<html>
    <head>
        <title>Javascript-@reluviari</title>
    </head>
    <body>
        <div id="app">
            <ul></ul>
            <input type="text" placeholder="Digite um Todo">
            <button>Adicionar</button>
        </div>
        <script src="todos.js"></script>
    </body>
</html>
````
- `todos.js`
````javascript
var listElement = document.querySelector('#app ul');
var inputElement = document.querySelector('#app input');
var buttonElement = document.querySelector('#app button');

var todos = JSON.parse(localStorage.getItem('list_todos')) || [];

function renderTodos(){

    listElement.innerHTML = '';

    for (todo of todos ){

        var todoElement = document.createElement('li');
        var todoText = document.createTextNode(todo);

        var linkElement = document.createElement('a');
        linkElement.setAttribute('href', '#');
        var pos = todos.indexOf(todo);
        linkElement.setAttribute('onclick','deleteTodo('+ pos +')');
        var linkText = document.createTextNode('Excluir');

        linkElement.appendChild(linkText);
        todoElement.appendChild(todoText);
        todoElement.appendChild(linkElement);
        listElement.appendChild(todoElement);

    }
}

renderTodos();

function addTodo(){
    var todoText = inputElement.value;
    todos.push(todoText);
    inputElement.value = '';
    renderTodos();
    saveToStorage();
}

buttonElement.onclick = addTodo;

function deleteTodo(pos){
    todos.splice(pos, 1);
    renderTodos();
    saveToStorage();
}

function saveToStorage(){
    localStorage.setItem('list_todos', JSON.stringify(todos));
}
````

### JS Assíncrono

#### 1. Requisições AJAX
- Requisitar informações do servidor sem precisar atualizar a página
- Recuperar informações do servidor
- Arquivo `main.js`
````javascript
var xhr = new XMLHttpRequest();

xhr.open('GET', 'https://api.github.com/users/reluviari');
xhr.send(null);

xhr.onreadystatechange = function(){
    if(xhr.readyState === 4){
        console.log(JSON.parse(xhr.responseText));
    }
}
````
- Consumir as informações do serviços

#### 2. Promises
- Funções para manipulação das informações vinda do servidor
````javascript
var myPromise = function() {

    return new Promise(function(resolve, reject){
        var xhr = new XMLHttpRequest();
        xhr.open('GET', 'https://api.github.com/users/reluviari');
        xhr.send(null);

        xhr.onreadystatechange = function(){
            if(xhr.readyState === 4){
                if(xhr.status === 200) {
                    resolve(JSON.parse(xhr.responseText));
                }else{
                    reject('Erro na requisição');
                }
            }
        }
    });
}

myPromise()
    .then(function(response) {
        console.log(response);
    })
    .catch(function(error) {
        console.warn(error);
    });
````

#### 3. Utilizando AXIOS
- Biblioteca AXIOS 
- `https://github.com/axios/axios`
- `npm install axios`

- main.js - exemplo
````javascript
axios.get('https://api.github.com/users/reluviari')
    .then(function(response) {
        console.log(response);
    })
    .catch(function(error) {
        console.warn(error);
    });
````
- index.html - exemplo
````html
<html>
    <head>
        <title>Javascript-@reluviari</title>
    </head>
    <body>
        @reluviari
        <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
        <script src="main.js"></script>
    </body>
</html>
````

#### Desafio
- Tarefa 0 - index.html e main.js
````html
<html>
    <head>
        <title>Tarefa 0</title>
    </head>
    <body
        <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
        <script src="main.js"></script>
    </body>
</html>
````

````javascript
function checaIdade(idade) {
    return new Promise(function(resolve, reject) {
      setTimeout(function() {
        return idade >= 18 ? resolve() : reject();
      }, 2000);
    });
  }
  
  checaIdade(15)
    .then(function() {
      console.log("Maior que 18");
    })
    .catch(function() {
      console.log("Menor que 18");
    });
````
- Tarefa 2 - 2_list_repositories.html
````html
<!DOCTYPE html>
<html lang="en">

<head>
  <title>Tarefa 2</title>
</head>

<body>
  <input type="text" name="user">
  <button onclick="listRepositories()">Adicionar</button>

  <ul></ul>

  <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
  <script>
    var listElement = document.querySelector('ul');
    var inputElement = document.querySelector('input');

    function renderRepositories(repositories) {
      for (repo of repositories) {
        const textElement = document.createTextNode(repo.name);
        const liElement = document.createElement('li');
        liElement.appendChild(textElement);
        listElement.appendChild(liElement);
      }
    }
    function messageUserNotFound(user){
      alert(`Usuário "${user}" não encontrado...`);
    }
    function listRepositories() {
      var user = inputElement.value;
      if (!user) return;
      axios.get('https://api.github.com/users/' + user + '/repos')
        .then(function (response) {
          renderRepositories(response.data);
        }).catch(function (error){
          console.log(error);
          messageUserNotFound(user);
        })
    }
  </script>
</body>

</html>
````
- Tarefa 3 - 3_list_repositories.html
````html
<!DOCTYPE html>
<html lang="en">

<head>
  <title>Tarefa 3 - Power</title>
</head>

<body>
  <input type="text" name="user">
  <button onclick="listRepositories()">Adicionar</button>

  <ul></ul>

  <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
  <script>
    var listElement = document.querySelector('ul');
    var inputElement = document.querySelector('input');

    function renderRepositories(repositories, user) {
      listElement.innerHTML = "";
      if (repositories.length > 0){
        for (repo of repositories) {
          const textElement = document.createTextNode(repo.name);
          const liElement = document.createElement('li');
          liElement.appendChild(textElement);
          listElement.appendChild(liElement);
        }
      }else{
        renderNoRepositories(user);
      }
    }

    function renderLoading() {
      listElement.innerHTML = "";
      var textElement = document.createTextNode('Carregando...');
      var loadingElement = document.createElement('li');
      loadingElement.appendChild(textElement);
      listElement.appendChild(loadingElement);
    }

    function renderNoRepositories(user) {
      var textElement = document.createTextNode(`Aviso: Usuário "${user}" encontrado, porém não possui repositórios...`);
      var warningElement = document.createElement('li');
      warningElement.style.color = "#EEAD2D";
      warningElement.appendChild(textElement);
      listElement.appendChild(warningElement);
    }

    function renderError(user) {
      listElement.innerHTML = "";
      var textElement = document.createTextNode(`Erro: Usuário "${user}" não encontrado...`);
      var errorElement = document.createElement('li');
      errorElement.style.color = "#F00";
      errorElement.appendChild(textElement);
      listElement.appendChild(errorElement);
    }

    function listRepositories() {
      var user = inputElement.value;
      if (!user) return;
      renderLoading();
      axios.get('https://api.github.com/users/' + user + '/repos')
        .then(function (response) {
          console.log(response);
          renderRepositories(response.data, user);
        })
        .catch(function (error) {
          console.warn(error);
          renderError(user);
        });
    }

  </script>
</body>

</html>
````