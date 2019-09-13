# Nome do documento

Todo documento deve ter um texto explicando o que é ele e pq fizemos

## Histórico de Revisões

|      Data     | Versão | Descrição                             | Autor(es) |
| :--: | :----: | :-------: | :-------: |
|   10/09/2019  | 0      |  Adicionando estrutura incial         |       Youssef Muhamad    |
|   11/09/2019  | 0.1    |  Entidades iniciais                   |       Lucas Dutra, Youssef Muhamad e Rogério Júnior    |
|   12/09/2019  | 0.2    |  Atributos iniciais                   |        Lucas Dutra, Youssef Muhamad e Rogério Júnior    |
|   12/09/2019  | 0.3    |  Relacionamentos iniciais                   |        Lucas Dutra, Youssef Muhamad e Rogério Júnior    |

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

* USER ( <u>user_id</u>, name, last_name, email, cpf, password, status, url_avatar, id_avaliacao )
  * PROVIDER( provider_id, rg( issuing_organ, state, number, uf ), url_rg_selfie, bio )
* ADDRESS ( <u>id_address</u>, cep, street, number, uf, county, complement, reference_point )
* RATING ( <u>rating_id</u>, user_id, charisma_rating, commentary )
  * SERVICE_RATING ( service_rating )
* PAX ( <u>id_pax</u>, price, status, name, description, place, date )
* REPORT ( <u>id_report</u>, status, { photos } )
* PROVIDER_CATEGORY ( <u>id_provider_category</u>, name )
* GENERAL_CATEGORY ( <u>id_general_category</u>, name )
* CHAT ( <u>chat_id</u>, message )


### Relacionamentos:

* USER - has - ADDRESS
  * Um USER pode possuir um ou vários ADDRESS(es) e um ADDRESS pode ser de um ou vários USER(s)
  * Cardinalidade: **N  : M**
* USER - has - RATING
  * Um USER pode possuir vários ADDRESS(es) e um ADDRESS pode ser de um ou vários USER(s)
  * Cardinalidade: **N  : M**

## Referências

- Suas referencias OBRIGATORIO
