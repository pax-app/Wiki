# Documento de Visão

O documento de visão captura restrições de design e requisitos de alto nível para que o cliente possa compreender o sistema que será desenvolvido. Seu objetivo é fornecer uma visão ampla do produto que se pretende desenvolver, sem se aprofundar em detalhes.

## Histórico de Revisão

|Data| Versão |Modificação|Autor|
|:---:|:---:|:---:|:--:|
| 27/08/2018 |   0.1  | Abertura do documento| Marcos Nery |
| 28/08/2018 |   0.4  | Preenchimento dos tópicos 1 e 4| Marcos Nery|
| 28/08/2018 |   0.5  | Preenchimento do tópico 3| Marcos Nery|
| 28/08/2018 |   0.6  | Preenchimento do tópico 1.3| Marcos Nery|
| 29/08/2018 |   0.8  | Preenchimento dos tópicos 1.2, 1.4 e 1.5| Marcos Nery|
| 30/08/2018 |   1.0  | Preenchendo tópico 4, de visão de produto| Marcos Nery|
| 30/08/2018 |   1.1  | Correções ortográficas| Marcos Nery|
| 01/09/2018 |   1.2 | Adicionando explicação do documento| Esio Freitas|

## 1. Introdução
Nesta introdução serão abordados tópicos referentes a uma visão geral do produto, definindo seu propósito, escopo, definições, acrônimos, abreviações e referências.

### 1.1 Finalidade
Esse documento visa especificar todo o escopo de funcionamento da aplicação, deixando claro seu objetivo, a razão de sua necessidade e a forma como busca solucionar os problemas aos quais se propõe, deixando claro possíveis restrições. Dessa forma, sua principal utilidade objetiva também, ao esclarecer o que é o sistema para os desenvolvedores, clientes e usuários, estabelecer entre os mesmos um alinhamento de ideias.

### 1.2 Escopo

O Pax é uma aplicação que visa ajudar pessoas a resolverem alguns dos seus problemas diários que requerem a contratação de serviços. Sendo estes de habilitação técnica elevada, como os realizados por um eletricista ou encanador, ou mesmo coisas simples como alguém para passear com os cachorros. 

Qualquer indivíduo que realize de forma autônoma algum tipo de trabalho pode se cadastrar no aplicativo e oferecer nele seus serviços, para que então os usuários que procuram contratar esses serviços possam contata-los e pela própria aplicação fechar negócio.


### 1.3 Não Escopo

Não cabe a aplicação estabelecer os parâmetros para como um determinado serviço deverá ser realizado. Também fogem do escopo da aplicação coisas como serviços por agendamento. O corpo alvo de prestadores de serviço é de trabalhadores sem vinculo empregatício, sendo assim, também não é visado o atendimento das necessidades de empresas.

### 1.4 Definições, Acrônimos e Abreviações

Para conhecer mais profundamente algumas definições terminológicas referentes ao escopo do projeto, pode ser checado o [glossário](docs/DS/dinamica-e-seminario-2/glossario.md).

### 1.5 Visão Geral

Nessa Wiki podem ser encontrados muitos documentos que definem cada uma das frentes envolvidas nesse projeto, bem como aprofundamentos dentro dos seus objetivos e recursos. Neste documento, alguns pontos principais acerca da descrição do problema em sí, do público alvo, e de visão de produto poderão ser encontrados nos tópicos seguintes.


## 2. Posicionamento

### 2.1 Oportunidade de Negócios

É grande a demanda diária das pessoas pelo consumo de serviços gerais, tais como um encanador, alguém para fazer manutenção de equipamentos eletrônicos ou até mesmo alguém para passear com os cachorros. Além disso, o mercado de trabalho informal no Brasil é expressivo, chegando a um total de mais de 39 milhões de trabalhadores de acordo com o IBGE, muitos destes profissionais independentes não tem um meio fácil para chegar aos seus clientes e divulgar seus serviços. Partindo de necessidades como essas, a aplicação aqui descrita busca servir de meio entre prestador e consumidor de serviço para que estes negociem os trâmites do trabalho a ser realizado, dando ao consumidor as facilidades que ele precisa para achar um prestador para o serviço que ele deseja consumir.

### 2.2 Descrição do Problema

|||
|:--:|:--:|
|O problema de|encontrar profissionais para prestar um serviço ou encontrar pessoas que precisem consumir um serviço|
|afeta|profissionais independentes e pessoas quaisquer com suas necessidades diárias|
|tendo o impacto de|as pessoas acabarem tendo que contratar um profissional qualquer que conseguiram achar, sem terem como escolher dentre opções diferentes que podem variar em custo/qualidade. Já o profissional acaba não conseguindo tantos clientes quanto poderia, mesmo havendo demanda, por não ter como chegar a eles. |
|Para este, uma boa solução seria |uma plataforma que conecte prestador a consumidor de serviços e facilite entre eles os trâmites da negociação, dando também ao consumidor uma forma fácil de pesquisar por profissionais dispostos a prover determinado serviço.|


### 2.3 Sentença de Posição do Produto
|||
|:--:|:--:|
|Público alvo|Profissionais independentes e consumidores de serviços gerais|
|Carência|Algo que conecte os profissionais que prestam um serviço as pessoas que podem consumi-lo|
|Solução|Um aplicativo mobile que permite ao usuário pesquisar por um profissional que preste um serviço do qual a mesma necessite e então ajuda os dois lados a cuidar dos trâmites presentes na negociação e realização do serviço.|
|Descrição da solução|Um profissional pode através do aplicativo cadastrar seus serviços, para que então um usuário consumidor possa acha-lo ao pesquisar por um prestador daquele serviço. Depois disso, ao escolher sua opção, o consumidor e o prestador tem recursos como chat na aplicação para negociarem os trâmites do trabalho. É feito também através do aplicativo o pagamento.|
|Diferenciais|Robusto sistema de busca e filtragem dos profissionais, pagamento dentro do app, chat entre as duas partes, mecanismos para validar a autenticidade do profissional.|



## 3. Perfil dos usuários

### 3.1 Prestador de serviços
|||
|:--:|:-:|
|Representante|Profissionais independentes|
|Descrição|Pessoas que prestam algum serviço de forma independente, sem vínculo trabalhista|
|Tipo|Usuário final de qualquer grau de conhecimento técnico|
|Responsabilidades|Cadastrar um perfil, que incluí algumas informações pessoais além do cadastro dos tipos de serviço que tal profissional realiza, negociar pelo chat do aplicativo os trâmites referentes a um trabalho com o seu cliente após contatado, realizar o trabalho, e então receber através do app o seu pagamento.|
|Críterios de sucesso|Ter a ajuda da plataforma para ser contatado por consumidores interessados no seu serviço, conseguir se comunicar eficientemente com o cliente através da plataforma, conseguir receber através do app o pagamento feito pelo cliente.|

### 3.2 Consumidor de serviços
|||
|:--:|:-:|
|Representante|Consumidores de serviços gerais|
|Descrição|Pessoas cujas necessidades diárias as levem a precisar da contratação de um serviço qualquer|
|Tipo|Usuário final de qualquer grau de conhecimento técnico|
|Responsabilidades|Cadastrar um perfil com algumas informações básicas sobre sí, escolher na plataforma um profissional que preste o serviço no qual ele está interessado, negociar os trâmites envolvidos na prestação do serviço através do chat na plataforma e realizar o pagamento após o cumprimento do mesmo.|
|Críterios de sucesso|Conseguir achar um profissional que preste o serviço desejado, ter variabilidade de escolhas possíveis, conseguir se comunicar com o contratado através da aplicação, realizar o pagamento através do meio mais conveniente.|


### 3.3 Ambiente do Usuário

A aplicação tem como alvo dispositivos mobile cujo sistema operacional operante é o Android.

### 3.4 Principais Necessidades dos Usuários

#### 3.4.1 Usuário consumidor de serviços
 
|Necessidade|Prioridade|Solução Atual|Soluções Propostas|
|:--:|:--:|:--:|:--:|
|Buscar por um prestador de determinado serviço|Alta|Pedir indicações, pesquisar manualmente em jornais/listas/internet|Compilado na aplicação de prestadores de serviços gerais disponíveis na área/horário que poderão ser escolhidos pelo consumidor.|
|Conseguir se comunicar com o prestador contratado|Alta|Utilizar meios de comunicação pessoais, como aplicativos de mensagens instantâneas, ou então ligando diretamente para o prestador.|Chat dentro do próprio aplicativo|
|Realizar o pagamento através do aplicativo|Alta|Pagar em dinheiro ou depender do prestador possuir maquina de cartão de crédito|Mecanismos dentro do aplicativo pelos quais o usuário consumidor paga da forma que preferir e o dinheiro vai para a conta do contratado|
|Avaliar o prestador contratado e ver as avaliações do mesmo|Alta|Perguntar, quando possível, para pessoas que tenham contratado o profissional como foi a experiência|Sistema de avaliações no aplicativo pelo qual o consumidor pode avaliar o contratado|

#### 3.4.2 Usuário prestador de serviços

|Necessidade|Prioridade|Solução Atual|Soluções Propostas|
|:--:|:--:|:--:|:--:|
|Cadastrar os serviços prestados para ser encontrado pelos interessados|Alta|Anunciar seus serviços por meio de jornais/panfletos/internet/etc|Perfil com os serviços prestados no aplicativo, que terá visibilidade e poderá ser contratado por qualquer consumidor interessado na área que use o aplicativo|
|Conseguir se comunicar com o seu contratante|Alta|Utilizar meios de comunicação pessoais, como aplicativos de mensagens instantâneas, ou então ligando diretamente para o cliente.|Chat dentro do próprio aplicativo|
|Receber pagamento através do aplicativo|Alta|Aceitar apenas dinheiro ou alugar uma máquina de cartão de crédito ou qualquer serviço de terceiros que permita receber os pagamentos por cartão|Mecanismos dentro do aplicativo pelos quais o usuário paga da forma que preferir e o dinheiro vai para a conta do contratado|
|Avaliar o contratante|Alta|Comentar com pessoas do meio de trabalho como foi a experiência com determinado consumidor|Sistema de avaliações no aplicativo pelo qual o prestador pode avaliar o consumidor|


### 3.5 Alternativas e Concorrências

Para um melhor comparativo entre os concorrentes e soluções alternativas para cada um dos problemas aos quais a aplicação se propõe a resolver foi feito um Benchmarking, que pode ser visto [aqui](docs/DS/dinamica-e-seminario-1/Benchmarking.md).


## 4. Visão Geral dos recursos do produto 

### 4.1 Cadastro de perfil

Ambos os tipos de usuário devem cadastrar um perfil para acessar a plataforma. Nesse perfil constam algumas informações básicas do usuário e sua avaliação. No caso do perfil de prestador de serviço além disso podem ser encontrados também os serviços que aquele prestador realiza e um histórico de trabalhos realizados. 

### 4.2 Pesquisa por serviços 

No sistema há um recurso pelo qual o usuário consumidor poderá pesquisar pelo serviço que quer consumir, gerando listas de prestadores realizando aquele serviço na área. Essa lista pode ser ordenada por características como preço ou avaliação e o usuário também pode navegar por categorias de serviço.

### 4.3 Chat 

Ao escolher um prestador de serviço existe na aplicação um chat para que o consumidor e o prestador do serviço possam conversar e negociar quaisquer trâmites necessários para o serviço.

### 4.4 Pagamento in-app

O consumidor poderá pela própria aplicação realizar o pagamento pelo trabalho contratado, que será então depositado na conta do prestador.

### 4.5 Sistema de avaliação

Existe na aplicação um sistema de feedback avaliativo, pelo qual tanto o prestador quanto o consumidor do serviço poderão se avaliar após a realização do serviço contratado. Dessa forma, ambos os tipos de usuário terão uma classificação baseada nas avaliações que receberam.
