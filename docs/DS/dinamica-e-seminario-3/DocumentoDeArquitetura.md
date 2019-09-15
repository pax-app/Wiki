# Arquitetura V 0.0.0

Este documento visa especificar de forma básica alguns tópicos referentes ao Documento de Arquitetura que será desenvolvido no decorrer da disciplina.

## Histórico de Revisões

|    Data    | Versão |      Descrição       |   Autor(es)   |
| :--------: | :----: | :------------------: | :-----------: |
| 08/09/2019 |  0.1   | Criação do documento | Felipe Campos |

## 2. Representação arquitetural

* **Flutter**      

<p style="text-align:justify">&emsp;&emsp;<i>React</i> é uma biblioteca de <i>JavaScript</i> flexível, declarativa e eficiente para construção de interfaces para exibição ao usuário. O <i>React</i> permite a criação desde interfaces complexas até pequenos e isolados pedaços de código chamados “Componentes”.</p> 

* **Flask**     

<p style="text-align:justify">&emsp;&emsp;<i>Flask</i> é um micro-<i>framework</i> de <i>python</i>, possui toda a flexibilidade da linguagem <i>python</i> e provê um modelo simples para desenvolvimento <i>web</i>. É baseado em 3 pilares: <i>Werkzeug</i>, uma biblioteca para desenvolvimento de <i>apps</i> WSGI, Jinja2, um <i>template engine</i> escrito em <i>Python</i> e <i>good intentions</i>, que são alta qualidade na legibilidade, liberdade de estruturar o <i>app</i> na maneira que desejar, entre outros aspectos.</p>

* **Node.js**     

<p style="text-align:justify">&emsp;&emsp;<i>Sass</i> é uma extensão de CSS para adicionar poder e elegância para linguagem. Ela permite usar variáveis, regras de aninhamento, mixins e importações de outros arquivos. Sass ajuda a manter as extensas folhas de estilo organizadas e as menores executando mais rapidamente, particulamente, com a ajuda da biblioteca Compass.</p>

* **Express**        

<p style="text-align:justify">&emsp;&emsp;<i>Flask</i> é um micro-<i>framework</i> de <i>python</i>, possui toda a flexibilidade da linguagem <i>python</i> e provê um modelo simples para desenvolvimento <i>web</i>. É baseado em 3 pilares: <i>Werkzeug</i>, uma biblioteca para desenvolvimento de <i>apps</i> WSGI, Jinja2, um <i>template engine</i> escrito em <i>Python</i> e <i>good intentions</i>, que são alta qualidade na legibilidade, liberdade de estruturar o <i>app</i> na maneira que desejar, entre outros aspectos.</p>



* **Microsserviços**   

<p style="text-align:justify">&emsp;&emsp;A arquitetura de microsserviços é uma abordagem que desmembra uma aplicação única em blocos de pequenos serviços independentes. Esses serviços executam o seu próprio processo e se comunicam, muitas vezes, por meio de métodos HTTP.</p>
<p style="text-align:justify">&emsp;&emsp;No <i>software</i> descrito neste documento os módulos serão:
<ul>
  <li><b>User</b>, bloco responsável somente pela extração do texto proveniente das notas fiscais escaneadas;</li> 
  <li><b>Rating</b>, responsável pelo tratamento dos dados brutos que foram extraídos das notas; </li>
  <li><b>Pax</b>, responsável por exportar os relatórios e as notas escaneadas pelo usuário para a extensão desejada;</li>
  <li><b>Payment</b>, responsável por usar os dados provenientes das notas para gerar relatórios de gastos, entre outros; </li>
  <li><b>Report</b>, bloco responsável por toda interação do usuário, como login, registro; </li>
  <li><b>Chat</b>,  será um serviço responsável por gerenciar todas as notas fiscais extraídas.</li>
  <li><b>Category</b>,  será um serviço responsável por gerenciar todas as notas fiscais extraídas.</li>
  <li><b>Gateway</b>, serviço responsável por intermediar a comunicação entre o Back-end e o Front-end.</li>
</ul>
</p>

* **Comunicação entre os serviços**        

<p style="text-align:justify">&emsp;&emsp;Comunicação entre os serviços será feita por meio de uma <i>API Gateway</i>, a qual será responsável por fazer o intermédio entre os microsserviços por meio de métodos do protocolo HTTP. </p>

### 2.1 Diagrama de Arquitetura

#### Diagrama de Arquitetura v1.0
![Diagrama de Arquitetura](../../../assets/arquitetura/representacao_v1.jpg)

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


## Referências 

s