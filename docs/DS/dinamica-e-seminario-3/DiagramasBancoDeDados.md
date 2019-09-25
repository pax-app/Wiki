# Diagramas de Banco de Dados

Com o intuito de modelar o banco de dados, de acordo com os requisitos exigidos pelo [Backlog](docs/DS/dinamica-e-seminario-2/Backlog.md), optou-se pelo uso de três documentos que precedem a criação do banco e guiam sua correta estruturação, são eles: *Modelo Entidade-Relacionamentos* (**ME-R**) , *Diagrama Entidade-Relacionamentos* (**DE-R**) e *Diagrama Lógico* (**DL**).

O **ME-R** é um modelo conceitual utilizado na *Engenharia de Software* para descrever os objetos (entidades) envolvidos em um domínio de negócios, com suas características (atributos) e como elas se relacionam entre si (relacionamentos). Já o **DE-R** é a representação gráfica e a principal ferramenta de visualização dos relacionamentos entre as entidades do sistema. E por fim, o **DL** descreve como os dados serão armazenados no banco e também seus relacionamentos.

## Histórico de Revisões

|    Data    | Versão |                                    Descrição                                         |                    Autor(es)                  |
| :--------: | :----: | :----------------------------------------------------------------------------------: | :-------------------------------------------: |
| 10/09/2019 |   0    | Adicionando estrutura inicial                                                        |                Youssef Muhamad                |
| 11/09/2019 |  0.1   | Entidades iniciais                                                                   | Lucas Dutra, Youssef Muhamad e Rogério Júnior |
| 12/09/2019 |  0.2   | Atributos iniciais                                                                   | Lucas Dutra, Youssef Muhamad e Rogério Júnior |
| 12/09/2019 |  0.3   | Relacionamentos iniciais                                                             | Lucas Dutra, Youssef Muhamad e Rogério Júnior |
| 14/09/2019 |  0.4   | Melhorando a entidade ADDRESS para seguir o modelo de filtragem pelo CEP             |                Youssef Muhamad                |
| 14/09/2019 |  0.5   | V1 dos relacionamentos                                                               |        Rogério Júnior e Youssef Muhamad       |
| 15/09/2019 |  0.6   | Corrigindo Cardinalidades e adicionando relacionamentos faltantes                    |        Rogério Júnior e Youssef Muhamad       |
| 15/09/2019 |  0.7   | Revisão Geral e atualizações nos atributos das entidade                              |        Rogério Júnior e Youssef Muhamad       |
| 15/09/2019 |  0.8   | Adicionando DE-R e DL V1                                                             |        Rogério Júnior e Youssef Muhamad       |
| 15/09/2019 |  0.9   | Corrigindo leitura das cardinalidades                                                |        Rogério Júnior e Youssef Muhamad       |
| 15/09/2019 |  1.0   | Adicionando descrição do documento e referências                                     |        Rogério Júnior e Youssef Muhamad       |
| 18/09/2019 |  1.1   | Adicionando CHAT nas entidades e removendo a chave avaliação_id do MER               | Rogério Júnior, Youssef Muhamad e Lucas Dutra |
| 18/09/2019 |  1.2   | Entidade CHAT relacionada com a nova entidade MESSAGE                                |        Rogério Júnior e Youssef Muhamad       |
| 18/09/2019 |  1.3   | Mudando o nome de RATING para REVIEW e adicionando a FK do destinatário do review    |        Rogério Júnior e Youssef Muhamad       |
| 18/09/2019 |  1.4   | Melhorando os nomes das colunas das tabelas para uma melhor semântica                |        Rogério Júnior e Youssef Muhamad       |
| 18/09/2019 |  1.5   | Adicionando os novos relacionamentos CHAT - has - MESSAGES e PAX - references - CHAT |        Rogério Júnior e Youssef Muhamad       |
| 18/09/2019 |  2.0   | Versão 2 do documento, com novos MER, DER e DL                                       |        Rogério Júnior e Youssef Muhamad       |
| 18/09/2019 |  2.1   | Adicionando referência de REVIEW A SERVICE como FK                                   |        Rogério Júnior e Youssef Muhamad       |
| 18/09/2019 |  2.2   | Mudando o tipo de data da tabela PAX                                                 |        Rogério Júnior e Youssef Muhamad       |
| 18/09/2019 |  2.3   | Mudando o nome de *photos* da tabela REPORT para *report_photos*                     |        Rogério Júnior e Youssef Muhamad       |
| 18/09/2019 |  2.4   | Adicionando atributo *pax_photos* à tabela PAX                                       |        Rogério Júnior e Youssef Muhamad       |
| 18/09/2019 |  3.0   | Atualizando o MER, DER e DL com novas modificações                                   |        Rogério Júnior e Youssef Muhamad       |
| 18/09/2019 |  3.1   | Adicionando *price_range* à tabela *PROVIDER*                                        |        Rogério Júnior e Youssef Muhamad       |

## Versão 3.0

!> Adição da tabela para fotos do *PAX*, adição do campo *price_range* do *PROVIDER* e referência entre *SERVICE* e *REVIEW*

### Modelo Entidade-Relacionamento(ME-R)

- #### Entidades:

  * USER
    * PROVIDER
  * ADDRESS
  * REVIEW
    * SERVICE
  * PAX
  * REPORT
  * PROVIDER_CATEGORY
  * GENERAL_CATEGORY
  * CHAT
  * MESSAGE

- #### Atributos:

  * USER ( <u>user_id</u>, name, email, cpf, password, url_avatar )
    * PROVIDER( provider_id, rg( issuing_organ, state, number ), url_rg_photo, bio )
  * ADDRESS ( <u>address_id</u>, cep, street, neighborhood, city, state, number, complement, reference_point )
  * REVIEW ( <u>review_id</u>, evaluated_id, evaluator_id, charisma_rate, commentary )
    * SERVICE ( <u>review_service_id</u>, evaluated_id, evaluator_id, service_rate )
  * PAX ( <u>pax_id</u>, user_id, provider_id, chat_id, address_id, price, status, name, description, date, { pax_photos } )
  * REPORT ( <u>report_id</u>, user_id, pax_id, status, description, { report_photos } )
  * PROVIDER_CATEGORY ( <u>provider_category_id</u>, name )
  * GENERAL_CATEGORY ( <u>general_category_id</u>, name )
  * CHAT ( <u>chat_id</u>, user_id, provider_id  )
  * MESSAGE ( <u>message_id</u>, chat_id, sender_id, date_time_sent, text_message )

- #### Relacionamentos:

  * USER - lives - ADDRESS
    * Um USER pode possuir um ou vários ADDRESS(es) e um ADDRESS pode ser de um ou vários USER(s).
    * Cardinalidade: **N  : M**
  * USER - has - REVIEW
    * Um USER pode possuir vários REVIEW(s) e um REVIEW é de somente um USER.
    * Cardinalidade: **1 : N**
  * USER - does - REVIEW_SERVICE
    * Um USER faz um ou vários REVIEW_SERVICE(s) e um REVIEW_SERVICE é feito por somente um USER.
    * Cardinalidade: **1 : N**
  * USER - participates - PAX
    * Um USER participa de um ou vários PAX(es) e um PAX tem a participação de somente um USER.
    * Cardinalidade: **1 : N**
  * USER - participates - CHAT
    * Um USER participa de um ou vários CHAT(s) e um CHAT tem a participação de somente um USER.
    * Cardinalidade: **1 : N**
  * PROVIDER - has - REVIEW_SERVICE
    * Um PROVIDER pode possuir vários REVIEW_SERVICE(es) e um REVIEW_SERVICE é de um único PROVIDER.
    * Cardinalidade: **1 : N**
  * PROVIDER - does - REVIEW
    * Um PROVIDER faz um ou vários REVIEW(s) e um REVIEW é feito por somente um PROVIDER.
    * Cardinalidade: **1 : N**
  * PROVIDER - participates - PAX
    * Um PROVIDER participa de um ou vários PAX(es) e um PAX tem a participação de somente um PROVIDER.
    * Cardinalidade: **1 : N**
  * PROVIDER - participates - CHAT
    * Um PROVIDER participa de um ou vários CHAT(s) e um CHAT tem a participação de somente um PROVIDER.
    * Cardinalidade: **1 : N**
  * PROVIDER - works - PROVIDER_CATEGORY
    * Um PROVIDER trabalha com um ou vários PROVIDER_CATEGORY(ies) e um PROVIDER_CATEGORY é trabalhado por um ou vários PROVIDER(s).
    * Cardinalidade: **N  : M**
  * PAX - has - ADDRESS
    * Um PAX possui um único ADDRESS(es) e um ADDRESS pode ser de vários PAX(es).
    * Cardinalidade: **N : 1**
  * PAX - references - CHAT
    * Um PAX referencia um único CHAT e um CHAT é referenciado em um único PAX.
    * Cardinalidade: **1 : 1**
  * REPORT - reports - PAX
    * Um REPORT reporta um único PAX(es) e um PAX é reportado por um único REPORT.
    * Cardinalidade: **1 : 1**
  * CHAT - has - MESSAGE
    * Um CHAT tem várias MESSAGE(s) e uma MESSAGE é de um único CHAT.
    * Cardinalidade: **1 : N**
  * GENERAL_CATEGORY - contains - PROVIDER_CATEGORY
    * Um GENERAL_CATEGORY contém um ou vários PROVIDER_CATEGORY(ies) e um PROVIDER_CATEGORY está contido em um único GENERAL_CATEGORY.
    * Cardinalidade: **1 : N**

### Diagrama Entidade-Relacionamento(DE-R)

![Conceitual_V3](../../../assets/database/Conceitual_Pax_v3.png)

### Diagrama Lógico (DL)

![Logico_V3](../../../assets/database/Logico_Pax_v3.png)

---

## Versão 2.0

!> Correta modelagem do *CHAT*, *FK's* com os nomes da tabela de origem, separação da tabela *PAX* e *REPORT* e especificação do espaço e *constraints* dos atributos

### Modelo Entidade-Relacionamento(ME-R)

- #### Entidades:

  * USER
    * PROVIDER
  * ADDRESS
  * REVIEW
    * SERVICE
  * PAX
  * REPORT
  * PROVIDER_CATEGORY
  * GENERAL_CATEGORY
  * CHAT
  * MESSAGE

- #### Atributos:

  * USER ( <u>user_id</u>, name, email, cpf, password, url_avatar )
    * PROVIDER( provider_id, rg( issuing_organ, state, number ), url_rg_photo, bio )
  * ADDRESS ( <u>address_id</u>, cep, street, neighborhood, city, state, number, complement, reference_point )
  * REVIEW ( <u>review_id</u>, evaluated_id, evaluator_id, charisma_rate, commentary )
    * SERVICE ( <u>review_service_id</u>, evaluated_id, evaluator_id, service_rate )
  * PAX ( <u>pax_id</u>, user_id, provider_id, chat_id, address_id, price, status, name, description, date )
  * REPORT ( <u>report_id</u>, user_id, pax_id, status, description, { photo } )
  * PROVIDER_CATEGORY ( <u>provider_category_id</u>, name )
  * GENERAL_CATEGORY ( <u>general_category_id</u>, name )
  * CHAT ( <u>chat_id</u>, user_id, provider_id  )
  * MESSAGE ( <u>message_id</u>, chat_id, sender_id, date_time_sent, text_message )

- #### Relacionamentos:

  * USER - lives - ADDRESS
    * Um USER pode possuir um ou vários ADDRESS(es) e um ADDRESS pode ser de um ou vários USER(s).
    * Cardinalidade: **N  : M**
  * USER - has - REVIEW
    * Um USER pode possuir vários REVIEW(s) e um REVIEW é de somente um USER.
    * Cardinalidade: **1 : N**
  * USER - does - REVIEW_SERVICE
    * Um USER faz um ou vários REVIEW_SERVICE(s) e um REVIEW_SERVICE é feito por somente um USER.
    * Cardinalidade: **1 : N**
  * USER - participates - PAX
    * Um USER participa de um ou vários PAX(es) e um PAX tem a participação de somente um USER.
    * Cardinalidade: **1 : N**
  * USER - participates - CHAT
    * Um USER participa de um ou vários CHAT(s) e um CHAT tem a participação de somente um USER.
    * Cardinalidade: **1 : N**
  * PROVIDER - has - REVIEW_SERVICE
    * Um PROVIDER pode possuir vários REVIEW_SERVICE(es) e um REVIEW_SERVICE é de um único PROVIDER.
    * Cardinalidade: **1 : N**
  * PROVIDER - does - REVIEW
    * Um PROVIDER faz um ou vários REVIEW(s) e um REVIEW é feito por somente um PROVIDER.
    * Cardinalidade: **1 : N**
  * PROVIDER - participates - PAX
    * Um PROVIDER participa de um ou vários PAX(es) e um PAX tem a participação de somente um PROVIDER.
    * Cardinalidade: **1 : N**
  * PROVIDER - participates - CHAT
    * Um PROVIDER participa de um ou vários CHAT(s) e um CHAT tem a participação de somente um PROVIDER.
    * Cardinalidade: **1 : N**
  * PROVIDER - works - PROVIDER_CATEGORY
    * Um PROVIDER trabalha com um ou vários PROVIDER_CATEGORY(ies) e um PROVIDER_CATEGORY é trabalhado por um ou vários PROVIDER(s).
    * Cardinalidade: **N  : M**
  * PAX - has - ADDRESS
    * Um PAX possui um único ADDRESS(es) e um ADDRESS pode ser de vários PAX(es).
    * Cardinalidade: **N : 1**
  * PAX - references - CHAT
    * Um PAX referencia um único CHAT e um CHAT é referenciado em um único PAX.
    * Cardinalidade: **1 : 1**
  * REPORT - reports - PAX
    * Um REPORT reporta um único PAX(es) e um PAX é reportado por um único REPORT.
    * Cardinalidade: **1 : 1**
  * CHAT - has - MESSAGE
    * Um CHAT tem várias MESSAGE(s) e uma MESSAGE é de um único CHAT.
    * Cardinalidade: **1 : N**
  * GENERAL_CATEGORY - contains - PROVIDER_CATEGORY
    * Um GENERAL_CATEGORY contém um ou vários PROVIDER_CATEGORY(ies) e um PROVIDER_CATEGORY está contido em um único GENERAL_CATEGORY.
    * Cardinalidade: **1 : N**

### Diagrama Entidade-Relacionamento(DE-R)

![Conceitual_V2](../../../assets/database/Conceitual_Pax_v2.png)

### Diagrama Lógico (DL)

![Logico_V2](../../../assets/database/Logico_Pax_v2.png)

---

## Versão 1.0

### Modelo Entidade-Relacionamento(ME-R)

- #### Entidades:

  * USER
    * PROVIDER
  * ADDRESS
  * RATING
    * SERVICE
  * PAX
  * REPORT
  * PROVIDER_CATEGORY
  * GENERAL_CATEGORY
  * CHAT

- #### Atributos:

  * USER ( <u>user_id</u>, name, email, cpf, password, url_avatar, id_avaliacao )
    * PROVIDER( provider_id, rg( issuing_organ, state, number ), url_rg_photo, bio )
  * ADDRESS ( <u>address_id</u>, cep, street, neighborhood, city, state, number, complement, reference_point )
  * RATING ( <u>rating_id</u>, provider_id, charisma_rate, commentary )
    * SERVICE ( <u>service_id</u>, user_id, service_rate )
  * PAX ( <u>pax_id</u>, user_id, provider_id, address_id, price, status, name, description, date )
  * REPORT ( <u>report_id</u>, user_id, pax_id, status, { photos } )
  * PROVIDER_CATEGORY ( <u>provider_category_id</u>, name )
  * GENERAL_CATEGORY ( <u>general_category_id</u>, name )
  * CHAT ( <u>chat_id</u>, user_id, provider_id ,message )

- #### Relacionamentos:

  * USER - livesIn - ADDRESS
    * Um USER pode possuir um ou vários ADDRESS(es) e um ADDRESS pode ser de um ou vários USER(s).
    * Cardinalidade: **N  : M**
  * USER - has - RATING
    * Um USER pode possuir vários RATING(s) e um RATING é de somente um USER.
    * Cardinalidade: **1 : N**
  * USER - participates - PAX
    * Um USER participa de um ou vários PAX(es) e um PAX tem a participação de somente um USER
    * Cardinalidade: **1 : N**
  * PROVIDER - participates - PAX
    * Um PROVIDER participa de um ou vários PAX(es) e um PAX tem a participação de somente um PROVIDER
    * Cardinalidade: **1 : N**
  * PROVIDER - has - RATING_SERVICE
    * Um PROVIDER pode possuir vários RATING_SERVICE(es) e um RATING_SERVICE é de um único PROVIDER.
    * Cardinalidade: **1 : N**
  * PAX - has - ADDRESS
    * Um PAX possui um único ADDRESS(es) e um ADDRESS pode ser de vários PAX(es)
    * Cardinalidade: **N : 1**
  * REPORT - reports - PAX
    * Um REPORT reporta um único PAX(es) e um PAX é reportado por um único REPORT.
    * Cardinalidade: **1  : 1**
  * PROVIDER - works - PROVIDER_CATEGORY
    * Um PROVIDER trabalha com um ou vários PROVIDER_CATEGORY(ies) e um PROVIDER_CATEGORY é trabalhado por um ou vários PROVIDER(s).
    * Cardinalidade: **N  : M**
  * GENERAL_CATEGORY - contains - PROVIDER_CATEGORY
    * Um GENERAL_CATEGORY contém um ou vários PROVIDER_CATEGORY(ies) e um PROVIDER_CATEGORY está contido em um único GENERAL_CATEGORY.
    * Cardinalidade: **1 : N**
  * USER - participates - CHAT
    * Um USER participa de um ou vários CHAT(s) e um CHAT tem a participação de somente um USER.
    * Cardinalidade: **1 : N**
  * PROVIDER - participates - CHAT
    * Um PROVIDER participa de um ou vários CHAT(s) e um CHAT tem a participação de somente um PROVIDER.
    * Cardinalidade: **1 : N**
  * PROVIDER - does - RATING
    * Um PROVIDER faz um ou vários RATING(s) e um RATING é feito por somente um PROVIDER.
    * Cardinalidade: **1 : N**
  * USER - does - RATING_SERVICE
    * Um USER faz um ou vários RATING_SERVICE(s) e um RATING_SERVICE é feito por somente um USER.
    * Cardinalidade: **1 : N**

### Diagrama Entidade-Relacionamento(DE-R)

![Conceitual_V1](../../../assets/database/Conceitual_Pax_v1.png)

### Diagrama Lógico (DL)

![Logico_V1](../../../assets/database/Logico_Pax_v1.png)


## Referências


- **Introdução ao Modelo de Dados e seus Níveis de Abstração**. Disponível em: <http://spaceprogrammer.com/bd/introducao-ao-modelo-de-dados-e-seus-niveis-de-abstracao/>. Acesso: 15 set. 2019.
- **Preenchimento de endereço via CEP com Javascript**. Disponível em: <https://viacep.com.br/exemplo/javascript/>. Acesso: 15 set. 2019.
- RODRIGUES, Joel. **Modelo Entidade Relacionamento (MER) e Diagrama Entidade-Relacionamento (DER)** Disponível em: <https://www.devmedia.com.br/modelo-entidade-relacionamento-mer-e-diagrama-entidade-relacionamento-der/14332>. Acesso: 15 set. 2019.