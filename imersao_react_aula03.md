**Mario:** Boas-vindas à terceira aula da Imersão React da Alura! Hoje conheceremos algo que resolve um dos maiores erros de quem trabalha com front-end. Mas antes, sei que você tem um recadinho para a galera, Paulo.

**Paulo:** Eu tenho. Estou muito feliz de estarmos na terceira aula, e você precisa acompanhar a hashtag #imersaoreact e ver o que está aparecendo no LinkedIn, Twitter e Instagram. Está incrível! 

Só de mostrar os primeiros passos da segunda página, as pessoas foram muito além. Parabéns para você que está elevando essa Imersão a um nível muito maior e entendendo os conteúdos que estamos apresentando. Lembrando que o `useState` do React e o `useRouter` do Next são ferramentas com as quais você trabalhará o tempo inteiro.

Se você entender bem esse funcionamento, e que não basta usar uma variável simples, esse universo do React já vai ficar mais evidente para você. Nós queremos que você realmente conheça o funcionamento do React, seus conceitos desde a base, e não só que aplique código. 

Nós estamos aplicando bastante coisa, e vamos aplicar muito mais, mas queremos que você saia dessa Imersão com conhecimentos sólidos e um portfolio para mostrar para as pessoas. Nós sempre batemos nessa tecla, e é por isso que as Imersões da Alura têm esse resultado fantástico. 

Inclusive estamos colocando essa ideia de portfolio dentro das formações da Alura, com sugestões de práticas, como exercitar seus conhecimentos, o que você pode criar e assim por diante, para realmente te desafiar a mostrar os seus passos. É assim que queremos que você prossiga, não é?

**Mario:** Exatamente, Paulo.

**Paulo:** Eu vou pedir aqui uma intervenção da produção para colocar mais um depoimento, para você ver onde que as pessoas que estudam conosco na Alura chegam na área de front-end. É sempre muito inspirador ouvirmos histórias reais dos nossos alunos e alunas, e tenho certeza que isso vai impactar o seu trabalho. 

**Rene Sena:** A Alura me apresentou muitos conhecimentos novos. Por exemplo, essa questão de criação de rotas dinâmicas, pré-renderização de dados no servidor, assuntos que eu nunca imaginei que aprenderia ou mesmo que o front-end conseguiria fazer. 

Essa é uma visão que me surpreendeu bastante, essa questão do que fazer como desenvolvedor front-end ou em outra função na área de TI, e você tem muitas possibilidades. Quando eu estava na Imersão, foi como naquele meme de explodir a cabeça das pessoas. 


**Paulo:** Muito legal não é Mario? Acho que é mais um motivo para levarmos os projetos até o fim e dedicarmos essas horas por dia durante a semana da Imersão React.

**Mario:** É legal aproveitar essa oportunidade, esse momento em que você não está sozinho ou sozinha estudando. Tem várias pessoas pelo Brasil todo, e até de outros países, pessoas que falam outras línguas, assistindo e compartilhando. É uma experiência muito legal, e espero que você esteja acompanhando e criando seu portfolio. Vamos começar, Paulo?

**Paulo:** Mario, fazendo um spoiler também. Você falou de outros países, outras línguas, quem sabe a gente não traz uma imersão com uns desafios em inglês para quem está treinando ou mesmo para outros públicos? Vamos ver a recepção dessa ideia.

**Mario:** Estou com a nossa janela da aplicação aberta. Basicamente, temos o código que fizemos na aula 02, com toda a parte de estado que nós vimos. Hoje vamos reforçar esse conceito, mas primeiramente começaremos a trabalhar na página do chat, que por enquanto está um pouco incompleta...

**Paulo:** Meio feinha.

**Mario:** É, meio feinha. Voltando ao VSCode, temos a função `ChatPage()` no arquvo `chat.js`, que é a página base. Nada mudou no restante do nosso código. Agora, eu quero carregar a "base" dessa página, que seria o template inicial para começarmos a trabalhar e colocar os nossos códigos. 

Vou copiar a URL da minha famosa "colinha" e abri-la no navegador. Lá, teremos um código que preparamos anteriormente com vários componentes. Ainda incluiremos outras coisas nas próximas aulas, mas essa é a parte inicial que nos ajudará a dar os primeiros passos.


Vou copiar o código disponível nessa página, lembrando que o link ficará disponível na descrição da aula, e colá-lo no arquivo `chat.js`. 

**Paulo:** Muita coisa, Mario. Quero que você me explique o que está aí.

**Mario:** Vamos por partes. Vou salvar e abrir a aplicação o navegador para visualizarmos. Repare que fiz até uma homenagem para uma das nossas instrutoras, a Vanessa, colocando uma mensagem padrão em nosso template. 

Basicamente, temos uma recepção da estrutura da página anterior. Começamos com uma caixa (`Box`) contendo o `backgroundImage` com a imagem do Matrix, com aquela chuva de caracteres; outra caixa com um background mais escuro, que é referente ao fundo do chat; além do texto "Chat" e um botão clicável de "Logout" para o usuário deslogar.

Mais adiante, temos componentes menores para facilitar a visualização. O foco daqui em diante será muito mais a parte central dessa página, onde inserimos e recebemos mensagens, entendendo como pegar essas informações. 

Temos, então, um componente do cabeçalho (`Header`). Se segurarmos o botão "Ctrl" e clicamos sobre ele, conseguiremos navegar dentro desse arquivo, uma dica importante para quem está começando a mexer com o VSCode. 

Encontramos a utilização do `Header` na página e, mais abaixo, a definição do componente `Header()`, que é "pequeno", sendo constituído por uma caixa (`Box`), o texto do "Chat" e o botão com um `variant='tertiary'`, atributo que faz com que o fundo do componente clareie quando passamos o mouse sobre ele. 


**Paulo:** Mario, o componente `Box` é aquele da biblioteca Skynex que estamos importando, certo?

**Mario:** Exatamente. 

**Paulo:** Estamos estilizando esse componente com vários atributos, para ficar bonito. Novamente, se você estiver assustado ou assustada com o CSS, você pode deletar, e terá o mesmo resultado, só que um pouco mais "feio". 

Já o componente `Header` é diferente, não é da Skynex nem de nenhuma outra biblioteca. Nós estamos criando - no caso o Mario -, como fizemos na primeira aula com o `Titulo`. Aqui criamos um componente `Header`, que seria algo como "cabeçalho", está no mesmo arquivo (`chat.js`) e consiste em uma função que retorna um `Box`.

Repare que essa função nem recebe nenhum parâmetro, é uma coisa "fixa" (algo que chamamos também de *hardcoded*), que define como serão todos os *headers*. Quem quiser, eventualmente, pode passar um parâmetro para o `Header` usando *props*, por exemplo. 

**Mario:** Perfeito. E é legal apontar isso, pois às vezes vamos criar componentes não só para reutilizá-los, mas também para deixar mais evidente o que estamos fazendo. Assim, é possível simplificar um longo trecho de código, separando-o de uma maneira mais visível - e essa foi a ideia do nosso componente `Header`.

Junto com ele, temos também a parte da lista de mensagens, localizada em um componente `MessageList`. Parece simples, pois é composto de uma imagem, um texto, a data e a mensagem, mas analisando com mais atenção percebemos que tem bastante código de estilo, a ativação do scroll, cor de fundo e diversas tags. 

Como usaremos esse código para mostrar várias mensagens, especificamente dessa parte da aplicação, acabamos deixando o componente no mesmo arquivo, removendo-o do conjunto total. Ao invés de termos cerca de 15 linhas a mais no meio do código da página, colocamos um atalho `<MessageList/>` que aponta para nosso componente. 

Isso é bom pois também nos ajuda a navegar pelo código. Quando você abre o arquivo, consegue identificar cada parte da estrutura, e a "carga" cognitiva para analisar o que está acontecendo fica menor, facilitando o trabalho. Valeu essa tour pelo *template*, Paulo?

**Paulo:** Perfeito. Você chamou de *template*, mas está se referindo ao código do `chat.js`.

**Mario:** Exato. 

**Paulo:** Se você reparar, nós temos somente alguns `Box`, um `Header` e um `MessageList`, que é o novo componente que criamos. Você pode verificar o código-fonte desse componente, que por sua vez são `Box` com textos. 

Já os outros `Box` são componentes muito comuns, e é rotineiro, com o React, usarmos componentes de tercerios, como calendários, botões, designs e assim por diante. Ao final da aula, podemos dar sugestões de desafios para que as pessoas coloquem mais componentes interessantes nessa página. 

A única coisa que aumentou a extensão do nosso código é o CSS, o estilo. Você pode inclusive comentar para ver o que acontece. Por exemplo, comentando o trecho de código da `Box` referente à mensagem do chat, ela vai perceber a sua posição e algumas outras estilizações.

A Vanessa Tonini, instrutora da Alura que já partipou de várias imersões, ficou doente durante esse período e infelizmente não conseguiu participar desta.

**Mario:** Mas deixamos uma homanegem a ela, eternizada na imersão. 

Nós fizemos essa parte base do nosso chat. Eu chamo de "template" porque é assim que nomeamos na descrição da aula e no e-mail que é enviado aos alunos e alunas. Agora, Paulo, vamos pensar no que é necessário para que esse chat funcione. 

Baseado nos chats que você já usou na vida, o que deveríamos ter de funcionalidades? O que o usuário fará nessa página para mandar as mensagens dele?

**Paulo:** Digitar e apertar o "enter"?

**Mario:** Boa. O usuário digita no campo `textarea`, aperta "enter" para enviar - até porque não temos um botão de enviar. E quando ele envia essa mensagem, ela deve aparecer na listagem junto à mensagem da Vanessa, certo?

**Paulo:** Isso, deve adicionar o texto em um array, ou em uma lista, não sei. 

**Mario:** Vou anotar tudo isso como comentário em nosso arquivo `ChatPage()`. Eu gosto bastante de fazer isso, inclusive fazia bastante no presencial, que é deixar evidente o que o usuário vai fazer e o que nós, como desenvolvedores, precisamos para implementar isso.

Por exemplo, para o usuário digitar no campo de `textarea` nós precisamos criar o campo, que inclusive já está criado. Para que ele pressione o "enter" e envie a mensagem, o que precisamos fazer? Queremos salvar a mensagem e que o React perceba que ela está sendo enviada.

**Paulo:** Usaremos o `onChange`?

**Mario:** Boa.

**Paulo:** A gente provavelmente vai chamando o `setState()` para trocar a variável que é o valor da mensagem. Também precisa ter um `if` lá dentro para verificar se o caractere digirado é um "enter", que aí faremos algo diferente, vamos limpar a variável e jogar o valor antigo para uma lista. 

Acredito que essa lista de mensagens também vai ser um state, e quando ele atualizar nós atualizaremos também a lista de mensagens colocadas. Então acho que tanto a lista quanto o campo de mensagens são states.

**Mario:** Perfeito, Paulo. Você mandou lindamente a resposta. Acho importante esse ponto, e todo mundo que está na imersão tem que conseguir ter esse raciocínio de como o usuário vai se comportar e o é necessário fazer com o código para permitir esse comportamento.

E você percebe que as nossas listas estão mais ou menos "um para um":

```
// Usuário
- usuário digita no campo textarea
- aperta enter para enviar
- tem que adicionar o texto na listagem

// Dev
- [] campo criado
- [] vamos usar o onchange, usa o useState (ter if para caso seja enter pra limpar a variavel)
- [] Lista de mensagens
```

Para que o usuário aperte "enter" e envie a mensagem, você tem que ter o raciocínio de que será necessário usar o `onChange` e o `useState`. 

Eu falo muito isso, porque quando comecei a programar eu tive um trauma. Eu queria fazer um botão de *"like"*, e eu procurava no Google "como fazer um botão de *like*". É muito claro para mim que com o tempo nós mudamos a forma como pesquisamos as coisas, e conseguimos abstrar, por exemplo, que fazer um botão de *like* é adicionar um evento de clique em um botão e manipular o HTML para alterar um valor.

No React, é fazer o `onClick` no botão e fazer o `useState`. É interessante ir praticando isso, porque vai te ajudar a participar até de tarefas mais complexas. Empresas maiores têm processos de whiteboarding, por exemplo, onde, sem escrever código os devs vão discutir e tentar desenhar como será determinada funcionalidade. Isso vai trazendo mais confiança para você participar dessas discussões e ir melhorando na carreira.

Como primeiro passo, podemos começar pelo `onChange` e `useState`, que são conteúdos que abordamos na última aula e estão mais frescos na memória. 

Temos o campo de texto do chat onde conseguimos digitar livremente. Vamos procurar no código esse `textarea` e começar a trazer as funcionalidades para ele. 

Nós temos um campo de texto `<TextField>` do tipo `textarea`. Existem outros tipos, como `password`, `number`, `phone`, `email` e assim por diante - basicamente os mesmos tipos suportados pelo HTML. Temos também o CSS estilizando esse conteúdo.

```
<TextField
	placeholder="Insira sua mensagem aqui..."
	type="textarea"
	stylesheet={{
		width: '100%',
		border: '0',
		resize:'none',
		borderRadius: '5px',
		padding: '6px 8px',
		backgroundColor: appConfig.theme.colors.neutrals[800],
		marginRight: '12px',
		color: appConfig.theme.colors.neutrals[200],
	}}
/>
```

Vamos começar a trabalhar a lógica do `onChange`. Primeiro, teremos um valor `value` que será sincronizado no React, e que será  a nossa `mensagem`. 

```
<TextField
	value=(mensagem)
	placeholder="Insira sua mensagem aqui..."
	type="textarea"
	stylesheet={{
		width: '100%',
		border: '0',
		resize:'none',
		borderRadius: '5px',
		padding: '6px 8px',
		backgroundColor: appConfig.theme.colors.neutrals[800],
		marginRight: '12px',
		color: appConfig.theme.colors.neutrals[200],
	}}
/>
```

Vou copiar essa `mensagem` e criar uma variável no início da nossa `ChatPage()`, lembrando de usar a sintaxe do `useState`: entre colchetes passaremos, primeiramente, o valor que usaremos para mostrar aquele conteúdo - no caso, `mensagem` -, e em seguida o método do tipo *setter* que será chamado para alterar esse valor, que chamaremos de `setMensagem`. 

Essas variáveis receberão a chamada de `React.useState('')`, passando como parâmetro uma string vazia que servirá de valor inicial para esse campo. 

```
export default function ChatPage() {
	const [mensagem, setMensagem] = React.useState('');

//...
```

Ao carregarmos a página, recebemos um erro que não está relacionado à funcionalidade que estamos implementando. Pode acontecer na sua aplicação, pois é algo referente ao próprio Next, e existe até uma *issue* aberta sobre o problema. Isso é bastante comum em projetos *open-source*, com a comunidade colaborando para reportar e solucionar problemas. 

Acontece que, no momento em que ele gera as classes automaticamente usando uma lib interna, às vezes o Next "se perde". Para que o erro deixe de aparecer, basta encerrar a aplicação e reiniciá-la no terminal. 

Agora, sempre que digitarmos algo, ativando o `onChange`, queremos atualizar o valor de `mensagem` seguindo os passos que descrevemos anteriormente. Vamos adicionar esse `onChange` ao nosso `TextField`, lembrando que ele sempre recebe uma função (`function`).

Na verdade, é mais comum trabalharmos com um tipo de sintaxe conhecida como *arrow function*:

```
() => {}
```

Essa é uma sintaxe mais "simplificada", que pode parecer estranha à primeira vista, mas aparece bastante no dia-a-dia. 

```
<TextField
	value=(mensagem)
	onChange=(() => {
		setMensagem();
	})
	placeholder="Insira sua mensagem aqui..."
	type="textarea"
	stylesheet={{
		width: '100%',
		border: '0',
		resize:'none',
		borderRadius: '5px',
		padding: '6px 8px',
		backgroundColor: appConfig.theme.colors.neutrals[800],
		marginRight: '12px',
		color: appConfig.theme.colors.neutrals[200],
	}}
/>
```

Agora eu quero dar outra dica, Paulo. Muitas vezes a pessoa não lembra como fez determinada funcionalidade. Só que se você já fez seu código, pode voltar nele para lembrar como trabalhar nesse caso. Se voltarmos nas nossas páginas até a *home* e procurarmos por "onChange", veremos que fizemos esse código e sabemos o valor, que está em `const valor = event.target.value;`.
 
Então esses comentários que fomos deixando, ajudam vocês, que estão assistindo e praticando agora, a conseguirem se achar no próprio código, em um primeiro momento, e com o passar do tempo você vai ganhando mais autonomia para procurar na documentação. Então se você já fez, tenta olhar novamente o código para recuperar a memória do dia que você fez.
 
Ao invés de copiar essa variável, analisaremos a ideia. Temos `const valor = event.target. value` e levaremos esse conceito para o código que estamos escrevendo.
 
```
onChange(event) => {
           	const valor = event.target.value;
```
 
Isso é uma ideia super válida, certo, Paulo? Você que já deu muitas aulas. Tentar evitar, no começo, copiar os códigos. Quando estivermos codando a funcionalidade, tentarmos sempre escrever enquanto criamos a lógica.
 
**Paulo:** Isso, Mauro.
 
**Mario:** Agora que temos esse valor, definimos ele com `setMensagem(valor);` e teremos definido o `value`, `onChange` e o `valor`. Salvamos.
 
**Paulo:** Podemos ver esse código de várias outras formas, certo, Mario?
 
**Mario:** Sim!
 
**Paulo:** Porque naquele trecho não precisávamos ter quebrado em duas variáveis, ao invés da *arrow function*, era possível escrever uma *function* mesmo. Tem várias formas de escrever esse trecho de código, certo?
 
**Mario:** Certíssimo, Paulo. Não existe uma forma de outro mágica que podemos fazer para tudo dar certo. Na verdade, dará tudo certo de várias formas, mas não tem um jeito melhor ou pior. Há diferentes formas.
 
Se escrevermos apenas código, não muda muita coisa. Escrevemos e a informação apenas aparece. Então podemos copiar o valor e colocá-lo em um pedaço do código. Em cima da lista de mensagens, codamos `(mensagem)`, que é o valor do `TextField`, e conferir se o valor muda. Portanto, escreveremos `Tá mudando o valor: (mensagem)`. Colocamos essa linha no meio do código, recarregamos a página e, enquanto digitamos, podemos reparar que o valor está mudando.
 
Essa é outra dica importante. Esse começo de aula está cheio de dicas. No React, o que acontece com frequência é a dúvida do que você poderá trabalhar: tenho uma *string* ou um número? Isso acontece até no Javascript, por não ter um intérprete *pine*, *flort* e outros, às vezes ficamos perdidos, sem saber o que usar.
 
Então tenta sempre colocar o valor na tela ou usar um `console.log` para ter clareza do que está trabalhando e, com isso, escrevemos um código melhor, evoluir a aplicação e tudo mais.
 
Observamos que o código está funcionando e mudando o valor. Apagaremos esse trecho do local onde colocamos e, no começo do código, Paulo, veremos que o próximo passo é usar o `onChange` e o `useState` para usar as ações. E você colocou um `if` para quando apertarmos “Enter”, limparmos a variável. Isso é no caso de realizarmos o *submit*, ou seja, quando apertarmos a tecla "Enter" conseguirmos enviar.
 
**Paulo:** Isso! Boa! Deixa de desafio ter também um botão ao invés de só o "Enter". É possível ter várias ideias.
 
**Mario:** Perfeito. Gosto bastante da sua ideia, mas acho que pode ser legal vermos como fazer para ter esse `if`. Porque caso aperte "Enter", temos que descobrir qual tecla a pessoa está apertando. Faz sentido? Temos que descobrir isso de alguma forma.
 
Ao conferirmos nosso código, o `(event)`, que tem as informações do evento `event: React.Change.event<HTMLInputElement>` , podemos codar `console.log` nele e descobrir se ele diz a tecla que está sendo apertada, porque saber qual a tecla é importante. Porque estamos digitando qualquer letra, mas às vezes a pessoa aperta o "Enter". E como sabemos que a pessoa apertou o "Enter"? Então temos que saber isso pelo `(event)` para debugarmos juntos.
 
Ao digitarmos quaisquer letras, notamos que o console apresenta o *synthetic event* e no *target* temos o valor, o tipo do evento, mas não traz informação de qual tecla apertamos. Se carregarmos a página, escrevermos qualquer coisa na caixa de texto e apertarmos "Enter", percebemos que para o evento do `onChange`, Paulo, o código não se importa muito com qual tecla foi apertada. Ele está mais preocupado com o valor que mudou do que com a tecla que apertamos.
 
Se quisermos um controle mais fino da tecla que apertamos, temos que verificar outro evento do campo de texto, ou seja, o *input*. Faremos isso com o comando `onKeyPress=()`, que é até sugerido.
 
Passamos a mesma lógica com *arrow function*.
 
**Paulo:** Pode receber o evento e codar um `console.log` para vermos o que acontece.
 
**Mario:** Exato. Vou codar o evento.
 
```
onKeyPress=((event) => {
       console.log(event);
})
```
 
Agora carregamos a página e, no console, temos o evento sintético *onKeyPress* com mais informações. Dessa vez ele mostra o código da tecla em `code: "KeyA"` e em `key: "a"` também.
 
Ele verifica se o "Alt" ou o "Ctrl" está apertado, então o `onKeyPress` é utilizado para criar atalhos de ferramentas como o Slack ou Facebook, onde apertamos "comand + K" ou "Ctrl + K" e alguma função acontece. Então essa curiosidade é legal de mostrar.
 
Temos, portanto, o *key* "a". Se apertamos "Enter", outro evento sintético aparece informando `code: "Enter"` e `key: "Enter"`. Então fica a dica para utilizar esses valores para se basear.
 
Se apertarmos agora a tecla "1", teremos um *synthetic code* informando o `code: "Digit1` e a `key: "1"`. Então notamos que várias informações aparecem para nos ajudar e funções também.
 
Vamos voltar para o nosso código e começar a fazer o `if`, mostrando o `console.log` apenas se apertarmos "Enter", para conseguirmos limpar a variável, como o Paulo falou.
 
No evento sintético temos tanto o *key* quanto o *code*, mas o *key* é mais utilizado. Então podemos escrever o `if(event.key)` . Nas sugestões aparecerá o `keyCode`, que antes era muito usado, mas hoje é depreciado. Isso é legal do VS Code, Paulo. Ele está integrado com a documentação da web, chamada documentação de bolso pelo pessoal, que é a **"MDN"**.
 
Então todas as descrições da MDN sobre tecnologia, especificações do CSS e tudo mais, por mais que usemos React, o VS Code está integrado ao ponto de indicar as propriedades desatualizadas e quais devemos dar preferência. É bem legal usar as ferramentas atualizadas e ter esse controle.
 
Voltando para o código, sabemos que o *key* receberá o valor "Enter" e, se esse evento ocorrer, ele deve aparecer no console, do contrário, não aparece. Portanto, nosso *if* será
 
```
if(event.key === 'Enter'){
      console.log(event);
}
```
Ao atualizarmos a página, enquanto estamos digitando o console não exibe nada. Ao apertarmos a tecla "Enter", aparece um evento sintético, e isso se repete todas as vezes que apertamos essa tecla. Então, aparentemente, nosso comando deu certo, mas faltou limparmos a variável.
 
```
if(event.key === 'Enter'){
                          	console.log(event);
                          	setMensagem(' ');
}
```
 
Recarregamos a página, apertamos "Enter" e o valor sumiu.
 
**Paulo:** Perdemos a variável. É só para brincar. Porque quando você apertou "Enter", a variável sumiu e ninguém guardou esse valor.
 
**Mario:** Exatamente. Digitamos ele e quando apertamos "Enter" ele some e ainda pula uma linha. Então agora, para codarmos do jeito certo, quando digitarmos a mensagem e apertarmos "Enter", essa mensagem precisa ser enviada para algum lugar, que é o terceiro tópico das nossas tarefas, para criarmos uma lista de mensagens. Então precisamos controlar as mensagens que temos de alguma forma.
 
Com o que já temos, Paulo, como você criaria essa lista?
 
**Paulo:** Eu criaria uma `const` com "listaDeMensagens" e "setMensagens". O *state* padrão dessa variável seria `[]`, porque é uma *array* vazia, sem nenhuma mensagem. portanto, `const(listaDeMensagens, setListaDeMensagens) = React.useState([]);` .
 
**Mario:** Perfeito, Paulo. É isso mesmo.
 
Agora cumpriremos as duas últimas tarefas em conjunto. A segunda está mais ou menos feita, então podemos preencher os colchetes com **`+/-`** e a terceira será o nosso foco.
 
Ao invés de já integrarmos com o *message list* e fazermos vária funções, primeiro faremos aparecer só a "listaDeMensagens" na tela. Então colocaremos `(listaDeMensagens)` embaixo do `<MessageList />`, salvar e obsrvarmos o que aparece no React.
 
Na página não apareceu nada. Podemos até colocar um valor antes.
 
```
<MessageList />
Lista de mensagens: (listaDeMensagens);
```
 
Ao recarregarmos a página, ainda não temos nenhum retorno. Tentaremos então colocar algum valor nessa lista, para quando apertarmos "Enter", ao invés de apenas apagar, o valor ser armazenado em algum lugar.
 
Paulo, em qual parte do código você alteraria para adicionar esse valor a lista?
 
**Paulo:** Acho que será o `onKeyPress`, porque quando aperta o "Enter", antes de remover e fazer o `setMensagem('');`, guardaremos a mensagem na array "listaDeMensagem", colocando esse comando depois do `console.log(event);`. Contudo, tem o seguinte perigo: não farei isso, mas tenho vontade de fazer da seguinte forma.
 
```
if(event.key === 'Enter'){
                          	console.log(event);
                          	listaDeMensagens.push(mensagem);
                          	setMensagem(' ');
}
```
 
Eu não tenho certeza se isso funciona ou não, porque `listaDeMensagens` é a variável que lemos, que teoricamente o React não saberá que alteramos ela, ou saberá, já que é um método dela? Ele me devolveu uma array mágica que, quando escrevo alguma alteração, o React sabe, ou precisa usar `setListaDeMensagens(ListaDeMensagens)`?
 
**Mario:** Vamos testar, Paulo. Digitaremos na nossa página uma mensagem qualquer e apertaremos "Enter". Repara que não aconteceu nada.
 
É justamente o que você disse. Essa lista é apenas para vermos, então, se quisermos adicionar algo, teremos que usar o `setListadeMensagens()`. E isso é algo que confunde um pouco no começo, porque como estaremos setando, teremos que passar todos os valores que tínhamos. Portanto, passaremos o *array* quanto qualquer coisa que tinha na lista e adicionar a nova mensagem que queremos trabalhar.
 
```
if(event.key === 'Enter'){
                          	console.log(event);
                          	setListaDeMensagens([
                                        	   listaDeMensagens,
                                        	mensagem
                          	]);
                          	setMensagem(' ');
}
```
 
**Paulo:** Nessa parte não precisamos usar aquela sintaxe para abrir a *array* listaDeMensagem?
 
**Mario:** Tem! Essa sintaxe é para resgatarmos todos os itens que já estão na lista e os colocarmos na lista nova.
 
**Paulo:** Porque se não iríamos criar uma *array* dentro de outra *array*, que não é o que queremos. Queremos que os itens que já existem na lista e a mensagem.
 
**Mario:** Exatamente.
 
Salvamos o código, atualizamos a página, digitamos uma mensagem e apertamos "Enter". Notamos que o valor aparece em cima do campo de input. Digitei uma nova mensagem e pressionei "Enter" e vemos que tudo que digito, Paulo, ele já coloca na nossa "Lista de Mensagens".
 
Se inspecionarmos a página, perceberemos que há vários textinhos separados.
 
Podemos recuperar esses textinhos e tentar exibi-los de forma mais bonita, ao invés de apenas o conteúdo. Porque se colocarmos apenas o *array* na página, observaremos o resultado. E se quiséssemos colocar, por exemplo, em uma TAG "li" antes de preenchermos com mensagem da Vanessa?
 
Você tem uma sugestão o que podemos colocar aqui?
 
**Paulo:** Lembrei. Quando temos uma *array* e queremos mostrar todos os elementos, normalmente pensamos em `forEach` . O problema desse comando é que ele não retorna nada, o `forEach` só executa algo para cada elemento, mas não é isso que queremos. Não queremos um `console.log` ou um `print`. Se for um `console.log`, funciona.
 
```
<MessageList />
Lista de mensagens: (listaDeMensagens.forEach{(mensagemAtual) => {
           	console.log(mensagemAtual)
})}
```
 
**Mario:** Funciona. Sempre que digitarmos algo, como "oi", aparecerá no console. Temos a informação do console que na linha 60 do chat tem o "oi".
 
Continua sua explicação do `forEach` para ajudarmos quem está no curso.
 
**Paulo:** Agora nós não conseguimos devolver, que é nosso objetivo.
 
**Mario:** Exato. A ideia é que, de alguma forma passássemos por cada item e retornássemos uma informação nova no lugar daquele item.
 
Por padrão colocar o *array* na tela mostra o que tem nele, mas se quisermos transformar cada item, o `forEach` não faz isso. Se quisermos uma "li" com a mensagem atual, o `forEach` não faz nada.
 
```
Lista de mensagens: (listaDeMensagens.forEach{(mensagemAtual) => {
           	console.log(mensagemAtual)
           	return (
                          	<li>
                                        	(mensagemAtual)
                          	</li>
})}
```
 
Salvando o código acima e recarregando a página, ao adicionarmos uma mensagem no input, notaremos que nada acontece no console.
 
É possível confirmar isso codando no próprio console, tentando retornar a mensagem.
 
```
['oi'].forEach[(valorAtual) => {
 
           	return 'Mensagem: ' + valorAtual;
})
```
O `forEach` sempre resulta em *"undefined"*, porque o que queremos não é apenas passar por cada um, mas transformar. Queremos mapear o valor de uma lista para outra lista. Então utilizamos `.map`, que já nos mostra, até no console, qual será a saída.
 
```
['oi'].map[(valorAtual) => {
 
           	return 'Mensagem: ' + valorAtual;
})
```
 
**Paulo:** Coloca outra *string* nesse mara para vermos.
 
**Mario:** Vou digitar "oi" e "segunda string".
 
```
['oi', 'segunda string'].map[(valorAtual) => {
 
           	return 'Mensagem: ' + valorAtual;
})
```
 
Olha que genial isso, Paulo. Ajuda muito a aprendermos esse contexto quando estamos começando, porque mostra o output das duas sem nem termos apertado "Enter".
 
Portanto, temos o valor de entrada e mapeamos para uma nova saída padronizada, que será com "li" no nosso caso.
 
Então trocaremos o `forEach` para `map` no nosso código, salvamos e recarregamos a página. Ao digitarmos "oi" e apertarmos "Enter", aparecerá a mensagem no console. Digitaremos "olá", apertaremo "Enter" novamente e inspecionaremos elemento. Observaremos que as duas mensagens aparecem na nossa lista.
 
**Paulo:** Mario, fiquei com uma dúvida. Quando imprimimos uma *array* com `console.log`, ou no `map`, o resultado é separado por vírgula. Porque nesse caso não está aparecendo o `[]` com as mensagens separadas por vírgula?
 
**Mario:** Como assim?
 
**Paulo:** O "oi" e o "olá" que você mostrou no "Mensagem" dentro do chat, por que não está separado por vírgulas?
 
**Mario:** Perfeito, Paulo. No navegador só existe texto, então todos os valores que você coloca, com exceção do valor boleano, o React utiliza um `.toString()` . No caso do *array*, ele usa o `toString` e retira as vírgulas.
 
**Paulo:** É o comportamento dele.
 
**Mario:** É algo do React, que tira as vírgulas, deixando um ao lado do outro.
 
**Paulo:** Entendi, ele trabalha assim. Quando ele recebe um *array* e precisa colocar na tela, o React já faz isso.
 
**Mario:** Exatamente. Para o React, ter uma *array* de texto ou de componentes é a mesma coisa, a diferença é que ele procura o componente para virar TAG e o texto será um elemento de texto no navegador.
 
**Paulo:** Então agora o que está me incomodando é o "Enter" na *text box*, porque você aperta "Enter" e acontece uma pulada de linha horrorosa na caixa de texto. E falta acertar como faz as mensagens.
 
**Mario:** A quebra de linha podemos mudar dentro no nosso evento no `onKeyPress`, informando que sempre que quando pressionarmos "Enter", realizaremos um `event.preventDefault();` , porque o comportamento padrão do "Enter" é fazer quebra de linha.
 
```
onKeyPress={(event) => {
           	if(event.key === 'Enter'){
                          	event.preventDefault();
                          	setListaDeMensagens([
                                        	   listaDeMensagens,
                                        	mensagem
                          	]);
                          	setMensagem(' ');
           	}
}
```
 
**Paulo:** Entendi. Na área de texto do HTML, se aperto "Enter", ele funciona.
 
**Mario:** Exato. Removemos o `console.log` do comando, salvamos o código e recarregamos a página. Agora se digitarmos e apertamos "Enter" não temos a quebra de linha.
 
No console apareceu um erro que já resolveremos. Se você percebeu o erro, pode se tranquilizar porque também vimos.
 
Mas olha, Paulo, não temos mais a quebra de linha na caixa de texto. O legal é que, passo a passo, estamos cumprindo a primeira lista de tarefas que criamos no começo.
 
Já conseguimos executar o `onChange`, usar o `if` e limpar a variável do jeito certo. Nosso funcionamento já está funcionando como queríamos.
 
Em seguida, podemos analisar o `setListaDeMensagens`. Dentro desse comando, o código parece a submissão do nosso formulário. Quando enviarmos a mensagem, esse será o código que irá gerenciar essa parte.
 
**Paulo:** Sim. Esse a e alinha de baixo, que limpa a caixa de texto.

**Mario:** Essas lógicas, são lógicas de estado. Com elas estão acontecendo juntas, podemos separá-las e deixá-las agrupadas. 

```
setListaDeMensagens([
   ...listaDeMensagens,
	 mensagens
]);
 setMensagem('');
 
 ```

Talvez usaremos isso quando tivermos, por exemplo, os *stickers* ou alguma outra interação na página, essa parte da lógica do envio é interessante isolarmos em uma função e deixarmos mais próximo do topo do arquivo. Poderíamos fazer, `handleNovaMensagem();`. Nós chamamos dentro do `onKeyPress`.

```
onKeyPress={(event) => {
    if(event.key === 'Enter') {
		    event.preventDefault();
				handlerNovaMensagem();
		}
	}}

```

E esse `handleNovaMensagem()`, nós criamos mais acima, `function handleNovaMensagem() {`. 

```
function handleNovaMensagem() {
 setListaDeMensagem([
   ...ListaDeMensagens,
	 mensagem
]);
 setMensagem('');
 }
 
 ```
 
 Algo que as pessoas gostam de fazer também, é: como estamos isolando uma função, passar o valor da `mensagem` para o `handleNovaMensagem`. Então, dizemos que vamos receber a nova mensagem, `function handleNovaMensagem(novaMensagem) {`, que nós vamos criar e também a passaremos em `mensagem: novaMensagem,`.

```
function handleNovaMensagem(novaMensagem) {
 setListaDeMensagem([
   ...ListaDeMensagens,
	 mensagem: novaMensagem,
]);
 setMensagem('');
 }
 
 ```

**Paulo:** Até porque, no futuro, talvez recebamos o nome da pessoa do Chat, outros parâmetros e concentramos tudo nesta parte, pois é necessário pegar, limpar, fazer a barra de rolagem, entre outros. 

**Mario:** Nós vamos fazer isso agora, é o próximo passo. Nós temos `handleNovaMensagem()` e o valor da mensagem que receberemos. No `handleNovaMensagem()`, nós passaremos o valor atual da mensagem, que é quando estamos digitando e vamos salvar.

```
onKeyPress={(event) => {
    if(event.key === 'Enter') {
		    event.preventDefault();
				handlerNovaMensagem(mensagem);
		}
	}}

```

Retornando ao navegador, no Chat, temos o campo "Insira sua mensagem aqui...", vamos escrever: "Ola"; "Funciona". Com o Console aberto em paralelo, inspecionando, notaremos que deu certo, funcionou. 

Agora, vamos usar a sua ideia, Paulo, para atacar outro problema, que é: toda vez que renderizamos uma lista de alguma coisa no React, ele tem alguns mecanismos internos e precisa saber como identificar cada um dos itens. Como saber que cada um dos itens é único na página, para facilitar alguns processos de otimização, performance, entre outros. 

Para isso, ele espera que cada item de uma lista tenha uma *prop* chamada de `key`, é a `unique "key" prop`. Se verificarmos nosso `.map`, poderíamos pegar `mensagemAtual` e passar no `key` o próprio valor da *string*, do texto que estamos recebendo na mensagem, passamos no `key` e ao verificar o Console, constataremos que ele para de mostrar o erro. 

```
<MessageList />
{listaDeMensagens.map((mensagemAtual) => {
    return (
		    <li key={mensagemAtual}>
				    {mensagemAtual}
				</li>
	  )
})}

```

Se, na página, rodarmos um "oi" e um "ola", notaremos que ele parou de mostrar o erro. Porém, se digitarmos "oi" de novo, outra mensagem de erro aparece, "warning: Encountered two children with the same key", informando, portanto, que ele "encontrou dois filhos com a mesma chave". Antes de nos preocuparmos em como lidar com isso, podemos pensar na possibilidade de ter um *id*, uma lista de mensagens. 

**Paulo:** Pode ser 1,2,3, isto é, mensagem 1, mensagem 2 e mensagem 3. Vale lembrar também que se trata de um *warning* e não de um erro. 

**Mario:** Exatamente, é um *warning*. Ele começa a ter alguns impactos de performance se a aplicação começa a crescer muito, passa a ter muitas lógicas dentro do componente em que essa lista está, mas é importante tentarmos contornar a situação de alguma forma.

Retornando ao cógido, constataremos que a mensagem atual não pode ser apenas um texto, um valor de *string*. Cada mensagem terá: usuário da pessoa; data de envio, que é o *timestamp*; e a mensagem em si. Vamos tentar formatar para que a nossa mensagem tenha essas informações. Ao definir a nova mensagem, ela terá mais informações para além do texto. 

Vamos adicionar o `const mensagem =`. Sempre que tivermos uma nova mensagem, ele será não só uma *string* ou uma lista de coisas, mas, sim, um item com múltiplas coisas, portanto, ele será um objeto com uma "mensagem", "*message*", ou "texto da mensagem", termo que usaremos: `texto`. O `texto` é a `novaMensagem` que estamos recebendo. 

```
function handleNovaMensagem(novaMensagem) {
   const mensagem = {
	 
	     texto: novaMensagem,
	};
   setListaDeMensagem([
     ...ListaDeMensagens,
	   mensagem: novaMensagem,
  ]);
   setMensagem('');
   }
 
 ```

Nós também teremos a informação sobre quem está enviando a mensagem. Para isso, usaremos o "*from*", "de quem" ou "de". Por exemplo, `de: 'omariosouto',` ou da Vanessa Metonini, `de: 'vanessametonini'`, que é quem está mandando a mensagem agora. 

```
function handleNovaMensagem(novaMensagem) {
   const mensagem = {
	     de: 'vanessametonini',
	     texto: novaMensagem,
	};
   setListaDeMensagem([
     ...ListaDeMensagens,
	   mensagem: novaMensagem,
  ]);
   setMensagem('');
   }
 
 ```

Agora podemos gerar um *id* nosso, informando que teremos um *id* para pegar a lista das mensagens  que está mais acima no código, `listaDeMensagem`, e o site dela, o tamanho dela, `.length`. Pegando o `.length`, resolveríamos o problema. Podemos começar colocando zero itens, um item e continuar somando. Aliás, vamos incluir um `+ 1`, indicando essa soma. 

```
function handleNovaMensagem(novaMensagem) {
   const mensagem = {
	     id: listaDeMensagens.length + 1,
	     de: 'vanessametonini',
	     texto: novaMensagem,
	};
   setListaDeMensagem([
     ...ListaDeMensagens,
	    novaMensagem,
  ]);
   setMensagem('');
   }
 
 ```

**Paulo:** Agora a mensagem não é mais uma *string*, mas, sim, um objeto que tem várias coisas. 

**Mario:** Exato! Tanto que, nós apenas criamos esse trecho de código acima, não estamos usando ainda, mas se voltarmos ao Chat, escrevermos qualquer coisa, carregarmos a página e apertarmos "Enter", perceberemos que ele funciona, com texto. Se colocarmos o objeto `mensagem` no lugar de `novaMensagem` (após `...ListaDeMensagens`), ele "quebra tudo", quer dizer que teremos um erro. 

```
function handleNovaMensagem(novaMensagem) {
   const mensagem = {
	     id: listaDeMensagens.length + 1,
	     de: 'vanessametonini',
	     texto: novaMensagem,
	};
   setListaDeMensagem([
     ...ListaDeMensagens,
		 mensagem,
	  
  ]);
   setMensagem('');
   }
 
 ```

A mensagem de erro informa que objetos não são válidos como *React child*. Ele encontrou um objeto com as chaves "*id*", "de" e "texto". Ou seja, se temos um objeto, não podemos só renderizá-lo, precisamos pegar cada um dos valores e distribuí-los da forma correta. 

**Paulo:** Ou é uma *array* de componente React, ou uma *array* de *strings*. Se não for isso, ele não aceita. Não vai transformar em texto magicamente, nem vai chamar o `toString()`. 

**Mario:** Não vai. Nós podemos pegar a `mensagemAtual` que está no trecho abaixo e se parece com algo que estamos recebendo.

```
<MessageList />
{listaDeMensagens.map((mensagemAtual) => {
    return (
		    <li key={mensagemAtual}>
				    {mensagemAtual}
				</li>
	  )
})}

```

Mas precisamos recordar que temos "*id*" (segundo a mensagem de erro que apareceu anteriormente), portanto, faremos `mensagemAtual.id`. 

**Paulo:** A que está abaixo pode ser o "de", dois pontos e o texto. Concatenando, desta maneira, com o texto. 

```
<MessageList />
{listaDeMensagens.map((mensagemAtual) => {
    return (
		    <li key={mensagemAtual.id}>
				    {mensagemAtual.de}: {mensagemAtual.texto}
				</li>
	  )
})}

```

O `key` é um mecanismo interno. Se não tivéssemos usado o `key`, a única coisa que aconteceria é que o React reclamaria com *warning*. O `de` e o `texto` são elementos que desejamos que apareçam no Chat, sendo que o `de` é a Vanessa Metonini e está *hardcoded*, e o `texto` é o que digitamos e apertamos "Enter". 

**Mario:** Retornando ao Chat, se digitarmos "Ola" e "Sejam bem vindos a aula 3", quando apertarmos "Enter", ele funciona. Já estamos conseguindo fazer o nosso Chat funcionar de forma *offline*. Agora, Paulo, para encerrar a aula, vamos apenas migrar o trecho de código acima para dentro do `MessageList`. 

Mas, antes, eu gostaria de comentar sobre uma questão com a qual muitas pessoas do Front-End sofrem no começo: as pessoas acham que é necessário ter o Back-End pronto para, então, escrever a funcionalidade. Na verdade, sabendo quais dados você terá e qual o design da tela, é possível criar tudo de forma estática, direto no código, e, fazendo isso, podemos só pegar depois e plugar a `// Chamada de um backend` para cadastrarmos algo, por exemplo. 

Assim alcançamos uma flexibilidade maior para cadastrar e plugar. Na próxima aula, teremos mais clareza sobre este ponto que estou trazendo agora, mas é importante tentar praticar e entender o  que usuário faz, no nosso caso, digita no campo, aperta para enviar, etc., e converter isso para a lógica necessária para integrar a tarefa que estamos lidando. 

```
/*
// Usuário
- Usuário digita no campo textarea
- Aperta enter para enviar
- Tem que adicionar o texto na listagem 

// Dev 
- [x] Campo Criado
- [x] Vamos usar onChange usa o useState (ter if para caso seja enter para limpar a variavel)
- [x] Lista de mensagens

*/

```

Algum ponto a adicionar, Paulo?

**Paulo:** Não. Perfeito!

**Mario:** Agora vamos comentar o `ListaDeMensagens`. 

```
<MessageList />
{/* {listaDeMensagens.map((mensagemAtual) => {
    return (
		    <li key={mensagemAtual.id}>
				    {mensagemAtual.de}: {mensagemAtual.texto}
				</li>
	  )
})}

```

E fazer com que ele funcione em cima do nosso `MessageList`, do componente.  Esse `MessageList()` é uma função. Tem como ele saber que a nossa lista de mensagens existe? 

```
function MessageList() {
   return (
	    <Box 
			   tag="url"
				 styleSheet={{
				     overflow: 'scroll',
						 display: 'flex', 
						 flexDirection: 'column-reverse',
						 flex: 1,
						 color> appConfig.theme.colors.neutrals["000"],
						 marginBottom: '16px',
					}}
       >
```

**Paulo:** Precisamos lembrar onde está declarada? Não, porque o `listaDeMensagens` está declarado dentro da `function` do `ChatPage`. 

```
export default function ChatPage() { 
    const [mensagem, setMensagem] = React.useState('');
		const [listaDeMensagens, setListaDeMensagens] = React.useState([]);

```

**Mario:** Essa é a "cereja do bolo", o toque final, da nossa aula. Se formos ao `MessageList`, apertarmos "Ctrl + Enter" e tentarmos dar um `console.log(listaDeMensagens);`, receberemos uma mensagem no Console dizendo que não existe, que não está definido, porque cada função é isolada, só tem os valores que estão dentro dela. 

**Paulo:** Então, temos que passar como argumento? 

**Mario:** Sim, perfeito! Teremos um `props`, isto é, `function MessageList(props) {` e um `props.listaDeMensagem`, ou seja, `console.log(props.listaDeMensagens);`. Teremos que ir em quem chama o `MessageList` e passar o valor `listaDeMensagens={listaDeMensagens}`. 

```
<MessageList listaDeMensagens={listaDeMensagens} />

```

Mas, vou até fazer diferente e dizer que no `MessageList` o nome é `mensagens`. 

```
<MessageList mensagens={listaDeMensagens} />

```

Fiz isso para desassociarmos o nome da variável do que o componente está recebendo. Isso é importante! Por mais que no Chat a `listDeMensagens` seja o nome da nossa variável, no `MessageList`, podemos receber qualquer nome. Não existe a obrigação de ser o mesmo nome. Tanto que se verificarmos o `MessageList` no Console, aparece `undefined` para `props.listaDeMensagens`. Porém, se verificarmos apenas o `props`, isto é, `console.log(props);`, no Console aparecerá "mensagens com array vazio", `{mensagens: Array(0)}`.

Se eu digitar algo no Chat, por exemplo, "oi", teremos no Console "mensagens com array com um item", `{mensagens: Array(1)}`. E assim por diante. 

**Paulo:** Tenho uma pergunta. Por que se chama "mensagens" e não "lista de mensagens"?

**Mario:** Justamente porque na hora de passar o atributo, fizemos o nome à esquerda e o valor à direita. Temos que considerar sempre essa ideia de chave e valor. Aplicamos aqui a mesma lógica do objeto. 

```
<MessageList mensagens={listaDeMensagens} />

```

**Paulo:** Agora pegamos o trecho de código comentado e, de alguma forma, colocamos dentro. 

**Mario:** Exatamente! Temos que pegar a lista, fazer o `.map` e preencher os itens. Basicamente, vamos até a `"ul"`, e, em volta da `li`, faremos `{props.mensagens.map() =>`, passamos uma função e o `return` dela e pegamos todo o nosso código do `li`. 

```
{props.mensagens.map(() => {
    return (
		
		)
})}

```

O código do `li` é um pouco maior, então, é importante copiá-lo com cautela até chegar ao próximo `</Text>`, onde temos a `Mensagem`. Após selecionar, vamos apertar "Ctrl + X" nesse bloco de código e o colaremos dentro do `return` do `.map`. Podemos identar o código de novo usando o "Format Document", "Ctrl + Shift + P". Salvamos a página. 

Retornando ao Chat e ao Console, perceberemos que a mensagem da Vanessa não aparece mais, porque o nosso *array* começa vazio. Se digitarmos "Ola", ele mostra no Console que existe um, isto é `{mensagens: Array(1)}`, mas também mostra o erro do `key` mais uma vez. Mas, nós temos nas mensagens o *id*, de quem veio essa mensagem e o texto. 

```
de: "vanessametonini"
id: 1
texto: "Ola"
[[Prototype]]: Object 
length: 1
[[Prototype]]: Array(0)
[[Prototype]]: Object 

```

Podemos ir ao `{props.mensagens.map(() => {` e, das mensagens, pegar a mensagem atual, `{props.mensagens.map((mensagem) => {`, e incluir `key={mensagem.id}`. 

```
{props.mensagens.map((mensagem) => {
    return (
		   <Text
			     key={mensagem.id}
					 tag="li"
					 styleSheet={{
					    borderRadius: '5px',
							padding: '6px',
							marginBottom: '12px',
							hover: {
							    backgroundColor: appConfig.tehem.colors.neutrals[700],
							}
					}}
      >
```

Agora, se digitamos no Chat, constataremos que o erro parou. Para cada vez que digitamos, ele roda de novo o código inteiro. O motivo é que o React está sempre executando as funções para dizer que a página vai atualizar. Mais abaixo no código, vamos trocar o nome da Vanessa, `{vanessametonini}` por `{mensagem.de}`. Em seguida, o valor de `Mensagem` será `{mensagem.texto}`. 

Verificando outra vez o Chat, ele está sempre jogando para cima as mensagens. 

```
?

Tudo bem

Ola

```

Podemos inverter a ordem. No trecho abaixo, é possível notar que estamos colocando `...listaDeMensagens,`.

```
setListaDeMensagens([
   ...listaDeMensagens,
	 mensagens
]);
 setMensagem('');
 
 ```
 
 **Paulo:** Tem que ser "mensagem vírgula lista de mensagens". 
 
 **Mario:** Exatamente! Esse é um CSS que fizemos para o *scroll*, que inverte a ordem estão aparecendo. 

 ```
setListaDeMensagens([
   mensagem,
   ...listaDeMensagens,
	
]);
 setMensagem('');
 
 ```
 
 **Paulo:** Mario, você poderia voltar lá? Foi muito rápido. Você só trocou a ordem? 
 
 **Mario:** Isso, desci o `...listaDeMensagens,` e deixei o `mensagem` antes. Desta maneira, as mensagens no Chat aparecem na ordem correta. 
 
 ```
 Oi
 
 Olá
 
 Agora foi!
 
 ```
 
 A causa da diferença na ordem que os elementos é o CSS que colocamos para fazer o *scroll* sempre começar de baixo, portanto, sempre estamos lendo a lista de maneira invertida. Mas, enfim, se trata de uma questão de CSS. O importante é termos a noção de que podemos colocar um item como primeiro da lista ou como último, de acordo com a ordem que fazemos o `set` da lista de mensagens. 
 
 Passamos com muito carinho por cada um dos pontos, como o `.map`. Os comentários menores permanecerão para nos acostumarmos com o código. Temos o nosso `TextField` mais abaixo e toda a lógica de percorrer pelos itens. Esse conteúdo e o da aula anterior é o que sempre faremos no React: pegar uma lista e renderizar na tela; fazer algum evento para customizar; cair em um estado para mudar alguma coisa. 

Então, esse é o dia a dia, o "feijão com arroz", com o qual vocês trabalharão. Acho que para essa aula é só. Estudamos muitos conteúdos e agora vocês podem evoluir seus projetos. 

**Paulo:** Meu desafio é colocar um botão de "Ok" do lado do "text" no Chat e, ao apertá-lo, aconteça o mesmo efeito do `onKeyPress` quando apertamos "Enter". Ter duas opções de fazer a mesma coisa, para que seja possível, inclusive, que os dois chamem a mesma função para adicionar mensagens. Esse é um desafio legal, nada difícil e é, como o Mario falou, grande parte do trabalho cotidiano com o React e Next.js. 

**Mario:** O meu desafio é colocar um botão de apagar, "x", para conseguirmos apagar a mensagem. Esse é um desafio um pouco mais complicado. Nenhum dos desafios são obrigatórios, são apenas exercícios, maneiras de você se desafiar, mas achei que esse seria interessante, pois já temos os dados. A minha dica é que você use o método `filter()` do JavaScript para fazer essa deleção. 

Ao invés de usar o `.map` para percorrer tudo, podemos usar o `filter()` para filtrar a lista de um jeito que ela tira o item que bate com alguma regra que você precisará descobrir qual é. 

**Paulo:** Mario, acho que é muito legal, porque reforça todo o nosso aprendizado do *state*. Estudamos agora, inclusive, com *array* e notamos a existência dos mesmos problemas. Não podemos ficar fazendo "push" na *array*. 

Precisamos trocar a *array* e avisar o React: sabe a *array* que eu mandava para você verificar o estado? Mudou. Agora não é mais aquela *array*, é essa. Normalmente elas são parecidas e têm um elemento a mais ou a menos. 

Geralmente é isso que acontecerá, mas pode aparecer uma completamente diferente. Ter "batido" em um banco de dados do Back-End e "puxado" outra coisa completamente diferente. Por exemplo, trocar a lista dos jogadores atuais do jogo que estão online. 

**Mario:** Exatamente! Eu pretendia trazer um exemplo desses, como site de lista de filmes. 

**Paulo:** É importante ter bastante atenção nisso que é o mecanismo. Repare que não ficamos mexendo no CSS do *Box*, pois o que importa estudar e reforçar é o funcionamento do React, *uses*, etc. Nós não nos concentramos no Back-End ou esperamos que ele devolvesse, porque é possível fazer o funcionamento na hora em que o Back-End ficar pronto. 

Na maioria dos casos, funciona desenvolver o Front-End inteiro ou quase inteiro sem o Back-End. Basta deixar *arrays* preparados que, em breve, serão "puxadas" de um HTTP, pegamos o JSON e devolvemos a *array*. Nem ficaremos sabendo se o Back-End é em Java, pouco importa. 

**Mario:** Perfeito, Paulo! Espero que tenhamos conseguido passar essa ideia para você que está assistindo e, junto a isso, gostaria de dizer que é importante entender as estruturas básicas do JavaScript, ter clareza de: quando temos uma *string*, um objeto; qual é a chave e qual é o valor do objeto; que objeto pode ter outro objeto, uma *string* ou um booleano; o que é um *array*. 

Enfim, ter clareza desses valores primários é a base. Nas primeiras aulas de JavaScript estudamos esses valores e conhecê-los bem fará total diferença no trabalho com o React, porque é possível "debugar", usar o `console.log()`, "printar" na tela. 

Recomendo que você use esses recursos visuais a seu favor, porque isso é o mais legal do Front-End, poder ver o que você está fazendo e ter esse *feedback* rápido, diferente do Back-End, em que seria necessário fazer um ambiente de testes ou algo mais complexo a depender do caso. 

**Paulo:** Te convido a marcar a Imersão React no seu projeto para aparecer na vitrine que linkamos nos e-mails, enfim, para que você apareça na galeria de projetos incríveis. 

Também te convido a conversar conosco no LinkedIn, no Instagram e mostrar para a comunidade do Brasil de React e Next.js o que você está fazendo e o que nós, enquanto Alura, estamos fazendo, porque certamente isso ajudará outras pessoas a se animarem com a carreira, com o Front-End e com o projeto. Isso é fundamental!

**Mario:** Então, não deixe de nos marcar! Até mais!


