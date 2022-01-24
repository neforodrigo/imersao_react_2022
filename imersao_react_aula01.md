**Mario:** Olá pessoas! Sou Mario Souto, e boas-vindas a mais uma Imersão React aqui da Alura!

Dessa vez, faremos um projeto mais sensacional que na última edição! E não estou sozinho para fazer isso, afinal vocês sabem que sempre há mais alguém na Imersão, e a pessoa especial que está conosco é o Paulo Silveira!

**Paulo:** Olá Mario! Sou o Paulo Silveira, CEO da Alura e estarei colocando perguntas para o Mario nessa Imersão junto com você que está estudando. Até nos separamos em dois estúdios diferentes.

E estou muito contente, pois quem para quer dar um passo a mais em frameworks de front-end, é uma ótima oportunidade de trabalho! Pois é como as pessoas costumam entrar no primeiro e segundo emprego nessa área de tecnologia, pegando CSS, JavaScript e HTML.

O React, sem dúvida, é uma das maiores bibliotecas, se não a maior de todas. Hoje em dia temos outras escutas do View e do Angular, inclusive o Next que veremos junto com o React. Mas com certeza está no mercado inteiro.

Há muitas vagas de trabalho, e não é à toa que temos muitos depoimentos de alunos e alunas que passaram pela Imersão React ou pelas formações de front-end da Alura, e conseguiram seu objetivo.

Claro que não é uma promessa, afinal ninguém dominará o React perfeitamente em apenas cinco dias, mas há muito conteúdo importante. Você criará realmente um projeto completo.

Nossa intenção é que você saia dessa Imersão com um bom projeto para o seu portfólio no ar do GitHub ou do Cloud, e assim poderá mostrar para as pessoas, desde quem for te contratar até seus amigos e amigas: "olha o que eu fiz, olha o que eu aprendi, olha de onde eu comecei até onde eu cheguei".

Afinal, as empresas hoje buscam a sua capacidade de aprender, e não necessariamente o quanto você já conhece da biblioteca. Claro que também é importante e aprenderemos sobre isso nesta Imersão, porém é mais importante ainda mostrar a sua habilidade em ir além e de querer conhecer o que está por trás dos fundamentos do React.

**Mario:** Focamos tanto em aprender os nomes certos, quanto o porquê de usar ou não as ferramentas. Se você conseguir dizer essas coisas em entrevistas, passará um sinal de conhecimento muito maior para o entrevistador do que só adicionar várias coisas no currículo.

Porém, no dia-a-dia de trabalho, é a sua capacidade real que irá resolver o problema de fato, e não necessariamente a quantidade de nomes que você sabe. Este é um ponto importante de frisar, e que cada vez mais é cobrado nas entrevistas.

**Paulo:** Exatamente, e iremos passar por isso. Você verá que é muito importante aprender assim. Esta é a metodologia da Alura, em que trazemos o Dev em T como mostraremos adiante para você compreender o que está acontecendo por "debaixo dos panos".

Claro que em começo de carreira isso acontece aos poucos, mas não queremos que você apenas use os frameworks, e sim que vá além e entenda tudo o que está acontecendo, seja no navegador, V8, TypeScript e etc.

É bastante conteúdo, mas avançaremos com calma para você realmente já colocar no ar o começo do nosso projeto feito nesta aula, e a partir disso iremos aprimorar e entender melhor alguns recursos, como o React funciona, o que você precisa entender do JavaScript, do ciclo de vida e assim por diante.

É fundamental ter domínio, e é sempre muito bacana quando conhecemos pessoas que são muito boas em suas profissões, mas é ainda mais legal quando de fato dominam o funcionamento da ferramenta.

**Mario:** Perfeito, ótima introdução. Vamos tentar dar os primeiros passos passando um pouco da nossa visão, como pensamos, como fazemos, como procuramos, como lemos a documentação e etc.

Todos esses detalhes irão somar na sua evolução das suas habilidades. 

**Paulo:** E Mario, antes de mostrarmos o site do React, o que é o GitHub e passarmos o projeto, traremos dois depoimentos muito importantes de pessoas que estudaram conosco na Imersão e nos cursos de front-end da Alura.

Assim você entenderá de onde podemos sair e até onde podemos chegar. É claro, contando muito com o seu esforço e dedicação. Então vamos lá!

Ana Paula: A minha experiência da Imersão foi muito positiva! Há um ano atrás eu comecei a faculdade e comecei a estudar um pouco, e quando chegou na parte de programação eu me assustei um pouco.

Talvez a didática usada pelo professor não tenha sido a melhor, e tive um bloqueio pensando que não era para mim. Mas resolvi dar uma segunda chance e me surpreendi!

Gabriel: Antes da Alura eu estava um pouco perdido no meio tech, e não sabia para onde ir. Eu queria muito estudar React, já que estava como autodidata aprendendo sobre HTML e CSS, então assinei a Alura para aprofundar mais, além de Python e questões de acessibilidade.

Intensifiquei o estudo em React, o que me ajudou muito no mercado de trabalho. Até consegui minha primeira vaga na área de tecnologia. Acredito que, sem a Alura, tudo seria muito mais difícil.

Inclusive, em entrevistas anteriores, alguns entrevistadores comentaram sobre eu ter estudado na Alura, e perguntavam sobre isso.  Às vezes as empresas fornecem o acesso à plataforma para os funcionários, e isso confirma a credibilidade da escola no mercado.

Então realmente foi um grande diferencial para mim.

**Paulo:** Legal né, Mario? Queremos trazer essa mesma motivação para você, conhecendo o que as alunas e alunos da Alura fazem e fizeram. Claro que as pessoas estão em estágios e têm disponibilidade diferentes, mas o que esperamos é compromisso.

Não à toa estamos fazendo esse grande evento, pois recomendamos que você se dedique e reserve pelo menos duas horas ao dia para assistir às aulas, praticar ao máximo, colocar seu projeto no ar, conversar conosco no Discord e publicar seu desenvolvimento.

Nos marque no LinkedIn e no Instagram, e também lembre-se de registrar sua evolução, pois isso realmente mostrará seu portfólio e servirá como uma "vitrine" do seu trabalho, como mostraremos com projetos de outras pessoas ao longo do curso. Então vamos lá!

**Mario:** A Alura está com tema do filme Matrix, o que tem a ver com o projeto que faremos nesta Imersão, mas o seu pode ser diferente se quiser.

Começaremos mostrando a documentação do React, pois muitos dizem que se deve começar pela documentação quando iniciamos o trabalho com uma tecnologia.

Como o Paulo sempre fala, é interessante termos uma noção da ferramenta antes de começarmos a escrever o código. Nem sempre precisa ler a documentação inteira, e basta clicar em "Comece a Usar" no site do React para já começar a ter uma ideia de como funciona.

Conforme a necessidade, vamos nos aprofundar nos recursos, afinal ler tudo sem praticar não é suficiente para absorver o conteúdo. É sempre importante unir estudo e prática para montar um bom aprendizado.

Paulo, você que está fazendo as perguntas, O React Costuma causar algumas dúvidas sobre o que é exatamente, se é JavaScript ou HTML.

**Paulo:** Exato, o que me causa surpresas no React e em outros frameworks, é que o navegador não entende esse código. Temos uma classe com um retorno sem aspas que abre chaves e inicializa uma tag, e isso não é um código JavaScript compatível. Até o nome deste arquivo se chama JSX.

**Mario:** JSX se traduz como "JavaScript XML", o que é interessante saber. 

**Paulo:** Os arquivos que iremos escrever com este código React não será entendido pelo navegador, e de alguma forma, algo acontecerá para gerar HTML, CSS e JavaScript de forma que o Chrome por exemplo possa entender, conforme aprendemos nas primeiras aulas de front-end.

**Mario:** E quem faz essa transformação é uma ferramenta chamada Babel. Então se estivermos trabalhando com algo de React e nos depararmos com `babel-config` seguido de outra coisa, é por conta desse compilador.

Antigamente chamávamos de transpilador, pois traduzia essa sintaxe que não existe para algo que existe, e atualmente chamamos de compilador. Há toda uma estrutura próxima, e há outras linguagens que também utilizam o Babel.

Porém, no caso do React, há o plugin `babel-react` que é capaz de traduzir todos esses códigos para as chamadas de função que o navegador entende e pode processar.

**Paulo:** Ainda não precisamos muito saber disso, afinal o Babel nem vai aparecer nesta aula. Inclusive, hoje em dia muitas pessoas aprendem a programar direto no react e não sabem que o navegador não lê este código.

Para início de carreira em que já sabe programar um pouco e não entende de JavaScript mas está começando pelo React, não tem problemas.

Porém, daqui a um tempo, será necessário entender melhor como este código vira algo que o navegador entende. Certo?

**Mario:** Outro ponto importante é que - e é uma experiência pessoal - quando eu comecei a aprender React, foquei muito em tentar aprender todo o ferramental, que na época era bem iniciante. Gastei cerca de dois meses tentando entender tudo, e hoje o ferramental atualizou e o React não.

Ou seja, demorei meses para aprender algo que, quando mudou, eu não conseguia entender direito. Então se focarmos na ferramenta  que nos ajudará a trabalhar e entregar resultados que é o React de fato, essa parte que está por "debaixo dos panos" vão ser compreendidas aos poucos.

Invariavelmente teremos que resolver problemas no dia-a-dia, como otimizar uma imagem para fazer algo por exemplo, então precisaremos utilizar melhor.

Com isso, resolvemos as questões sob demanda. É bom evitar pegar tudo de uma vez, pois pode ser que às vezes não haja um bom motivo para se dedicar àquilo.

Então, encontrar a motivação do porquê estamos estudando é fundamental. Portanto, primeiro aprendemos sobre a ferramenta, depois teremos que resolver problemas ou simplesmente nos aprofundar, e seguimos descendo as "camadas" para trabalhar.

Lembrando que a curiosidade é muito importante, além de um grande diferencial. Mas outro ponto interessante é que, como foi no meu caso em que tive de aprender a fazer por conta de antigamente ser bem mais "manual", não havia uma forma clara dos passos para um projeto React ou Angular.

Mostraremos uma maneira atual de iniciar um projeto usando o Next.js. Inclusive, no site encontramos o título em inglês dizendo que é o "framework de React pronto para produção".

O Next.js se posiciona desta forma porque tem uma "casca" para trabalharmos que tem vários recursos que nos ajudam tanto no desenvolvimento quanto na hora da compilação da aplicação para produção.

Ou seja, organiza o Babel e usa várias outras ferramentas de otimização que auxiliam muito, e se dizem também como "SDK da web", o "kit" de desenvolvimento web.

Portanto, se quisermos fazer um site, irão querer que usemos o Next.js e, diferente de muitos debates sobre qual ferramenta serve para qual tamanho de projeto, o Next.js tem um conjunto de funcionalidades que auxiliam na construção de acordo com a escala.

No básico, será apenas uma ferramenta para trabalhar com React, e conforme o projeto aumenta como novas páginas ou chamadas ao longo do tempo e a necessidade cresce, possui suporte nativo que nos permite explorar a documentação para resolver as questões e adicionar recursos.

**Paulo:** Só para entender, quando formos fazer a instalação para criar o projeto, teremos o Next.js na linha de comando. Porém é um framework "em cima" da biblioteca do React.

Ou seja, tudo o que uma pessoa sabe sobre React pode ser usado em nosso projeto da Imersão.

**Mario:** Exatamente, todo conhecimento que houver sobre React funcionará no Next.js, pois esta é a proposta da "camada externa" no código para ajudar a fazer algumas coisas, principalmente de building timing, lidar com páginas, roteamento e outras coisas que, no passado, aparecia muito ao configurar, e hoje em dia há outras soluções mais "opinionated", ou seja, "opinativas", em que alguém define como deve ser e nós só seguimos e trabalhamos.

**Paulo:** Mas por que usar o React e não usar o javascript normal, além dos mecanismos clássicos da internet? É justamente porque facilita o trabalho, pois o HTML, CSS e JavaScript ficaram muito complexos com o tempo.

Inclusive o criador do React é o Facebook, que é uma rede social com uma enorme quantidade de funcionalidades em que cada componente visual possui alguma reação de acordo com algo que acontece, seja no server side, no back-end, ou no visual do mouse over. Então começou a ficar bem complicado gerenciar tudo em um gigantesco HTML e CSS.

**Mario:** É exatamente isso. Pensando nestes "pedaços" de tela, o mais relevante não somente no React, mas também em todas as ferramentas atuais, essa ideia de componentes.

Falo como ideia, pois pode ser que aprendamos React hoje e entremos em um projeto que use View e Angular por exemplo, afinal as empresas têm diferentes tecnologias. Portanto sempre focaremos em ideias nas Imersões.

É interessante focar nos componentes porque há várias bibliotecas open source que nos permitem pegar os trechos de código e aplicar nos projetos. Claro que algumas exigem algumas configurações seguindo a documentação, mas por exemplo o Material UI, possui vários componentes baseados no material design do Google e Android, e acessando sua documentação, encontramos a parte de "Componentes".

**Paulo:** A página inicial do Material UI mostra os componentes de calendário, temperatura, botão de "comprar" e outros.

**Mario:** E ainda é interativo! Há imagens e botões para clicarmos.

**Paulo:** E com cada tag, o React sabe pegar e gerar JavaScript e etc. para criar esse componente visual, ao invés de copiarmos e colarmos de vários lugares, ou escrevermos nosso próprio.

Não necessariamente os componentes são visuais, mas na maioria dos casos é. Então cada um estará pronto para trabalharmos no React.

**Mario:** E são infinitos! Há até bibliotecas que nos ajudam a catalogar esses componentes. Usaremos um conjunto no Storyboard ao longo do projeto, e podemos clicar e mostrar o código para podermos testar e definir o que queremos.

Então há muitos recursos focados atualmente em ajudar na documentação, pois muitos times possuem apenas um pequeno botão, mas quando vamos para empresas maiores, pode ser que precisemos fazer uma página nova de produtos, por exemplo.

A própria equipe de design já criou e selecionou alguns templates. Depois, mandam para a equipe de desenvolvimento juntá-los para criar a página. Desta forma, teremos mais autonomia dentro do ecossistema do React, tanto na documentação quanto nos componentes que nos ajuda a reutilizar código e escrever em cima de algo que já está pronto, como o calendário do Airbnb que é usado em várias companhias aéreas.

É muito interessante conseguir começar a enxergar e identificar a origem dos componentes. Então realmente o open source deu bastante certo e se expande cada vez mais, com mais recursos e organização.

Teremos ícones e várias outras coisas, mas nosso projeto especial ainda não foi mostrado. Com o link, poderemos ver a página com os componentes que poderão ser customizados. É muito inspirado na página da Alura.

Basicamente, pegamos a ideia de trabalhar tanto com os componentes quanto com as bases do React,e a questão de reatividade e algo mudar outra coisa, resolvemos fazer um chat inspirado no Discord, mas que você dará o tema.

O nosso foi inspirado no Alura Matrix e nas ideias do Paulo, e possui todo o processo de digitarmos o nome de usuário do GitHub. Usaremos a app do Matrix que terá um lugar que buscará os dados das mensagens, as fotos do GitHub e etc.

Fizemos uma grande interação que será construída com vocês. Quando clicarmos em "Entrar", exibiremos a parte interna do site com as mensagens, botão de logout, campo de texto e etc. Tudo isso iremos construir juntos ao longo das aulas da Imersão.

**Mario:** Olá pessoas! Sou Mario Souto, e boas-vindas a mais uma Imersão React aqui da Alura!

Dessa vez, faremos um projeto mais sensacional que na última edição! E não estou sozinho para fazer isso, afinal vocês sabem que sempre há mais alguém na Imersão, e a pessoa especial que está conosco é o Paulo Silveira!

**Paulo:** Olá Mario! Sou o Paulo Silveira, CEO da Alura e estarei colocando perguntas para o Mario nessa Imersão junto com você que está estudando. Até nos separamos em dois estúdios diferentes.

E estou muito contente, pois quem para quer dar um passo a mais em frameworks de front-end, é uma ótima oportunidade de trabalho! Pois é como as pessoas costumam entrar no primeiro e segundo emprego nessa área de tecnologia, pegando CSS, JavaScript e HTML.

O React, sem dúvida, é uma das maiores bibliotecas, se não a maior de todas. Hoje em dia temos outras escutas do View e do Angular, inclusive o Next que veremos junto com o React. Mas com certeza está no mercado inteiro.

Há muitas vagas de trabalho, e não é à toa que temos muitos depoimentos de alunos e alunas que passaram pela Imersão React ou pelas formações de front-end da Alura, e conseguiram seu objetivo.

Claro que não é uma promessa, afinal ninguém dominará o React perfeitamente em apenas cinco dias, mas há muito conteúdo importante. Você criará realmente um projeto completo.

Nossa intenção é que você saia dessa Imersão com um bom projeto para o seu portfólio no ar do GitHub ou do Cloud, e assim poderá mostrar para as pessoas, desde quem for te contratar até seus amigos e amigas: "olha o que eu fiz, olha o que eu aprendi, olha de onde eu comecei até onde eu cheguei".

Afinal, as empresas hoje buscam a sua capacidade de aprender, e não necessariamente o quanto você já conhece da biblioteca. Claro que também é importante e aprenderemos sobre isso nesta Imersão, porém é mais importante ainda mostrar a sua habilidade em ir além e de querer conhecer o que está por trás dos fundamentos do React.

**Mario:** Focamos tanto em aprender os nomes certos, quanto o porquê de usar ou não as ferramentas. Se você conseguir dizer essas coisas em entrevistas, passará um sinal de conhecimento muito maior para o entrevistador do que só adicionar várias coisas no currículo.

Porém, no dia-a-dia de trabalho, é a sua capacidade real que irá resolver o problema de fato, e não necessariamente a quantidade de nomes que você sabe. Este é um ponto importante de frisar, e que cada vez mais é cobrado nas entrevistas.

**Paulo:** Exatamente, e iremos passar por isso. Você verá que é muito importante aprender assim. Esta é a metodologia da Alura, em que trazemos o Dev em T como mostraremos adiante para você compreender o que está acontecendo por "debaixo dos panos".

Claro que em começo de carreira isso acontece aos poucos, mas não queremos que você apenas use os frameworks, e sim que vá além e entenda tudo o que está acontecendo, seja no navegador, V8, TypeScript e etc.

É bastante conteúdo, mas avançaremos com calma para você realmente já colocar no ar o começo do nosso projeto feito nesta aula, e a partir disso iremos aprimorar e entender melhor alguns recursos, como o React funciona, o que você precisa entender do JavaScript, do ciclo de vida e assim por diante.

É fundamental ter domínio, e é sempre muito bacana quando conhecemos pessoas que são muito boas em suas profissões, mas é ainda mais legal quando de fato dominam o funcionamento da ferramenta.

**Mario:** Perfeito, ótima introdução. Vamos tentar dar os primeiros passos passando um pouco da nossa visão, como pensamos, como fazemos, como procuramos, como lemos a documentação e etc.

Todos esses detalhes irão somar na sua evolução das suas habilidades. 

**Paulo:** E Mario, antes de mostrarmos o site do React, o que é o GitHub e passarmos o projeto, traremos dois depoimentos muito importantes de pessoas que estudaram conosco na Imersão e nos cursos de front-end da Alura.

Assim você entenderá de onde podemos sair e até onde podemos chegar. É claro, contando muito com o seu esforço e dedicação. Então vamos lá!

Ana Paula: A minha experiência da Imersão foi muito positiva! Há um ano atrás eu comecei a faculdade e comecei a estudar um pouco, e quando chegou na parte de programação eu me assustei um pouco.

Talvez a didática usada pelo professor não tenha sido a melhor, e tive um bloqueio pensando que não era para mim. Mas resolvi dar uma segunda chance e me surpreendi!

Gabriel: Antes da Alura eu estava um pouco perdido no meio tech, e não sabia para onde ir. Eu queria muito estudar React, já que estava como autodidata aprendendo sobre HTML e CSS, então assinei a Alura para aprofundar mais, além de Python e questões de acessibilidade.

Intensifiquei o estudo em React, o que me ajudou muito no mercado de trabalho. Até consegui minha primeira vaga na área de tecnologia. Acredito que, sem a Alura, tudo seria muito mais difícil.

Inclusive, em entrevistas anteriores, alguns entrevistadores comentaram sobre eu ter estudado na Alura, e perguntavam sobre isso.  Às vezes as empresas fornecem o acesso à plataforma para os funcionários, e isso confirma a credibilidade da escola no mercado.

Então realmente foi um grande diferencial para mim.

**Paulo:** Legal né, Mario? Queremos trazer essa mesma motivação para você, conhecendo o que as alunas e alunos da Alura fazem e fizeram. Claro que as pessoas estão em estágios e têm disponibilidade diferentes, mas o que esperamos é compromisso.

Não à toa estamos fazendo esse grande evento, pois recomendamos que você se dedique e reserve pelo menos duas horas ao dia para assistir às aulas, praticar ao máximo, colocar seu projeto no ar, conversar conosco no Discord e publicar seu desenvolvimento.

Nos marque no LinkedIn e no Instagram, e também lembre-se de registrar sua evolução, pois isso realmente mostrará seu portfólio e servirá como uma "vitrine" do seu trabalho, como mostraremos com projetos de outras pessoas ao longo do curso. Então vamos lá!

**Mario:** A Alura está com tema do filme Matrix, o que tem a ver com o projeto que faremos nesta Imersão, mas o seu pode ser diferente se quiser.

Começaremos mostrando a documentação do React, pois muitos dizem que se deve começar pela documentação quando iniciamos o trabalho com uma tecnologia.

Como o Paulo sempre fala, é interessante termos uma noção da ferramenta antes de começarmos a escrever o código. Nem sempre precisa ler a documentação inteira, e basta clicar em "Comece a Usar" no site do React para já começar a ter uma ideia de como funciona.

Conforme a necessidade, vamos nos aprofundar nos recursos, afinal ler tudo sem praticar não é suficiente para absorver o conteúdo. É sempre importante unir estudo e prática para montar um bom aprendizado.

Paulo, você que está fazendo as perguntas, O React Costuma causar algumas dúvidas sobre o que é exatamente, se é JavaScript ou HTML.

**Paulo:** Exato, o que me causa surpresas no React e em outros frameworks, é que o navegador não entende esse código. Temos uma classe com um retorno sem aspas que abre chaves e inicializa uma tag, e isso não é um código JavaScript compatível. Até o nome deste arquivo se chama JSX.

**Mario:** JSX se traduz como "JavaScript XML", o que é interessante saber. 

**Paulo:** Os arquivos que iremos escrever com este código React não será entendido pelo navegador, e de alguma forma, algo acontecerá para gerar HTML, CSS e JavaScript de forma que o Chrome por exemplo possa entender, conforme aprendemos nas primeiras aulas de front-end.

**Mario:** E quem faz essa transformação é uma ferramenta chamada Babel. Então se estivermos trabalhando com algo de React e nos depararmos com `babel-config` seguido de outra coisa, é por conta desse compilador.

Antigamente chamávamos de transpilador, pois traduzia essa sintaxe que não existe para algo que existe, e atualmente chamamos de compilador. Há toda uma estrutura próxima, e há outras linguagens que também utilizam o Babel.

Porém, no caso do React, há o plugin `babel-react` que é capaz de traduzir todos esses códigos para as chamadas de função que o navegador entende e pode processar.

**Paulo:** Ainda não precisamos muito saber disso, afinal o Babel nem vai aparecer nesta aula. Inclusive, hoje em dia muitas pessoas aprendem a programar direto no react e não sabem que o navegador não lê este código.

Para início de carreira em que já sabe programar um pouco e não entende de JavaScript mas está começando pelo React, não tem problemas.

Porém, daqui a um tempo, será necessário entender melhor como este código vira algo que o navegador entende. Certo?

**Mario:** Outro ponto importante é que - e é uma experiência pessoal - quando eu comecei a aprender React, foquei muito em tentar aprender todo o ferramental, que na época era bem iniciante. Gastei cerca de dois meses tentando entender tudo, e hoje o ferramental atualizou e o React não.

Ou seja, demorei meses para aprender algo que, quando mudou, eu não conseguia entender direito. Então se focarmos na ferramenta  que nos ajudará a trabalhar e entregar resultados que é o React de fato, essa parte que está por "debaixo dos panos" vão ser compreendidas aos poucos.

Invariavelmente teremos que resolver problemas no dia-a-dia, como otimizar uma imagem para fazer algo por exemplo, então precisaremos utilizar melhor.

Com isso, resolvemos as questões sob demanda. É bom evitar pegar tudo de uma vez, pois pode ser que às vezes não haja um bom motivo para se dedicar àquilo.

Então, encontrar a motivação do porquê estamos estudando é fundamental. Portanto, primeiro aprendemos sobre a ferramenta, depois teremos que resolver problemas ou simplesmente nos aprofundar, e seguimos descendo as "camadas" para trabalhar.

Lembrando que a curiosidade é muito importante, além de um grande diferencial. Mas outro ponto interessante é que, como foi no meu caso em que tive de aprender a fazer por conta de antigamente ser bem mais "manual", não havia uma forma clara dos passos para um projeto React ou Angular.

Mostraremos uma maneira atual de iniciar um projeto usando o Next.js. Inclusive, no site encontramos o título em inglês dizendo que é o "framework de React pronto para produção".

O Next.js se posiciona desta forma porque tem uma "casca" para trabalharmos que tem vários recursos que nos ajudam tanto no desenvolvimento quanto na hora da compilação da aplicação para produção.

Ou seja, organiza o Babel e usa várias outras ferramentas de otimização que auxiliam muito, e se dizem também como "SDK da web", o "kit" de desenvolvimento web.

Portanto, se quisermos fazer um site, irão querer que usemos o Next.js e, diferente de muitos debates sobre qual ferramenta serve para qual tamanho de projeto, o Next.js tem um conjunto de funcionalidades que auxiliam na construção de acordo com a escala.

No básico, será apenas uma ferramenta para trabalhar com React, e conforme o projeto aumenta como novas páginas ou chamadas ao longo do tempo e a necessidade cresce, possui suporte nativo que nos permite explorar a documentação para resolver as questões e adicionar recursos.

**Paulo:** Só para entender, quando formos fazer a instalação para criar o projeto, teremos o Next.js na linha de comando. Porém é um framework "em cima" da biblioteca do React.

Ou seja, tudo o que uma pessoa sabe sobre React pode ser usado em nosso projeto da Imersão.

**Mario:** Exatamente, todo conhecimento que houver sobre React funcionará no Next.js, pois esta é a proposta da "camada externa" no código para ajudar a fazer algumas coisas, principalmente de building timing, lidar com páginas, roteamento e outras coisas que, no passado, aparecia muito ao configurar, e hoje em dia há outras soluções mais "opinionated", ou seja, "opinativas", em que alguém define como deve ser e nós só seguimos e trabalhamos.

**Paulo:** Mas por que usar o React e não usar o javascript normal, além dos mecanismos clássicos da internet? É justamente porque facilita o trabalho, pois o HTML, CSS e JavaScript ficaram muito complexos com o tempo.

Inclusive o criador do React é o Facebook, que é uma rede social com uma enorme quantidade de funcionalidades em que cada componente visual possui alguma reação de acordo com algo que acontece, seja no server side, no back-end, ou no visual do mouse over. Então começou a ficar bem complicado gerenciar tudo em um gigantesco HTML e CSS.

**Mario:** É exatamente isso. Pensando nestes "pedaços" de tela, o mais relevante não somente no React, mas também em todas as ferramentas atuais, essa ideia de componentes.

Falo como ideia, pois pode ser que aprendamos React hoje e entremos em um projeto que use View e Angular por exemplo, afinal as empresas têm diferentes tecnologias. Portanto sempre focaremos em ideias nas Imersões.

É interessante focar nos componentes porque há várias bibliotecas open source que nos permitem pegar os trechos de código e aplicar nos projetos. Claro que algumas exigem algumas configurações seguindo a documentação, mas por exemplo o Material UI, possui vários componentes baseados no material design do Google e Android, e acessando sua documentação, encontramos a parte de "Componentes".

**Paulo:** A página inicial do Material UI mostra os componentes de calendário, temperatura, botão de "comprar" e outros.

**Mario:** E ainda é interativo! Há imagens e botões para clicarmos.

**Paulo:** E com cada tag, o React sabe pegar e gerar JavaScript e etc. para criar esse componente visual, ao invés de copiarmos e colarmos de vários lugares, ou escrevermos nosso próprio.

Não necessariamente os componentes são visuais, mas na maioria dos casos é. Então cada um estará pronto para trabalharmos no React.

**Mario:** E são infinitos! Há até bibliotecas que nos ajudam a catalogar esses componentes. Usaremos um conjunto no Storyboard ao longo do projeto, e podemos clicar e mostrar o código para podermos testar e definir o que queremos.

Então há muitos recursos focados atualmente em ajudar na documentação, pois muitos times possuem apenas um pequeno botão, mas quando vamos para empresas maiores, pode ser que precisemos fazer uma página nova de produtos, por exemplo.

A própria equipe de design já criou e selecionou alguns templates. Depois, mandam para a equipe de desenvolvimento juntá-los para criar a página. Desta forma, teremos mais autonomia dentro do ecossistema do React, tanto na documentação quanto nos componentes que nos ajuda a reutilizar código e escrever em cima de algo que já está pronto, como o calendário do Airbnb que é usado em várias companhias aéreas.

É muito interessante conseguir começar a enxergar e identificar a origem dos componentes. Então realmente o open source deu bastante certo e se expande cada vez mais, com mais recursos e organização.

Teremos ícones e várias outras coisas, mas nosso projeto especial ainda não foi mostrado. Com o link, poderemos ver a página com os componentes que poderão ser customizados. É muito inspirado na página da Alura.

Basicamente, pegamos a ideia de trabalhar tanto com os componentes quanto com as bases do React,e a questão de reatividade e algo mudar outra coisa, resolvemos fazer um chat inspirado no Discord, mas que você dará o tema.

O nosso foi inspirado no Alura Matrix e nas ideias do Paulo, e possui todo o processo de digitarmos o nome de usuário do GitHub. Usaremos a app do Matrix que terá um lugar que buscará os dados das mensagens, as fotos do GitHub e etc.

Fizemos uma grande interação que será construída com vocês. Quando clicarmos em "Entrar", exibiremos a parte interna do site com as mensagens, botão de logout, campo de texto e etc. Tudo isso iremos construir juntos ao longo das aulas da Imersão.

**Paulo:** E vai trocar essas mensagens mesmo, porque ficarão guardadas em algum lugar. Mesmo sem fazermos back-end, o Mário vai mostrar soluções que dá para acoplar. Mario, abre a página do Dev em T da Alura para darmos uma olhada. Essa é uma página que quando lançamos marcou muito o mercado no Brasil.

Vale a pena você ler o nosso <a href="https://www.alura.com.br/dev-em-t" target="_blank">manifesto Dev em T</a>, ele mostra como pensamos que você pode organizar sua carreira. Por exemplo, em front-end, pense que você vai se aprofundar na sua carreira de front-end, vai entender não só o React, mas também o JavaScript, o TypeScript, vai ler o código fonte de algumas dessas bibliotecas daqui a alguns anos, vai entender como o navegador funciona, o V8; e também vai pegar um pouco de DevOps, entender o tal do CICD para colocar o build, que vamos fazer aqui, vamos fazer o deploy no Cloud, vai entender um pouco do back-end para consumir microsserviços, vamos fazer isso aqui na Imersão.

Hoje em dia, não basta ser aquela pessoa que faz só uma parte do sistema, porque no squad de uma empresa você precisa conversar com outras pessoas que têm trabalhos um pouco diferentes, mas que estão conectados com o seu. Front-end está conectado com back-end.

Se você não conhecer nem um pouco essa outra área, fica batendo cabeça. Não é à toa que ali na home da Alura temos sete escola que têm muito a ver entre si. Programação com Front-End, Data Science, DevOps, UX & Design, é nessa área que as pessoas utilizam muito o Figma para desenhar, você vão ver que deixaremos para vocês o link do arquivo no Figma que explica como deve ser o layout do nosso projeto Aluracord. os designer fazem no Figma e explicam como deve ser o layout.

A partir daí, essa pessoa que trabalha com UX vai entregar o arquivo no Figma para a pessoa que trabalha com front-end e falar: "front-end, se vira!". Então você precisa entender um pouco do Figma.

Está tudo conectado. Essa Imersão está toda conectada, a Alura está toda conectada e é assim que trabalhamos.

**Mario:** Lembrando que não vai ser do dia para a noite. É um conhecimento que se cria com o tempo. Ter curiosidade para saber disso é um caminho sem volta e agora você vai conhecer isso.

Na Imersão, uma de nossas metas é te dar autonomia, então não vamos criar todo o back-end, mas você terá uma ferramenta que ajuda a fazer essa parte. Você pode levar essa solução para o seu time, usar em outros lugares e ver as possibilidades.

Eu até brinco que todo mundo que trabalha com programação cria seu cinto de utilidades, igual ao Batman, com várias ferramentas e utilidades que guardamos com o tempo e usamos nos mais diversos cenários, seja para fazer coleta de dados, para salvar informação etc. O dia a dia começa a nos cobrar para termos soluções ao nosso alcance. Daremos algumas dessas soluções para você ao longo da Imersão.

Falando em dar soluções para a galera, vamos começar o nosso projeto Aluracord?

Vou acessar a <a href="https://nextjs.org/docs/getting-started" target="_blank">documentação do Next JS</a>, gosto bastante do jeito que eles a organizam. Logo no início tem esse "Getting Started", que é a introdução explicando como fazer para criar um projeto com essa ferramenta.

Vou descer a página, repare que logo de cara ele tem uma parte de setup recomendado, ele fala: "Recomendamos que você crie um projeto usando esse `create-next-app`...".

Nós recomendamos que você faça esses passos do setup depois do seu primeiro projeto da Imersão, porque esse setup traz vários arquivos que, num primeiro momento, podem te confundir.

Sei que é estranho irmos contra a primeira indicação da documentação. Mas é justamente porque queremos trabalhar em você a ideia de ter um pouco mais de conhecimento do que está acontecendo.

Então, vamos pular para a parte do "Manual Setup" e faremos juntos esse setup manual. Para isso, esperamos que na sua máquina já esteja instalado o Visual Studio Code, que é a ferramenta de editor de código que usaremos, o Node também que é superimportante e junto com o Node vai ter essa ferramenta chamada NPM, que você vai conseguir ver no seu terminal e daqui a pouco te ajudaremos a testar.

**Paulo:** Na página dessa primeira aula da Imersão estão disponíveis os links para instalar o Node e o Visual Studio Code seja no Windows ou Mac.

**Mario:** Precisamos ter essas ferramentas, sem elas não dá para rodar o projeto. Lembrando que tanto o Next quando o React são bibliotecas, são códigos que estão na internet, você pode pesquisar no Google por "github react", vai aparecer o link da documentação que está no GitHub, tem a descrição da ferramenta, os arquivos, então teremos uma ferramenta para nos ajudar a baixar esses pedaços de código da internet, essa ferramenta é esse tal de NPM.

Não só o NPM, uma outra que vocês podem ter em suas máquinas é o Yarn, que faz basicamente a mesma coisa. Tanto o NPM quanto o Yarn são agregadores, eles permitem que você procure essas bibliotecas. Se eu procurar, por exemplo, o React no site do Yarn, ele mostra o React, o read me dele e como instalar usando o Yarn. A mesma coisa acontece no site do NPM.

Vamos voltar para o setup manual da documentação do Next e começar a instalar essas coisas e iniciar nosso projeto. Para isso, vou copiar o comando da documentação:

```
npm install next react react-dom
# or
yarn add next react react-dom
```

**Mario:** Vou vir aqui na minha área de trabalho e criar uma pasta nova chamada "aluracord" e vou abrir o Visual Studio Code que já está instalado na minha máquina. Na maioria dos sistemas operacionais basta você arrastar a pasta para dentro do Visual Studio Code e ele já abre seu projeto.

Se, por algum motivo, no seu sistema operacional isso não funcionar, para abrir essa pasta que criamos basta vir em "File > Open Folder".

Vou começar a rodar comandos no terminal para iniciarmos o nosso projeto. Para abrir o terminal devemos ir no menu superior e selecionar "View > Terminal". Para facilitar no dia a dia você pode ver, nesse mesmo caminho, qual é o atalho configurado para abrir o terminal.

Por este ser um projeto JavaScript, e termos essas bibliotecas, precisamos de um arquivo que registra todas as bibliotecas e deixa clara a informação de qual versão React e qual versão das bibliotecas esse projeto tem. Para que todo mundo que vá usar o nosso código consiga ter a mesma versão. 

**Paulo:** Muitas linguagens têm tipo um arquivo de build, não é? O arquivo que usamos para pedir que algo seja baixado da internet e jogue algo no servidor de determinada forma. Cada linguagem tem mecanismos para escrever esse arquivo de configuração que tem uma cara de script.

**Mario:** Exato. E aqui, para usar essa ferramenta de script, vou usar o Yarn, que está mais configurado aqui na minha máquina, mas na sua pode ter a NPM, você pode usar a que preferir.

Na descrição eu vou deixar um vídeo mostrando como eu configuro meu ambiente. Se você quiser configurar mais próximo do que eu estou usando aqui, pode fazer isso também.

Antes de colar o comando que copiei da documentação, eu vou inicializar esse arquivo que o Paulo falou. No meu terminal do Visual Studio vou escrever `yarn init -y`. O `-y` é porque quando você inicializa um projeto ele faz várias perguntas que no momento não faz sentido responder, só queremos começar.

Após escrever esse comando pressionaremos "Enter". E foi criado o arquivo `package.json` que é o arquivo que vai gerenciar os pacotes do projeto. Esse `package.json` tem o nome, a versão, o arquivo principal, informa a licença do projeto… Podemos ver mais dele depois.

Agora veremos esse arquivo ser preenchido. Vou colar no terminal aquele comando que copiei da documentação, `yarn add next react react-dom`.

**Paulo:** É bom quem está nos assistindo usar o Yarn também, na página da Imersão tem o link de instalação.

**Mario:** Exato. Lembrando que neste caso não existe melhor nem pior, é mais uma questão de preferência para o projeto. Na minha máquina tem o Yarn porque uso muito o React Native - a versão de fazer aplicativos do React - que recomenda o uso do Yarn por conta do Facebook, do ecossistema etc. Só um contexto para você que está assistindo e podermos seguir adiante. É algo que você pode explorar depois das aulas da Imersão. A ideia do React Native é você reaprovitar os conhecimentos que você tem de React em uma outra plataforma. Indico fazer esse teste depois.

Logo após rodar o comando de instalação que fizemos, ele adicionou no `package.json` o que chamamos de dependências, que são as nossas bibliotecas com suas respectivas versões. Assim teremos o controle de saber qual versão estamos usando, para não quebrar nada e tudo funcionar corretamente.

Feito isso, vamos seguir a documentação, onde ele diz: "Abra agora o `package.json` e adicione os seguintes scripts".

```
"scripts": {
  "dev": "next dev",
  "build": "next build",
  "start": "next start",
  "lint": "next lint"
}
```

**Mario:** O que cai na parte de build que o Paulo comentou. Teremos comandos para nos ajudar a rodar o projeto, gerar versão de produção dele para colocar no ar, entre outras coisas. Copiaremos esse trecho de código dos scripts e vamos colar no `package.json` depois das dependências. Lembrando de, antes de colar esse trecho, colocar uma vírgula depois da chave `},`. Se você não colocar a vírgula vai aparecer um erro meio estranho, então vamos colocar vírgula para garantir.

Perfeito, já temos os scripts. De volta à documentação, ela explica o que cada script faz. Fiquem tranquilos, pois vamos passar por eles, principalmente o `dev`, o `start` e o `build`. 

Basicamente, o próximo passo para vermos algo rodando na prática é criar uma pasta "pages" e dentro dela um arquivo `index.js` com esse conteúdo para criar uma página home, o começo do nosso projeto, que é um site, estamos usando o React para fazer uma aplicação web.

```
function HomePage() {
  return <div>Welcome to Next.js!</div>
}

export default HomePage
```

**Mario:** Vou copiar esse código da documentação, voltar para o Visual Studio Code e, no menu lateral esquerdo, criar uma pasta "pages" e dentro dessa pasta criar o arquivo `index.js` onde vou colar o código que copiei.

Feito isso, vamos rodar no terminal o comando `yarn dev`, que é um dos comandos de script que colamos no código. Esse `dev` é um atalho para rodar o `next dev` que é para rodar o modo de desenvolvimento do Next.

Vamos rodar o comando `yarn dev`, ir para o navegador e entrar no endereço http://localhost:3000. Agora conseguimos ver no navegador o nosso código rodando. Fizemos nosso primeiro output, a primeira saída de alguma coisa.

Agora vamos parar e reanalisar o que fizemos. Nós criamos o `package.json`, instalamos as bibliotecas, definimos os comandos para rodar o projeto, criamos um arquivo e rodamos no terminal.

Comparado à maioria dos projetos de front-end, principalmente com frameworks, esse é um setup que vai bem direto ao ponto para entendermos. Ele guarda muita coisa "por debaixo dos panos" e é mais tranquilo de replicar em casa, de fazer teste para você entender o que é esse `package.json`, o que são os scripts, convido você a explorar tudo isso.

Mas agora vamos explorar o arquivo `index.js`. Nele já temos um primeiro código React rodando, se eu mudar qualquer coisa aqui dentro e salvar, sem recarregar o navegador ele já muda, por exemplo, se eu substituir "Welcome to Next.js!" por "Olá pessoas!" e salvar, ele vai exibir essa mudança no navegador. Então, tem toda uma inteligência para facilitar o desenvolvimento e você, literalmente, só sentar, escrever seu código e ir vendo as alterações sendo aplicadas no seu projeto.

O Next é bem esperto nesse ponto e vai ajudar bastante no que chamamos de developer experience, que é você ter uma experiência legal para trabalhar no seu projeto, refatorar as coisas e assim por diante.

À primeira vista, é importante falar que por mais que pareça uma coisa de outro mundo, temos basicamente uma função JavaScript que retorna esse trecho que parece HTML, `return <div>Olá pessoas!</div>`. 

Tentar deixar claro o nome das coisas ajuda bastante. Isso é um componente React. Já temos o nosso primeiro componente, que foi criado pela própria documentação.

```
// Componente React
function HomePage() {
// JSX
  return <div>Olá pessoas!</div>
}

export default HomePage
```

Nossa meta é, até o final da aula, ter uma estrutura como este layout que temos pronto, com imagem de fundo, texto de boas-vindas, campo para digitar seu usuário do GitHub, um botão "Entrar"... Vocês poderão customizar e fazer os ajustes que querem em seu projeto.

Para isso, vamos começar pelo título "Boas vindas de volta!" e temos também o subtítulo "Discord - Alura Matrix". Vamos tentar escrever isso no arquivo `index.js` dentro do nosso JSX.

Podemos copiar esse "Boas vindas de volta!" e colá-lo dentro da `div` que está sendo retornada. Para ficar mais fácil fazer a quebra de linha e indentar melhor, normalmente o pessoal coloca parênteses em volta de tudo.

Porque se você não coloca o parênteses a fonte do código fica mais escura no VS Code. Então vamos abrir e fechar parênteses e escrever todo o código da tela dentro desse parênteses.


```
// Componente React
function HomePage() {
// JSX
  return  (
	<div>
	Boas vindas de volta!
	</div>

	)
}

export default HomePage
```

**Mario:** Vou colocar o "Boas vindas de volta!" dentro de uma tag HTML normalmente, dentro de uma tag `<h1>`, `<h1>Boas vindas de volta!</h1>`.

Agora, vamos copiar o subtítulo "Discord - Alura Matrix". Vamos colocá-lo no nosso código dentro de uma tag `<h2>`, `<h2>Discord - Alura Matrix</h2>`.

```
// Componente React
function HomePage() {
// JSX
  return  (
	<div>
	<h1>Boas vindas de volta!</h1>
          <h2>Discord - Alura Matrix</h2>
	</div>

	)
}

export default HomePage
```

**Mario:** Vamos salvar e podemos verificar como ficou a nossa página no navegador. Nossa página foi atualizada. Está longe do layout ainda, mas vamos trabalhando aos poucos e entendendo como trabalhar com as coisas aqui.

O React tem essa característica de misturar muitas coisas, estamos escrevendo o HTML no JavaScript e até o CSS vai ficar aqui dentro também. 

Para conseguirmos escrever o CSS dentro do JavaScript e começarmos a estilizar a página, vamos trabalhar com uma técnica chamada "CSS in JS". Se você pesquisar por isso no Google Imagens vai vir algumas coisas genéricas, mas vamos tentar ver juntos o jeito que o próprio Next se propõe a resolver esse problema.

O Next tem uma ferramenta chamada "styled jsx". Só de você estar com o Next rodando no seu projeto, ele tem esse styled-jsx e eles mostram aqui na <a href="https://github.com/vercel/styled-jsx" target="_blank">página do GitHub acessível neste link</a>, um exemplo dele, dentro do que seria um componente:

```
export default () => (
  <div>
    <p>only this paragraph will get the style :)</p>

    {/* you can include <Component />s here that include
         other <p>s that don't get unexpected styles! */}

    <style jsx>{`
      p {
        color: red;
      }
    `}</style>
  </div>
)
```

É basicamente uma função que tem o parênteses e retorna um trecho de HTML, aqui tem uma tag `<style jsx>`, mas essa não é uma tag style normal do HTML, essa tem o atributo jsx que mostra que é um style diferente do tradicional e podemos fazer coisas a mais aqui dentro.

Vou copiar esse trecho da tag style que está como exemplo no GitHub para começarmos a estilizar algumas coisas no nosso código.

```
<style jsx>{`
      p {
        color: red;
      }
    `}</style>
```

**Mario:** Se eu só copiar e colar esse estilo aqui dentro da `div` do `index.js`, não vai mudar nada porque não tem uma tag `p` aqui, mas eu posso substituir o `p` por `h1` e começar a trabalhar na nossa tag de título.

Vou salvar e ver como ficou nossa página no navegador. Ele pintou a fonte do nosso título de vermelho. Antes de mostrar o que tem de diferente nesse estilo, Paulo, quero te fazer uma pergunta. Você chegou a sofrer com CSS, de alguma forma, na sua vida? 

**Paulo:** Acho que o complicado do CSS é que ele é meio global, por exemplo, quando você define que quer que todo `h1` seja pintado de uma cor, todo `h1` será pintado daquela cor - tudo bem que `h1` geralmente só temos um, o do título, mas vale como exemplo - aí você precisa começar a definir classes...

**Mario:** Hoje em dia, se você coloca o `h1` dentro de uma tag `<article>` é possível ter múltiplos `h1`s dentro de uma página.

**Paulo:** Olha só, isso é novidade pra mim. E aí se eu quisesse que cada artigo tivesse um `h1` diferente eu teria que tomar cuidado com as classes, com os ids etc. Aí fica aquela briga, vocês escreve uma coisa no HTML e precisa lembrar como está no CSS lá no outro arquivo.

Então parece que a proposta do React e de outros frameworks é tentar dar uma juntada. À primeira vista, isso que você está escrevendo me dói um pouco o olho. Estamos mostrando várias linguagens de programação, misturando JavaScript, HTML e CSS no mesmo trecho de código.

Fica meio embolado o que é o quê. Mas entendo que tem vantagens. Pelo que entendi, estamos falando que a cor desse `h1` do componente `HomePage`, que por enquanto é nosso único componente, tem a fonte vermelha. Então entendo que, ao criar outros componentes, o `h1` desses outros componentes não ficarão em vermelho porque ele consegue entender e diferenciar isso.

**Mario:** Exato. Boa parte de usarmos essas coisas mais prontas é ganharmos de bandeja esses recursos. Se, no navegador, eu clicar com o botão direito no texto do título e selecionar "Inspecionar", conseguimos ver que só de ter colocado o trecho de código do `<style jsx>` são adicionadas várias classes no código da página.

O próprio Next, com a lib do `style jsx`, está gerenciando como os estilos devem ser aplicados na página e ele cria essa questão do escopo sobre o qual você comentou.

Se eu colocar outros `h1` na nossa página, todos esses `h1`s receberão essa cor vermelha, mas se tiver um outro componente que também tem `h1`, ele não vai passar. Ou seja, ele quebra esses estilos por componente. Só vai receber o estilo, as tags e o componente que você colocou.

Isso nos ajuda a ter que lidar menos com essa responsabilidade de ter que nomear as coisas. Porque é muito comum em projeto CSS o código crescer e por mais que você tente arquitetar, usando metodologias como BEM (Block Element Modifier) ou DRY (Don't Repeat Yourself) no CSS, com o tempo a galera foi vendo que dar nomes para todas as classes do CSS é difícil de manter no longo prazo.

Tanto que projetos de CSS que não usam ferramenta, por exemplo, o Tailwind CSS, que é um que está bastante popular, <a href="https://tailwindcss.com/docs/utility-first" target="_blank">ao ver a documentação do Tailwind acessível neste link</a>, repare que ele traz um exemplo com classe, mostrando como seria o modelo tradicional.

Nesse exemplo vemos que para fazer um chat precisamos dar um nome com várias classes. E mesmo as coisas que são com CSS, muitas pessoas estão usando uma abordagem de ter pequenas classes que têm coisas específicas. Por exemplo, você define que a margem do eixo x é "auto", aí ele vai gerar um CSS baseado nessas classes. 

No React, veremos que tem outra forma de escrever, mas tanto as ferramentas de CSS puro quanto as ferramentas do ecossistema do React, estão tentando evitar que você precise se preocupar com o nome da classe. Então você usa alguma coisa de utilitário, descreve o que você quer e o estilo vai aparecer ali.

**Paulo:** Já estamos dando um passo mais profundo. É óbvio que queremos colocar para você, desde já, que não queremos fazer um tutorial em que é só copiar e colar o nosso código sem entender o que está acontecendo.

Nós queremos, a cada passo, mostrar o que está debaixo e que você tenha essa curiosidade. É assim que se vai longe em uma carreira de tecnologia, não tenha dúvidas. Para o seu futuro, você vai precisar entender: "Porque tem esse `class` aqui? Eu não escrevi isso no meu código, por que ele fez isso?", "Foi para não dar conflito com um outro possível `h1` de outro lugar, ele gerou isso em tempo real, a própria biblioteca gerou isso para nós"...

Então, começar a entender as "entranhas" da biblioteca mesmo. Estamos dando só um aperitivo. Tanto que na formação de Next que lançaremos no final dessa Imersão teremos bastante desse conteúdo. Além de uma visão geral de uso do framework, temos muito de entender e construa você mesmo um pedaço do framework".

Nossa metodologia, o modo como as imersões da Alura e todo o Aluraverso ensina é que você seja uma pessoa que quer entender o que está funcionando atrás da biblioteca, que não está satisfeita em apenas usar.

**Mario:** E nessa de construir coisas, vamos começar a criar nossos componentes agora. Falamos bastante que tem coisas diferentes juntas no código, mas também é mais fácil de separar.

Por exemplo, se quisermos dizer que o título da nossa aplicação vai ter um tamanho, cor e outras coisas específicas, podemos vir aqui na parte de cima do código e só criar outra função, podemos chamar de "Title", se quiser deixar em inglês, ou "Titulo" se quiser deixar em português. Use o nome que achar mais pertinente para o código do projeto.

Adicionaremos um `return` e já teremos a estrutura de um componente. Então, vamos colar o título `h1` dentro dele.

```
function Title() {
		return (
			<h1>	Boas vindas de volta!</h1>
		
		);
}
```

**Mario:** O que eu quero fazer aqui não é só criar uma cópia, quero dizer que teremos o nosso jeito de fazer título. 

**Paulo:** Só para ficar mais óbvio, esse `Title` não é palavra-chave, não é um tag title do HTML. Podia, inclusive, chamar "Titulo". Em vez de `Title`, vamos deixar `Titulo` para ver como fica.

Isso não é HTML, isso é algo que o React vai entender e procurar se existe algum componente no escopo com esse nome "Titulo". Se não tiver ele vai dar erro, se tiver ele substitui isso por "Boas vindas de volta".

**Mario:** Exatamente. Só de colocar isso, nós informamos que criamos a nossa tag, colocamos o `h1` com o título. Está duplicado aqui. Podemos verificar no navegador que ele parou de aplicar o estilo. 

Nesse momento, conseguimos mostrar para a galera como criar o componente, que o estilo do `style jsx` só aplica no componente a que ele pertence, e que esse `Titulo` está ignorando qualquer coisa da tag.

O que faltou para conseguirmos pegar esse valor "Boas vindas de volta" dentro da `HomePage` e jogá-lo no `h1` da função `Titulo()`?

**Paulo:** Agora, de alguma forma, temos que passar como argumento, como parâmetro da função `Titulo()`, quero pegar essa string e jogar para o `h1` dela. Como se fosse argumento1 e argumento2.

```
function Titulo(argumento1, argumento2) {
		return (
			<h1>	Está ignorando qualquer coisa da tag</h1>
		
		);
}
```

**Mario:** Isso é uma coisa importante, Paulo. Vejo que muita gente que aprende React decora essa estrutura, não vêem isso como uma função, e sim como um componente do React. É importante falar dessa questão de argumento, porque é justamente o argumento que receberemos no `Titulo`, que têm as `props` que são as propriedades que o React nos passa para que possamos trabalhar.

Se eu der um `console.log()` de `props`, repare que no console do navegador, para chegar no console clicamos com o botão direito e selecionamos "Inspecionar" e clicamos na aba "Console". E ele traz para nós um objeto.

```
Object
	children: "Boas vindas de volta!"
	[[Prototype]]: Object
```

**Mario:** Isso que aparece à direita no console, "index.js?bee7:3", são coisas internas da ferramenta. Esse "3" é referente à linha 3 do código, foi onde colocamos o `console.log()`.

O valor do props é o `children`, `children` tem o valor do "Boas vindas de volta!", que é o que estamos passando aqui no `<Titulo>` do componente `HomePage`. Esse valor que vai no miolo da tag é o que chamamos de `children`. Se pegarmos o `props.children` em `console.log(props.children)` conseguimos ver o valor do "Boas vindas de volta!".

Antes era objeto, virou "Boas vindas de volta!", se eu carregar,  o navegador mostra só o "Boas vindas de volta!".

Dado que temos o `props. children`, em teoria, é só passar esse valor aqui no meio da tag `h1` de `Titulo`. 

```
function Titulo(props) {
		console.log(props.children);
		return (
			<h1>props.children</h1>
		
		);
}
```

**Mario:** Salvei. E voltando no navegador vemos que no lugar de título ele só colocou o texto "props.children". Paulo, pegando seus conhecimentos mais gerais de programação, o que você acha?

**Paulo:** É porque ele não sabe que você está falando "por favor, pegue uma variável". O que você escrever aí nessa tag `h1` vai sair como texto, tem que usar um cifrão? Um cerquilha ou algo assim para informar que quero buscar uma variável chamada `props` e quero pegar o atributo `children` dela.

**Mario:** Para isso, basta usarmos as chaves, ou, como eu chamo, os "bigodinhos", `{}`,`{props.children}`. E o valor que estiver dentro dessas chaves é tratado como valor dinâmico do JavaScript. Se você tiver uma variável, um objeto, uma prop, você consegue receber esse valor aqui e trabalhar em cima dele.

```
function Titulo(props) {
		console.log(props.);
		return (
			<h1>{props.children}</h1>
		
		);
}
```

**Mario:** Vamos salvar. E voltou a aparecer o "Boas vindas de volta!" no navegador. Mas eu falei que a ideia do componente era começar a juntar as coisas, então podemos trazer esse style para o `Titulo` também, para começar a agrupar. Então, teremos tanto o componente com o trecho de HTML dele e com o trecho de CSS dele.

O que bate justamente nessa conversa que tivemos sobre o Material UI, ele tem lá o componente calendário, que tem todas as lógicas para montar um calendário, inclusive os estilos dele.

Por isso o pessoal começou a juntar tudo mais próximo uma coisa da outra. A gestão fica mais fácil. Você olha para um pedaço do código e vê que tudo o que você precisa está lá, o HTML, o CSS e o JavaScript.

Vou recortar o trecho do `style jsx` que está no `HomePage()` e colar no `Titulo()`.

```
function Titulo(props) {
		console.log(props);
		return (
			<h1>{props.children}</h1>
			<style jsx>{`
             h1 {
                color: red;
            }
           `}</style>
		
		);
}
```

**Mario:** Vai aparecer um erro dizendo "JSX expressions must have one parent element.",ou seja, expressões JSX devem ter apenas um elemento pai. Para resolver esse problema, por enquanto, podemos colocar uma `div` em volta, assim fica mais fácil de mexer. Agora temos, dentro do `Titulo`, uma `div`, um `h1` e o `style jsx`. 

```
function Titulo(props) {
		console.log(props);
		return (
			<div> 
			<h1>{props.children}</h1>
			<style jsx>{`
             h1 {
                color: red;
            }
           `}</style>
		   </div> 
		);
}

```

**Mario:** Vou salvar. E o título está novamente com a cor vermelha no navegador. Aí tem outra coisa, no console da página no navegador podemos ver que começamos a "sujar" o HTML, colocamos uma `div` só para resolver um pequeno problema.

O JSX tem um suporte para isso, ele nos possibilita passar uma tag vazia. Em vez de colocar `<div> </div>` podemos deixar `<> </>`. Fica uma tag meio fantasma, mas ela tira esse elemento extra que está em volta e deixar só o `h1`. Ele só serve para conseguirmos agrupar as coisas mesmo e assim colocar tanto o style quanto o `h1` juntos.

Agora, podemos colocar mais estilos, além da cor vermelha podemos passar tamanho da fonte de 24 pixels, `font-size: 24px;` e peso da fonte de 600, `font-weight: 600;`.

```
function Titulo(props) {
		console.log(props);
		return (
			<> 
			<h1>{props.children}</h1>
			<style jsx>{`
             h1 {
                color: red;
				font-size: 24px;
				font-weight: 600;
            }
           `}</style>
		   </> 
		);
}
```

**Mario:** Vou salvar. E, no “Inspecionar” do navegador, vemos que ele está aplicando tudo o que passamos no estilo. Está funcionando corretamente. Paulo, todo título necessariamente vai ser um `h1`?

**Paulo:** Não.

**Mario:** Faz sentido que a tag desse título possa mudar dependendo de onde vamos colocá-lo?

**Paulo:** Em alguns casos, sim.

**Mario:** O React também nos dá essa flexibilidade. Parece algo de outro mundo, mas basta informar que queremos que, por exemplo, o título seja `h2`, `<Titulo tag="h2">`.

```
function HomePage() {
  //JSX
  return (
      <div>
         <Titulo tag="h2"> Boas vindas de volta!</Titulo>
         <h2>Discord - Alura Matrix</h2>
      </div>
  )
}
``` 

**Mario:** Se voltarmos no console do navegador, veremos que ele tem agora a `children` e recebeu uma propriedade `tag:"h2"`. Ou seja, todos os atributos das tags do HTML viram props do seu componente. E com esse valor de tag, posso criar uma variável aqui na função `Titulo` de `const Tag = props.tag;` e podemos trocar o `h1` pela `Tag`.

```
function Titulo(props) {
		console.log(props);
		const Tag = props.tag;
		return (
		<>
			<Tag>{props.children}</Tag>
			<style jsx>{`
      h1 {
        color: red;
        font-size: 24px;
        font-weight: 600;

      }
    `}</style>
		</>
		);
}
```

**Mario:** Esse valor de texto que estamos passando passa a trocar qual tag estamos renderizando. Então você pode passar uma `div`, um `h1`, qualquer tag que você quiser aqui que ele vai fazer isso funcionar do jeito que esperamos.

Quando copiamos o estilo teve um detalhe que passou despercebido e é muito importante. Esse `style jsx`, além da prop, ele tem aqui dentro abertura de chaves e tem um recurso do JavaScript que é a template string, um recurso em que você pode vir aqui dentro e passar aquela anotação de cifrão e chaves `${}`, ou, como eu gosto de chamar, "ostentação bigodinhos", e passar algum valor dinâmico. Então podemos dizer que essa `Tag` vai gerar esse estilo também.

```
function Titulo(props) {
		console.log(props);
		const Tag = props.tag;
		return (
		<>
			<Tag>{props.children}</Tag>
			<style jsx>{`
      ${Tag} {
        color: red;
        font-size: 24px;
        font-weight: 600;

      }
    `}</style>
		</>
		);
}
```

**Mario:** Então, acabamos de criar um componente de título que funciona com qualquer tipo de tag. Isso aqui é a chave de muita empresa que começa a querer normalizar como a equipe de design fala com o pessoal de código. Não necessariamente o estilo do título da empresa tem a mesma semântica do HTML para todo lugar, então pode ter essa diferença de você querer aproveitar o estilo, mas a semântica ser diferente.

Se eu salvar e voltar para o navegador, ele aplicou no `h2` esse estilo. E se mudarmos a tag lá, ele vai mudando as coisas para nós. 

Estamos usando os poderes do React para valer agora, temos o `Titulo`, conseguimos passar qual tag ele deve ter, recebe essa tag aqui em cima no `const Tag`, passa o `children`, o conteúdo que queremos renderizar, e gerencia os estilos que essa tag de título que estamos criando vai ter.

Esses estilos não são globais, a fonte do projeto é uma coisa que fica meio global, uma definição mais genérica que temos, o body também tem uma margem, são várias coisas que o pessoal usa o estilo que chamam de reset do CSS.

Para conseguirmos fazer essa parte do reset junto com as fontes, espaçamento e tudo mais, vamos criar o nosso global style. Criaremos uma tag que terá esses estilos globais e vai aplicá-los na página inteira, `<GlobalStyle>`. Esse `GlobalStyle` é uma convenção, é como o pessoal chama esse lugar que tem os estilos globais da aplicação. Tudo que for genérico para resetar as coisas e organizar fica nesse `GlobalStyle`.

Legal que isso bate muito com o conceito de reset de CSS. Inseri a tag `<GlobalStyle>` na `HomePage()` e gerei um erro de propósito aqui, para mostrar que sempre que você tentar usar um componente que não foi criado ainda, o navegador vai apresentar esse erro "ReferenceError: GlobalStyle is not defined", ou seja, não criamos ainda.

Vamos criá-lo aqui no início do código. 

```
function GlobalStyle() {
   return (
	 
	 );

}
```

**Mario:** Como é só estilo aqui, em teoria, que valor retornamos aqui?

**Paulo:** Vamos colocar aquele `style jsx`?

**Mario:** Exatamente. Para fazer isso passamos também as chaves, a template string e o valor `global`.

```
function GlobalStyle() {
   return (
	   <style global jsx>{`
		 
		 `}</style>
	 );

}
```
 
**Mario:** Se colocarmos que tudo vai ter background da cor preta,`*{background: black}`, ele pintou tudo de preto no navegador.

Se comentarmos a tag `<GlobalStyle>` que está na `HomePage`, para comentar no JavaScript usamos essa sintaxe das chaves com barra e asterisco, `{/*<GlobalStyle>*/}`, aqui estou usando o atalho "Ctrl + Barra" para inserir esses sinais de comentário.

Para testar enquanto vai fazendo, você pode comentar e descomentar linhas, mudar valor etc. Para se acostumar com o que está acontecendo aqui.

Vou descomentar a linha `<GlobalStyle>`, e nesse estilo global podemos colocar várias coisas. Podemos resetar o `margin` que é uma coisa que muita gente faz. E colocar também o espaçamento (padding) de zero, e `box-sizing: border-box`.

```
function GlobalStyle() {
   return (
	   <style global jsx>{`
		    *{
				  margin: 0;
					padding: 0;
					box-sizing: border-box;
		 `}</style>
	 );

}
```

**Mario:** Tem um vídeo excelente da Vanessa da Alura indicando como funciona o modelo de caixa do CSS e porquê muita gente usa isso no reset e tudo mais.

Então, Paulo, isso vai crescendo, colocaremos mais coisas e é um código mais específico. Em cada projeto o pessoal vai criando o seu reset e nós resolvemos trazer algumas coisas para facilitar a vida da galera que está fazendo.

Para não termos que fazer toda essa arquitetura de CSS, porque para fazer uma aplicação não é só sentar e escrever os estilos. Tem bastante coisa a se fazer e vamos trazer coisas que nos ajudarão a fazer esses estilos. E cada pessoa vai poder personalizar, fazer não só o do Matrix, mas fazer um do Pokémon, do Cavaleiros do Zodíaco, o que vocês quiserem. Para isso, vamos pegar o `GlobalStyle` que foi definido para o nosso projeto. Vou acessar um link que também está na página da Imersão. 

**Paulo:** Nós já entendemos o funcionamento básico de um componente. Para fazer uma página bonita como esse layout da nossa página de boas-vindas do Discord Alura – Matrix, tem alguns detalhes de CSS para essa aparência. Nós vamos pegar alguns desses detalhes no código do link que está disponível na página da Imersão. Agora vai ter um pouco de copiar e colar, mas lembrando que tudo o que vamos copiar e colar aqui você já entendeu.

O que você ainda não entendeu pode ser algum detalhe de CSS, de estilo. Já o componente em si é, basicamente, como criamos. Mas agora em vez de apenas título, teremos box, input text, imagem, outros componentes menores. E poderemos trabalhar dessa forma componentizada que vimos na biblioteca do Material UI, que veremos na biblioteca Skynex UI. 

**Mario:** No Skynex UI teremos vários desses utilitários de botão, de componente, campo de texto, entre outros. Vai ter o link para você pegar, vai ter vídeo no meu canal. Criamos isso especificamente para você conseguir fazer os estilos de um jeito mais fácil, conseguir replicar e ter seu próprio tema.

Vamos começar a trazer com calma, aos poucos, e colocar no ar também. No final dessa aula colocaremos o projeto no ar, em menos de cinco minutos.

Vamos pegar os estilos no link do `GlobalStyle.js`. Um dos ajustes que fizemos aqui foi esse App fit Height, para nossa app ficar com tamanho 100%. Quem nunca fez um site em que o rodapé não ficava 100%? Ficava meio feio, no meio da página. Aqui conseguimos corrigir só com CSS.

Vamos copiar e colar no nosso código, no lugar do `GlobalStyle()`.

```
function GlobalStyle() {
  return (
    <style global jsx>{`
      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        list-style: none;
      }
      body {
        font-family: 'Open Sans', sans-serif;
      }
      /* App fit Height */ 
      html, body, #__next {
        min-height: 100vh;
        display: flex;
        flex: 1;
      }
      #__next {
        flex: 1;
      }
      #__next > * {
        flex: 1;
      }
      /* ./App fit Height */ 
    `}</style>
  );
}
```

**Mario:** Também vamos aplicar essa questão do tema. É uma coisa que às vezes passa despercebido, mas é importante também. Por enquanto, estamos usando a cor vermelha na fonte, mas no layout está branco e pode ser que na sua aplicação você queira deixar com outra cor. Para isso, padronizamos um arquivo que nomeamos de `config.json`. 


**Mario:** este arquivo `config.json` tem um spoiler do que vai ser a última aula, que são os `"stickers"` que iremos passar.

Mas também tem a parte de tema com apenas duas paletas de cores: as primárias que definem o verde do botão, e as neutras que definem a caixa, e podemos definir como quisermos.

No coolors.co, apesar dos muitos pop-ups que aparecem, conseguimos gerar novas cores apertando a tecla de espaço, e podemos ter diversos tons das cores clicando em no ícone de "View shades".

Podemos ter diferentes tons de cores usando a paleta que selecionamos, e mesmo quem não é designer pode criar uma página interessante.

Copiaremos o código de `config.json`, criaremos o arquivo na raiz do projeto com o mesmo nome e colaremos o texto.

Também rodaremos o `Format Document` usando "Ctrl + Shift + P" ou "Command + Shift + P" para formatarmos o documento.

Com isso, a cor vermelha em `color:` do `index.js` deverá vir a partir do `config.json`. Fazemos isso indo ao topo do arquivo `index.js` e importando `appConfig` a partir de `'./'` se fôssemos usar o atual, mas como subiremos da pasta "pages" para a superior, escreveremos `'../'` para que o próprio VSCode nos ajude a importar as coisas, e depois o arquivo `config.json`.

```
import appConfig from '../config.json';
```

**Mario:** Queremos trazer todo o conteúdo e armazená-lo em `appConfig`. Ao passarmos o cursor do mouse sobre este caminho, o VSCode indica que está declarado mas ninguém está usando. Então no lugar de `color: red`, usaremos a sintaxe de cifrão e chaves ou "ostentação e bigodinhos", que receberá `appConfig.` e, após o ponto, é sugerido os próximos valores possíveis.

Portando, digitaremos `appConfig.theme.colors.meutrals.`, e após o ponto teremos várias opções de valores, que são as escalas de cor muito usadas por designer e empresas.

Escolheremos `[000]` entre colchetes e salvaremos.

```
//código anterior omitido

function Titulo(props) {
	console. log(props) ;
	const Tag = props.tag;
	return (

		<>
			<Tag>(props.children:</Tag>
			<style jsx>("`
			${Tag} {
				color: ${fappConfig.theme.colors.neutrals[000]};
				font-size: 24px;
				font-weight: 600;
			}
			`}</style>
		</>
	);
}

//código posterior omitido
```

**Mario:** Feito isso, voltaremos ao navegador e teremos um erro "Legacy octal escape is not permitted in strict mode", mas para resolver esse problema, basta colocar este valor numérico da cor como string da chave `.neutrals['000']` entre aspas simples.

Feito isso, atualizaremos a página e, ao abrirmos o inspetor de código, veremos a cor branca. Se colocássemos `'900'` por exemplo, já seria uma cor cinza bem escuro.

Podemos trabalhar com isso, mas agora há vários componentes para criarmos.

**Paulo:** Isso será para refletirmos a página que queremos

**Mario:** Para ganharmos tempo e focarmos em React, também passaremos essa base do template da página, a qual você pode alterar como quiser, e já fornecemos um suporte todo integrado com a biblioteca SkynexUI no Storyboard.

**Paulo:** Vale lembrar que esta lib foi criada e desenvolvida por brasileiros, principalmente o Mario Souto.

**Mario:** Exatamente, e ela foi toda pensada para simplificar o acesso mesmo, então possui suporte para ícones, podemos mudar para ícone do Ebay, Facebook, entre outros.

Conforme escolhemos as opções, a biblioteca vai gerando o componente com as configurações, então podemos copiar o código e explorar os recursos.

O mais interessante é que ela usa tudo o que já fizemos, em que cada componente é a mesma coisa que fizemos em nosso `Titulo()`. Portanto, recebe até o CSS dinamicamente.

Por exemplo, podemos ir ao componente React `HomePage` e dizer que temos um `style`,o qual receberá `backgroundColor:` como `'black'` para termos um fundo preto.

```
//código anterior omitido

// Componente React

function HomePage() {
// JSX
	return (
		<div style={{ backgroundColor: 'black'}} >
			<GlobalStyle />
			<Titulo tag="h2">Boas vindas de volta!</Titulo>
			<h2>Discord - Alura Matrix</h2>
		</div>
	)
}

export default HomePage
```

**Mario:** Salvando desta forma e atualizando a página no navegador novamente, veremos que o fundo ficou preto. Porém, o `style` não nos permite trabalhar com resoluções da tela, apenas com media queries com tela pequena, tela grande, tela de celular e etc.

Mas se formos na documentação do SkynexUI no Storyboard e acessar o componente "Box Component" na lista lateral, poderemos notar que, se passarmos uma propriedade chamada `styleSheet` como uma "folha de estilo".

Na verdade, podemos passar tanto seu valor quanto às resoluções. Podemos alterar os nomes das cores em cada um dos atributos da forma como quisermos.

No Storyboard, podemos clicar no ícone de resolução de tela na aba superior e testar os diferentes tamanhos de exibição.

**Paulo:** Encontramos o link do Storybook aqui, com a documentação dos componentes. É uma live em que podemos pegar os componentes e testá-los.

**Mario:** Exato. Também deixarei um vídeo no canal aqui, para que as pessoas possam criar a documentação no Storybook corretamente. Perceberemos que tudo que mudamos foi refletido no texto, então se quisermos copiar, será exatamente o código do tema configurado.

Então é muito prático para termos autonomia dentro de um time. Particularmente, gosto muito dessa biblioteca e fico feliz em compartilhar tudo o que usamos até agora.

Quando clicamos no valor da tag, aparece e descrição de quais tags HTML podemos passar para os componentes, então está pronto para uso!

Para isso, temos que fazer a instalação. Iremos novamente ao VSCode, abriremos o terminar e faremos "Ctrl + C". Pararemos o processo e rodaremos `yarn add @skynexui/components`.

Se acessarmos este <a href="https://GitHub.com/skynexui/components">link do GitHub</a>, encontraremos vários elementos interessantes. A Vercel é patrocinadora desse projeto, então libera o acesso.

A Alura também é sponsor e acredita neste prometo, e poderemos copiar o comando tanto via `yarn` quanto via `npm`. Há todos os porquês para podermos avançar.

Lembrando que estamos livres para usarmos o que quisermos, então por mais que tenhamos essa versão usando o `styled-jsx`, também poderíamos usar o `styled-components`, mas a questão é que teremos que fazer todos os componentes manualmente, oq eu daria muito mais trabalho.

Mas no próprio GitHub da Vercel neste link, encontraremos vários exemplos, e inclusive o `pull request` aberto para exercitarmos essa lib que estamos usando.

Ao clicarmos em "with-styled-components", teremos a mesma estrutura base que aprendemos a criar no caminho, então não teremos mais dúvidas. Encontraremos o `package.json`, os scripts, as dependências, o que tem a mais e a menos e etc. Assim teremos mais autonomia para trabalhar da melhor forma.

Depois de instalarmos no terminal do VSCode, iremos ao `index.js` de "pages" e faremos o `import` a partir de `'@skynexui/components'`. Teremos vários componentes, como a caixa, o botão, ícone, imagens, campos de texto e etc. Como estamos fazendo um por um, importaremos o `Box, Button, Text, TextField, Image`.

```
import { Box, Button, Text, TextField, Image } from '@skynexui/components';
import appConfig from '../config.json';

//código posterior omitido
```

**Mario:** Já mais adiante para a parte do miolo, comentaremos o que fizemos na função `HomePage()` para não termos um erro por enquanto, e abaixo deste colaremos a estrutura inteira a partir de `PaginaInicial()` disponível neste link.

O `export default` define o padrão do arquivo que será a página. Formataremos o documento, chamaremos `yarn dev` no terminal e abriremos no navegador novamente.

Com isso, teremos um Server Error dizendo que o `Title` não está definido, então mudaremos para `<Titulo>`.

**Paulo:** É verdade, nós mudamos. Mas quem quiser pode mudar também.

**Mario:** Exatamente, por isso temos o link com tudo corrigido disponibilizado para as alunas e alunos.

Porém, na função `Titulo()`, poderemos colocar qualquer tag, mas não há uma tag padrão, e temos que indicar isso. Então, caso não tenha nada em `props.tag`, adicionamos `||` para pegar o valor padrão caso haja, e se não houver, pega o `'h1'`.

```
//código anterior omitido

function Titulo(props) {
  const Tag = props.tag || 'h1';
  return (
    <>
      <Tag>{props.children}</Tag>
      <style jsx>{`
            ${Tag} {
                color: ${appConfig.theme.colors.neutrals['000']};
                font-size: 24px;
                font-weight: 600;
            }
            `}</style>
    </>
  );
}

//código posterior omitido
```

**Mario:** Com isso, teremos tudo funcionando corretamente. Teremos nosso título e `h1` por padrão, mas se formos até o `<Titulo>` que acabamos de corrigir e passarmos a `tag` como `"h2"` por exemplo, o programa irá mudá-lo, pois só pega o valor de `'h1'` caso nada passe um valor para `props.tag`. Desta forma, podemos ter a versão do projeto rodando sem problemas.

Mas se formos para `config.json` e mudarmos a cor primária de `"500":` para `"red"`, veremos a diferença interessante na versão vermelha da nossa página.

Podemos usar qualquer cor, mas o importante é fazer o projeto customizado e nos mandar para colocarmos no ar.

**Paulo:** Perfeito. Lembrando, a tag `<Box>` é da biblioteca que estamos usando, e ela recebe como parâmetro várias coisas de CSS que podemos mandar. Quem está fazendo pode não saber o que é cada elemento, então podemos até deletar para ver o que acontece e entender melhor.

A parte de CSS não é nosso foco, mas já estamos entregando com configurações bem bonitas para seu portfólio. Mas claro, quem domina CSS pode explorar mais as possibilidades.

Quem não tem domínio, não precisa se preocupar com essa parte de código dos componentes do React, e sim apenas a estilização, como atributos do photoshop ou Figma para customizar.

Reepararemos que tudo está em `<Box>`, e se deletarmos o `styleSheet` ficará feio, mas o que queremos irá funcionar.

**Mario:** Exato, se fizermos isso  voltarmos ao navegador, veremos as diferenças visuais na página, mas as funcionalidades estão funcionando. Com isso, as pessoas poderão ter algo mais apresentável no portfólio.

Também é interessante assistir a série "Pare de chutar CSS" com Marco Bruno neste link para melhorar as habilidades.

Não há nenhuma magia, é CSS da mesma forma com as tags normal, e cada `<Box>` virará uma `<div>` por padrão, então podemos ir ao navegador e inspecionar cada um deles.

Como são `<div>` normais, podemos passar outra tag para termos tudo certo para colocarmos o que quisermos.

Terei o meu usuário por padrão, mas nas próximas aulas, ao trabalharmos mais com estado, campos de textos e outras customizações, podemos mudar.

Por enquanto já colocaremos no ar, pois já passamos bastante conteúdo nesta aula. Para isso, colocaremos no site da empresa por trás do Next.js, que é a Vercel.

Na <a href="https://Vercel.com/home">Home da Vercel aqui</a>, iremos nos familiarizar. A proposta é facilitar o trabalho e colocar o projeto no ar o mais rápido possível.

Para isso, a única coisa que temos que fazer é subir o código no GitHub. Então criaremos um novo repositório chamado "aluracord-matrix", mas podemos colocar qualquer outro nome que quisermos.

O nome do projeto é importante para montarmos a vitrine, mas explicaremos melhor. Deixaremos público, mas por enquanto ficará privado para as pessoas não verem antes de terminarmos a aula.

Criado o projeto, há o tutorial do Git com `git init`. Então copiaremos isso, fecharemos os arquivos no VSCode e escreveremos o comando no terminal.

Ao executarmos, receberemos uma mensagem dizendo que há muitos arquivos, e nos pergunta se queremos colocar no `.gitignore`. Fecharemos a mensagem e perceberemos que está monitorando cerca de dez mil arquivos no ícone lateral.

Para resolvermos isso, faremos o comando `npx gitignore node` no terminal para gerarmos o arquivo para o `git`, que é essa ferramenta de compra de versão que irá monitorar o arquivo, gerenciar as versões e outras tarefas, a qual irá ignorar tudo o que tiver dentro deste arquivo `.gitignore`.

**Paulo:** esse `npx` já veio com o Node.js quando instalamos.

**Mario:** Exato, está por padrão. Se instalarmos o Node.js, teremos `node -v`, o `npm -v` e o `npx` junto, o qual é o atalho para o `npm` rodar alguma coisa mais remota sem instalarmos na máquina.

Na aba de "source control" do `git`, podemos clicar na seta circular para recarregar. Com isso, mostrará somente cinco arquivos ou mais, se tivermos criado mais.

Clicamos em "Staged Changes" na aba lateral do VSCode, que é equivalente ao comando `git add .` no terminal. Fazendo o refresh, exibiremos "Staged Changes", que é justamente o próximo comando que o GitHub exibe no tutorial.

Em seguida, teremos o `git commit` para criarmos um pacote com todas as orientações. Inclusive, há uma série "Git e GitHub para sobrevivência" aqui na plataforma Alura comigo, Mario Souto, aprofundando no assunto para quem se interessar. Há muito conteúdo avançado, mas as primeiras aulas são básicas.

Depois, teremos o comando `git branch` para renomearmos caso tenhamos nossa Branch Master ou algo do gênero. No caso já está como `main`. Após isso, colocaremos o `git remote add origin` no terminal para vincularmos nossa pasta local com a remota do GitHub, mas em breve entenderemos o porquê de "pasta".

Por fim, escreveremos o `git push` para "empurrar" nosso código para a pasta remota. Nesta mesma página do GitHub, clicaremos no ícone de engrenagem ao lado do título "About" no canto superior direito para abrirmos a janela de "edit repository details".

No campo "Description" colocaremos a descrição do projeto, como "Projeto criado na Imersão React com a @alura, @omariosouto e o @peas".

Já em "Topics", adicionaremos "aluracord", "imersao-react" e várias opções para marcarmos e exibirmos no "About".

Para finalizarmos, iremos publicar. Portanto, iremos à home da Vercel, faremos o login em que basta ter uma conta no GitHub para acessar, abriremos o dashboard, clicaremos em "New Project", depois em "aluracord-matrix" para importarmos apertando o botão de "Import" ao lado do projeto, e irá aparecer automaticamente.

Com isso, chegaremos em "Configure Project" onde poderemos alterar o nome do projeto se quisermos. Por fim, clicaremos em "deploy" e pronto.

Aguardaremos o build e acessaremos a parte com título de "Congratulations!" indicando que publicamos com sucesso, e em que poderemos ver o nosso trabalho exibilido na tela.

Ao clicarmos em "Go to Dashboard", veremos a url do projeto, e inclusive poderíamos comprar um domínio, mas por enquanto conseguimos cumprir nosso objetivo.

Nas próximas aulas, preencheremos alguns campos, faremos os botões funcionarem corretamente, entre outras ideias.

Agora é o momento de compartilhar conosco, pois queremos ver as criações para fazermos uma exposição de projetos.

**Paulo:** Teremos uma live para mostrar os projetos mais interessantes. Como ainda criaremos o chat e tudo irá se interligar, veremos que o projeto ficará incrível!

Não somente em questão visual, mas também de funcionalidades. É justamente o que queremos, afinal o Desenvolvimento em T se aprofunda em front-end mas terá noções de back-end e UX.

Na próxima aula, começaremos repassando este código para revisarmos, e em seguida partiremos para as funcionalidades e criação de outra tela.

**Mario:** Sim, estruturaremos essa parte para entendermos bem, aprenderemos a criar novas páginas com algumas novas configurações, e avançaremos para a tela do chat, rodaremos o chat offline para depois fazermos integração com a parte remota, entre outros processos para completarmos o melhor projeto possível.

**Paulo:** As próximas aulas serão mais curtas pois fomos bastante minuciosos nesta, e neste momento final vimos bastante cola de CSS, e inclusive as tags podem ser alteradas e criadas.

**Mario:** Exatamente! O `<Box>` é uma `<div>`, e o título já é uma caixa também, pois podemos passar qualquer tag, basta criarmos.

Algo que aprendemos bastante é tentar copiar as libs que usamos para aprendermos mais sobre as ferramentas.

**Paulo:** Perfeito, estamos aguardando vocês no Discord para conversarmos e compartilharmos ideias juntas e juntos, afinal queremos que vocês participem do Aluraverso.

A Alura se expande cada vez mais com pessoas de diferentes profissões que aprenderam muito conosco, o que veremos bastante mais adiante.

Estou muito animado de trazer mais uma Imersão React para vocês, que é um framework muito importante. Mas também vamos além, e mostramos Nex.js, JavaScript, conceitos por trás, e não só copiando e colando mecanicamente.

Isso também é importante, mas  queremos aprofundar mais para que vocês possam conhecer mais sobre como a Alura funciona e pensa os cursos e formações.

Assim, conseguirmos ter a experiência em grupo de uma verdadeira escola. Portanto, até breve!

**Mario:** Até a próxima aula!








