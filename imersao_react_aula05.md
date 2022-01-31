**Mario:** Olá, pessoas! Boas-vindas à última aula da Imersão React. Acho que essa imersão foi a mais legal em nível de projeto e do que veremos de resultado hoje. Teremos resultados finais incríveis para mostrar para nossa família e amigos.

Antes de finalizarmos essa nossa réplica de aplicativo mensageiro, como WhatsApp, Discord etc. O Paulo tem recados incríveis.

**Paulo:** Esse é um dos recados mais importantes. Essas aulas da Imersão React ficarão disponíveis até segunda-feira (31/01), o dia em que teremos a nossa <a href="https://youtu.be/eiORX8iLEj4" target="_blank">Live de encerramento</a>. Ative o lembrete. Inclusive, na página da Imersão tem os links de todas as lives.

A live de encerramento vai mostrar próximos passos na carreira de React, Next, front-end, mostraremos os projetos mais incríveis que tivemos nessa Imersão e explicaremos mais sobre a formação de Next JS que o Mario Souto e o time da escola de front-end estão desenvolvendo e que será lançada na segunda-feira.

Inclusive, na segunda-feira (31/01) vamos oferecer um desconto para quem quiser se matricular naquela semana. Então, espere até segunda-feira para se matricular na Alura que teremos uma condição legal.

E assim como o pessoal da Vercel já conhece a Alura, o pessoal do Supabase está conhecendo a Alura, conhecendo o poder da comunidade dev brasileira. É claro que alguns de vocês vão virar clientes da Supabase na sua empresa, então esse barulho é interessante para a Supabase.

Fica aqui o meu agradecimento a todo mundo que participou, da edição, do Discord, o Scuba Teen da Escola de Front-End, agradecer também a Vanessa que não pôde participar dessa Imersão.

E teremos mais Imersões, a Alura está criando muita coisa. É um momento incrível para você que é front-end e quer expandir sua carreira. 

Agora, vamos mostrar a tela do nosso projeto.

Hoje colocaremos os stickers. Algumas pessoas já fizeram algumas soluções, mas hoje traremos uma solução completa, já trazendo um pouco de JavaScript preparado.

Tem gente que já adora os stickers da Alura. Vamos compartilhar com vocês esse <a href="https://www.alura.com.br/artigos/stickers-dev-aluraverso-whatsapp-telegram" target="_blank">link com stickers do Aluraverso</a>, esse foi o primeiro pack que criamos, no final do ano passado, tem um monte de sticker do Aluraverso. Pode baixar para o seu Telegram, para o seu WhatsApp.

Hoje veremos como colocar esses stickers no nosso projeto e, além disso, faremos o *real time*. Lembra como está o nosso chat? 

Hoje, se escrevemos alguma coisa e outra pessoa escreve no mesmo endereço que está "deployado" na Vercel, a mensagem não vai. Mario, abre outra aba para testarmos e escreve "Oi, Paulo". Vamos ver naquela primeira aba se a mensagem aparece.

**Mario:** Não apareceu, só aparece se carregar.

**Paulo:** O `useEffect` só aconteceu no primeiro carregamento, e só atualiza com as novas mensagens quando alguém recarrega a página.

Será que tem como fazer o back-end nos avisar quando acontecer alguma coisa? Tem como deixar um *trigger*, um gancho não no sentido do Hooker do React, tem como deixarmos isso em *real time* mesmo usando API da web, mas de uma maneira fácil? Para que esse chat ocorra em tempo real de tal maneira que se você compartilhar o seu endereço "deployado" da Vercel vai funcionar?

Veremos tanto sticker quanto chat em tempo real hoje, além de vídeos extras no canal do Mario. Hoje vai ficar incrível, vamos fechar esse projeto com chave de ouro.

**Mario:** E eu quero até dar um spoiler. Na Alura já temos a formação de React JS, tem muita coisa só de React. E essa formação que será lançada com Next, que é quase uma formação de arquitetura de front-end, terá não só os conteúdos de Next, mas também conteúdo de deploy na Vercel, monitoramento, como gerenciar projeto que cresce usando o Turborepo para fazer seu monorepo, essa palavra que está tão na moda e que cada vez mais gente está trabalhando em projetos maiores que precisam não só criar isso mas também entender como trabalhar. Aqui na Alura sempre tivemos essa filosofia de fazer você entender o que está acontecendo, os porquês, que é o que te ajuda a se virar no dia a dia. 

Agora, vamos fazer esse chat funcionar e adicionar os stickers.

A estrutura do nosso chat já está meio pronta. Já conseguimos clicar no "Logout", conseguimos entrar, já estamos fazendo bastante coisa.

Antes dos stickers, podemos fazer um ajuste, que é para só poder publicar mensagem como a pessoa que está logada. Não faremos uma estratégia super avançada de autenticação, porque isso levaria um pouco mais de tempo e de esforço.

No nosso caso, para simplificar, ao invés de ser o usuário da Vanessa, precisamos, de alguma forma, pegar o usuário ativo. Uma forma de fazer isso é passar essa informação via URL. É a forma mais simples, sabemos disso, mas vai ter tanto conteúdo extra para vocês nas formações da plataforma da Alura, um conteúdo dedicado a essa parte da autenticação.

Então, vamos fazer esse "omariosouto" vir para a URL quando entrar na página do chat.

No VS Code, vamos para o código do arquivo `index.js`. Aqui temos a nossa `PaginaInicial`, o `useState`, o `username`. O que precisamos adaptar aqui agora, será no `onSubmit` do formulário, nesse `onSubmit` mandaremos direto para a página do chat.
 
 Para poder ter acesso ao valor com o login do usuário na outra página, podemos só substituir o `('chat')` por ``(`/chat?username=${username}`)``. Então, transformamos em uma *template string*, e concatenamos o valor de `username`.
 
```
 onSubmit={function (infosDoEvento) {
  infosDoEvento.preventDefault();
  console.log('Alguém submeteu o form');
  roteamento.push(`/chat?username=${username}`);
	//window.location.href = '/chat';

}}
//...
```

Quando clicarmos para mudar de página, esse valor `username=${username}` estará na URL. Vou salvar e voltar na home, clicar em entrar, e na página do chat a barra de endereços está assim: `http://localhost:3000/chat?username=omariosouto`.

**Paulo:** Volta no código, para vermos um detalhe nesta linha que você escreveu. Notem que o Mario trocou as aspas simples pela crase. Quem quiser pode usar as aspas simples e concatenar com o sinal de mais: `roteamento.push('/chat?username=' + username);`. Mas hoje em dia, as pessoas estão usando a primeira forma, com a *template string*.

**Mario:** É mais um lance de costume, muita gente usa e vira padrão para outras pessoas da comunidade usarem.

Então, vimos que o nome do usuário já está aparecendo na URL da página do chat e também estamos conseguindo trocar de usuário. Vou logar com o usuário do Paulo, "peas".

Dado que sabemos que é o Paulo que está logado aqui, precisamos, de alguma forma, acessar esse valor. Como estamos trabalhando com Next, o que podemos usar para acessar essas informações de roteamento e aqui no chat ter acesso àquele valor da *query string* no nosso componente React?

Como temos aqui o sistema de gerenciamento do `useRouter`, o roteamento gerencia não só criação das páginas, como também fazer o `push` e dar acesso a tudo que envolve a URL em geral, manipulação de parâmetro...

**Paulo:** Vamos fazer uma query.

**Mario:** Exatamente, será um `.query`.

**Paulo:** Podíamos ter usado também a API pura do JavaScript para perguntar qual a URL que está sendo acessada no navegador, mas não é legal porque deve ter um monte de problemas de atualização e outras coisas.

**Mario:** O do navegador seria `window.location`, mas ele não vai trazer puramente o valor, você precisa pegar um objeto.

O `useRouter` padroniza, então basta chamarmos o `useRouter` lá na outra página, vou copiar a linha `const roteamento = useRouter();` que temos na `PaginaInicial` e colar no código do `chat.js`, na `function ChatPage()`.

```
export default function ChatPage() {
            const roteamento = useRouter();
            const [mensagem,setMensagem] = React.useState('');
            const [listaDeMensagens, setListaDeMensagens] = React.useState([]);

//...
```

Lembrando de importar o `useRouter` no topo do código, `import { useRouter } from 'next/router';`. Agora, vamos colocar abaixo da linha que colamos anteriormente um `const usuarioLogado = roteamento.query.username;`. Com isso já conseguimos acessar o usuário logado.

```
export default function ChatPage() {
            const roteamento = useRouter();
            const usuarioLogado = roteamento.query.username;
           	const [mensagem,setMensagem] = React.useState('');
           	const [listaDeMensagens, setListaDeMensagens] = React.useState([]);

//...
```

Vou fazer dois `console.log()` para mostrar o `usuarioLogado` e o `roteamento.query`.

```
export default function ChatPage() {
            const roteamento = useRouter();
            const usuarioLogado = roteamento.query.username;
							console.log('roteamento.query', roteamento.query);
            console.log('usuarioLogado', usuarioLogado);
           	const [mensagem,setMensagem] = React.useState('');
           	const [listaDeMensagens, setListaDeMensagens] = React.useState([]);

//...
```
	
Carreguei a página no navegador. A princípio, o `roteamento.query` veio como vazio, provavelmente na primeira vez que estava carregando as informações. E, logo na sequência, ele pegou o `username` e definiu como o do Paulo, `username: 'peas'`.

Já temos esse controle, agora precisamos pegar esse `usuarioLogado` e trocar por quem é o `de:` no `handleNovaMensagem`.

```
function handleNovaMensagem(novaMensagem) {
 const mensagem = {
   	// id:listaDeMensagens.length + 1,
			de: 'usuarioLogado',
   	texto: novaMensagem,
 };
```

Salvamos. Vou recarregar a página do chat e enviar uma mensagem, "Olá, Aluraverso". Apareceu a mensagem com o usuário do Paulo.


**Paulo:** Alguém pode perguntar assim: "Por que no meu código eu declarei um monte de `useState`, `useRouter` e essa não é nada de `use`?". Porque essa variável não fica trocando e não precisamos gerar um efeito no React que atualiza outras pessoas.

Se fosse, por exemplo, possível trocar qual foi o usuário que falou todas as mensagens aí faria sentido usar essa variável com o Hook.

**Mario:** Exato. E é isso, sempre observe o seu código. Eu acredito que é melhor escrever sempre o menor código possível para fazer a solução, desde que funcione e dê para fazer manutenção .

Se cairmos em um caso desse, em que você precisa ter o valor em tempo real, ou algo do tipo, na hora em que a página carrega, recomendo que você não use esse formato e sim o `useEffect`.

Beleza, Paulo. Resolvemos a parte do login. Agora podemos ter dois usuários mandando mensagens.

Feito isso, vou mostrar para a galera mais um gist com bloco de código, o do sticker, <a href="https://github.com/alura-challenges/aluracord-matrix/blob/aula05/src/components/ButtonSendSticker.js" target="_blank"> o ButtonSendSticker que está acessível aqui</a>.

Basicamente, ele importa box, botão, texto e imagem da lib de componentes; ele tem uma caixa para fazer esse botão, tem um botão redondo, e quando você clica para abrir a caixa ele mostra uma opção com os stickers disponíveis.

Vou copiar esse bloco de código do `ButtonSendSticker.js` e, como estamos colocando muita coisa num arquivo só, o ideal no dia a dia é ir quebrando. Vamos trabalhar isso agora. Na raiz do projeto, no *menu explorer*, vou criar uma pasta chamada "src", a *source*. Que é o que vemos muita gente fazer para guardar componentes criados. Dentro de "src", criaremos uma pasta chamada "components".

Na descrição do vídeo vai ter um vídeo meu explicando como você pode organizar as pastas de um projeto, o porquê de criá-las, qual o sentido que elas têm e não só por estética, mas sim por ter uma razão funcional no seu projeto. No caso, a "components" é a pasta de guardar todos os componentes, dentro dela criaremos o `ButtonSendSticker.js` e nele vamos colar o código que copiamos.

Vamos importar esse `ButtonSendSticker` lá no nosso `chat.js`. No topo do código do `chat.js`. Como estamos usando o `export` no `export function ButtonSendSticker()`, vamos passar com chaves: `import {ButtonSendSticker} from '../src/components/ButtonSendSticker';`.


**Mario:** Lembrando que o **`../`** em `import { ButtonSendSticker } from '../src/components/ButtonSendSticker';` é porque estamos partindo da pasta *pages* dentro da, raiz, ou seja, a pasta central. Nessa raiz, abaixo da pasta *pages*, está a pasta ***"src"***, e dentro dela está a pasta *components*. Em *componets* acessamos o código do `ButtonSendSticker.js` que exporta esse componente a partir do comando `export function ButtonSendSticker(){}` .
 
Sempre digite o passo-a-passo, apertando "CTRL + Espaço" para o programa fazer sugestões. Se apagarmos tudo depois de `../` , voltando para *home*, e digitarmos `src/` , que é a pasta que queremos acessar, será sugerido `components` . Colocando **`/`** após *componentes* , aparecerá a sugestão do `ButtonSendSticker` . O próprio VSCode nos ajuda, a partir do *autocomplete*.
 
Agora, Paulo, vamos colar nosso componente após o fechamento da tag `<TextField />`. Utilizaremos a sintaxe `<ButtonSendSticker />` , como se ele fosse uma tag existente, e recarregaremos o nosso site. Notamos que, ao lado do campo de texto, o botão de stickers aparece.
 
É possível ajustar as cores e customizar. Eu coloquei o ícone de emojis aleatórios, porque é o mesmo que acontece no Discord quando passamos o mouse sobre o botão. Quando clicamos no botão, Paulo, o chat mostra a lista de stickers do pessoal do Gaveta e da Alura. Temos o Darth Vader, o Pikachu, a criança que ganhou o Nintendo 64 e ficou muito feliz.
 
**Paulo:** Mario, vamos atualizar isso para ter mais coisas do Aluraverso. Só um não. Achei pouco. Vamos atualizar.
 
**Mario:** Calma. Vamos carregar os do Aluraverso. Quando o disponibilizarmos o código para o pessoal em casa, estará com toda lista dos Stickes do Aluraverso. Tudo que vimos aqui estará no código.
 
**Paulo:** Está bem.
 
**Mario:** Seguinte, Paulo. Quando clicamos no botão de stickers, o pop-up abriu, e quando clicamos de novo, ele fechou. Se clicamos em um sticker, o botão também já está com o comportamento de fechar. Essa aula é para explicar para o pessoal como criar componentes que estendem, trabalhando com um dos princípios legais da programação, chamado de *open-closed*. Primeiramente vamos entender o porquê desse aberto ou fechado.
 
Quando clicamos no botão, aparecem os stickers e, ao clicarmos em algum deles, o pop-up fecha. Se observarmos no código do nosso componente "ButtonSendStickes.js", a função `ButtonSendStickers()` tem um estado que identifica se o pop-up está aberto ou não, na `const [isOnpen, setOpenState] = React.useState ('');` . Também temos a tag `<Button />` , na qual tem várias especificações, como o `hover{}` e o `filter` .
 
**Paulo:** (especificações) de estilo. Para ficar bonito.
 
**Mario:** Após a tag `<Button />` , colocamos o `{isOpen && () }` informando que, caso o pop-up esteja aberto, ele carrega uma série de comando.
 
**Paulo:** Esse é o *if*, correto? É a forma que escrevemos o *if* no React, certo, Mario?
 
**Mario:** Exatamente.
 
**Paulo:** Escrevemos assim porque o *if* não retorna nada. Uma expressão boleana retorna, certo?
 
**Mario:** Isso.
 
**Paulo:** Quando queremos mostrar algo ou não, é essa sintaxe que usamos. Não escrevemos um código enorme com *if*, correto?
 
**Mario:** Exato. Se colocarmos no nosso código, antes do `{isOpen && ()}` , o comando `{ true && 'Algum Valor' }` , no nosso chat aparece "Algum valor" abaixo do botão de stickers. Se alterarmos o código para `{ false && 'Algum Valor' }` , essa informação some.
 
Então essa lógica do estado fará com que, sempre que codarmos `{true &&}` , a alteração aparece no chat. Quando trocamos para `{false &&}` , a mudança para de aparecer. Esse é como se fosse o "*if*" da página.
 
E para mudar o estado "aberto", temos o código `onClick ={() => setOpenState (!isOpen)}` , sendo que `(!isOpen)` significa "o contrário do *isOpen*". Portanto, se o estado está `false`, quando clicamos muda para `true` , e se está `true` , quando clicamos altera para `false` .
 
Essa é uma lógica super comum de Front-End. Acredito que esteja em alguma parte do código de todos os projetos, e podemos aproveitar para usar no dia-a-dia. É uma dica bem importante de projetos no geral.
 
Então temos no nosso código o `ButtonSendSticker()` e o `setOpenState`. Na função `{isOpen &&()}` , observamos que, a qualquer momento que clicamos no pop-up que está descrito na tag `<Box/>` , o comando `onClick={() => setOpenState(false)}` é ativado, trocando o estado do nosso botão para falso e fechando o pop-up.
 
Abaixo desse comando, temos a tag `<Text />` com as definições do título "Stickers", que aparece na parte de cima do pop-up de stickers. Depois do trecho `<Text /> `, há outra tag `<Box />` contendo com cada item da `li` , sendo as imagens dos stickers, Paulo.
 
Coloquei vários GIFs para ficar mais impactante, mas temos todas as imagens nessa tag `<Box />`.
 
**Paulo:** Esse `{appConfig.stickers.map((sticker) => ()}` é onde estão todos os nossos stickers. Onde ele foi armazenado?
 
**Mario:** Ele está dentro da pasta principal, Paulo.
 
**Paulo:** Esse a gente copiou?
 
**Mario:** Isso. Ele é um *import* do componente "config.json", que eu disponibilizarei para o pessoal com o máximo possível de stickers do Aluraverso. Colocamos alguns de exemplo para gravarmos a aula, mas terão todos o do Aluraverso nesse arquivo.
 
**Paulo:** Entendi. E quem quiser adicionar um novo, é nesse documento que precisa adicionar.
 
**Mario:** Exato! Porque se o seu (sticker) for do "Cavaleiros do Zodíaco", do "Sailor Moon" ou qualquer outra coisa que você goste, você poderá colocar os seus stickers dentro desse arquivo e mandar por mensagem no app. Então tudo está interconectado e vai dar certo o resultado.
 
Agora queremos fazer os stickers funcionarem. Após repassarmos pelo componente dos stickers, conseguimos entender um pouco a lógica do *box* e do texto dos stickers. Temos o `<Text />` dentro do `{appConfig.stickers.map((sitcker) => ()}` . Por onde começaremos?
 
Sabemos o que acontece sempre que clicamos em um dos itens dentro do pop-up. Inclusive podemos usar o *Inspect* sobre um desses itens e observaremos no código em *"Elements"*, uma série de **`li`** . Poderíamos trocar esses stickers por botões, mas colocamos os GIF's por questões estéticas. De toda forma, ao clicarmos sobre eles, o que deveria acontecer com esse sticker, Paulo?
 
**Paulo:** É uma boa pergunta.
 
**Mario:** Pensando no código que já temos.
 
**Paulo:** Porque ele tem que criar uma mensagem para enviar, certo?
 
**Mario:** Certo.
 
**Paulo:** Só que essa mensagem não pode ser texto. Temos que pensar em uma forma de termos um código nessa mensagem para informar para aplicação que é um sticker. É isso que faremos?
 
**Mario:** Então, isso eu ia sugerir como desafio, mas é possível juntar as duas coisas.
 
**Paulo:** Você quer apenas colocar na tela, então?
 
**Mario:** Só colocar na tela.
 
**Paulo:** Entendi. Por enquanto ela não irá para o servidor. É isso?
 
**Mario:** Ela também vai.
 
**Paulo:** Não funcionou a charada para eu resolver. Vai lá.
 
**Mario:** Vamos lá. O ponto que você trouxe está certo, porque se pensarmos em quando usamos um emoji, acho o Github um bom exemplo, se você digita **":heart:"** e aperta "Enter", a mensagem é trocada para outra coisa, por exemplo, o emoji do coração.
 
Então precisamos informar que estamos digitando o sticker para trocar a mensagem pela imagem.
 
**Paulo:** Então você seguirá a abordagem de criar um código dentro da mensagem, ao invés de alterar o banco de dados para ter uma mensagem do tipo "sticker" e utilizar uma fórmula *if* para o caso do campo “mensagem” estar vazio, mas o sticker ser incluído.
 
Você seguirá outra abordagem, certo? E provavelmente ficará mais bonito, pensando em um sistema maior, apesar de agora estarmos em um sistema menor.
 
**Mario:** Isso. Então o que faremos? De alguma forma informaremos que a mensagem que iremos enviar é um sticker.
 
Se enviarmos a mensagem ":sticker:" e a URL da imagem que está no arquivo *"{} config.json"*, já funciona. Se quiser uma abordagem mais próxima do que o Slack, o Github e outros programas fazem, ao invés de uma *array*, ou seja, `"stickers": []` , precisaríamos criar um objeto. Acho que isso fica um pouco mais complexo para explicar e fazermos juntos.
 
Contudo, a funcionalidade de clicar em uma das imagens que aparecem no pop-up e enviaremos uma mensagem com **":sticker: URL"** já nos possibilita mandarmos esse sticker. Se você quiser customizar ou exibir alguma coisa, dará certo dessa forma.
 
Fez sentido?
 
**Paulo:** Sim.
 
**Mario:** Beleza, Paulo. O que vou sugerir?
 
Primeiramente, antes de codarmos várias coisas, temos a mensagem que carregamos, certo? O `[]` . Tentaremos implementar sem escrever nenhuma linha de código da interação. Apenas faremos esse novo tipo de mensagem ser aceito.
 
Eu dei um exemplo, será **":sticker: URL_da_imagem"**.
 
**Paulo:** Inventamos o nosso formato.
 
**Mario:** Isso. Lembrando, pessoal, existem formas melhores de fazer isso. Faremos uma forma que funciona mais facilmente para o nosso contexto, mas você pode usar a forma que preferir.
 
Por enquanto, comentaremos o `setListaDeMensagens(data)` no trecho `supabaseClient` . E na `const [listadeMensagens,setListaDeMensagenS] = React.useState([]);` colocaremos uma mensagem de teste dentro da *array* no formato de objeto, ficando da seguinte forma.
 
```
const[listaDeMensagens,setListaDeMensagens] = React.useState([
           	{
                          	id: 1,
                          	de: 'omariosouto',
                          	texto: ':sticker: URL_da_imagem',
           	}
]};
```
 
**Paulo:** Deixa eu entender. Você está forçando uma (mensagem) inicial, é isso?
 
**Mario:** Exatamente. Quando conferimos o chat, temos a mensagem **":sticker: URL_da_imagem"**.
 
**Paulo:** Por que ela não mostrou aquelas outras mensagens do banco de dados?
 
**Mario:** Porque colocamos a lista de mensagens como um comentário no nosso código para não mostrar as outras, para vermos apenas uma mensagem.
 
**Paulo:** Está certo. Ele até lê o comando, mas não faz nada.
 
**Mario:** Exatamente.
 
Isso aqui, Paulo, é uma técnica de bug. Eu queria até esclarecer isso para o pessoal. Essa é uma técnica boa para conseguir entender um pouco do código.
 
Não usem a integração do Back-End, escrevam todo o código, entendam o que está acontecendo e depois interliguem tudo.
 
**Paulo:** Perfeito. Então já coloca um sticker da Alura no lugar de `URL_da_imagem` . Escolhe um link do *"() config.jason"* .
 
**Mario:** É o terceiro link.
 
**Paulo:** Copia o terceiro link. Se não for o da Alura, não tem problema.
 
**Mario:** Então copiamos o GIF animado e colamos no lugar da URL em `texto: ':sticker: '` .
 
**Paulo:** Esse nome *"sticker"* é, na verdade, GIF, certo? Não importa, depois vemos como fazer isso.
 
**Mario:** Sim! É que no Telegram tem o sticker animado. Nesse caso vai do critério que cada um quiser usar.
 
**Paulo:** Perfeito.
 
**Mario:** Olha, Paulo, ele mandou a mensagem com o link do sticker, certo? Então temos ":sticker:" com o link.
 
Qual seria o correto, Paulo, ao invés de mostrar a URL?
 
**Paulo:** Colocar a imagem, certo? Melhor ainda, chamar um componente de imagem de sticker. Se tiver, melhor ainda.
 
**Mario:** Exato! Se tiver, melhor ainda. No nosso caso, o que podemos fazer?
 
Temos a `listaDeMensagens` no `const` . E essa lista de mensagens é passada para `<MessageList mensagens={listaDeMensagens} />` . É importante falar que *Message List* já tem a lógica de interface em que os componentes não serão apenas para reuso ou para deixar mais fácil de mexer. Eles terão pedaços de lógica de UI.
 
Para o Slack é extremamente importante, por toda lógica de desenhar as coisas. Para o Discord também. Para todas as ferramentas de chat é importante ter essa lógica de replicar pedaços do código. Então o *Message List*, sempre que recebe as mensagens no *props*, em `console.log(props);` , aplica em `{props.mensagens.map(mensagem)}` e, por padrão, ele apenas renderiza o texto.
 
Agora, Paulo, começaremos a usar condicionais para renderizar esse texto.
 
**Paulo:** Alguma coisa como
 
```
if mensagem de texto possui stickers:
           	mostra a imagem
else
           	mensagem.texto
{mensagem.texto}
```
 
Ou seja, "*if* essa mensagem de texto possui stickes no começo, pega o fim do stickers e renderiza o image src", aquela tag HTML clássica.
 
**Mario:** Exato.
 
**Paulo:** Caso contrário, "mensagem.texto". Por isso você não explicou o *if*, porque teremos um agora. Entendi.
 
Porém esse *if* tem o mesmo problema no *forEach* no React.
 
**Mario:** Exato.
 
**Paulo:** Ele retorna *undefined*.
 
**Mario:** Eu posso até dar um nome bonito, Paulo. Tudo o que for *statement*, ou seja, declaração de variável, estrutura (if, while, for), não conseguimos usar dentro do código do React.
 
Só conseguimos retornar o que estiver baseado em expressão, presente nos livros como *expression*. É necessário executar e ter o retorno imediato, não havendo bloco de código para tomar alguma decisão de estrutura.
 
Então se colocarmos o código `{if}` na nossa estrutura, ele aparecerá como erro, com um sublinhado vermelho, porque o código não permite. Porém se colocarmos `{mensagem.texto.startsWith(':sticker:')}` , ou seja, a mensagem começa com ":sticker:", podemos descobrir se temos um `true` ou `false` . Podemos até colocar `Condicional: {mensagem.texto.startsWith(':sticker:')}` para conferirmos na prática.
 
Após salvarmos o código e recarregamos o chat, podemos conferir que na mensagem que enviamos anteriormente não há nada de diferente, porque o React não realiza o `toSting` em boleano. Temos que alterar manualmente o código para `{mensagem.texto.startsWith(':sticker:').toString` . Agora, ao recarregarmos a página, a mensagem que enviamos mudou para "Condicional:true:if mensagem de texto possui stickers: mostra a imagem else mensagem.text:sticker:" junto com a URL.
 
Nossa primeira mensagem ficou misturada com o *if* que escrevemos no código, então caso também tenha escrito, basta selecionar e deixar como comentário, ou apagar, para não deixar bagunçado. Dessa forma, ao voltarmos no site, poderemos observar que a mensagem que enviamos começa com ":sticker:", então esse comando dará certo.
 
Agora, Paulo, copiamos o trecho `mensagem.texto.startsWith(':sticker:')` e colamos em uma nova linha, abaixo do que escrevemos, como
 
```
{mensagem.texto.startsWith(':sticker:') && (
           	mensagem.texto
)}`
```
 
**Paulo:** Mas se é sticker, não queremos mostrar a mensagem de texto, e sim a imagem.
 
**Mario:** Chegaremos lá.
 
**Paulo:** Concatena com "É sticker", apenas para termos certeza que é um sticker.
 
**Mario:** Boa, então o código fica
 
```
{mensagem.texto.startsWith(':sticker:') && (
           	'É sticker'
)}`
```
 
Perfeito, Paulo. Agora quando voltamos para o chat, nossa mensagem está como "Condicional: trueÉ sticker".
 
**Paulo:** E como eu faço o *"else"* nessa linguagem?
 
**Mario:** Agora vamos evoluir. Queremos um "*if*" e um "*else*". Para isso, usaremos um "*if* ternário". Ao invés de passarmos a condição diretamente, faremos uma sintaxe de pergunta dentro do trecho de código. Portanto trocaremos o `&&` por `?`.
 
Nosso código lerá como "Essa mensagem é um sticker?". Se for, ele irá mostrar a mensagem "É sticker", caso não seja, utilizaremos o **`:`** para retornar como mensagem, ou seja, `mensagem.texto` . Portanto nosso novo código é:
 
```
{mensagem.texto.startsWith(':sticker:')
? (
           	'É sticker'
)
: (
           	mensagem.texto
)}
```
 
Esse código, Paulo, é complexo em um primeiro momento. Eu sei que é complicado de ler esse ternário para você que está assistindo e reflete sobre ele. Porém ele é o mais comumente visto no meio dos códigos React. Tanto que, no chat, percebemos que a "Condicional:" retornou *"true"* e apareceu a mensagem "É sticker".
 
Então a `Condicional: {mensagem.texto.startsWith(':sticker:')}` que codamos está funcionando e, se voltarmos na parte inicial do código e passar uma mensagem que não é sticker, a mensagem irá aparecer com *"false"*. Por exemplo:
 
```
const [listaDeMensagem, setListaDeMensagens] = React.useState([
           	{
                          	id: 1
                          	de: 'omariosouto',
                          	texto: ':sticker: URL_da_imagem',
           	},
           	{
                          	id:2,
                          	de: 'peas',
                          	texto: 'O ternário é meio triste',
           	},
]);
```
 
No nosso chat, a mensagem do Paulo, com o usuário "peas", irá aparecer como "Condicional: falseO ternário é meio triste". Essa condicional se refere ao trecho que codamos sobre a mensagem começar com `(':sticker:')` . Então temos esse controle de exibir o que quisermos.
 
De acordo com a forma que você evoluir essa lógica, é possível que tenha muitos *if*s, então você precisará de um *strategy*. Terá um vídeo meu na descrição explicando como fazer melhor essa organização de *if*s no código. Por enquanto temos apenas dois tipos, então já funciona.
 
**Paulo:** Perfeito. Agora está bem claro. A sintaxe é um pouco feia para quem não está muito acostumado com operador ternário que tem na maioria das linguagens.
 
Porque se fosse Javascript puro, teríamos feito "*if* em HTML é esse, *else* em HTML é esse". Porque estávamos pedindo para ser modificado. No React é diferente. Estamos retornando algo para o componente visual.
 
**Mario:** Exato. E essa é a diferença. Esse é o modo chamado de "declarativo", porque declaramos o que deve ser retornado. No outro modo, damos uma ordem. "Se acontecer isso, injeta isso nesse pedaço". Nesse modelo nós apenas descrevemos. "Se for assim, quando estiver renderizando faz desse jeito ou do outro".
 
Então, Paulo, feito nosso código mais declarativo, vou comentar `{/* Condicional: {mensagem.texto.startsWith(':sticker:').toString()} */}` . Com isso, nosso código determina que, se a mensagem começar com ":sticker:", será necessário replicar a `mensagem.texto` e renderizar no componente de imagem, ou seja:
 
```
{mensagem.texto.startsWith(':sticker:')
? (
           	<Image src={mensagem.texto.replace(':sticker:')} />
)
: (
           	mensagem.texto
)}
```
 
Contudo, não pode ser apenas a `mensagem.texto` , porque precisa tirar a parte ":sticker:". Por isso usamos o comando `.replace(':sticker:')` . É importante lembrar que o `<Image />` veio da lib de componentes do começo do código, que faz a imagem ser responsiva e as demais funcionalidades dessa imagem.

**Paulo:** Poderíamos usar uma tag `<img>` e `<src>` normalmente. O `.replace()` deve ter vírgula e aspas simples após o `':sticker:'` dos parênteses. Na verdade, estamos deletando o `':sticker:'`, pois se começa com este, devemos deletar o que está escrito e poderíamos fazer outras validações para termos certeza, mas estamos "arredondando".

**Mario:** Exatamente, fomos direto ao ponto. Se esperarmos um pouco, já veremos o *sticker*.

**Paulo:** Sem dar o reload, o programa já colocou e está muito lindo este projeto!

**Mario:** Agora está responsivo e está mais interativo. Se quisermos que a imagem fique um pouco menor, por exemplo, podemos colocar um valor no tamanho máximo. Enfim, podemos customizar e e melhorar da forma que quisermos.

Então já temos nossa definição e o contato de como deve ser um sticker. Feito isso, voltaremos ao código e, em `chat.js`, podemos comentar o conteúdo de `const [listaDeMensagens, setListaDeMensagens] = React.useState()` caso queiramos testar algo. Assim, as mensagens iniciais voltam a ser uma lista vazia.

Vamos pegar a `listaDeMensagens` do back-end e faremos com que, quando clicarmos no botão que exibe os stickers, a imagem apareça no chat.

Porém, teremos que alterar este componente para inserirmos o princípio de Open/Closed que já citamos. Sabemos que, por enquanto, a janela de sticker só abre e fecha sozinho, pois só colocamos o `ButtonSendSticker` sem receber nem passar nada.

**Paulo:** Normalmente, usando React e bibliotecas, faríamos isso com comandos no terminal, mas neste código copiamos e colamos um arquivo gist porque queremos entender bem como criamos componentes.

Em geral, no momento em que o `ButtonSendSticker` já estivesse pronto, este pegará o open source e o usaria. Então nem teríamos este código no meio dos arquivos, pois ficaria em algum pacote do Node.js em outro formato.

Porém em nosso caso não está empacotado, porque ainda estamos aprendendo e queremos ler como alguém criou um componente visual para o botão de enviar stickers.

**Mario:** Exato! Também estamos mostrando as boas práticas, e o mais importante de saber - até se for criar um componente em sua empresa - é que devemos criar meios das pessoas interceptarem as ações do componente

Então se abrirmos a janela de sticker clicando no botão da aplicação e clicarmos na imagem da Alura, ele deve saber que irá rodar uma função que o componente não precisa saber qual é, mas será a responsável por de fato inserir o sticker na tela.

Para fazermos isso, procuraremos dentro de `ButtonSendSticker.js` onde está o texto da `tag="li"`, e acima adicionaremos `onClick` contendo `console.log()` recebendo `'Clicou no sticker:'` e a url `sticker`.

```
//código anterior omitido

{appConfig.stickers.map((sticker) => (
	<Text
		onClick={() => {
			console.log('Clicou no sticker:', sticker);
		}}
		tag="li" key={sticker}
		styleSheet={{
			width: '50%',
			borderRadius: '5px',
			padding: '10px',
			focus: {
				backgroundColor: appConfig.theme.colors.neutrals[600],
			},
			hover: {
				backgroundColor: appConfig.theme.colors.neutrals[600],
			}
		}}
	>

//código posterior omitido
```

**Mario:** Se abrirmos o Console, poderemos visualizar o chat, clicar no botão de enviar o sticker e escolher um para ver o resultado.

Notaremos que cada sticker muda a mensagem no Console. Então o componente ja sabe abrir e fechar, e identificar o clique de um item.

Agora, quem está usando a lib quer executar seu código quando acontecer a interação com o componente.

Normalmente, isso será o `on`. Da mesma forma que há o `onChange()`, `onSubmit()` e outros, o componente que queremos que outras pessoas usem deve ter uma forma de interceptar.

Então podemos fazer o `onStickerClick` em `<ButtonSendSticker>` do `chat.js`, para que quando alguém clicar no sticker, o elemento que estiver usando o componente passe uma função sua. Portanto o `console.log()` receberá `'Salva esse sticker no banco'`.

**Paulo:** Desta forma, quem criou o componente também criou o `onStickerClick`. É diferente de um evento JavaScript padrão de navegador, e muitos componentes React terão outros tipos de eventos que precisar.

**Mario:** Isso é chamado interceptação, em que podemos prover algo para quem estiver usando nosso componente. Se instalarmos usando os comandos como o Paulo citou, não precisaremos saber o código, e sim saber que podemos usar `onStickerClick` e que estará configurado dentro da função `ButtonSendSticker()`  como uma `props` que receberemos.

```
import React from 'react';
	import { Box, Button, Text, Image } from '@skynexui/components';
	import appConfig from '../../config.json';
	
	export function ButtonSendSticker(props) {
		const [isOpen, setOpenState] = React.useState('');
		
		return {

//código posterior omitido
```

**Mario:** Já no clique do sticker que acabamos de colocar, faremos `props.onStickerClick()` para executarmos passando qual o `sticker` que estamos trabalhando.

Isso também é comumente chamado de inversão de controle, pois a própria biblioteca avisa quem a está utilizando e o que está acontecendo. É importante também fazer o `if()` recebendo `props.onStickerClick()`. Podemos colocar inclusive que, caso seja `Boolean` e `true`, tentará executar a função.

Portanto, dentro do `console.log()`, escreveremos `[DENTRO DO COMPONENTE]'` antes de `Clicou no sticker:'`.

```
//código anterior omitido

{appConfig.stickers.map((sticker) => (
	<Text
		onClick={() => {
			console.log('[DENTRO DO COMPONENTE] Clicou no sticker:', sticker);
			if(Boolean(props.onStickerClick)) {
				props.onStickerClick(sticker);
			}
		}}
		tag="li" key={sticker}
		styleSheet={{
			width: '50%',
			borderRadius: '5px',
			padding: '10px',
			focus: {
				backgroundColor: appConfig.theme.colors.neutrals[600],
			},
			hover: {
				backgroundColor: appConfig.theme.colors.neutrals[600],
			}
		}}
	>

//código posterior omitido
```

**Mario:** Depois, abriremos o `chat.js` novamente e, no `console.log()` do `onStickerClick`, adicionaremos `'[USANDO O COMPONENTE]` antes de `Salva esse sticker no banco'`.

```
//código anterior omitido

<ButtonSendSticker
	onStickerClick={() => {
		console.log('[USANDO O COMPONENTE] Salva esse sticker no banco');
	}}
/>

//código posterior omitido
```

**Mario:** Salvaremos o código e carregaremos a página. Quando clicarmos no botão de enviar o sticker, primeiro irá rodar o código que chama o `.log()` de quem está dentro do componente e exibe a imagem.

Já quem usa o componente, irá salvar este sticker escolhido no banco. Portanto, no `onStickerClick`, receberá o `sticker` de dentro do componente.

```
//código anterior omitido

<ButtonSendSticker
	onStickerClick={(sticker) => {
		console.log('[USANDO O COMPONENTE] Salva esse sticker no banco');
	}}
/>

//código posterior omitido
```

**Mario:** Então, no `ButtonSendSticker.js`, passamos o `onStickerClick`, o componente recebe na `props` e registra para que toda vez que alguem clicar na imagem, irá passar o `.log()` e, caso tenha a propriedade, chamará a função que passamos recebendo o `sticker`.

**Paulo:** Certo, então fizemos algo bem avançado. 

**Mario:** É chamado de call-back, e já usamos isso o tempo todo e o JavaScript Funciona.

**Paulo:** Usamos os que outras pessoas haviam criado.

**Mario:** O `fetch()` e o `.then()` que vimos têm o call-back por exemplo, então estamos sempre usando esse recurso que é sempre uma chamada de retorno, ou seja, quando alguma coisa que queríamos terminar, o código irá executar a função que foi passada.

Para fecharmos essa parte do sticker e seguirmos para a parte do real time, iremos confirmar se de fato a figura está aparecendo. Tiraremos o `console.log()` interno da biblioteca e colocaremos somente a parte mais externa do chat.

Exibindo a aplicação, clicaremos no botão e escolhemos uma opção de sticker. No Console, veremos a url do `.gif` com a mensagem que colocamos.

Falta-nos pegarmos este sticker e montarmos a mensagem na função `handleNovaMensagem()` no arquivo `chat.js`.

**Paulo:** Bastará colocarmos a mensagem com o sticker na frente.

**Mario:** Isso mesmo. Então iremos até a tag `<ButtonSendSticker>` e adicionaremos o `handleNovaMensagem()` recebendo `':sticker:'` seguido de `+ sticker`, que é a concatenação que o Paulo havia citado, e podemos usar crases tbm que irá funcionar.

```
//código anterior omitido

<ButtonSendSticker
	onStickerClick={(sticker) => {
		console.log('[USANDO O COMPONENTE] Salva esse sticker no banco');
		handleNovaMensagem(':sticker:' + sticker);
	}}
/>

//código posterior omitido
```

**Mario:** Para reforçar, é a mesma coisa que já tínhamos passado no bloco comentado anteriormente no mesmo arquivo.

Agora, salvaremos e faremos o teste final de enviar um sticker no chat. E apareceu! Carregaremos novamente para termos certeza.

**Paulo:** Perfeito. Se colocarmos o sticker na mensagem, também pegará inclusive outro novo sticker escrevendo ":sticker:" com a nova imagem no campo de texto da aplicação.

**Mario:** Podemos colocar condicional e trabalhar de outras formas, pois isso é um processo contínuo. Não à toa que os stickers do Discord, Slack e Whatsapp possuem diversos devs e gerentes de produto, entre outros profissionais de UX para ver qual a melhor experiência.

Nesta aula, fizemos apenas um experimento para ser customizado e colocado no portfólio.

Chegamos no momento em que falta apenas um recurso para terminarmos o projeto, sem contar com o vídeo especial secreto. A última feature nos permitirá duplicar a aba, logar com o nosso usuário novamente após o logout, entrando como "omariosouto" desta vez, para conversarmos via chat.

**Paulo:** Agora temos o efeito que mostramos no início da aula, em que se mexermos em um, não pegará em outro elemento, pois se escrevermos uma mensagem no chat em outra aba ou em outro computador "deployado" na Vercel, não irá atualizar.

Mas se escrevermos uma mensagem e apertarmos a tecla "Enter", virá esta e a antiga, pois atualizou.

**Mario:** É verdade, não irá pegar esta, somente a que o Paulo criou.

**Paulo:** Não estamos puxando toda a lista, e sim só o que inserimos, o que é um problema.

Mas temos dois problemas; basicamente, para resolver, precisamos saber se, quando o back-end recebe uma mensagem nova, podemos ficar sabendo que precisamos atualizar em todo o data da tabela "mensagens" do back-end do `supabase`.

Algumas pessoas fazem isso como em real time com aspecto síncrono ou de web socket. Mesmo que não utilizemos nada disso, precisamos do efeito de que tudo está acontecendo e as pessoas estão interagindo, mas ainda não é bem isso.

**Mario:** Podemos fazer isso indo no `supabaseClient` em `chat.js` para que toda vez em que houver uma nova mensagem na lista, possamos pedir para o servidor pegar as informações.

Também podemos colocar um timer para ficar o tempo todo conferindo, mas há um custo que já comentamos.

Falando sobre a elegância da solução que o Supabase nos fornece.

**Paulo:** É como se fosse um gatilho. Toda vez que a tabela `'users'` tiver `.on('INSERT'`, acontecerá algo. Neste caso abaixo, é o `sendSlackAlert()` que é como se existisse uma função que faz isso.

Exemplo:

```
supabase
	.from('users')
	.on('INSERT', data => {
		sendSlackAlert(data)
	})
	.subscribe()
```

**Paulo:** Então a própria API do `supabase` que instalamos do pacote já nos oferece outras ações e reações, chamando as funções que queremos.

Provavelmente pegaremos esses dados, teremos o `.setState()` e atualizaremos tudo. E o `.subscribe()` está justamente falando para ativarmos este trigger ou listener entre sistemas, como um pequeno sistema de mensageria.

**Mario:** Começaremos a fazer isso no nosso código. Indo ao `chat.js`, apagaremos o bloco de texto que comentamos anteriormente em `const[listaDeMensagens, setListaDeMensagens]`.

Em seguida, na linha anterior à função `ChatPage()` e posterior a `const supabaseClient`, adicionaremos a `function` chamada `pegaMensagensEmTempoReal()`.

Esta terá o retorno do `supabaseClient` seguido de `.from()` recebendo `'mensagens'` para indicarmos a tabela de origem. Depois, traremos o `.on()`, e o próprio VSCode nos irá sugerir o `DELETE`, ou `UPDATE` e o `INSERT`.

Colocaremos este último entre aspas simples e letras maiúsculas, e toda vez que essa inserção acontecer, teremos que inscrever no código.

**Paulo:** Já chamaremos o `.subscribe()` abaixo para decidirmos o que iremos colocar no "miolo". 

**Mario:** Então faremos o `console.log()` recebendo `'Houve uma nova mensagem'`.

**Paulo:** Na verdade, este nome `pegaMensagensEmTempoReal()` talvez não expresse a função, seria melhor ser `escutaMensagensEmTempoReal()` para fazer a alusão a listener, pois chamaremos isso apenas uma vez.

```
//código anterior omitido

function escutaMensagensEmTempoReal() {
	return supabaseClient
		.from('mensagens')
		.on('INSERT', () => {
			console.log('Houve uma nova mensagem');
		})
		.subscribe();
}

export default function ChatPage() {

//código posterior omitido
```

**Mario:** Exatamente. É justamente por isso que deixamos propositalmente separado para o chamarmos dentro do `.useEffect()` que só roda uma vez.

Então depois de pegarmos todas as mensagens, queremos pegá-las e escutá-las em tempo real.

```
//código omitido

React.useEffect(() => {
	supabaseClient
		.from('mensagens')
		.select('*')
		.order('id', {ascending: false })
		.then(({ data }) => {
			console.log('Dados da consulta:', data);
			setListaDeMensagens(data);
		});
	escutaMensagensEmTempoReal();
}, []);

//código posterior omitido
```

**Paulo:** Creio que aquele `return` que fizemos antes não é necessário.

**Mario:** Não o apagaremos por enquanto, pois temos que fazer alguns ajustes depois no momento em que saímos da página. Do contrário, pode travar o computador, entre outros problemas.

Salvaremos e entraremos na aplicação no navegador com o Console do inspetor de código aberto. Se digitarmos qualquer coisa no campo de mensagem e apertarmos a tecla "Enter", receberemos o texto "criando mensagem".

Comentaremos todos os `console.log()` de `chat.js`, deixando apenas o do `escutaMensagensEmTempoReal()` para vermos apenas essa feature. Carregaremos a página e escreveremos outra mensagem aleatória e enviaremos novamente.

Irá carregar, mas não mostrará, pois o `Realtime` do `supabase` é uma feature opcional, e temos que dizer que determinada tabela do campo a tenha.

**Paulo:** Certo, precisamos configurar em algum lugar.

**Mario:** Só precisamos apertar um checkbox, mas teremos que acessar o site "supabase.io" e clicar em "Start your project" por mais que já tenhamos a conta.

Em seguida, clicaremos para logarmos em "Sign In With Github" e acessarmos nossa página. O Supabase assume que já tentamos fazer uma conexão Realtime, e nos mostra a quantidade de chamadas e outras informações.

Temos o ícone do Table Editor na aba lateral de opções onde conseguimos ver tudo o que já cadastramos. Temos também os ícones de autenticação, armazenamento, editor do SQL e Database.

Dentro desta última, teremos a parte de tabelas na opção "Table" da aba lateral que aparece, mostrando todas as que temos, réguas, extensões e a opção "Replication". Clicando nesta última, encontraremos a configuração do `supabase_realtime`, e bastará clicar no botão "0 tables" na coluna "Source" para ativarmos o modo Realtime do Supabase.

Ao fazermos isso, clicaremos no check para que fique positivo na mensagem, que é a nossa tabela `mensagens` com a descrição ao lado.

Assim que clicarmos nesse checkbox, voltaremos ao projeto no navegador e escreveremos no campo de texto do chat novamente. 


**Mario:** Recebemos, no Console, o alerta de que "Houve uma nova mensagem".

**Paulo:** Perfeito! Agora basta pegar o dado, porque ele retorna um *data*. Mas, talvez nem seja necessário pegar o *data*. Quando acontece isso, podemos pegar todas as mensagens do banco de dados. Pode ser assim também, não? Mas ele vai trazer só um que foi inserido. 

**Mario:** Isso! Vou pegar `oQueVeio`. 

```
function escutaMensagensEmTempoReal() {
   return supabaseClient
	      .from('mensagens')
				.on('INSERT', (oQueVeio) => {
				   console.log('Houve uma nova mensagem', oQueVeio);
				})
				.subscribe();
	}
	
	```

**Paulo:** Vamos dar um `console.log()` nele para sabermos o que ele devolve.

**Mario:** Vamos tentar pegar as coisas com mais clareza. No Chat, vamos escrever "nova msg". No Console, aparece, `new` e é nele que está o `texto: "nova msg"`. Da mesma maneira, se digitarmos no Chat "Agora vai", no `new` teremos o `texto: "Agora vai"`. Se verificarmos a outra aba do localhost, o Console está mostrando os dois textos. 

Então, para fecharmos esse assunto e testarmos, na prática, esses processos acontecendo, vamos pegar o `new` e passaremos uma função que é o `adicionaMensagem`. Estamos usando a mesma lógica de inverter os controles para fazer o `adicionaMensagem()` receber o `new`.  

```
function escutaMensagensEmTempoReal(adicionnaMensagem) {
   return supabaseClient
	      .from('mensagens')
				.on('INSERT', (new) => {
				   adicionaMensagem(new);
				})
				.subscribe();
	}
	
	```

**Paulo:** É porque o `adicionaMensagem` está na parte de dentro e nós não conseguiremos acessar de fora sem passar. 

**Mario:** Exato! Um detalhe que apareceu agora: tivemos um problema com esse trecho de código, mais especificamente com o `new` em `.on('INSERT', (new) => {`, porque ele é uma palavra-chave. Então, podemos corrigir substituindo por `.on('INSERT', (respostaLive) => {` e, embaixo, por `adicionaMensagem(respostaLive.new);`.

```
function escutaMensagensEmTempoReal(adicionnaMensagem) {
   return supabaseClient
	      .from('mensagens')
				.on('INSERT', (respostaLive) => {
				   adicionaMensagem(respostaLive.new);
				})
				.subscribe();
	}
	
	```

Quem chama, isto é, quem quer escutar a mensagem, `escutaMensagensEmTempoReal()`, precisa executar algo quando essa mensagem chega. No nosso caso, vamos passar a nossa função para quem escuta. O `onclick` e o `escutaMensagens()` têm a mesma lógica. Sendo que, no primeiro, disparamos a função e, no segundo, queremos executar a mensagem. 

Vamos pegar o `handleNovaMensagem()`. Nós passaremos a função abaixo, chamada da mesma maneira que a função `adcionaMensagem`. Ela vai receber a mensagem nova, `adicionaMensagem(respostaLive.new)`, vai para o trecho abaixo de novo, recebe em `escutaMensagensEmTempoReal((novaMensagem) => {` e joga na tela, `handleNovaMensagem(novaMensagem)`. 

```
escutaMensagensEmTempoReal((novaMensagem) => {
    handleNovaMensagem(novaMensagem)
 });
}, []);

```

Vamos retornar ao Chat e recarregar a página. Vamos escrever no campo de mensagem do Chat "Será que deu certo?" e enviar apertando "Enter". Ele "explodiu". Tivemos um *loop* infinito. Paulo, não dá para terminar o dia com tudo perfeito, esses erros acontecem e poderiam ter acontecido com quem está em casa também. Aconteceu comigo e é até bom, porque quem está acompanhando o curso consegue acompanhar em que parte errei. 

Eu coloquei um comando para que toda vez que tivéssemos uma nova mensagem, ele cadastrasse. 

```
escutaMensagensEmTempoReal((novaMensagem) => {
   console.log(novaMensagem);
   //handleNovaMensagem(novaMensagem)
 });
}, []);

```

A lógica é, basicamente, se escrevemos "ola" no Chat, ele cadastra no Back-End e joga na tela. Mas, toda vez que temos uma nova mensagem, estamos, de novo, cadastrando, por isso entramos em um *loop* infinito recadastrando as mensagens e geramos mil e quinhentas escritas. De certa maneira foi bom para atestarmos que o banco de dados aguenta bastante informação. 

Agora, no momento em que estamos fazendo `handleNovaMensagem(mensagem)`, pegamos o `insert`, deixaremos de fazer a parte do `setListadeMensagens([`. 

```
])
.then(({ data }) => {
    // console.log('Criando mensagem: ', data);
		setListaDeMensagens([
		    data[0],
				...listaDeMensagens,
		]);
});

setMensagem('');

}

```

Nós faremos apenas o `insert` na página e, ao invés de fazer o `handleNovaMensagem(novaMensagem)` para cadastrar, temos que atualizar a lista. Faz sentido? 

**Paulo:** Sim, do contrário estaríamos adicionando de novo e fazendo outro `insert`. 

**Mario:** O `handleNovaMensagem()` vai parar de atualizar a lista. Vamos comentar essa parte. 

```
])
//.then(({ data }) => {
//    // console.log('Criando mensagem: ', data);
//		setListaDeMensagens([
//		    data[0],
//				...listaDeMensagens,
//		]);
// });

setMensagem('');

}

```

Ao salvar,acontece o erro do "textarea". Vamos resolver no Terminal. 

```
aluracord git:(aula05) yarn dev 

yarn run v1.22.17

```
Em seguida, recarregaremos a página e escreveremos, no campo de mensagem do Chat, "Teste". Não está indo mais. Vamos até o `escutaMensagensEmTempoReal((novaMensagem)`, em teoria, a mensagem nova deveria estar nesse trecho. 

```
escutaMensagensEmTempoReal((novaMensagem) => {
   console.log('Nova mensagem', novaMensagem);
   //handleNovaMensagem(novaMensagem)
 });
}, []);

```

Vamos fazer um novo teste no Chat, "Nova mensagem". Não funcionou de novo. Faltou rodarmos ao menos o `.then`, por isso, vamos voltar com esse trecho, tirando apenas a lista. Precisamos do `.then` para disparar o cadastro. 

```
])
.then(({ data }) => {
    // console.log('Criando mensagem: ', data);
		//setListaDeMensagens([
		//   data[0],
		//		...listaDeMensagens,
		//]);
});

setMensagem('');

}

```

Outra vez no Chat, vamos escrever "oi". No Console, percebemos que o criando nova mensagem está na ilha 58. É o que fazíamos antes. Mas, ao invés de fazer o 7 da lista ou de chamar o `handleNovaMensagem()`, que foi o meu erro, precisamos apenas rodar o código acima que pegará a mensagem nova com o que existia da lista. 

Então, quem vai gerenciar a atualização da tela não é mais o `handleNovaMensagem()`, será esse outro pedaço abaixo, apenas com esse trecho de código e não todo o código de nova mensagem. 

```
escutaMensagensEmTempoReal((novaMensagem) => {
   console.log('Nova mensagem', novaMensagem);
   setListaDeMensagens([
	     data[0],
	     ...listaDeMensagens,
	   ]);
 });
}, []);

```

**Paulo:** Só ele?

**Mario:** Sim, tudo que já existia na lista de mensagens com a nova mensagem. Foi o meu erro fatal que fez com que acontecesse das mensagens ficarem se subscrevendo. Então, estamos escutando a mensagem em tempo real. Sempre que tiver uma nova, jogamos na lista. De volta à página, vamos carregar e escrever "Oi Paulo". No Console, perceberemos que ele pegou apenas a nossa mensagem que aparece agora, `de: "omariosouto"`. 

Existe um segredo no React que é importante mencionar. Ele carrega a página com as mensagens no Chat, quando escrevemos, por exemplo, "Nova Mensagem", apenas essa aparece e somem as outras. O motivo é que quando registramos o "escutador", `escutaMensagensEmTempoReal((novaMensagem)`, ele pega o valor inicial da lista, que é o valor vazio. Nós estamos registrando tudo e ele salva esse valor. O React não está avisando a esse pedaço de código que as coisas mudaram. 

```
escutaMensagensEmTempoReal((novaMensagem) => {
   console.log('Nova mensagem', novaMensagem);
   setListaDeMensagens([
	     data[0],
	     ...listaDeMensagens,
	   ]);
 });
}, []);

```

Para garantir que teremos de mensagens atualizada, ao invés de apenas passar o *array*, nós o tiraremos, passaremos uma função e retornaremos o valor. 

```
escutaMensagensEmTempoReal((novaMensagem) => {
   console.log('Nova mensagem', novaMensagem);
   setListaDeMensagens(() => {
	     return [
			     novaMensagem,
					 ...listaDeMensagens
			 ]
	   ]);
 });
}, []);

```

Isso porque o `setListaDeMensagens())`, recebendo uma função, sempre passará o valor atual que ele tem da lista. Portanto, teremos o `valorAtualDaLista`, que será o valor da lista de mensagens que está mais abaixo. 

**Paulo:** Normalmente, nós passávamos um valor para o `set`, não uma função. Nós sempre trabalhamos com *setter* de *state* passando o valor direto. Agora não, nós estamos passando um tipo de função que recebe o valor da lista atual e o que ele deve fazer com ela para retornar a nova lista. Eu não entendi porque antes não funcionava. Você poderia comentar e mostrar como era antes, deixando um do lado do outro, para que seja possível comparar? 

**Mario:** Sim, com certeza. 

```
escutaMensagensEmTempoReal((novaMensagem) => {
   console.log('Nova mensagem', novaMensagem);
	 console.log('listaDeMensagens:', listaDeMensagens);
	 setListaDeMensagens([
	    novaMensagem,
			...listaDeMensagens
])
  // setListaDeMensagens((valorAtualDaLista) => {
	//     return [
	//		     novaMensagem,
	//				 ...valorAtualDaLista,
	//		 ]
	//   ]);
  //   });
}, []);

```

Salvamos e vamos recarregar a página. Agora, escreveremos no campo de mensagem do Chat "crirei uma nova mensagem". No Console, é possível notar que o `listaDeMensagens: []`  é um *array* vazio. É antes de rodar o `setState()`. O `listaDeMensagens`, como nós registramos essa função para ser rodada sempre que existir uma mensagem nova, ela pega a versão inicial do *array*. Quer dizer que ela pega a primeira foto que o React tirou. 

**Paulo:** Entendi! Primeira foto do React e não do banco de dados, porque a foto que o React tirou era vazia. Correto? 

**Mario:** Isso! É essa primeira, `React.useState([]);` que passamos no seguinte trecho.

```
export defautl function ChatPage() { 
   const roteamento = useRouter();
	 const usuarioLogado = roteamento.query.username;
	 const [mensagem, setMensagem] = React.useState('');
	 const [listaDeMensagens, setListaDeMensagens] = React.useState([]);
	 
	 ```
	 
**Paulo:** Outra solução seria, nesta parte, carregar do banco de dados ao invés de passá-la vazia. Quando criamos a mágica do `.useState()`, dizemos: "React, a lista de mensagens é uma coisa mágica que você cuida e o valor inicial dela é vazio". O problema é justamente esse, como é vazia, na hora em que ele faz a primeira atualização, ele atualiza vazia para o primeiro *insert* que aconteceu, apagando o que aparecia no começo. 

**Mario:** O nosso "escutador" não sabe que a variável mudou. Ele cria a função, guarda na memória e fica esperando. Quando chega o momento de executar, ele executa com o valor inicial que ele tinha.

**Paulo:** Há outras maneiras de mudar e resolver? 

**Mario:** Sim, mas o mais comum, que as pessoas da documentação recomendam, é quando caímos nesse caso em que `//Quero reusar um valor de referência (objeto/array)`, nós também precisamos `// Passar uma função pro setState`. Portanto, liberamos o código de novo e, ao carregar a página, se escrevemos no Chat "Teste", funciona. 

```
escutaMensagensEmTempoReal((novaMensagem) => {
   console.log('Nova mensagem', novaMensagem);
	 console.log('listaDeMensagens:', listaDeMensagens);
	 //Quero reusar um valor de referencia (objeto/array)
	 //Passar uma função pro setState
	 
	 //setListaDeMensagens([
	 //   novaMensagem,
	 //			...listaDeMensagens
   //      ])
   setListaDeMensagens((valorAtualDaLista) => {
	     return [
			     novaMensagem,
					 ...valorAtualDaLista,
			 ]
	   ]);
	});
}, []);

```

A lista de mensagens que estava na linha 40 ainda está vazia, porque está considerando a primeira versão, mas se pegarmos o valor da lista atualizado, o React nos apresenta tudo que já existe. Esse é sim um assunto um pouco mais avançado, mas como estamos construindo um Chat que lida com inscrição de evento e outros conteúdos, é válido aprendermos, até porque, é um problema que pode aparecer no nosso dia a dia. 

Além disso, é importante passarmos por todo o processo, tanto errar, quanto ajustar, corrigir o código e assim por diante.

**Paulo:** Eu sempre fico bravo nas Imersões em que o Mario, na última aula, avança muito nos conteúdos, mas esse é um ponto que exemplifica bem a maneira como a Alura ensina e a importância do Dev em T. Não podemos o nosso aprendizado a uma cópia dos conteúdos das aulas, é necessário envolvimento, precisamos aprender como tudo funciona. 

Por isso, durante a imersão, eu pedi que o Mario retomasse o passo a passo, porque ele fez e já continuou. Esse "faz e já vai" é porque o Mario já conhece, nós precisamos fazer e entender o que estamos fazendo. Entender por que funcionou e porque não funcionou. 

Esse é o caso dessa aula, em que investigamos por que ele "limpou" o Chat naquele momento. Descobrimos que está relacionado com o `userFact` e com o  `useState`, mais especificamente porque ele não é uma variável comum, existe o `hook` que aciona uma série de elementos. Enfim, para compreendermos o React e conseguirmos trabalhar com ele, precisamos dominar o `useState` e os `hooks`. 

Até o mecanismo antigo de classe - que não aprendemos nessa aula, não havia necessidade - precisa ser entendido, porque, do contrário, apenas copiaremos e colaremos os conteúdos, ou arriscaremos alguns comandos sem compreendê-los de fato. Nós não desejamos ter esse perfil Dev, queremos compreender bem os conteúdos e seus usos. 

Claro que nas primeiras vezes nos confundimos, é complicado mesmo, mas precisamos sempre parar e buscar compreender. As nossas formações na Alura são organizadas assim, tanto que algumas pessoas perguntam o motivo de insistirmos em determinado assunto, e a resposta é que, em algum momento, será necessário entender o que está por trás dos conteúdos, inclusive, será necessário, em algum momento, ler o Código-fonte de um componente. 

Mesmo tendo uma boa compreensão da biblioteca, dos componentes e conseguindo fazer o visual rapidamente, em algum momento da carreira, para ser pleno, sênior ou *principal*, é preciso ter esse domínio. 

**Mario:** Paulo, eu gostaria de comentar sobre um caso bem banal. Muitas pessoas acham que se criamos dois *arrays* e comparamos, vai dar *true*. Esse problema que aconteceu aqui é exatamente a explicação do porquê comparar dois *arrays* não dá *true*. 

Existe uma versão do *array* que é a primeira que carregamos e que aquela função salvou na memória, em algum lugar do JavaScript. Nas outras vezes em que o React foi reexecutando a função, o nosso "escutador" só gerou na primeira vez. Ele não sabe o que aconteceu depois com esse valor, porque o React sempre está gerando um novo valor, sempre estamos gerando um novo *array*. 

Isso exige um pouco mais de conhecimento da linguagem, mas quando temos a base da linguagem, caímos em um *corner case* e pensamos no motivo dele ter acontecido: existe *arrays*, cada um com uma referência, o React sempre gera um novo, guardou a primeira referência e não a última. Desta maneira, conseguimos ter um domínio maior do que está acontecendo. 

**Paulo:** Perfeito. Agora, poderíamos abrir a outra tela e mostrar que com o login do Paulo também conseguimos escrever. 

**Mario:** Certo, vamos duplicar a página do Chat, fazer o logout, apertar "Inspect" para que a página e Console fiquem dispostos lado a lado. Preencheremos o campo de login com "peas", em seguida, apertaremos o botão "Entrar" para acessar o Chat. 

**Paulo:** Agora temos duas abas de Chat. O Paulo entrou e pegou as mensagens do Mario. Tudo que escrevemos no Chat com o login do Paulo, em teoria, na hora em que chegar no `supabase`, o React saberá que alguém inseriu e que existia uma pessoa fazendo *subscribe* nesse mecanismo de mensagem, *publisher-subscriber*.

No mecanismo de mensagerias o termo *subscribe* é comum, quer dizer que "eu quero ouvir essa fila de mensagens/acontecimentos". 

**Mario:** Eu escrevi no campo de mensagens "Tudo que eu escrever aqui óh! Em teoria ele aciona na hora que chega lá no supabase ele vai ver que alguém inseriu e tinha alguém fazendo subscribe... esse lance de Pub e Sub", apertei "Enter". 

**Paulo:** A mensagem que você escreveu apareceu no Chat em que eu estou logado. Vamos até o Chat que está com o seu login. 

**Mario:** A mensagem apareceu também. Agora você "*deployar*" isso na Vercel e compartilhar o seu sistema do Aluracord no Discord - é um metaverso - para que possamos comentar, conversar com você, criar um Chat real, enfim, as pessoas perceberão que você foi além do *sticker* e tem *upload* de áudio e muitos outros elementos. 

Nós fizemos um ótimo projeto, um "projetaço" envolvendo *Back-End as a service*, estudando os *uses*, *router*, *effect*, *state*, que é o que você usará no dia a dia do Next.js e React. Estamos, de fato, estudando conteúdos que são úteis no nosso cotidiano e com muitos detalhes.

A parte em que mais copiamos e colamos foi a do CCS, para que ficasse mais bonito, o resto nós fizemos do zero. Pegamos um componente do Mario, analisamos, alteramos, criamos o nosso *listener*, fomos muito além. 

Estamos chegando ao final da Imersão. Acho que foram cinco aulas incríveis. Gostaria de reforçar o convite de que, até a segunda-feira, você faça os projetos. Nós queremos ver os melhores! Na segunda-feira, durante a live das 18h30, nós mostraremos os projetos incríveis que encontramos. Quem sabe não chamamos alguém para contar um pouco do projeto. 

Também falaremos da nossa formação Next.js nova, sobre o andamento dela, o que o Mario está trazendo, "linkaremos" com a formação React que tem **Bugan** e outros instrutores, também relacionaremos com a formação JavaScript para Back-End que está sendo lançada na Alura. 

Enfim, temos um ecossistema completo de Node.js, Back-End, para quem deseja se tornar aluna/aluno. Mas não se matricule hoje na Alura, porque teremos um desconto na segunda-feira e durante a semana para quem participou da Imersão. Temos muitas novidades esse ano. 

Se você chegou ao final de semana com o conteúdo completo, que sabemos que é muita coisa, tem um vídeo hoje, sexta-feira, no canal do **Dev Soutinho**, em que ele discute um pouco mais *subscribe* e *unsubscribe*. 

Também discute sobre a possibilidade de nos conectarmos ao Back-End de outra pessoa com o nosso Front-End e analisar se o nosso com o de outra pessoa, que é completamente diferente, se integram minimamente e temos uma API em comum. Algo assim. O Mario mostrará nesse vídeo o que é possível fazer para ir além desse projeto do Aluracord que está muito bacana mesmo!

Estou muito feliz em ver o que você está trazendo, acompanhar as discussões no Discord e por ajudarmos as comunidades de Next.js e React, "fazer barulho" com o fundador da Vercel e com o fundador do Supabase. Esse momento de uma Imersão da Alura é incrível, nós teremos outras em diversos modelos e assuntos, porque desejamos expandir o Aluraverso e trazer você para ele. 

**Mario:** Perfeito, Paulo! Acho que isso mesmo! Nós estamos sempre trazendo muitos conteúdos e te convidamos a interagir conosco, sugerindo, inclusive. Nós queremos te ouvir para conseguir trazer conteúdos bacanas e, a partir dos *feedbacks*, ir moldando a Imersão para que ela aconteça de acordo com o que vocês acham que seria interessante ter. 

Nós sabemos o que queremos trazer, mas sempre podemos somar elementos à nossa visão. Queremos fazer tudo em conjunto e que vocês sejam parte do Aluraverso. 

**Paulo:** Até a próxima Imersão! Até a live de segunda-feira, 18h30. Tchau!! 

**Mario:** Tchau, tchau!!




