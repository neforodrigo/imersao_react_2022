**Mario:** Olá, pessoas!! Boas-vindas à **segunda aula** da **Imersão React** da **Alura**. Estamos aqui, eu, **Mario Souto**, e o **Paulo Silveira**. Paulo, o que temos para hoje? Você pode inciar o assunto da nossa aula? 

> Mario é um homem branco, de bigode, cavanhaque e cabelos curtos na cor castanho escuro. Ele veste uma blusa preta e usa headphones também na cor preta. Está sentado em uma cadeira gamer, com um microfone próximo ao rosto. Ao fundo, é possível ver uma estante com cds e alguns bonecos sob uma luz rosa do lado esquerdo e outra azul do lado direito. 

> Paulo Silveira é um homem branco, de barba e cabelos curtos na cor castanho escuro. Ele usa óculos e está vestindo uma camiseta branca. Há um microfone que sai da lateral direita e se aproxima do seu rosto. Ele está sentado em frente a uma prateleira com alguns livros e objetos, como um quadro do Hipsters Ponto Tech, uma planta e uma miniatura da escultura "O Pensador". 


**Paulo:** Pois é, Mario, nós tivemos uma aula muito potente, com vários passos até chegar ao *deploy* e colocar no ar, no Cloud. Algumas pessoas usaram outros clouds, mas já temos muitos projetos no GitHub. Se você for ao GitHub e procurar por **#ImersãoReact**, notará que muitas pessoas colocaram. 

Inclusive, se você não colocou, te convidamos a editar o seu projeto e incluir a hashtag da Alura e da Imersão React, porque temos muitas atividades para fazer nessa semana, são muitos conteúdos, exercícios e desafios extras que, ao final dessa aula, já começaremos a passar. 

Na primeira aula tivemos muitos códigos e informações. Nessa, teremos também desafios para que você consiga melhorar o seu projeto e ir além do que propomos. No método da Alura, temos roteiro, cursos, e desejamos que você personalize, "dê a sua cara", para o seu projeto e para o curso, criando portfólio, colocando no GitHub, mostrando quem você é.

Nós chamamos isso de "vitrine de Dev", é uma forma de mostrar como você aprende, pensa e sua capacidade de ir além. É esse profissional que as empresas estão buscando. 

Eu estou no mercado de educação, tecnologia e contratação há mais de uma década e percebo que, cada vez mais, as empresas estão propagando essa ideia, porque a tecnologia muda, o React daqui a cinco anos será outro, já existe o Next.js, que estamos estudando também, e isso tudo mudará, a versão mudará. Tendo este contexto eu e as empresas queremos saber se você é uma pessoa preparada para aprender e reaprender.

Para começarmos a aula, eu queria mostrar, Mario, que a Alura está muito além da Imersão, dos cursos e da formação. Existe uma página, que chamamos carinhosamente de **AluraVerso**, é o multiverso da Alura. Nós somos mais que uma plataforma, somos uma escola. No AluraVerso é possível encontrar todos os canais, influenciadores e cientistas que patrocinamos. Futuramente incluiremos as ONGs e os grupos minorizados que patrocinamos e ajudamos. 

Portanto, no AluraVerso há algumas dessas empresas e pessoas que estamos muito perto, por exemplo, Átila Iamarino, BrazilJS, Manual do Mundo, são pessoas que ajudam a ciência no Brasil e no mundo e eu gostaria de mostrar que você pode ir muito além conosco. Muito além da escola. 

Agora, vou aproveitar a deixa, começou um barulho de furadeira na minha casa, para que você, Mario, recapitule o momento em que paramos e explique quais os próximos passos.

**Mario:** Perfeito, Paulo. Inclusive, é uma honra fazer parte do AluraVerso e estar aqui, passando esse conteúdo de React que eu sei que ajuda muitas pessoas a conseguirem mudar de emprego ou até mesmo o primeiro emprego. Enfim, é uma honra imensa. Vamos revisitar o nosso projeto, que publicamos durante a última aula. 

Estou com o Terminal aberto, mostrando que estamos na aula 2, `aluracod git:(aula2)`. Não mudei nada no código, apenas a *branching* no GitHub para termos a *main*. Estou na aula 2 agora. Você pode seguir na *main*, não é obrigatório quebrar a *branching*. Vamos rodar o `yarn dev` para subirmos o nosso projeto e revisitarmos um pouco da última aula, contextualizando o que faremos agora. 

Vamos abrir uma aba nova, acessar [localhost 3000](http://localhost:3000/). O usuário do Paulo já está habilitado e aberto. Em "Explorer > Open Editors", dentro da pasta "pages" e nela o arquivo "index.js", no VSCode, temos os nosso GlobalStyle, que vamos minimizar apertando a seta à frente de `function GlobalStyle() {`. Vamos minimizar o título também, `function Titulo(props) {`.

Mais abaixo, temos o nosso código base e, ao final da aula, colocamos uma página inicial customizada, `export default function PaginaInicial() {`, também tínhamos o usuário do Paulo no começo, `const username = 'peas';` e o `GlobalStyle`.

```
export default function PaginaInicial() {
    const username = 'peas';
		
		return {
		   <>
			     <GlobalStyle />
					 <Box 
					 
					 ```

Vários *boxes* são *divs*. Um deles tem o `as="form"`, que está mudando algo como a *tag* dele, um *box* como formulário. Em seguida, o `styleSheet={{` com todos os estilos que estamos passando. Mais abaixo, existe a área da foto, que comparamos no GitHub. Inclusive, fica esse segredo: se você pegar qualquer usuário do GitHub e colocar `.png` no final, você consegue pegar a imagem `.png` da pessoa que você segue ou do seu próprio usuário. 

```
<Image 
    styleSheet={{
		   borderRadius: '50%',
			 marginBottom: '16px',
	  }}
		src={'https://github.com/${username}.png'}
	
	/>

```

Para isso, basta acessar o GitHub, por exemplo, vamos até o meu usuário acessando a URL https://github.com/omariosouto. Se ao invés de barra, eu colocar ".png", isto é, https://github.com/omariosouto.png, ele traz a minha foto. Fica esse *easter egg* do GitHub para vocês. 

Portanto, nós temos todo esse trecho de código. Vamos pegar o `username` que aparece acima, atribuir na variável na imagem e do texto. São conteúdos que já estudamos na última aula, usar o "bigodinho" e atribuir variáveis. 

```
<Text 
   variant="body4"
	 styleSheet={{
	     color: appConfig.theme.colors.neutrals[200],
			 backgroundColor: appConfig.theme.colors.netrauls
			 padding: '3px 10px'
			 borderRadius: '1000px'
		}}
  >
     {username}
	  </Text>
  </Box>
 {/* Photo Area * /}
</Box>

```

**Paulo:** Nós estudamos o componente do título que era passado como argumento. 

```
export default function PaginaInicial() {
   const username = 'peas';
	 
```

Agora estamos separando uma variável *hardcoded*, a `username`, e estamos substituindo essa variável - que é o meu login no GitHub - em dois lugares. Um deles é na imagem, e temos um truque famoso que é usar `github.com/` e o seu `username.png`. Ao entrar no site, ele mostrará a imagem. O `username` também está aparecendo em um `Text`. Ele é um componente da biblioteca. 

Nós poderíamos usar um componente da biblioteca Material-UI do android ou de outra biblioteca. Nós estamos usando uma nossa, mas cada pessoa pode criar seu próprio componente, por exemplo, "textobonitinho". Então, você cria a *function* "Textobonitinho" e faz, assim como criamos ontem, a *function* "Título". 

Tudo que estamos usando, nós estudamos anteriormente. O que aparece grande e pode assustar um pouco pela quantidade é o `TextField`, `fullWidth`, `textFieldColors={{`. Essa é a parte que mais tem a ver com a estilização, com o CSQS. 

**Mario:** Quase todas as estilizações que vocês estudarão, nos componentes como o `Button` e `TextField`, são sempre de cor, por exempo, `mainColorLight: appConfig.theme.colors.primary[`, porque ele já tem algum tamanho específico: pequeno, médio ou grande. E nas caixas, existe a especificação, não do destino, mas de espaçamento, de display, que compete muito mais à parte estrutural da página. 

Então, todo *box* tem estrutura e todo componente tem a parte visual. Essa parte está bem separada no código, mas o importante, Paulo, é fazermos o `username` ser alterado quando digitarmos no campo de login (No localhost 300 temos: "Boas vindas de volta! - Discord - Alura Matrix". Abaixo um campo de login seguido do botão "Entrar"). Essa será a nossa meta. 

Como fazemos esse processo todo acontecer? Vamos ao nosso código. Nele temos a `PaginaInicial()` e o `TextField`. Nós comentaremos o `TextField`, `{/* <TextField`, e adicionaremos a *tag* `input` básica do navegador. 

**Paulo:** Essa é HTML, não é? Não que não pudesse ser de outro jeito. 

**Mario:** Isso! Só para conseguirmos trabalhar garantindo a quem está com um pouco de receio do componente que perceba se tratar da mesma coisa e que conseguimos fazer os dois funcionarem sincronizados. 

```
 <input type="text" />
 {/* <TextField 
      fullWidth
			textFieldColors={{
			 
		```

Ao voltar à página (localhost 3000), tivemos um `input` meio "feio", mas funcional. Se digitarmos o *username* no campo de login, ele está aparecendo. Gostaria de perguntar sobre o `input`, Paulo, você se lembra, no tempo em que fazia as integrações do Java para HTML, qual era a propriedade com que definimos um valor inicial para um campo?

**Paulo:** É o `value`? 

**Mario:** Sim! É o `value`. 

**Paulo:** Nossa! Eu não faço isso há uma década!

**Mario:** Não tem problema! Em qualquer campo, se adicionarmos um `value` padrão, por exemlo, o usuário do Paulo, o `peas`

```
 <input
     type="text"
		 value="peas"
	/>
	
	```

Ao retornar à página, notaremos que "peas" já aparece no campo de login. Ou seja, o `value` apareceu. A nossa meta será: sempre que digitarmos, mudar tanto a foto que pegaremos do GitHub, quanto o texto que aparece abaixo da foto, "peas". Essa é a nossa primeira missão. 

> No centro da tela há um retângulo. Dentro dele, à esquerda, aparece a mensagem: Boas vindas de volta - Discord - Alura Matrix, com um campo de login abaixo e o botão "Entrar". À direita, uma imagem recortada em formato circular do rosto de Paulo Silveira, ele é um homem branco, usa óculos de armação quadrada na cor marrom, tem barba e cabelos curtos e usa uma touca cinza.

Basicamente, teremos que digitar e fazer funcionar. Mas, Paulo, repare que "bizarro", estou digitando no campo de login e nada acontece, isso se dá porque quando colocamos o `value` no `input` e no `React`, ele faz parar de funcionar. 

Se retornarmos ao código e apagarmos o `value="peas"` e dermos um *reload* (recarregarmos a página) para digitar, ele permite de novo. A reposta disso está no Console. 

**Paulo:** Não era esperado funcionar assim. 

**Mario:** Não era esperado. No HTML normal, se você escreve o `value`, ele te deixa digitar. Vamos abrir o Console e verificar o que está ocorrendo. Estamos digitando no campo de login da página. Se adicionamos o `value="peas"` ao código, no Console aparece uma mensagem de erro: um componente está mudando um input que não está sendo controlado. Isso está causando algo como o value trocar de undefined para um valor definido, o que não deveria acontecer. 

Portanto, ele está alertando que deveríamos ter um componente controlado ou um não controlado. Nós discutimos bastante o conceito de componente. Ele é "quem manda". Quando estamos trabalhando com interfaces, o componente é quem ajuda a montar. Porém, a chave da popularidade do React vem de um outro conceito chamado de **estado**. 

Para o React, cada vez que digitamos no campo de login, é como se ele estivesse tirando uma nova foto de como está o código no exato momento em que digitamos. É como a água, encontrada nos estados sólido, líquido e gasoso. No código, cada alteração que fazemos é um novo estado. Cada mudança, cada *menu* que abrimos e fechamos, ou até cada letra que digitamos, é uma alteração de estado.

Quando o React fala de *controlled* e *uncontrolelled* é porque ele sabe que se o `input` tem o valor de `value` associado a ele, provavelmente esse valor muda. E se ele muda, é necessário dizer ao React que esse valor tem a possibilidade de interagir com esse estado, de gerar uma nova versão. Precisamos de alguma forma dizer que esse valor pode ser alterado mesmo que definamos um valor que está estático, por exemplo, `value="peas"`.

Fez sentido essa ideia de poder mudar? Então, que o React precisa saber de cada caractere que mudou? Por enquanto, ele não sabe. Só escrevemos um texto direto. Para ligar essa parte de mudança de estados e gerar uma nova versão com o React, vamos vincular o `value` com alguma variável. Se vamos mudar para algo que varia, o caminho lógico é usarmos uma "variável". 

Podemos colar a variável `usarname`, que aparece mais acima no código, no valor que está mais abaixo. Seguiremos a seguinte lógica: abrimos chaves (também conhecidas como "bigodinhos") e chamamos o `username`. 

```
 <input 
     type="text"
		 value={username}
	/>

```

Se voltarmos na página e carregarmos, verificando em paralelo o Console, notamos que ainda aparece o erro. Porém, se alterarmos o código em `const username = 'peas';` para `const username = 'omariosouto';`, ele passa a pegar o meu usuário. Na página, perceberemos que está sincronizado o nome com a imagem e o campo. O erro, no entanto, ainda aparece. 

Para que o erro pare de aparecer, precisamos recordar que ele mostrou uma mensagem, dizendo: você proveu uma propriedade value para um campo de formulário sem um `onChange handler`. Significa que passamos a variável, então o React sabe que esse valor vai variar, mas, além do valor da variável, ele precisa saber o que acontece quando ele vai capturar essa foto da página. 

Ou seja, ele precisa acompanhar e saber o que fazer cada vez que o usuário digitar. Para isso, ele pede o valor de `onChange`. Portanto, vamos incluir esse `onChange handler` no nosso código, que é, basicamente, uma função. Precisamos ir até o `input`, incluir `onChange` e passar uma `function`.

O nome pouco importa, vamos colocar `handler` apenas para seguir a nomenclatura que geralmente colocam, mas, é possível passar sem nome e vai funcionar da mesma maneira. 

```
<input
    type="text"
		value={username}
		onChange={function handler() {
		
		}}
	
	/>

```

Também vamos colocar `console.log('usuario digitou')`. 

```
<input
    type="text"
		value={username}
		onChange={function handler() {
		  console.log('usuario digitou')
		
		}}
	
	/>

```

Em seguida, carregaremos a página de novo. Ao conferirmos o Console, notaremos que parou de dar erro. Nesse momento, resolvemos o problema. Se digitarmos no campo de login, o React agora sabe que o usuário digitou, sabe também que o valor deveria variar, mas não sabe como mudar esse valor. Fez sentido, Paulo?

**Paulo:** Fez sentido! 

**Mario:** Nós conseguimos colar as coisas de maneira que o React sabe do valor, sabe que está capturando a digitação do usuário, mas ele ainda não sabe como muda. Se temos uma variável `username`, o que deveríamos fazer todas às vezes em que o usuário digita?

**Paulo:** Trocar a variável. 

**Mario:** Sim! Trocar a variável, queremos `// Trocar o valor da variável`. Mas a pergunta é, `// Onde ta o valor?`. 

**Paulo:** Com certeza, vai ter que receber como parâmetro.

**Mario:** Exato! Esse valor vem da ação do usuário, logo, a função `onChange` só é executada quando o usuário digita. Toda vez que digitamos, ele chama essa função de novo. Coloca parênteses no final e executa. 

**Paulo:** Mario, basicamente, o que você está nos mostrando é o funcionamento mais importante do "coração" do React. É quando você quer disparar que outra coisa aconteça em outro lugar. Algo assim. 

**Mario:** Exatamente. É isso mesmo. Sempre que digitamos, o navegador nos dá uma variável chamada `evento` ou `infosDoEvento`, ou ainda, `event`. Pode chamar da maneira que você preferir, o nome pouco importa. O importante é a ordem, o primeiro parâmetro terá o evento. Se dermos um `console.log()` nele, você perceberá que ele é um tanto "bizarro".

```
<input
    type="text"
		value={username}
		onChange={function (event) {
		  console.log('usuario digitou', event);
			 // Onde ta o valor?
			 // Trocar o valor da variavel
		
		}}
	
	/>

```

Cada vez que digitamos, ele mostra no Console o `SynteticBaseEvent`, com `bubbles`, `cancelable`, `currentTarget`, enfim, uma série de informações, e dentre elas há um valor chamado de `target` com `value`. Dentro dele, há o valor atual do campo que estamos digitando. No caso, `"omariosouto"`. 

```
target: input
  value: "omariosouto"

```

**Mario:** Nesse caso, ele está pegando o `omariosouto`. Vamos tentar acessar o `event.target.value`.

**Paulo:** Aí eu não preciso usar um cifrão, porque está dentro de um bloco Javascript puro, certo?

**Mario:** Exatamente. Se você passa o mouse sobre o `event`, o VSCode inclusive mostra: 

```
(parameter) event:
ChangeEvent <HTMLInputElement>
```

Já sobre o `.target`, o VSCode mostra:

```
(property)
ChangeEvent<HTMLInputElement>.target
EventTarget & HTMLInputElement
```

E no `value`:

```
(property) HTMLInputElement.value:
string
```

**Paulo:** Nossa, ele sabe todas essas informações?

**Mario:** Sabe, está bem especificado. Vamos salvar. Repare que quando eu digito a letra "a" na caixa de texto, ela é exibida no final da string que é mostrada no console, por exemplo "omariosoutoa". Se eu digitar "b", essa é a letra exibida, resultando em "omariosoutob". 

Isso acontece pois o navegador está tentando colocar mais um caractere ao final do nosso input, mas o React entende que precisa preservar o estado antigo da página, bloqueando essa alteração. Dessa forma, a última letra na string exibida no console vai mudar, mas o que está acontecendo na página não.

O React precisa desbloquear o navegador para que uma nova versão seja gerada e a página atualizada. Nós já temos o valor do campo e uma variável, e agora precisaremos usar um recurso do React.

O valor de `username` não poderá mais ser somente uma variável, mas também precisará ser capaz de ser alterado internamente de acordo com o estado do React. Para trabalharmos isso, vou comentar a variável `username` e recriá-la.

Antes de declarar a variável, usarei a instrução `React.useState()`.

```
export default function PaginaInicial() {

	const = React.useState('');
	
	return {
//...
}
```

Feito isso, o React será importado no cabeçalho da página. Na declaração da variável, ao invés de passarmos somente `username`, que é o nome dessa variável, usaremos também `setUsername`, uma função que permite definir um novo valor a essa variável. 

```
export default function PaginaInicial() {

//const username = 'omariosouto';
	const [username, setUsername] = React.useState('');
	
	return {
//...
}
```

**Paulo:** Essa é uma sintaxe do Javascript na qual o `useState()` devolve dois valores, certo?

**Mario:** Isso. Parece magia, mas vou mostrar para deixar mais claro. Se declararmos uma variável `stateDoReact` recebendo a chamada de `useState()` e executarmos o `console.log()` dessa variável, teremos:

```
export default function PaginaInicial() {

	const username = 'omariosouto';
	const stateDoReact = React.useState('');
	
	console.log('stateDoReact', stateDoReact)
	return {
//...
}
```

O retorno no console será um array na qual o primeiro item é um valor vazio e o segundo uma função. Se passarmos o valor `omariosouto` na chamada de `useState()`, o primeiro valor do array será `omariosouto` e o segundo uma função - no caso, a função que altera esse primeiro valor, ou seja, faz o "set".

Como é um array, podemos "desestruturá-lo", pegando o valor de `username` e o de `setUsername`. Por convenção, sempre utilizamos essa sintaxe parecida com a de array - `[username, setUsername] ` -, mas expandindo o resultado daquilo que vem depois do igual. 

```
export default function PaginaInicial() {

//const username = 'omariosouto';
	const [username, setUsername] = React.useState('');
	
	return {
//...
}
```

**Paulo:** Preste atenção, pois essa parte da explicação é muito importante, já que é algo que você fará o tempo inteiro em React. Você dificilmente trabalhará com variáveis "puras" como já estávamos acostumados, e bem mais com `useState()`, com o qual você inicializa uma variável - às vezes até vazia - e recebe o valor que será exibido e quem deverá ser chamado quando for necessário alterá-lo. 

Quando você alterar esse valor, o React acionará diversos mecanismos internos para atualizar o que for preciso. É o que chamamos de "observer" (ou "listener"), entidades responsáveis por acompanhar os estados dessas variáveis e fazer as alterações devidas, como alterar uma cor, ativar uma notificação e assim por diante. Às vezes um único evento, como alterar uma simples variável, dispara diversas ações na tela ou no próprio backend. 

**Mario:** É verdade, coisa que nós faremos também, por exemplo um chat cuja tela atualiza sempre que há uma nova mensagem. 

Continuando, temos o nosso `username`. Se eu recarregar a página, não teremos nenhum erro e o usuário continua funcionando. Ainda não é possível alterá-lo, já que não utilizamos a função `setUsername()`, responsável por alterar o valor e gerar um novo estado da página.

Vamos acessar o campo `<input>` e inserir `const valor = event.target.value;` em nosso `onChange`. 

```
<input
	type="text"
	value={username}
	onChange={function {event} {
		console.log('usuario digitou', event.target.value);
		// Onde ta o valor?
		const valor = event.target.value;
		//Trocar o valor da variavel
		}}
	}

```

Em seguida, para trocarmos o valor da variável, chamaremos `setUsername()` passando o novo `valor`.

```
<input
	type="text"
	value={username}
	onChange={function {event} {
		console.log('usuario digitou', event.target.value);
		// Onde ta o valor?
		const valor = event.target.value;
		//Trocar o valor da variavel
		//através do React e avise quem precisa saber 
		setUsername(valor);
		}}
	}

```

Eu gosto de deixar esses comentários, e recomendo que vocês deixem também para que fique evidente o que está acontecendo e por que. Isso ajuda bastante a analisar o código no futuro e estudar.

**Paulo:** Isso é mais do que trocar o valor da variável, é trocar por meio do React e avisar quem precisa ficar sabendo, certo?

**Mario:** Exatamente. 

**Paulo:** Se eu pegasse aquela variável `username = valor`, não iria funcionar - primeiramente porque é um `const`, e também porque o resultado não seria o esperado. É fundamental utilizarmos essas funções do tipo "set". 

**Mario:** Sim, sempre vai ser "set" seguido do nome da variável que estamos alterando. Vou salvar as alterações e carregar a página. Agora nós conseguiremos apagar o texto do input, o que também alterará a imagem que é carregada. Se digitarmos "omariosouto", aparecerá minha foto; se digitarmos "alura", será exibido o logo da Alura, e assim por diante.

Isso acontece justamente por essas questões que o Paulo comentou. Conforme alteramos o campo input, o React muda o estado da página em tempo real. Vou inspecionar a página e acessar o código-fonte, pois acho que demonstra bem o que está acontecendo.

Nele, encontramos o nosso `<input>`, o `<img>` e o `<span>`. Repare que, conforme alteramos o que é digitado no input, somente os campos que possuem a variável são alterados - nosso componente de imagem e o campo de texto com o `username`. 

O React é inteligente ao ponto de alterar somente aquilo que é necessário na página, o que costuma ser chamado de "virtual dom". Ele mantém uma cópia, que é aquilo que está na página, e as alterações são feitas em uma versão duplicada dessa página na memória, alterando o que é necessário e comparando as diferenças entre o que está no HTML e o que foi editado, aplicando essas diferenças.

Toda alteração que fazemos na página tem um custo muito grande para o navegador, e o React otimiza esse processo gerando um lote de alterações e aplicando-o de uma só vez. Por isso o React é famoso por sua performance, já que consegue agrupar várias alterações para realizá-las de uma vez só. Isso pode ser visto claramente pelo código-fonte da página, onde todos os elementos são alterados ao mesmo tempo.

**Paulo:** Perfeito. Isso é algo que, se a gente fosse fazer usando Javascript puro, teríamos que alterar em vários pontos do código, talvez até fazer um `for`.  

Aqui as coisas estão "invertidas": o React sabe os pontos em que `username` é utilizado e, quando chamamos o `setUsername()`, ele altera não só o valor da variável, mas também todos os trechos que utilizam essa variável nos elementos.

Esse é basicamente o funcionamento geral do React, o que acontece muitas vezes. Na maneira antiga de trabalharmos com a web, a pessoa digitaria o nome nesse campo input e recarregaríamos a tela inteira, pegando essa variável e mandando para o back-end, renderizando tudo novamente, para então mostrar o resultado. 

Com o React esse processo fica mais leve e mais fácil, sem precisar de muito trabalho manual.

**Mario:** Perfeito, Paulo. É exatamente isso que você trouxe para a galera. Quando alguém te perguntar em uma entrevista "por que o React é bom?", você pode responder isso, sobre a otimização. É isso que mostra que você conhece a ferramenta, não é só criar componentes ou usar várias libs.

Vou até deixar um vídeo aqui na descrição no qual, em menos de 30 minutos, eu refaço o React do zero. Então eu crio um arquivo Javascript e saio criando todas as coisas que fazem o React funcionar, e acho que é uma ótima referência para você que está começando a carreira e quer entender um pouco de como o React funciona por baixo dos panos. É um bom ponto de partida para você dar esses primeiros passos e ir se aprofundando, conforme for necessário e você for se sentindo mais confiante. 

Acho que já conseguimos entender bem essa ideia de termos variáveis e alterarmos seus valores. Outra coisa importante é fazermos testes. O Paulo disse uma coisa muito importante: e se não usássemos o `setUsername()`?

Vou comentar a linha do `setUsername` na função `PaginaInicial()` e voltar a usar a variável `username` que tínhamos antes.

```
export default function PaginaInicial() {

	const username = 'omariosouto';
//const [username, setUsername] = React.useState('');
	
	return {
//...
}
```

Com isso, não conseguiremos mais digitar no campo que temos na página. Agora tentaremos atribuir o valor em nosso `<input>`.

```
<input
	type="text"
	value={username}
	onChange={function {event} {
		console.log('usuario digitou', event.target.value);
		// Onde ta o valor?
		const valor = event.target.value;
		username = valor;
		//Trocar o valor da variavel
		//através do React e avise quem precisa saber 
		setUsername(valor);
		}}
	}

```

Após salvarmos, veremos que as alterações que fizermos no campo input não serão atribuídas e nada será exibido na página, ainda que nenhum erro seja exibido no navegador. Em teoria, como temos um valor constante, ele não deveria mudar. 

De qualquer forma, nosso código não funciona pois é o `setState()` quem avisa ao React de que é necessário alterar cada um dos valores e que pedaços da página precisam ser atualizados. Por isso devemos usar o `setUsername()` e não só atualizar o valor diretamente.

**Paulo:** Isso pode ser estranho para quem usava Javascript puro e está aprendendo agora, já que sempre usávamos o nome de uma variável recebendo um novo valor. Aqui nós precisamos "avisar", chamar uma função, do contrário o React não ficará ciente dessa mudança de estado. 

Sempre que tivermos uma variável que precisa refletir em outros pontos da aplicação, provavelmente usaremos o `useState()` e chamaremos pelo *setter*, ou não teremos o efeito desejado. 

**Mario:** Perfeito, Paulo. Aqui nós conseguimos fazer essa primeira parte. Agora eu vou comentar o `<input>` e descomentar o `TextField`, que é o nosso campo de texto. 

Se inspecionarmos esse elemento, veremos que por baixo dos panos ele é uma tag `<input>` comum. O que muda é que passaremos o `value=(username)` e o `onChange`.

```
<Textfield
	value=(username)
	onChange={function {event} {
		console.log('usuario digitou', event.target.value);
		// Onde ta o valor?
		const valor = event.target.value;
		//Trocar o valor da variavel
		//através do React e avise quem precisa saber 
		setUsername(valor);
		}}
/...
``` 

Após salvarmos, conseguiremos alterar o campo input livremente, com o React atualizando a página de acordo com essas alterações. 

É legal reparar nisso. Olhar o que está sendo renderizado na tela vai te ajudar muito quando você estiver utilizando componentes criados por outras pessoas, porque às vezes você precisa ver qual o HTML que está sendo gerado para entender como determinadas coisas estão funcionando. Portanto, crie o hábito de inspecionar a página e verificar na aba "elements" o que está acontecendo, o que está renderizando e assim por diante. 

No console, temos alguns erros que ocorrem porque às vezes não existe uma imagem do Github correspondente ao que foi digitado no input. Isso vai até virar um desafio no final da aula. 

Paulo, estamos falando bastante do React, mas acho que faltou uma coisa, que é entrarmos no chat de fato usando o botão de "Entrar" na nossa página.

**Paulo:** Perfeito, como submeter um formulário. Como funciona isso? Nós já vimos o `onChange` de um componente de texto, e acho que até funciona de maneira similar com outros. Agora quero entender como o botão de "Entrar" pode redirecionar para outra tela, fazer um pop-up ou outra coisa, fazer o `onChange` dele, ou `onSubmit` que tínhamos no Javascript. 


**Mario:** Perfeito. Repare que toda vez que clico em "Entrar" a página atualiza. Esse é o comportamento que você citou agora há pouco, de mandar uma requisição para o servidor e recarregar a página. Isso acontece, principalmente, se você estiver trabalhando dentro de uma tag de formulário (`<form>`), como podemos verificar inspecionando a página. 

Se procurarmos por "form" em nosso código, encontraremos um `<Box>` que está como formulário (`as="form"`), incluindo também os seus estilos. O padrão de um formulário é sempre recarregar a página, mas quando trabalhamos com frameworks como o React e o Next, passamos a evitar ao máximo esse recarregamento total, preferindo alterar somente um pedaço da página.

**Mario:** Temos que prevenir esse comportamento padrão da página de mudar as coisas. E você comentou de submeter o formulário, o que me lembra que sempre que temos uma tag de formulário podemos usar um valor chamado `onSubmit`, você pode passar uma função para ele e, tal como o `onChange`, que é sempre que tiver uma mudança, o `onSubmit` vai monitorar e sempre que tiver uma submissão vai fazer alguma coisa. Vou colocar um `console.log()` também.

```
onSubmit={function () {
   console.log('Alguém submeteu o form');
}}
```

**Mario:** Vou salvar, carregar a página e ao clicar no botão "Entrar" ele mostra rapidamente no console a mensagem do `console.log()`.

Temos que prevenir esse carregamento. Para prevenir isso pagamos de novo as `infosDoEvento`. Eu falo: "`infosDoEvento` previne o default, por favor". Prevenindo o default ele para de recarregar a página e agora nós temos o controle de como ir para a próxima página.

```
onSubmit={function (infosDoEvento) {
  infosDoEvento.preventDefault();
  console.log('Alguém submeteu o form');
}}
```

**Paulo:** Porque o comportamento default do *submit* de um form é ir para uma URL que ele definiu como destino e se não definiu vai para a URL dela mesma.

**Mario:** Então, queremos ir para a próxima página, que seria a página de chat, http://localhost:3000/chat, que não existe. Se tentarmos ir para essa URL o próprio Next retorna uma página "404".

Agora, vou mostrar como criar uma nova página. No VS Code, vamos no menu *explorer*, à esquerda, e dentro da pasta "pages" criaremos um arquivo chamado `chat.js`. Dentro desse arquivo vamos escrever:

```
export default function PaginaDoChat() {
  return (
    <div?>Página do Chat </div>>
    
  )
}
```

**Mario:** O Next já sabe que isso é uma página e que ele tem que renderizá-la. Podemos carregar no navegador o endereço http://localhost:3000/chat. Cria um arquivo e já tem uma página, não precisa se preocupar com roteamento, ele já faz isso para nós.

**Paulo:** Então, `chat.js`. Por ela ser a única em que fazemos `export default` pode ser o nome que quisermos aí onde você colocou `PaginaDoChat`.

**Mario:** Exatamente, eu deixei `PaginaDoChat`, mas pode ser qualquer nome.

É importante dizer que o Next gerencia as páginas para nós. É ele que faz as coisas acontecerem. Se quisermos mudar de página tem várias formas. Vou mostrar uma delas. Podemos inserir no `onSubmit` um `window.location.href = '/chat';`. 

```
onSubmit={function (infosDoEvento) {
  infosDoEvento.preventDefault();
  console.log('Alguém submeteu o form');
  window.location.href = '/chat';
}}
```

**Mario:** Esse é o jeito tradicional de o navegador fazer isso. Inclusive, se colarmos essa linha de código e colarmos no console do navegador, na home, ao pressionarmos "Enter" ele muda de página, vai para a página do chat.

Se eu carregar a home e clicar em "Entrar" ele vai para a página do chat também. Mas repare que ele está sempre recarregando a página durante essa transição, podemos ver que o ícone de atualizar, na área superior da página, está recarregando.

Como é o Next que gerencia essa parte de roteamento, o Next tem um recurso certo para fazer troca de páginas. No topo do arquivo `index.js` vou fazer `import {useRouter} from 'next/router';`. Vamos pegar o sistema de roteamento do Next.

Viram que tem uma semelhança em como se escreve `useRouter` e `useState`? Eles fazem parte de um padrão do React chamados "Hooks", são ganchos para você interceptar algo.

**Paulo:** E o `setUsername` também é um hook?

**Mario:** Sim, exatamente. Deixei para trazer agora para mostrar justamente isso. É o gancho do roteamento, o gancho de manipular o estado, o gancho de efeito. Sempre tem algum gancho no React para fazer alguma coisa. É sempre acompanhado do "use".

Então, na `PaginaInicial()` vou fazer `const roteamento = useRouter();`. Basta fazer isso para usarmos. Se dermos um `console.log(roteamento)`, podemos ver lá no console do navegador que ele mostra uma lista informando qual é a pasta em que estamos, qual o `basePath`, qual a função para voltar página, um monte de coisas.

A navegação da web é como se ela fosse uma pilha, um array, estamos sempre colocando uma coisa em cima da outra. Tanto que olhando essas funções que temos para trabalhar, temos aqui o `push`, que serve para adicionar mais uma URL nessa pilha de navegação.

Voltando para o VS Code, vou apagar o `console.log(roteamento)` e dentro no nosso `onSubmit` vou escrever `roteamento.push('/chat')`.

```
onSubmit={function (infosDoEvento) {
  infosDoEvento.preventDefault();
  console.log('Alguém submeteu o form');
  roteamento.push('/chat');

}}
```

**Mario:** Fazendo isso, ao clicar no "Entrar" ele vai para a página do chat e não faz mais aquele carregamento. Podemos ver na aba "Elements" do Inspecionar o que muda nessa transição. Mudou só os pedaços que precisavam.

Aqui já fechamos o conteúdo dessa aula. Só quero trazer um adicional antes do desafio. Está vendo que aqui na página do chat a fonte do texto mudou, voltou a ficar com a serifa? O `GlobalStyle` não está funcionando aqui. Ele está global, mas está global na página inicial.

Precisamos colocar o `GlobalStyle` aqui na página do chat também. A forma correta de fazer isso, é o seguinte. O Next tem um arquivo em que ele encapsula todas as páginas que serão carregadas, ou seja, se você quer que algo realmente fique em volta de tudo, você coloca nesse arquivo. Vamos entrar no link do <a href="https://nextjs.org/docs/advanced-features/custom-app" target="_blank">Custom App na documentação do Next</a>.

O que faremos é, basicamente, copiar esse código da documentação e criar o arquivo `_app.js` dentro da pasta "pages".

Esse `_app.js` não vai virar uma página. Precisa fazer o `export default` dele e a vantagem é que tudo o que colocarmos aqui será carregado em todas as páginas.

```
export default function MyApp({ Component, pageProps}) {
  console.log('Roda em todas as páginas');
  return ( 
    <Component {...pageProps} />
  );
}
```

**Mario:** Essa mensagem "Roda em todas as páginas!" vai aparecer no console da página do chat e na home também. Está em volta de tudo, é um *wrapper*, ele carrega em volta de todas as páginas.

Importante falar que no React é muito comum, quando você instala uma lib ou quer algo genérico na sua aplicação inteira, você configurar nesse arquivo `_app.js`. Por isso é importante saber que ele existe. No nosso caso, a configuração será de CSS.

Vamos recortar o trecho de código do `GlobalStyle()` que está no `index.js` e colar dentro do `_app.js`, no topo do código. E no `function MyApp` vamos chamar o `<GlobalStyle>` lembrando de colocar aquela estrutura da tag vazia em volta, `<> </>`.

```
export default function MyApp({ Component, pageProps}) {
  console.log('Roda em todas as páginas');
  return ( 
    <>
    <GlobalStyle />
    <Component {...pageProps} />
    </>
  );
}
```

**Paulo:** Todas as páginas `.js` vão chamar essa function que está no `_app.js`. Essa função está como `MyApp`, mas podia ser qualquer coisa.

**Mario:** Exato. Podia ser só `App`, ou `CustomApp`, por exemplo.

**Paulo:** O importante é esse `_app.js`, esse é um nome que o Next reconhece e o que estiver aí todo mundo tem acesso.

**Mario:** Lembrando que não precisamos mais chamar o `<GlobalStyle>` no código da `PaginaInicial`, podemos apagar essa linha.

Vamos ver como está nossa página inicial. Claro, tem mais detalhes para gerenciar tudo isso, mas continuaremos nas próximas aulas. 

**Paulo:** Hoje mostramos os principais recursos do React e do Next. O Hook do state e do roteador são coisas que você vai mexer no React o tempo inteiro. 

**Mario:** Para tudo, para abrir formulário, abrir menu etc. Tudo vai mexer com esses dois de alguma forma.

**Paulo:** Mario, por que no `useRouter` não foi preciso colocar "React.useRouter"?

**Mario:** Porque esse `useRouter` é do Next. Estamos importando direto do Next.

Então, nessa aula vimos `useState`, vimos que ele propaga alteração para todos os lugares; vimos o `useRouter`; trabalhamos com eventos, `onSubmit` para o formulário; `onChange` para campo de texto; a importância de sincronizar o `value` com o `onChange`, de usar a função `setUsername` para avisar o React que mudou e vimos como criar uma página nova, que basta criar um arquivo `.js` dentro da pasta "pages".

Eu até gosto de falar que a pasta "pages" é do Next, não é sua, tudo que está dentro dela o Next usa para montar as estruturas dele e fazer a organização da aplicação.

Paulo, qual vai ser o desafio da aula de hoje para a galera?

**Paulo:** O meu primeiro desafio - ainda não é nem desafio de implementação - é que você teste e tenha total domínio do `useState`, do `useRouter` e do que fizemos no `onSubmit` e no `onChange`, que é um pouco diferente de como faríamos no JavaScript clássico.

Quando você entender essa parte, vai começar a entender todo o mecanismo do React. Cerca de 90% do que vamos usar está muito atrelado a essa aula aqui.

Na primeira aula entendemos sobre componente, mas agora entendemos como o componente é vivo na tela, como atualiza só uma parte, como ele fica sabendo o que mudou, o que clicou e repercute isso onde precisa repercutir.

Os detalhes do CSS, de onde buscou cada coisa, se o `_app.js` é do Next ou do React etc, vai ficar mais claro no decorrer da Imersão.

Agora eu quero que você se concentre nessa parte que o Mario passou hoje, porque realmente vai aparecer o tempo inteiro tanto aqui na Imersão quanto no seu dia a dia profissional.

**Mario:** E para te ajudar nessa missão, eu gostaria de desafiar você a fazer com que se o campo tiver menos de dois caracteres, você desabilita o campo e não mostra a imagem, ou seja, só mostra a imagem se tiver mais de dois caracteres no campo de texto e a validação.

**Paulo:** Essa é uma boa ideia. Acho que usa o `onChange`, é por aí?

**Mario:** Já está feito, só precisa criar uma variável e passar para o botão. Essa é a dica que vou dar.

**Paulo:** Perfeito. Esse já é um mecanismo muito bom para começar a validar e entender onde passa a variável, entender se vai ou não ter "use", testar e errar, que faz parte. 

O que eu queria ver também, de desafio, é você customizar mais a sua tela. Ele não precisa puxar só sua imagem do GitHub, dá para puxar mais coisas. Tem uma página que dá para você acessar e pegar um JSON com vários dados. Vamos compartilhar a tela para mostrar isso?

**Mario:** Vamos. Vamos acessar a página https://api.github.com/users/omariosouto, você pode acessá-la inserindo o seu usuário no final. Essa página exibe um JSON com várias informações do seu usuário, nome, id, foto, a URL do perfil, os seguidores, entre outras coisas.

**Paulo:** Perfeito. Dá para brincar bastante com isso.

**Mario:** Vamos deixar materiais para consulta na descrição dessa aula. Se você quiser fazer esse desafio, pode ver um vídeo no meu canal em que mostro como pegar essas informações. Inclusive, usando o GitHub como exemplo.

**Paulo:** Estamos esperando para ver seu projeto no Discord, nos marque, use nas redes sociais as hashtags #imersaoreact, #alura, compartilhe no LinkedIn. Já tem muita gente nos marcando e estamos muito orgulhosos de ver seu trabalho e sua evolução. 

Inclusive, vamos trazer algumas empresas para ver os projetos de vocês, empresas que precisam contratar não só React, mas JavaScript puro e Angular, por exemplo. Mesmo a Imersão focando no React Next, que é o maior mercado de front-end, você verá que ao mostrar sua capacidade de aprender e encarar uma Imersão da Alura do início ao fim, as empresas enxergam valor nisso.

Não é à toa a quantidade de empresas parceiras do Aluraverso e que estão conosco como clientes da nossa escola. Essas pessoas estão buscando pessoas como você, que está demonstrando sua capacidade de aprender.

Nos vemos amanhã na próxima aula. Tchau!