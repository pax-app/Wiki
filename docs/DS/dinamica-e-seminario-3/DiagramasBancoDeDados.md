# Nome do documento

Todo documento deve ter um texto explicando o que é ele e pq fizemos

## Histórico de Revisões

|      Data     | Versão | Descrição                             | Autor(es) |
| :--: | :----: | :-------: | :-------: |
|   10/09/2019  | 0      |  Adicionando estrutura incial         |       Youssef Muhamad    |
|   11/09/2019  | 0.1    |  Entidades iniciais                   |       Lucas Dutra, Youssef Muhamad e Rogério Júnior    |
|   12/09/2019  | 0.2    |  Atributos iniciais                   |        Lucas Dutra, Youssef Muhamad e Rogério Júnior    |
|   12/09/2019  | 0.3    |  Relacionamentos iniciais                   |        Lucas Dutra, Youssef Muhamad e Rogério Júnior    |
|   14/09/2019  | 0.4    |  Melhorando a entidade ADDRESS para seguir o modelo de filtragem pelo CEP                  |        Youssef Muhamad    |
|   14/09/2019  | 0.5    |  v1 dos relacionamentos                  |       Rogério Júnior e Youssef Muhamad    |

## MER(Modelo Entidade Relacionamento)

### Entidades:

* USER
  * PROVIDER
* ADDRESS
* RATING
  * SERVICE_RATING
* PAX
* REPORT
* PROVIDER_CATEGORY
* GENERAL_CATEGORY

### Atributos:

* USER ( <u>user_id</u>, name, email, cpf, password, status, url_avatar, id_avaliacao )
  * PROVIDER( provider_id, rg( issuing_organ, state, number, uf ), url_rg_selfie, bio )
* ADDRESS ( <u>address_id</u>, cep, street, neighborhood, city, state, complement, reference_point )
* RATING ( <u>rating_id</u>, user_id, charisma_rating, commentary )
  * SERVICE ( <u>service_id</u>, service_rating )
* PAX ( <u>id_pax</u>, user_id, provider_id, address_id, price, status, name, description, date )
* REPORT ( <u>id_report</u>, user_id, pax_id, status, { photos } )
* PROVIDER_CATEGORY ( <u>provider_category_id</u>, name )
* GENERAL_CATEGORY ( <u>general_category_id</u>, name )
* CHAT ( <u>chat_id</u>, user_id, provider_id , message )


### Relacionamentos:

* USER - livesIn - ADDRESS
  * Um USER pode possuir um ou vários ADDRESS(es) e um ADDRESS pode ser de um ou vários USER(s).
  * Cardinalidade: **N  : M**
* USER - has - RATING
  * Um USER pode possuir vários RATING(s) e um RATING pode ser de um USER.
  * Cardinalidade: **1  : N**
* PROVIDER - has - RATING_SERVICE
  * Um PROVIDER possuir vários RATING_SERVICE(es) e um RATING_SERVICE é de um único PROVIDER.
  * Cardinalidade: **1  : N**
* PAX - has - ADRESS
  * Um PAX possui um único ADDRESS(es) e um ADDRESS pode ser de vários PAX(es)
  * Cardinalidade: **1  : N**
* REPORT - reports - PAX
  * Um REPORT reporta um único PAX(es) e um PAX é reportado por um único REPORT.
  * Cardinalidade: **1  : 1**
* PROVIDER - works - PROVIDER_CATEGORY
  * Um PROVIDER trabalha com um ou vários PROVIDER_CATEGORY(ies) e um PROVIDER_CATEGORY é trabalhado por um ou vários PROVIDER(s).
  * Cardinalidade: **N  : M**
* GENERAL_CATEGORY - contain - PROVIDER_CATEGORY
  * Um GENERAL_CATEGORY contém um ou vários PROVIDER_CATEGORY(ies) e um PROVIDER_CATEGORY está contido em um único GENERAL_CATEGORY.
  * Cardinalidade: **N  : 1**
* USER - participate - CHAT
  * Um USER participa de um ou vários CHAT(s) e um CHAT tem a participação de somente um USER.
  * Cardinalidade: **N  : 1**
* PROVIDER - participate - CHAT
  * Um PROVIDER participa de um ou vários CHAT(s) e um CHAT tem a participação de somente um PROVIDER.
  * Cardinalidade: **N  : 1**


## Referências


- Preenchimento de endereço via CEP com Javascript. Acessado dia **014/09/2019** em: <https://viacep.com.br/exemplo/javascript/>