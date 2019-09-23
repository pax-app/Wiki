# Documento de Arquitetura

Este documento visa especificar de forma básica alguns tópicos referentes ao Documento de Arquitetura que será desenvolvido no decorrer da disciplina.

## Histórico de Revisões

|    Data    | Versão |                    Descrição                    |   Autor(es)   |
| :--------: | :----: | :---------------------------------------------: | :-----------: |
| 08/09/2019 |  0.1   |              Criação do documento               | Felipe Campos |
| 15/09/2019 |  0.2   |        Adição do Diagrama de arquitetura        |  Lucas Dutra  |
| 15/09/2019 |  0.3   | Atualizando descrição dos frameworks utilizados |  Lucas Dutra  |
| 15/09/2019 |  0.4   |     Inserindo descrições dos microsserviços     |  Lucas Dutra  |
| 15/09/2019 |  0.5   | Atualizando estrutura do documento e descrições | Felipe Campos |
| 15/09/2019 |  0.6   | Arrumando linkagem para o Léxico "Pax"          | Rogério Júnior |
| 15/09/2019 |  0.7   | Adição da visão de casos de uso                 | Marcos Nery |
| 21/09/2019 |  0.8   | v2 do diagrama de contexto dos microsserviços   | Youssef Muhamad e Lucas Dutra |
| 22/09/2019 |  0.9   |         Formatando referências ABNT         |                 Rogério Júnior               |

## 1. Introdução

### 1.1. Finalidade

Este documento de arquitetura tem a função de especificar e documentar decisões arquiteturais relevantes na produção e implementação do projeto Pax descrevendo os aspéctos do sistema de forma clara, estruturada e objetiva.

### 1.2 Escopo

Este documento se aplica ao processo de desenvolvimento do Pax App, aplicação desenvolvida na disciplina Arquitetura e Desenho de Software, na Universidade de Brasília.

## 2. Representação Arquitetural

Modelo de representação dos serviços implementados e as interações estabelecidas entre esses serviços, bem como a natureza dessas interações.

### 2.1 Tecnologias 

### 2.1.1 Front End

* **Flutter**      

<p style="text-align:justify">&emsp;&emsp;<i>Flutter</i> é o kit de ferramentas de interface do usuário do Google para criar aplicativos belos e compilados nativamente para dispositivos móveis, Web e desktop a partir de uma única base de código. É um framework que possui como linguagem base o <i>Dart</i> </p> 


### 2.1.2 Back End

* **Flask**     

<p style="text-align:justify">&emsp;&emsp;<i>Flask</i> é um micro-<i>framework</i> de <i>python</i>, possui toda a flexibilidade da linguagem <i>python</i> e provê um modelo simples para desenvolvimento <i>web</i>. É baseado em 3 pilares: <i>Werkzeug</i>, uma biblioteca para desenvolvimento de <i>apps</i> WSGI, Jinja2, um <i>template engine</i> escrito em <i>Python</i> e <i>good intentions</i>, que são alta qualidade na legibilidade, liberdade de estruturar o <i>app</i> na maneira que desejar, entre outros aspectos.</p>

* **Express**        

<p style="text-align:justify">&emsp;&emsp;O <i>Express</i> é um framework para aplicações web em Node.js. Pequeno e flexível, fornecendo um conjunto robusto de recursos para aplicativos web e mobile.</p>

### 2.1.2 Banco de dados

* **PostgreSQL** 

<p style="text-align:justify">&emsp;&emsp;<i>PostgreSQL</i> é um poderoso sistema de banco de dados relacional de objetos de código aberto, com mais de 30 anos de desenvolvimento ativo, que ganhou uma forte reputação de confiabilidade, robustez de recursos e desempenho.</p>

* **Firebase** 

<p style="text-align:justify">&emsp;&emsp;O Realtime Database do Firebase é um banco de dados não relacional (NoSQL) que permite a distribuição de conteúdos cross-platform.</p>

### 2.2 Motivação Arquitetural


<p style="text-align:justify">&emsp;&emsp;A motivação para a escolha de cada tecnologia empregada no desenvolvimento desta aplicação pode ser consultada em maiores detalhes em nosso estudo sobre tecnologias.</p>

[Estudo sobre Tecnologias](https://pax-app.github.io/Wiki/#/docs/DS/dinamica-e-seminario-2/Tecnologias)
### 2.3 Abordagem Arquitetural

* **Microsserviços**   

<p style="text-align:justify">&emsp;&emsp;A arquitetura de microsserviços é uma abordagem que desmembra uma aplicação única em blocos de pequenos serviços independentes. Esses serviços executam o seu próprio processo e se comunicam, muitas vezes, por meio de métodos HTTP. A divisão dos serviços neste projeto foi feita levando em conta a abordagem de sub-domínios, técnica que leva em conta o ponto de vista de negócio para estabelecer a distribução de responsabilidades entre os serviços.</p>
<p style="text-align:justify">&emsp;&emsp;No <i>software</i> descrito neste documento os módulos serão:
<ul>
  <li><b>User</b>, bloco responsável por toda interação do usuário, como login, registro; </li> 
  <li><b>Rating</b>, responsável pelo tratamento e armazenamento das avaliações entre usuários da aplicação; </li>
  <li><b>Pax</b>, responsável por gerenciar os <a href="#/docs/DS/dinamica-e-seminario-2/lexico.md?id=l8">pax</a> feitos entre consumidor de serviços e prestador de serviços;</li>
  <li><b>Payment</b>, responsável por efetuar e gerenciar os pagamentos realizados após o <a href="#/docs/DS/dinamica-e-seminario-2/lexico.md?id=l8">pax</a> concluído; </li>
  <li><b>Report</b>, bloco responsável pela interação de reports que podem ser feitos ao <a href="#/docs/DS/dinamica-e-seminario-2/lexico.md?id=l8">pax</a> necessário; </li>
  <li><b>Chat</b>,  será um serviço responsável por estabelecer e orquestrar a comunicação por chat entre dois usuários; </li>
  <li><b>Category</b>,  será um serviço responsável por armazenar e gerenciar as categorias de serviço disponíveis na aplicação; </li>
  <li><b>Gateway</b>, serviço responsável por intermediar a comunicação entre o Back-end e o Front-end.</li>
</ul>
</p>

* **Comunicação entre os serviços**        

<p style="text-align:justify">&emsp;&emsp;Comunicação entre os serviços será feita por meio de uma <i>API Gateway</i>, a qual será responsável por fazer o intermédio entre os microsserviços por meio de métodos do protocolo HTTP. </p>

### 2.4 Diagrama de contexto

![Diagrama de Arquitetura](../../../assets/DiagramaContextoV2.png)

## 3. Restrições e Metas Arquiteturais

### Metas

|     Metas      |                                                                            |
| :------------: | :------------------------------------------------------------------------: |
| Escalabilidade |                       A aplicação deve ser escalável                       |
|   Segurança    | A aplicação deve tratar de forma de segura os dados sensíveis dos usuários |
|     Deploy     |                A aplicação deve possuir deploy automatizado                |

### Restrições

|  Restrições   |                                                                |
| :-----------: | :------------------------------------------------------------: |
| Conectividade |   É necessária a conexão com internet para utilização do App   |
|  Plataforma   |         A aplicação terá suporte somente para Android          |
|    Público    |  A aplicação será desenvolvida voltada ao público brasileiro   |
|   Linguagem   |      A aplicação será desenvolvida em português do Brasil      |
|    Equipe     |             A equipe possui apenas 10 integrantes              |
|     Prazo     | O escopo proposto deve ser terminado até o final da disciplina |


## 4. Visão de Casos de Uso

Abaixo segue o diagrama com os casos de uso da aplicação, visando expor os caso de uso do sistema através da representação de cada um dos atores envolvidos no seu uso.

### 4.1 Atores envolvidos

#### 4.1.1 Usuário consumidor de serviços

Como definido no Léxico [L3](../dinamica-e-seminario-2/lexico.md#L3), é o usuário que utiliza o aplicativo com a finalidade de consumir algum dos serviços gerais oferecidos.

#### 4.1.2 Usuário prestador de serviços

Como definido no Léxico [L2](../dinamica-e-seminario-2/lexico.md#L2), é o usuário que utiliza o aplicativo com a finalidade de se colocar a disposição para ser contratado para realizar algum serviço.

#### 4.1.3 Serviço de Suporte do PAX 

<p style="text-align:justify">&emsp;&emsp;Equipe interna responsável por prestar suporte aos usuários do aplicativo solucionando problemas que possam aparecer durante a realização de um serviço. Sendo estes portanto os responsáveis por tomar medidas mediante a reclamações feitas por usuários acerca de inconvenientes de quaisquer categorias dentro do fluxo da prestação/contratação de um serviço.</p>

#### 4.1.4 Serviço bancário externo

<p style="text-align:justify">&emsp;&emsp;Organizações bancarias responsáveis pelo processamento dos pagamentos feitos pelo aplicativo.</p>

### 4.2 Diagrama

![CasosDeUso](../../../assets/arquitetura/PAXCasosDeUsoV2.png)


## Referências 

- DONG, Tao. **Flutter**. [S. l.], 2019. Disponível em: https://medium.com/flutter. Acesso em: 15 set. 2019.
- **FLASK (FRAMEWORK WEB)**. In: WIKIPÉDIA, a enciclopédia livre. Flórida: Wikimedia Foundation, 2019. Disponível em: <https://pt.wikipedia.org/w/index.php?title=Flask_(framework_web)&oldid=55329171>. Acesso em: 15 set. 2019.
- MALLAWAARACHCHI, Vijini. **10 Common Software Architectural Patterns in a nutshell**. [S. l.], 2017. Disponível em: https://towardsdatascience.com/10-common-software-architectural-patterns-in-a-nutshell-a0b47a1e9013. Acesso em: 15 set. 2019.
- **NODE.JS**. In: WIKIPÉDIA, a enciclopédia livre. Flórida: Wikimedia Foundation, 2019. Disponível em: <https://pt.wikipedia.org/w/index.php?title=Node.js&oldid=55592828>. Acesso em: 15 set. 2019.
- PANT, Prabhu. **A complete guide to PostgreSQL**. [S. l.], 2018. Disponível em: https://medium.com/@heyPrabhu/a-complete-guide-to-postgresql-e4d1cefb9866. Acesso em: 15 set. 2019.
- RICHARDSON, Chris. **Pattern**: Decompose by subdomain. [S. l.]. Disponível em: https://microservices.io/patterns/decomposition/decompose-by-subdomain.html. Acesso em: 15 set. 2019.
- RICHARDSON, Chris. **What are microservices?**. [S. l.]. Disponível em: https://microservices.io/index.html. Acesso em: 15 set. 2019.
- WAYNER, Peter. **The top 5 software architecture patterns**: how to make the right choice. [S. l.]. Disponível em: https://techbeacon.com/app-dev-testing/top-5-software-architecture-patterns-how-make-right-choice. Acesso em: 15 set. 2019.