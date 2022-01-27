**Mario:** Olá, pessoas! Sejam muito bem-vindos e bem-vindas a nossa quarta aula da Imersão React da Alura. Essa edição está espetacular. Eu nunca vi tanta gente feliz de estar recriando o seu Discord.

As pessoas têm o Discord e agora estão empolgadas. "Agora quero fazer *real time*, quero a mensagem em tempo real". Chegaremos lá nesta aula.

Paulo, o que você tem para hoje? Como estão suas expectativas? O que está achando? Conte-nos.

**Paulo:** Estou animado, Mario. Estou um pouco chateado porque esqueci de passar o desafio ontem, não sei se você vai passar, o desafio para colocar stickers. Já tem pessoas pedindo para colocar stickers no site com transparência. Se precisa colocar URL ou um botão.

Terá esse desafio?

**Mario:** Vou dizer que hoje já é possível colocar sticker. Até porque passamos vários stickers, até os da Alura, que agora lançou o pacote de stickers.

**Paulo:** Tem o link na descrição do vídeo.

**Mario:** Tem o link na descrição do *config JSON*.

**Paulo:** Do WhatsApp, do Telegram.

**Mario:** No fluxo das aulas, o sticker será para coroarmos o projeto e finalizarmos amanhã com um design bem bonito.

**Paulo:** Ok.

**Mario:** Já é possível fazer com o que temos hoje, só ajustarmos o componente da lista de mensagens, mas amanhã será nossa coroação. Inclusive com dicas de como estender esse projeto, como o Slack faz algumas funções e lógicas dos programas.

Está bem bacana e esperamos vocês amanhã com essas dicas.

**Paulo:** Mario, hoje eu vim com a minha camiseta do Github e você com a sua, certo?

**Mario:** Estou com a minha aqui, mas o microfone atrapalhou que eu mostrasse agora.

**Paulo:** Não é possível ver, mas no meu notebook também tem o adesivo do Github.

**Mario:** Eu tenho a Mona em cima da minha estante.

**Paulo:** Olha só! Eu tinha um também, mas quebrei o meu bonequinho.

Hoje começaremos a fazer integração com Back-End, certo?

**Mario:** Certíssimo.

**Paulo:** E melhor ainda: sem escrever Back-End, porque usaremos sistemas relacionados a uma forma mais independente de trabalho, sem ficar esperando o Back-End para realizar alguma tarefa por não saber os mecanismos que se deve usar.

Existem mecanismos que podemos usar até para não escrever uma parte de Back-End se o seu sistema é menor.

**Mario:** Vou falar, para esse ano, de lançar uma vez por mês, ou a cada dois meses, um mini-app, que terá versão web e versão app, com coisas do canal. Eu vou usar o ano inteiro os conteúdos que estamos trabalhando aqui.

Tenho testado nos últimos meses e eu achei sensacional a praticidade para usar essa estrutura e das facilidades para integração. Estou realmente apaixonado nessa ferramenta.

Eu poderia fazer o Back-End, sei como fazer por ter trabalhado por um tempo, mas essa ferramenta me dá mais tempo para eu focar nas atividades do canal e no Front, que é o conteúdo principal que estou apresentando, ajudou demais! Será incrível fazer esse teste.

Eu vou apresentar minha tela agora para comentar que esse curso está totalmente relacionado com o **dev em < T >**, que falamos nas primeiras aulas e faz muito sentido agora.

Estamos bastante focados em Front-End, mas o Back-End está bem próximo. Eu até brinco que quando você termina de aprender HTML, CSS e Javascript, e já estudou o protocolo *http*, você está no meio termo entre Front-End e Back-End. Porque é necessário entender como realizar uma chamada e quais são suas requisições.

Entender isso ajuda no Front, na performance e em vários outros focos, que deixaremos até materiais extras na descrição para vocês. Tem um vídeo no meu canal explicando porque o site fica lento, sobre latência e várias outras coisas.

Tudo isso se interliga. O Front-End é uma parte que, quando você expande para outras áreas, terá mais conhecimento e **autonomia**. Autonomia é a palavra-chave do dev em < T >.

**Paulo:** Isso mesmo. Sem ter medo de Back-End, de Figma e de Cloud. Claro que, se sua carreira for de Front-End, você se especializará em React, Javascript, Next, Chrome, além de entender as ferramentas de *debugger* do Chrome, Safari e outros navegadores, sendo essa parte a que você mais investirá tempo.

Contudo, você não pode esquecer que trabalha com um time. Então agora que conheceremo uma API de Back-End, entenderemos como funciona a quantidade de mensagens, como os dados vão e voltam e como devemos nos comunicar.

É muito importante que a equipe inteira esteja em sintonia, e o dev em < T > é sobre isso, sermos especialista na nossa área, neste caso Front-End, mas sem deixar de ser um pouco generalista em outras áreas de tecnologia. Isso faz com que pensemos mais longe e sermos autocríticos em relação aos cuidados que tomamos com nossos colegas de outras áreas.

**Mario:** Perfeito, Paulo. Acho que fechou bem.

Vamos começar a entender isso na prática, e acabar com o medo, trabalhando no código do nosso chat, que por enquanto não tem nenhuma mensagem geral. Basicamente só carregamos o chat, vemos os `console.log` e, quando enviamos a mensagem, temos a nossa homenagem à Vanessa, mas faltou rodarmos algo mais integrado.

Para começarmos, a ferramenta que utilizaremos é o "<a href="https://supabase.com/" target="_blank">supabase.com</a>". O ***supabase*** é uma ferramenta chamada de "BAAS", que significa *"Back-End As A Service"*.

**Paulo:** Então já existe esse termo.

**Mario:** Sim. É algo cada vez mais comum porque começaram a surgir muitas startups de pessoas que trabalham com Front-End, mas às vezes a empresa não tem alguém de Back-End para criar a estrutura  da WS, ou um pessoal de Infra para montar tudo. Então essas ferramentas ajudam a ter agilidade para realizar esses processos.

Caso não tem dinheiro para montar um time, ou está criando uma ideia do zero, é possível, com os conhecimentos de Front-End, criar rede, modelar estruturas e criar uma estrutura base. Com o tempo, claro, pode não atender, mas possibilita autonomia para ao menos testar as ideias e validar as funções.

Então caso você se depare com um *corner case*, é possível entender como chegou nele, como melhorar e assim por diante. No caso, para quem conhece um pouco de Back-End e usa o famoso banco de dados **Postgres**, o pessoal gosta bastante de trabalhar com ele, o **supabase** é uma ferramenta *Open Source* alternativa ao **Firebase**.

É possível trabalhar com o Firebase, da Google, mas uma coisa que não gosto nele é o processo de criar o *setup* inicial. Veremos que o supabase não é muito complexo, basta ter uma conta do Github, clicar no botão *"Start your project"*, no canto superior direito da página, e criaremos o *setup* base.

Lembrando que trabalharemos com o exemplo base. Passaremos documentações e materiais complementares para vocês se aprofundarem, e a curiosidade guiará vocês até onde quiserem chegar no uso dessa ferramenta.

Então, Paulo. Você tem algo a acrescentar nesse ponto ou podemos começar a criar a estrutura?

**Paulo:** Vamos começar. Eu só quero entender o que queremos do nosso Back-End. Ele será apenas um repositório que recebe mensagens? Guarda na *array* e devolve?

**Mario:** Exatamente, Paulo, você disse isso muito bem. Ele será literalmente a `[]` em `const [listaDeMensagens, setListaDeMensagens] = React.useState([]);` . A diferença é que salvaremos em um servidor remoto, ou seja, em uma máquina fora do Front-End do navegador, que fornecerá todos os mecanismos para sincronização.

Então eu posso acessar o seu chat, você pode acessar o meu, e conversaremos por mensagens.

**Paulo:** Entendi. Nesse caso aparecerá mais usuários além da "vanessametonini".

**Mario:** Exato.

**Paulo:** Esse *Back-End As A Service*, como o Firebase, o supabase e outros, vão além dos repositórios que parece apenas um pequeno banco de dados. Eles fazem coisas a mais, correto? Eu consigo criar scripts dentro deles ou não?

**Mario:** Eu usei mais a parte de banco de dados deles, mas se eu não me enganos tem um recurso para você criar "lambdas", que são mini-servidores. Tem o link para vídeos no meu canal explicando sobre lambdas, mas são, basicamente, mini-servidores que, quando mandamos uma inquisição, eles devolvem algum resultado.

Por exemplo, o supabase tem um método de autenticação, que não chegaremos a estudar, porque levaria mais algumas aulas para entendermos o conceito. Faremos uma autenticação mais simples e simbólica, para mostrarmos esse processo.

Contudo, o supabase fornece toda parte de autenticação, é possível criar alguns scripts. Ele também oferece várias estruturas, por padrão, para conseguirmos criar várias tabelas e descrevermos os dados, como em um Excel.

Temos dados de nome, CPF e quantos mais quisermos. Deixamos esses dados salvos no banco e enviamos para ele via API. O mais legal é que, baseado no que descrevemos na interface desses bancos, eles já fazem toda validação. Então se mandarmos um dado errado, seja maior, menor ou de outro tipo do que o Back-End espera, esse dado é validado para nós. É bem produtivo trabalhar com o supabase, eu gosto bastante. 

Vamos começar a entender essas questões na prática. Clicando em "Start your project", somos direcionados para outra aba, que pedirá para realizarmos o *sign in* com o Github.

Então precisamos apenas da conta no Github, que você pode criar após ler e autorizar os termos. O Github enviará uma confirmação por e-mail e, após isso, você pode usar sua conta para logar no supabase, clicando no botão *"Sing In With Github"*.

É legal falar, Paulo, que todo o sistema que estamos criando está próximo. Por exemplo, na última conferência da Versell, a empresa por trás do Next.js, usou o supabase para realizar algumas interações em tempo real com quem estava assistindo.

O pessoal do Next.js também tem exemplos de como usar o supabase. A comunidade é bem próxima, no sentido de criarem juntos e interligarem as funcionalidades.

Quando fizermos login no supabese, seremos conduzidos para a *Home* do projeto. Eu tenho até um teste que fiz, nomeado "alura-test". Basicamente o que faremos é um novo projeto para armazenarmos as mensagens do **Aluracord** do Matrix.

Clicaremos no botão *"New Project"*,na parte superior da página, que pedirá para colocarmos uma organização. Normalmente o nome de usuário do Github será uma organização, então basta clicar sobre ele. A janela seguinte pedirá informações gerais do projeto que estamos criando.

O primeiro campo é para nomearmos o projeto, que será "aluracord_matrix' e, em seguida, ele pede uma senha forte. Precisamos ter cuidado para não perdermos essa senha, porque ela será necessária em alguns momentos. Eu tenho uma senha pré-definida, que inclusive está salva aqui no Chrome.

O supabse informou que minha senha é bem forte, mas coloque uma que você consiga lembrar. De preferência, não coloque a senha do e-mail ou de alguma rede social, crie uma senha só para isso. Agora virou uma aula sobre segurança de senhas, mas enfim, colocando o nome e a senha, não precisamos nos preocupar com mais nada, basta clicarmos no botão *"Create new project"*, no canto inferior direito da página.

Estou explicando com calma para você que está em casa não se perder. Temos o passo-a-passo para você conseguir acompanhar.

A criação do projeto demora um pouco porque, um pouco acima do botão que clicamos, temos a informação *"East US (North Virginia)"*, ou seja, Virgínia do Norte, nos Estados Unidos. Isso significa que ele está criando um servidor para conseguirmos acessar os códigos que trabalharemos, portanto, ele faz uma certa configuração para trabalharmos.

Enquanto isso, Paulo, é legal retomarmos o assunto sobre o conceito de coletar as mensagens de um servidor que está em outro lugar. Uma coisa que lembrei agora é que podemos abrir o <a href="https://github.com/" target="_blank">site do Github</a> e a <a href="http://api.github.com/user/omariosouto" target="_blank">página com a API</a>.

Então, Paulo, esclarecendo enquanto nosso servidor está sendo criado, todos os sites e apps atuais têm as informações armazenadas em algum computador de algum lugar do mundo, onde estão guardados os dados com o meu nome, meu usuário, o *read me* e as demais informações. Tudo isso fica armazenado em algum lugar que acessamos via URL.

Inclusive tenho uma imagem, que gosto bastante de usar, de um <a href="https://medium.com/@omariosouto/entendendo-como-fazer-ajax-com-a-fetchapi-977ff20da3c6" target="_blank">post</a> que expressa bem como gosto de falar desse assunto.

Então pensa que será essa imagem.

![No canto superior esquerdo há logos de vários navegadores. Delas sai uma seta apontando para um banco de praça com dois dados de seis faces em cima dele, representado o banco de dados. No meio dessa seta há o link fictício "https://meusite.com". Saindo do banco de dados, há uma seta apontando de volta para as logos de navegadores. Nela há os símbolos do Node.js, Java e PHP](https://miro.medium.com/max/3000/0*OWmh5tFwe13FhM_v)

Toda ver que usamos qualquer app no dia-a-dia, seja Android, IOS ou pelo navegador, acessamos através de uma URL que pede um conteúdo de um banco de dados. Esse conteúdo será trazido para o servidor e depois para o seu navegador. O Github não é diferente. Ele extrai as informações da URL <a href="https://api.github.com/" target="_blank">api.github.com</a> e monta elas em uma *array* de objetos, através do Javascript , para exibir a tela de usuário.

Então a mesma estrutura de objeto do link da api, temos no nosso código. Quando observamos o objeto, ele é o que estará trafegando pela rede. É importante termos a clareza que, principalmente no Javascript, o *array* do objeto, que chamamos de JSON, sendo esta a notação de React no Javascript, é muito próximo do que teremos em uma URL de API.

Tanto que se copiarmos o código da <a href="https://api.github.com/" target="_blank">api.github.com</a>, abrir o *Inspect* e colar no console, mostrará como se fosse um objeto válido. Teremos a *string*, os números, o e-mail e os demais dados. Então ele realmente é muito bom em converter de uma coisa para outra.

Veremos agora, Paulo, como fazer para acessar esses dados a partir de outra página.

**Paulo:** Você quer fazer um *http get* para coletar o JSON e usar essa informação em algum lugar.

**Mario:** Isso.

**Paulo:** Porque esse será o ponto inicial. Depois extrairemos do supabase. Por enquanto extrairemos do Github que está bem evidente.

**Mario:** Eu gosto de fazer isso para deixar claro que não tem magia. Às vezes vamos usar alguma função e tudo mais. Como esse Supabase é mais esperto, ele vai nos dar algumas funções dele para pegarmos os dados. Mas, na prática, é a mesma coisa que estamos fazendo aqui, depois mostrarei passo a passo para vocês.

Agora vou pegar essa URL https://api.github.com/users/omariosouto e quero ter acesso aos dados dessa URL na página do nosso chat. Como fazer isso?

Aqui no console do navegador, pode ser no código do projeto também, sem problema. Vou escrever no console do navegador: `fetch('https://api.github.com/users/omariosouto')` , esse `fetch` é uma função do navegador, se passarmos uma URL para ele e pressionarmos "Enter", ele traz a promessa (*promise*) de que vai tentar pegar esse dado e fazer alguma coisa com ele.

Como assim promessa? É promessa porque quando rodamos esse código, o navegador dispara uma chamada para tentar abrir essa URL. Como podemos ver na aba Network, não tinha nada e ao rodarmos esse código ele tenta pegar as mensagens via rede. Repare que o *status code* deu "200", ou seja, ele conseguiu pegar.

Nós ainda não vimos, só vimos a promessa. Esse "200" indica que ele conseguiu, por mais que não tenhamos visto no código.

Podemos consultar o site <a href="https://httpstatusdogs.com/" target="_blank">HTTP Status Dog</a> para verificar o que significa esse "200". Ele é um status para sabermos se alguma chamada deu certo ou deu errado. No caso, o "200" significa "OK", deu certo.

Cada um desses números, que vemos na aba Network, vai dar alguma dica do que aconteceu com a chamada que fizemos.

Para pegar aquele conteúdo JSON, estamos literalmente acessando essa URL, mas em vez de ser via navegador, estamos acessando-a via JavaScript.

Agora podemos complementar o `fetch` com um `.then` para dizermos: "fetch, tenta pegar e, então, quando você tiver alguma resposta me fala o que aconteceu":

```
 fetch('https://api.github.com/users/omariosouto')
 .then((respostaDoServidor) => {
   console.log(respostaDoServidor);

})
```

Passamos o `.then`, que é o "então" e passamos uma função que vai receber a `respostaDoServidor`. E podemos fazer um `console.log()` para a `respostaDoServidor`. Ao executarmos, ele traz várias informações:

```
Response {type: 'cors', url: 'https://api.github.com/users/omariosouto', redirected: false, status: 200, ok: true, ...}

body: ReadableStream
bodyUsed: false
headers: Headers {} 
ok: true
redirected: false
status: 200
statusText: ""
type: "cors"
url: "https://api.github.com/users/omariosouto"
```

Entre elas o `status: 200`, informando que deu certo, e esse `body: ReadableStream`. Isso é outra coisa legal de comentar, esse `ReadableStream` é porque tudo o que baixamos na internet vem de pedaço em pedaço, esse "*stream*" é o mesmo conceito do filme que você assiste na Netflix ou algo do tipo. Você nunca pega de uma vez, sempre vai pegando de pedacinho por pedacinho, isso acontece mesmo que seja texto.

Então, não basta nos informar quando tiver a resposta, além disso, temos que pedir para ele convertê-la baseando-se nesse JSON que ele está recebendo. Queremos convertê-lo para JSON, vamos adicionar um `.json` no `console.log(respostaDoServidor)` e essa conversão também é uma promessa.

```
 fetch('https://api.github.com/users/omariosouto')
 .then((respostaDoServidor) => {
	   console.log(respostaDoServidor.json());

})
```

Reparem que agora ele retornou duas linhas com `Promise {<pending>}`. Ele vai ter que esperar chegar cada um dos pedaços, juntá-los e gerar o objeto para nós. Para isso dar certo vamos inserir um `await`, para pedir que ele espere essa resposta.

```
 fetch('https://api.github.com/users/omariosouto')
 .then((respostaDoServidor) => {
	   await respostaDoServidor.json();

})
```

Agora, se eu só pressionar "Enter", ele retorna um erro dizendo que o `await` só é válido dentro de uma `async function`:

> Uncaught SyntaxError: await is only valid in async functions and the top level bodies of modules.

Então, ao invés de só colocar o `await` temos que informar que a função a que ele pertence é `async`. Assim o JavaScript consegue relacionar as duas coisas e fazer acontecer. Em seguida, podemos salvar esse resultado em uma variável `respostaEsperada`.

```
 fetch('https://api.github.com/users/omariosouto')
 .then(async (respostaDoServidor) => {
   const respostaEsperada = await respostaDoServidor.json();
   console.log(respostaEsperada);

})
```

Executar o `fetch` faz ele retornar a promessa, ou seja, a promessa está acontecendo ali. Em milissegundos ele traz a resposta esperada. Com isso, temos o conteúdo da URL que passamos no `fetch`.

Fizemos o JavaScript acessar uma URL que bateu no banco de dados, que bateu no servidor de novo, e trazer esse conteúdo para nós via a URL da API do GitHub.

É exatamente isso que o Supabase faz, o Supabase será um meio de campo que nos ajudará com esse trabalho.

**Paulo:** Só para eu entender, esse `fetch` é uma API que todo navegador tem, porque ele é oficial dos navegadores. O `fetch` está na documentação do Mozilla, isso não é React e não é Next, todo navegador tem. É uma forma de ir buscar informações que estão em outro site no nosso front-end.

Tem uma série de detalhes aqui, de programação assíncrona, que obviamente não é o foco da Imersão, mas são fundamentais. Você pode estudar sobre isso nos vídeos do Mario, nos cursos da Alura dentro das formações de JavaScript.

Não precisa se aprofundar nisso agora. Agora queremos só pegar a informação que está no GitHub e guardar em um objeto JSON. É isso que o Mario passou, mas com o tempo você precisa entender isso com profundidade, é fundamental para sua carreira. Concorda, Mario?

**Mario:** É isso mesmo. Isso é tão importante que tem dois vídeos no meu canal só falando sobre programação assíncrona. Já é um conteúdo a mais para você pegar, um só falando de *callback* - essa função que fizemos tem um nome no JavaScript, chama-se *callback* - ter clareza desses nomes e termos técnicos te ajuda muito a conversar com outras pessoas no trabalho e a propor soluções. É bom você saber esses nomes, o motivo de eles existirem e como tratá-los.

Agora, dá para fazer um atalho para dizer que o Supabase vai ter que nos dar uma URL e um jeito de ele saber que queremos bater no nosso banco de dados que criaremos lá. Faz sentido?

**Paulo:** Sim. Talvez seja na própria URL ou em algum parâmetro no POST, algo assim.

**Mario:** E tem um detalhe importante, que podemos ver aqui na aba Network, essas chamadas para o GitHub foram chamadas de GET, ou seja, "pega", `Request Method: GET`. Estamos pegando alguma coisa aqui. Existem outros tipos de chamadas, por exemplo, o POST para criar alguma coisa, o DELETE para apagar alguma coisa, o PUT ou PATCH para fazer atualização. Esses são os "verbos do HTTP", você dá essa dica na hora em que faz a chamada.

Veremos mais sobre isso em breve, mas é só para você entender isso que o Paulo comentou do POST. Por ora, voltaremos para a página do Supabase, que criou o nosso projeto "aluracord_matrix". E o Supabase exibe algumas chaves para trabalharmos, dessas chaves tem algumas que vamos pegar agora e salvar.

A primeira delas será na área de Project API Keys, a chave `anon public`. Vamos copiá-la e, por enquanto, vamos deixá-la no index do nosso código, no VS Code:

```
const SUPABASE_ANON_KEY = 'cole aqui a anon key que você copiou'
```

Isso é porque ele assume que você pode querer acessar de um navegador, igual vamos fazer aqui, sem ter algum back-end no meio, então ele deixa você ter esse `SUPABASE_ANON_KEY` aqui.

Outro dado importante está nesse Project Configuration, que é justamente a URL. Então ele tem uma URL para fazer o papel de servidor que vai receber a chamada e fazer alguma coisa. Vamos copiar a URL e colá-la também no nosso código:

```
const SUPABASE_ANON_KEY = 'cole aqui a anon key que você copiou'
const SUPABASE_URL = 'cole aqui a url que você copiou'
```

E cada URL vai ser diferente uma da outra.

**Paulo:** Lembrando a todos, nunca façam isso que nós fizemos, de mostrar chaves, por mais que seja brincadeira. Cuidado para não expor sua chave do Cloud, da Amazon, etc. Aqui estamos usando uma conta específica para a aula da Imersão.

**Mario:** Essa parte de segurança realmente é muito crítica, principalmente se for uma coisa que está atrelada ao seu cartão de crédito.

Não exponha nada que tem o seu cartão de crédito atrelado, porque podem fazer um estrago bizarro. Outra coisa: se um dia for praticar AWS, nunca deixe a máquina da AWS ligada, senão depois de um ano você vai descobrir que deve muito dinheiro para a Amazon.

Então, Paulo, o Supabase é legal porque ele tem vários recursos, tem tanto banco de dados quanto a parte de autenticação e a parte de *storage*. Dá para fazer uma Imersão só falando de Supabase. Para a nossa Imersão vamos usar essa parte de Database.

Basicamente, teremos que criar esse nosso array, `React.useState([])`, com todos os campos que esperamos que ele tenha, lá no Supabase. Os campos são: `id`, `de` e `texto`, como podemos ver aqui na `function handleNovaMensagem` que fizemos.

```
function handleNovaMensagem(novaMensagem) {
   const mensagem = {
	     id: listaDeMensagens.length + 1,
	     de: 'vanessametonini',
	     texto: novaMensagem,
	};
//...
```

Vamos começar a trabalhar em cima disso. Na home do site do Supabase, vamos clicar em "Table editor". Aí ele abre a página do editor de tabelas e informa que ainda não tem nenhuma tabela, vamos clicar em "Create a new table". Agora vamos preencher os campos, o nome da tabela pode ser "mensagens". Na descrição vamos escrever "Lista com todas as mensagens do nosso projeto maravilindo".

Logo abaixo, tem uma checkbox do "*Enable Row Level Security (RLS)*", como acessaremos tudo via front-end, via navegador, não vamos habilitar essa opção. Pois, para habilitar essa opção precisaríamos ter um back-end no meio, a estrutura seria mais complexa. Então, não habilitaremos.

Em seguida, ele tem esse botão "Import data via spreadsheet", você consegue criar a planilha e importar os dados aqui. Para a explicação usaremos a interface mesmo. Mas recomendo você explorar também essa funcionalidade.

Seguindo aqui na criação do banco de dados, teremos o campo `id` que será um valor inteiro, manteremos tipo "int8". Vou adicionar outro valor que teremos nessa lista que será o valor `de`, que é quem está enviando a mensagem. Quando você clica para selecionar o tipo ele tem várias coisas, podemos deixar o `de` como tipo "text".

É importante falar que nessa parte, mesmo sem saber banco de dados, você consegue usar o básico que estamos passando aqui. Claro que se você for expandir o projeto pode esbarrar em uma ou outra dificuldade, mas a documentação do Supabase é muito bem escrita.

E aí voltamos ao assunto do **Dev em T**. Você quer fazer uma coisa que vai além do front-end, ela pega um pouco do back-end. Isso exige que você busque conhecimento para se aperfeiçoar.

**Paulo**: Perfeito.

**Mario**: Passando aqui, vamos sair de `de` e vamos colocar o nosso `texto` da nossa mensagem de fato. 

**Paulo**: É válido lembrar que estamos usando aqui, mas não precisa bater exatamente os nomes. O nome você pode criar o seu. Só lembrando, né, Mario, se você que está fazendo conosco seguir exatamente essa especificação nossa do nome e etc, vamos conseguir usar o servidor um do outro e fazer uma brincadeira de que o Front End que criamos usa o Back-End do outro que reflete no Front-End de outra pessoa. É isso, Mario?

**Mario**: É, dá pra fazer isso tranquilamente. E fica até como um desafio pra galera tentar usar o servidor do outro, tentar aproveitar e tudo mais. 

**Paulo**: Tentem respeitar esse `created_at`, o `de` e o `texto` porque assim quem está um pouco mais próximo vai conseguir fazer coisas bem malucas. 

**Mario**: Perfeito, Paulo. Feita essa parte, clicamos em "Save" no canto direito inferior da tela. Ele sempre demora um pouquinho porque eles estão escrevendo no banco de dados de uma máquina na WS em algum canto dos Estados Unidos. ]

Criamos aqui. A primeira coisa que podemos fazer é clicar em "+ Insert row".  Assim se abrirá uma aba  "Add new row to". Aqui, o "id" será gerado automaticamente e o "created_at" já pega a data em que estamos. Notem que na última Imersão usamos bastante aquelas ferramentas de CMS, que são ferramentas que nos ajudam a gerenciar conteúdo. E por mais que isso seja um banco de dados que estamos mexendo, ele dá uma estrutura muito próxima dessas ferramentas de gerenciar conteúdo. Ele dá um campinho "spare" para você mexer com a data, tem um componente de calendários. Então, é bem espertinho aqui. 

No nosso caso, vou colocar a mensagem "de" como  "omariosouto" e o "texto" será "Olá, pessoas" e vou cadastrar. Está aqui! 

**Paulo**: Perfeito.

**Mario**: Essa primeira parte que fizemos está nos esquemas. 

**Paulo**: Mario, adiciona mais uma mensagem. Adiciona já outra mensagem porque quando puxar fica mais legal. Adiciona o "de" como “peas", que sou eu, e o "texto" pode ser "Olá, Aluraverso". Perfeito.

**Mario**: Certo. Temos o nosso chat! Paulo, chegou a hora de fazermos essa integração acontecer. Para isso, vamos precisar usar uma lib do pessoal do Supabase e vou mostrar como ela funciona debaixo dos panos.

Basicamente, vamos procurar no Google "npm @supabase/supabase-js", ou você também pode procurar por "GitHub", ambos servem. Você terá o link da lib do Supabase, que terá uma série de utilitários para facilitar a busca, a pegar as coisas, o modo de “real time” para as funcionalidades padrão e tudo mais.

Vamos copiar o nome "@supabase/supabase-js". Aqui, temos a documentação também. Além da url para copiarmos assim como a chave pública. Tudo friamente calculado para ganharmos tempo. 

Voltamos ao nosso VSCode, abrimos o terminal, paramos o projeto e rodamos `yarn add @supabase/supabase-js` e damos um "Enter". Lembrando que rodamos o `yarn` porque estamos usando ele no projeto, se você usar o `npm` vai ter que usar o `npm install @supabase/supabase-js`. 

**Paulo**: Mario, eu aposto que o que essa biblioteca faz é um monte de fetch(). Ela já sabe qual o endereço do Supabase, sabe qual o parâmetro de chave e já verifica se deu erro... Eu aposto que daria pra fazer usando o `fetch()`, o `await()` e o `async()` que você nos mostrou. Porém, essa biblioteca já deve facilitar de alguma forma. 

**Mario**: Vou até tentar fazer na mão aqui. Pode ser que dê algo errado, mas vamos tentar. Eu tentei fazer uma notação breve de como funcionaria, porque estava investigando esses tempos e é possível fazer. Mas eu gosto desse lance, isso que você disse é a chave: sempre que formos usar alguma biblioteca é bom ter noção do que ela está fazendo, porque vamos  ganhando uma confiança de que sabemos o que está acontecendo no projeto sem a impressão de que está acontecendo mágica e os dados estão simplesmente aparecendo na tela.

Bom, instalou aqui, vamos agora e fazer  o `import { creatClient } from '@supabase-supabase-js'`. Depois,  embaixo de `const SUPABASE_URL`  escrevemos `const supabaseCliente`. Tem gente que vai deixar só `supabase`, mas eu gosto de deixar claro que tem o `Client`. Ela será igual a `creatClient()` recebendo a `SUPABASE_URL` e depois a `SUPABASE_ANON_KEY`.

```
const supabaseClient = creatClient(SUPABASE_URL, SUPABASE_ANON_KEY); 
```

**Mario**: Lembrando: Mario, onde estava isso? Pegamos esses valores dentro da Supabase, em  "Home > Settings > API", onde temos a chave pública, e o Config URL. 

**Paulo**: É muito comum quando vamos usar algum Back-End você ter a chave que você tem que falar para a pessoa ter certeza que é você. Essa chave fica em um arquivo de propriedades que não vai no GitHub, que é feita em um deploy automático... Tem uma série de regras de boas práticas de devotos. Aqui estamos realmente fazendo do jeito feio. 

**Mario**: Exato. É o jeito para conseguirmos fazer funcionar a ideia. E, claro, tem uma série de coisas... Tem até vídeo meu! Eu estou preparadíssimo, Paulo, depois de dois anos eu tenho muito vídeo. Tenho um vídeo dando dicas de como lidar com essa parte. O próprio Supabase tem as recomendações de segurança dele e os projetos de exemplo. Enfim, material não falta para vocês irem olhando e se especializando.

Então, Paulo. Depois de pegarmos esses dois valores, podemos pegar nosso `supabaseClient.` e ele já indica `.auth`, `.from`, entre outros. Neste caso, vamos usar `supabaseClient.from()`. 

O typescript no VSCode é uma maravilha porque ele deixa tudo autocompletar. No caso a lib do Supabase é feita com typescript e ele passa aqui. Qual a nossa tabela? Vamos voltar no Supabase em  "Table editor > All Tables" e copiar "mensagens", que é o nome da tabela. Em seguida colamos em `supabaseClient.from()`. 

Em seguida, adicionamos o que queremos fazer, se queremos deletar, pegar algo, escutar e assim vai. Nesse caso, queremos selecionar então `select()`. Aqui agora é tudo descrito, quais colunas você quer pegar e tudo mais. No caso, queremos pegar tudo, ou seja, `*`. 

```
supabaseCliente
	.from('menssagens')
	.select('*')
```

**Mario**: Lembrando: tudo isso é está na documentação do Supabase Client, que você pode pegar no GitHub. Agora vamos tentar salvar em uma variável `const dadosDoSupabase` e  finalizar com `console.log(dadosDoSupabase)`. 

```
const dadosDoSupabase = supabaseCliente
	.from('menssagens')
	.select('*')

console.log(dadosDoSupabase);
```

**Mario**: Carreguei a página! Opa, faltou subir o servidor com `yarn dev` dentro do VSCode, do terminal. Subiu o servidor de novo! 

Olha só, ele trouxe aqui um `chat.js?4cc9:14`. Ele trouxe um `PostgressfilterBuilder` que tem uma série de coisas meio diferentes, ele tem um `fetch`... Me parece que não foi muito bem aqui, Paulo, ele ficou meio solto. 

Isso porque esse `dadosDoSupabase` espera ser chamado com essa lógica de esperar, ele faz o `fetch`... 


**Paulo**: Assíncrono. Ainda não está pronto, aquilo lá ainda não está pronto. 

**Mario**: Isso. É possível ir no `const dadosDoSupabase` e mandar o `.then()` recebendo `(dados)`. E `console.log()` recebendo `'Dados da consulta:'`.

```
const dadosDoSupabase = supabaseCliente
	.from('menssagens')
	.select('*')
	.then((dados) => { 
		console.log('Dados da consulta:');
	});
```

**Mario**: Salvamos e carregamos a página. Agora ele traz para nós o `body` da resposta, o `count`, os dados que temos cadastrados, ou seja, as duas mensagens. E por fim, traz o `status`, ou seja, as mesmas coisas que vimos lá do código de antes ele está nos trazendo mas encapsulado e pronto para usarmos. 

Se olharmos na aba "Network", quando carregamos a página está acontecendo uma chamada para a URL que definimos em nossos valores de `SUPABASE_URL`. Ele está pegando os valores, fazendo as mensagens, os selects e tudo mais. Então, essa URL que está fazendo aqui podemos até pegar do código que tínhamos separado...

**Paulo**: E fazer o `fetch()`, né? E colocar lá na internet se você quiser, no Browser. 

**Mario**: No Brownser dá um pouquinho mais de trabalho porque ele tem algumas configurações extras. 

**Paulo**: Ele tem um `GET` mas tem parâmetros, né, no "Headers"?

**Mario**: Isso. Ele passa um cabeçalho fazendo a autenticação aqui. 

**Paulo**: Quem quiser pode usar o tal do Postman para brincar?

**Mario**: Sim. Para ter uma ideia de como estamos encurtando o caminho, esse código abaixo seria o código sem a lib. 

```
fetch('${SUPABASE_URL}/rest/v1)/messages?select=*', { 
	headers: {
		'Content-Tyoe': 'application/json',
		'apikey': supabaseAnonKey,
		'Authorization': 'Bearer ' + supabaseAnKey,
	}
})

.then((res) => { 
	return res.json();
})

.then((response) = > {
	console.log(response);
});
```


**Mario**: Aqui teríamos o código com `fetch()` que é pegar a URL, bater nessa URL `rest/v1/messages`. A chave anônima `SUPABASE_ANON_KEY`. A parte `apikey` e `Authorization` são padrões. `apikey` é o Supabase que usa e esse `Authorization` é meio padrão do mercado. O `Bearer` avisa que você está usando tal token e tudo mais. E esse token, pessoal, pensem nele como se fosse um crachá. Você tem um crachá para entrar em um prédio, o token tem justamente esse papel de identificador. 

Depois temos a resposta convertida para `json()` e o `console.log()` pegando ela ali por fim. Aqui de uma forma diferente do que havíamos feito do async/await, mas a lógica é a mesma. Em uma `promisse` sempre que você retorna um valor você pode continuar trabalhando com ele. Paulo, acho que para essa aula, ficou faltando só... 

**Paulo**: Deixa eu ver o console, Mario? 

**Mario**: Aqui. 

**Paulo**: Clica lá no `data` e `0`... Pronto, aí temos `omariosouto` e `peas`. Então, agora estamos usando a api, né? A biblioteca que instalamos agora nosso projeto de React, as ferramentas do npm, Node, etc, vão saber baixar essa biblioteca e colocar para nós. Essa biblioteca facilita o trabalho para o Supabase. Se fossemos usar o Firebase, teríamos uma biblioteca para ajudar. Se fossemos usar outras coisas, teríamos uma outra biblioteca para ajudar. Normalmente é possível usar "na unha", como o `fetch()`, mas no dia a dia as pessoas usam bibliotecas que deixam o trabalho mais simples e mais claro. 

**Mario**: Outra exemplo disso é, por exemplo… Ele bate em `rest/v1` e pode ser que no futuro eles deixem de dar suporte para esse `rest/v1` e se você espalha esse URL no seu código, quando mudar a versão você vai ter que mudar no código todo. 

**Paulo:** Agora o que nos falta é, ao invés inserirmos os dados e codar `console.log`, temos que buscar essa mensagem com o `listaDeMensagens`, chamando o `setListaDeMensagens` para ser o `(dados)`, certo?
 
**Mario:** Paulo, você disse com precisão.
 
Esse código estará no exemplo para vocês. Então eu vou apagar os comentários, ou serão muitos e ficará uma bagunça.
 
**Paulo:** Perfeito. E eu vou pedir para você aumentar mais um pouco a fonte.
 
**Mario:** Beleza.
 
Vou fechar a aba *"Explorer"* e apagarei os comentários que estão antes do `function handleNovaMensagem(novaMensagem){}`. Podem manter no de vocês. Estou apagando porque, para explicação, o código fica muito grande.
 
Então temos o código do `supabaseClient`. Se cortamos ele do código e colarmos dentro do `export default function ChatPage() {}`, tomando o cuidado de arrumar a identação, notaremos no console que ele continuará chamando as informações do servidor.
 
```
export default function ChatPage() {
           	const [mensagem, setMensagem] = React.useState('');
           	const [listaDeMensagens, setListaDeMensagens] = React.useState([]);
           	
           	supabaseClient
                          	.from('mensagens')
                          	.select('*')
                          	.then((dados) => {
                                        	console.log('Dados da consulta', dados);
                          	});
```
 
Contudo, olha que surpreendente, cada letra que digitamos é mandada para o Back-End. Então eu te pergunto, Paulo, faz sentido cada letra ir para o Back-End?
 
**Paulo:** Não, precisa ser de tempo em tempo ou, quando enviarmos, recuperamos do servidor para saber se tem alguém. Existem várias opções, mas a cada letra fazer um *request* parece exagerado.
 
**Mario:** Exatamente. Tem esse ponto. Então lembra disso.
 
Um requerimento para cada interação é muito oneroso, tem um custo que pode até derrubar o servidor se muitas pessoas usarem ao mesmo tempo. É equivalente ao ataque DDOS. Se houver 100 usuários digitando e mandando a informação, é quase um ataque ao servidor. Então o que faremos para mudar isso?
 
O React executa repetidamente a função `supabaseClient` quando mudarmos o estado. Para resolvermos esse problema, Paulo, nos aprofundaremos no seguinte conceito.
 
Essa repetição do nosso código tem até um nome bonito, chamam de **"efeito colateral"**. É algo extra do nosso componente que, quando chega um dado externo, esse efeito dispara uma alteração do nosso código. Contudo, ele não faz parte do fluxo padrão, ou seja, a execução simples da nossa função. Esse trecho de código só precisa ser executado em determinado momento, coletando os dados e disparando uma nova execução.
 
Pensando nessa função como algo a parte do nosso código, que será executado apenas uma vez ou algo do gênero, o React, da mesma forma que tem o `React.useState()` , para lidar com estado, tem o `React.useEffect()` para lidar com tudo que foge do fluxo padrão do componente.
 
O fluxo padrão é a execução, ou seja, o ciclo de ter todos os valores do `return()` aparecendo. Se o dado chega de um servidor externo, demorando um pouco para acontecer, ele não faz parte do fluxo padrão, sendo um efeito colateral, um extra.
 
Então, Paulo, esclarecendo esses efeitos, ou seja, tudo que não faz parte do dado simples do componente, que não tem processos assíncronos, e precisa entrar em contato com o servidor, demorando um pouco mais para acontecer, utilizamos `React.useEffect` e passamos uma função.
 
Paulo, eu colocarei essa *array* vazia no final para não corrermos o risco de sermos bloquados, mas eu explicarei o porquê daqui a pouco. Vamos selecionar todo o código do `supabaseClient` e arrastar para dentro do `.useEffect` .
 
```
export default function ChatPage() {
           	const [mensagem,setMensagem] = React.useState('');
           	const [listaDeMensagens, setListaDeMensagens] = React.useState([]);
           	
           	React.useEffect(() => {
                          	supabaseClient
                                        	.from('mensagens')
                                        	.select('*')
                                        	.then((dados) => {
                                                       	console.log('Dados da consulta', dados);
                                        	});
           	}, []);
```
 
Dessa forma, isolamos o efeito de mandar para o servidor, informando para o código que a atualização ocorre no `.useEffect()` .
 
**Paulo:** O *chat page* não será renderizado toda vez, porque agora essa função está dentro de um comando que só será acionado em determinados casos.
 
**Mario:** Exato. Então, Paulo, quais são esses determinados casos?
 
Por padrão, o `.useEffect` roda sempre que a página carrega, ou seja, carregamos a página, ele roda. Se digitarmos, ele não é executado novamente. Caso queiramos que, em decorrência de um estado mudar, ele rode de novo, precisamos voltar no `[]` do final desse trecho de código, e informar que, caso a mensagem mude, ele deve observar a mudança e ser executado novamente, ou seja, escrevermos `[mensagem]` .
 
Salvaremos essa alteração e, ao recarregarmos a página, toda vez que mudarmos a mensagem ele será chamado. Contudo, não queremos que isso aconteça a cada alteração da mensagem, somente quando a `listaDeMensagens` mudar. Então trocaremos o `[mensagem]` por `[listaDeMensagens]` e salvaremos a alteração.
 
Ao recarregarmos a página, notaremos no console que o comando foi carregado, mas enquanto digitamos, ele não foi executado novamente. Ao apertarmos "Enter", o console mostra que os dados foram coletados e mandados para o servidor.
 
Beleza até aqui?
 
**Paulo:** Perfeito.
 
**Mario:** Conseguimos deixar claro essa parte do que está acontecendo com a coleta de dados. Agora, Paulo, sabendo que temos esses dados e o *array* está na seção `data`, só precisamos incluí-lo no nosso código.
 
```
supabaseClient
           	.from('mensagens')
           	.select('*')
           	.then(({data}) => {
                          	console.log('Dados da consulta', data);
                          	setListaDeMensagens(data);
           	});
}, []);
```
 
Mostrarei do jeito certo, Paulo, porque nessas variáveis que agrupam várias informações, o pessoal, normalmente, não usa direito, por exemplo, o props. Essas pessoas costumam apenas extrair o objeto `(dados)` e codam o que está vindo dele. Inclusive o *autocomplete* já ajuda nisso, sugerindo diretamente `.then(({data})` .
 
**Paulo:** Nossa!
 
**Mario:** E uma vez que temos o `.then(({data}))` , para encontrarmos o erro nas chaves pressionamos "Ctrl + Espaço" e a própria lib sugere quais as próximas coisas podemos colocar.
 
**Paulo:** Incrível, porque o `{data}` é a *array* com as mensagens que estávamos querendo, lembra?
 
**Mario:** Exatamente. Ela que aparece no console.
 
Salvaremos nossas alterações, que não tem mais nenhum objeto `dados` nesse trecho, apenas `data` . No chat observamos que ele extraiu essa informação. Temos as mensagens do "peas" e do "omariosouto".
 
Se deixássemos o `[listaDeMensagens]` no final do trecho do `supabaseClient`, ele acabaria sendo executado várias vezes, então é importante apagá-lo, ou seremos bloqueados. Isso acontece porque o `setListaDeMensagens(data)` acontece a cada atualização, então se colocarmos a `[listaDeMensagens]` no final, o código entenderá como uma mudança e rodará o *set* em *looping*.
 
Temos as mensagens, mas ainda não tem nossas fotos, porque no código ainda estão as informações da `vanessametonini`. Ao buscarmos o nome dela, no código, encontraremos o link da foto no `<Image/>` . Mudaremos o `src` da mesma forma que a *home*, para obtermos a imagem de quem está mandando a mensagem.
 
```
src={`https://github.com/${mensagem.de}.png`}
/>
```
Ao salvarmos o código e recarregarmos a página, teremos a exibição da foto de cada usuário que mandou a mensagem.
 
**Paulo:** Volta novamente no código, Mario. Antes do `{mensagem.de}` tem um **`$`**, porque está dentro de uma *string*.
 
**Mario:** Isso, é por causa da *string*, marcada pela crase dentro do nosso das chaves `src={``}` . No topo do código, escrevemos o `.useEffect` , que usa o `supabaseClient` para resolver essa parte do código.
 
Então, Paulo, já está carregando as mensagens, já está bonito de ver. E, Paulo, qual seria a última coisa que faltou nessa aula para conseguirmos ver, de fato, o impacto do que fizemos?
 
**Paulo:** Falta, quando digitarmos a mensagem, não aparecer só no local, mas ela ser enviada para o servidor, é isso?
 
**Mario:** Exatamente, Paulo.
 
**Paulo:** Porque agora fizemos um `select`, certo? Nós queremos
 
**Mario:** Poder enviar também.
 
Então no código temos `function handleNovaMensagem(novaMensagem) {}`. Olha que legal, nosso código começou a crescer, como você falou. No começo só alterávamos a lista, apagávamos um campo, depois tínhamos o objeto e agora temos mais uma responsabilidade, que é colocar a informação no servidor.
 
Dentro dessa `function()` , teremos que seguir, aproximadamente, a mesma lógica. Codamos o `supabaseClient` , que já está configurado com autenticação e os demais *setings* e no `.from` colocamos as mensagens.
 
```
           	supabaseClient
                          	.from('mensagens')
```
Colocamos essa parte direto no código, mas uma **boa prática** seria separar uma função apenas para coletar os usuários e outra para criar os usuários. Isso facilita os testes. Sabemos disso, mas para facilitar a explicação deixamos junto. Contudo, fica a dica de separar em funções menores e refatorar o código.
 
Em seguida colocamos o `.insert` , lembrando que quando apertamos **`.`** já aparece as opções de comando, e passaremos a `mensagem` . Fazendo isso, estará tudo certo.
 
 
```
           	supabaseClient
                          	.from('mesagens')
                          	.insert([
                                        	mensagem
                          	])
 
```
 
Nesse momento, Paulo, temos o detalhe que prefiro não usar o `id: listaDeMensagens.length + 1` que temos na `const mensagem = {}` , e sim o *id* que vem do servidor. Então colocaremos a linha do *id* atual como comentário, para não ser executada, e deixarmos o `setListaDeMensagens()` também como comentário, deixando apenas o `.insert([mensagem])` dentro do `supabaseClient` . No final colocaremos um `.then();` para sabermos quando teve a mudança e ver o retorno.
 
```
funcrion handleNovaMensagem(novaMensagem) {
           	const mensagem = {
                          	// id:listaDeMensagens.length + 1,
                          	de: 'vanessametonini',
                          	texto: novaMensagem,
           	};
           	
           	supabaseClient
                          	.from('mensagem')
                          	.insert([
                                        	mensagem
                          	])
                          	.then((oQueTaVindoComoResposta) => {
                                        	console.log('Criando mensagem: ', oQueTaVindoComoResposta);
                          	});
                          	
                          	// setListaDeMensagens([
                          	//	mensagem,
                          	//   	listaDeMensagens,
                          	// ]);
                          	setMensagem('');
```
 
Salvamos o código e carregamos a página. A Vanessa está como usuário e enviaremos a mensagem "Oi".
 
No console aparece o "Criando Mensagem: ". Expandindo esse retorno e, em seguida, expandindo a seção `data Array(1)` , teremos todo o perfil que queremos colocar na página.
 
Nos inspirando nessa informação, podemos alterar o `.then()` para `.then(({data}))` e arrastamos o `setListaDeMensagens` para dentro desse comando.
 
```
                          	.then(({data}) => {
                                        	console.log('Criando mensagem: ', oQueTaVindoComoResposta);
                                        	setListaDeMensagens([
                          		data[0],
           	           	   	listaDeMensagens,
                                        	]);
                          	
                          	});
```
 
Agora a `mensagem` do `setListaDeMensagem()` não será a diretamente do código, e sim do `data[0]` que, como vimos no console, com as informações que precisamos. Assim podemos fazer o *set* da lista novamente.
 
Na próxima aula melhoraremos esse código. Ele não é o melhor, existem formas melhores de fazer isso, mas temporariamente ele serve para fazer tudo funcionar.
 
**Paulo:** Volta no código. Eu quero ver novamente a função `novaMensagem` inteira para entender.
 
Então no chat eu recebo uma nova menagem como objeto, porque você me chamou. Quando apertam o “Enter”, eu recebo a mensagem, que cria um objeto. Esse objeto tem os campos, que, não por um acaso, são os mesmo do banco de dados do supabase. No supabase do código, eu informei que quero realizar um *insert*.
 
Então o *insert* se tornou trivial. Você, inclusive, colocou um comentário de que precisa ser um objeto com os mesmo campos.
 
```
.insert([
           	//Tem que ser um objeto com os MESMOS CAMPOS que você escreveu no supabase
           	mensagem
])
```
Para usar dessa forma, o data e o texto precisam ter os mesmo campos do supabase.
 
**Mario:** Exato.
 
**Paulo:** E pelo que entendi, ele já retorna o `select` de tudo, certo? Você colocou o `.then(({data})` e, com o `console.log`, você mostra `oQueTaVindoComoResposta` . Essa variável existe?
 
**Mario:** Essa não mais, é o que tinha antes no `.then()` . Podemos apagar e deixar apenas o `data` , ou seja, `console.log('Criando mensagem: ', data);` .
 
**Paulo:** Ok. E no `setListaDeMensagens()` colocamos o `data[0]` com o resto da mensagem.
 
Nessa parte não poderíamos fazer `setListaDeMensagens(data)` ? Já que estou coletando a informação primeiro e depois inserindo no código, não podemos trocar tudo por `data` ?
 
**Mario:** Se você trocar por `data` , ele devolverá apenas o que foi inserido.
 
**Paulo:** Só o que foi inserido!
 
**Mario:** Isso.
 
Salvamos o código e enviamos a mensagem "Teste 2" no chat. No console temos os dados do "Criando mensagem: ", que retornou apenas a nova mensagem.
 
**Paulo:** Entendi. Não tem jeito. Ficaria apenas com uma mensagem.
 
Perfeito, Mario. Agora quero recapitular outra coisa. Qual parte do código executa a atualização de mensagens para colocar na tela? O `.useEffect()` que atualiza? Ou agora só tem esse?
 
**Mario:** Aí está, Paulo. Ele só chama o `.useEffect()` na primeira vez que a página carrega.
 
**Paulo:** Então se alguém for no nosso banco de dados e inserir alguma informação, nossa tela não será atualizada enquanto não digitarmos uma nova mensagem.
 
Pode ser que neste instante eu esteja inserindo uma informação no seu supabase, mas se formos no chat, não estará atualizado, porque o React não fez esse *request*.
 
**Mario:** Exato. Perfeito, Paulo. Isso mesmo, não vai retornar.
 
**Paulo:** Ok.
 
**Mario:** Beleza, nosso código está funcionando, mas a ideia é, na próxima aula, aprendermos a integração mais eficiente, chamada pelas pessoas de *"web socket's"*. Sincronizaremos em tempo real, usando o supabase para facilitar o processo, com o Back-End, deixado mais a parte.
 
É legal vermos esses conceitos porque, com as informações que tínhamos antes, conseguimos apenas mandar novas mensagens e fazer com que elas apareçam. A lógica é essa.
 
No Front-End, dificilmente você pedirá constantemente as informações repetidas. A ideia dessas aplicações é pedir apenas o que mudou. Se o Back-End informa que algo mudou, você mostra a mudança e trabalha em cima do novo ao invés de coletar todas as informações a todo momento, porque isso tem custo. Custo de banco de dados, de rede, de transferência e de dados do usuário. Se o usuário estiver na rua, ele pagará mais caro por algo que você fez no seu código.
 
Temos um último ajuste, porque enviamos a mensagem "Teste 2" no final, mas quando recarregamos a página, ela vai para o topo, porque está vindo na ordem que o *array* estava. Temos que inverter a ordem desse *array*.
 
Voltaremos no `supabaseClient` .
 
**Paulo:** No primeiro.
 
**Mario:** Isso, o do `.useEffect()` . Após o `.select('*')`, incluiremos uma linha com o código `.order('id', {ascending: false}),` .
 
**Paulo:** Então você está usando isso porque sabe que a biblioteca do supabase tem um método chamado `.order()` , onde podemos passar um argumento com essa sintaxe.
 
**Mario:** Exato. Fazendo isso e recarregando a página, a mensagem "Teste 2" volta para o final. Se enviarmos a mensagem "Novo teste 3", ela aparecerá na parte inferior também.
 
Viu, Paulo? A atualização aconteceu corretamente, apresentando a mensagem no final do chat. Se recarregarmos a página novamente, a ordem se mantém.
 
**Paulo:** Perfeito. Poderia ser pelo *id*, talvez fosse até melhor pelo *create dat*, que é um data, mas é possível executar essa função de várias formas.
 
**Mario:** Isso, podemos fazer de várias formas.
 
**Paulo:** Fechado. Está lindaço.
 
**Mario:** Então, Paulo, nessa aula conseguimos ver toda essa questão de integração com os serviços externos, sendo a parte de trabalhar com o Back-End externo.
 
**Paulo:** Sendo fundamental não apenas no React. A parte de usar um Back-End, um Firebase, um supabase não é apenas no React. Precisamos disso o tempo inteiro.
 
**Mario:** Exato, vou até deixar o link para o<a href="https://medium.com/@omariosouto/entendendo-como-fazer-ajax-com-a-fetchapi-977ff20da3c6" target="_blank">post que mencionei</a> como comentário na linha 6.
 
Também aprendemos a debbugar, a partir da aba *network*, algo que esquecem muitas vezes. Então se der erro, é a aba *network* que informa o que está acontecendo. Se não estivermos autenticados, ou estivermos usando uma chave errada, qualquer coisa assim.
 
Por exemplo, se formo no `const SUPABASE_URL` e adicionarmos um "a" no link, nosso chat irá buggar e, imediatamente, o erro é indicado e explicado na aba *network*. Se retirarmos o "a" que colocamos na URL, teremos o link certo e a chamada funciona, constando o status 200.
 
Então usar a aba *network* para nos guiar é essencial e que, no Front-End, é o que mais será usado, a partir da sua evolução na carreira, para realizar atividades mais complexas.
 
Paulo, para essa aula, eu acho que é isso, então podemos passar os desafios para galera.
 
Eu tenho o meu, mas deixarei você passar o seu primeiro.
 
**Paulo:** Você primeiro, Mario.
 
**Mario:** Vou passar um bem tranquilo. Sabemos que a lista está vazia, e que enquanto ela estiver vazia, não temos nenhuma mensagem. Então podíamos mostrar um *loading* quando não temos mensagem para carregar.
 
**Paulo:** Enquanto o `.useEffect()` não passou, é isso?
 
**Mario:** Exatamente.
 
**Paulo:** Enquanto o `.useEffect()` não passou, queremos que, de alguma forma, aparece "Estamos carregando". Claro que ele piscará na tela, ficando pouco tempo, mas não fica a impressão de vazio e, em um segundo, aparece informação.
 
**Mario:** Isso. E eu desafio quem fará o *loading* mais criativo. Se, quem jogava em espanhol, será aquele *"cargando"*, se será um CD rodando, se colocará o rosto do Paulo rodando com os óculos do Morfeu e a logo da alura de fundo. Quero ver o que vocês farão.
 
**Paulo:** Acho que, o mais tradicional atualmente, seria mostrar algo que finja que tem escrito, mas não tem. Sabe quando você abre uma app e, enquanto carrega, todos os componentes estão opacos? Só para não dar a impressão que a tela está em branco.
 
**Mario:** Perfeito. Esse é com classe, mas quem quiser ir pelo lado da brincadeira, fica à vontade.
 
**Paulo:** O meu desafio é você fazer um mouse *over* na imagem da pessoa.
 
Sabe quando aparece a minha foto do Github, a do Mário e dos demais usuários? Está muito pequena. Então quando passar o mouse sobre a imagem, pode abrir o perfil da pessoa, aparecendo o rosto maior, o link para o Github da pessoa e outras informações vindas da API que aprendemos, do <a href="http://api.github.com/users/" target="_blank">api.github.com/users/</a> o nome do usuário, como "/peas".
 
Nessa página tem um monte de informações, então você pode mostrar quantos repositórios, o link para o perfil do Github, a foto um pouco maior e assim por diante. Talvez exista algum componente em algum lugar do React que abre essa janela e o mouse deixa você clicar, ao invés de precisar escrever no Javascript puro.
 
Meu desafio é esse. Não sei como resolver, mas tenho certeza que vocês terão ideias, componentes extras, certo, Mario?
 
**Mario:** Exatamente.
 
**Paulo:** Estamos deixando listas, além do *Material* e do *Why*, que tem vários componentes prontos e *CarNext*. Existem outras bibliotecas que você pode usar para criar o calendário e várias outras funcionalidades interessantes.
 
Mario, vou passar mais um desafio. Sei que você deixará os stickers para amanhã por vários motivos, mas além de mandar mensagens, e depois mandar sticker, podemos mandar *pool*, enquete e outras coisas que não sejam texto.
 
Então poderia ter outros botões além do "OK", para quem cumpriu esse desafio. Um botão para mandar *pool*, uma imagem, um anexo ou outras coisas.
 
No começo pode ser apenas os botões, mas quem quiser ir além. Lembram que no *Material* e no *Why* tem os componentes React? Tinha ferramentas de puxar, de *pool*, de componentes visuais de várias coisas. Provavelmente será mais fácil do que você imagina, o complicado será que, na nossa base de dados, qual será a mensagem que você colocará ali para realizar *upload*?
 
Esse desafio é bem complicado. Toma cuidado para não bagunçar muito o banco de dados.
 
**Mario:** Acho super válido, e aproveita para tentar debuggar. Olha no Github, as *issues*, usa o Discord para consultar as pessoas. Alguém tentará resolver isso. E olhar o código das pessoas pode te ajudar a aprender.
 
Aproveita que tem muitas pessoas fazendo a mesma coisa, porque fica mais fácil chegar a uma solução bacana e diferente.
 
Então, Paulo, por hoje é isso?
 
**Paulo:** Até amanhã!
 
**Mario:** Até amanhã, gente. A última aula, não pode perder. Será especialíssima para vocês.
Tchau!