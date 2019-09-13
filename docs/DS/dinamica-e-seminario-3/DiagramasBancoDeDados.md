# Nome do documento

Todo documento deve ter um texto explicando o que é ele e pq fizemos

## Histórico de Revisões

| Data | Versão | Descrição | Autor(es) |
| :--: | :----: | :-------: | :-------: |
|      |        |           |           |

MER(Modelo Entidade Relacionamento)

USER(user_id, name, last_name, email, cpf, password, avatar, id_avaliacao)

PROVIDER(provider_id, rg(issuing_organ, state, number, uf), url_rg_selfie, bio)

RATING(id_avaliacao, id_usuario, charisma_rating, commentary)

SERVICE_RATING(service_rating)

ADDRESS(id_address, cep, street, number, uf, county, complement, reference_point)

PAX(id_pax, price, name, description, place, date)

REPORT(id_report, status, {fotos})

PROVIDER_CATEGORY(id_provider_category, name)

GENERAL_CATEGORY(id_general_category, name)


## Referências

- Suas referencias OBRIGATORIO
