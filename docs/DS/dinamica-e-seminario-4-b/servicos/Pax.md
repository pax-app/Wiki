# [Pax](https://github.com/pax-app/Pax)

Microsserviço responsável pelos contratos cliente-prestador.

## Padrões usados:

### Factory method

O Application Factory, é uma evolução do design _Pattern Factory_, sendo essa evolução proposta em plataformas emergentes orientadas à convenção, e adaptada à tecnologia de Micro-framework _Flask_. Por um lado é um padrão emergente, mas por outro tem em sua base o original conceito de fábrica do padrão de projeto GoF.

Este padrão é aplicado na criação da instância de um _app_ proveniente da biblioteca padrão do _Flask_.

![ApplicationFactory](../../../../assets/design-patterns/Pax/Factory.png)

Arquivo: [init.py](https://github.com/pax-app/Pax/blob/devel/project/__init__.py)

### [⬅](docs/DS/dinamica-e-seminario-4-b/criacionais.md#factory-method)

### Facade

O padrão de faixada é implementado por padrão em uma ferramenta do _Micro-Framework_ _Flask_ chamada _Blueprint_. Isso acontece pois, essa estrutura, tem como papel destribuir para as rotas uma _URL_ base e ao mesmo tempo, ao instanciá-la, cria-se um vínculo da rota que faz uso dessa _Blueprint_ com todas as outras que implementam ela.

![Facade](../../../../assets/design-patterns/Pax/Facade.png)

Arquivo: [init.py](https://github.com/pax-app/Pax/blob/devel/project/__init__.py)

### [⬅](docs/DS/dinamica-e-seminario-4-b/estruturais.md#facade)

### Iterator

Os iterators, por mais que sua implementação purista não esteja presente, a abstração feita pela linguagem de programação _Python_ atráves dos loops como _for_, _while_, está implentada no serviço de Pax.

A aplicação deste padrão é dada no ato de percorrer listas de dicionários para transformar cada um deles em JSONs.

![Iterator](../../../../assets/design-patterns/Pax/Iterator.png)

Arquivo: [creation_utils.py](https://github.com/pax-app/Pax/blob/devel/project/api/utils/creation_utils.py)

### [⬅](docs/DS/dinamica-e-seminario-4-b/comportamentais.md#iterator)

### Singleton

O Singleton foi utilizado para garantirmos a instância única da aplicação com o banco de dados.

![Singleton](../../../../assets/design-patterns/User/Singleton.png)

Arquivo: [database_singleton.py](https://github.com/pax-app/Pax/blob/devel/database_singleton.py)

### [⬅](docs/DS/dinamica-e-seminario-4-b/criacionais.md#singleton)

### Strategy

Utilizamos do Strategy para implementar a diferenciação entre quatro rotas que seriam muito semelhantes. Assim, aplicamos o padrão para filtrar o retorno dos Pax de acordo com seu _status_, sendo dividos em quatro estratégias: _InitiatedStrategy_, _CanceledStrategy_, _PendentStrategy_ e _FinalizedStrategy_.

![Strategy](../../../../assets/design-patterns/Pax/Strategy.png)

Arquivo: [status_strategy.py](https://github.com/pax-app/Pax/blob/devel/project/api/utils/status_strategy.py)

### [⬅](docs/DS/dinamica-e-seminario-4-b/comportamentais.md#strategy)

## Controle de Manutenabilidade

Esse microsserviço foi modelado desde o início com a aplicação desses padrões, dessa forma, é possível ver que o _Code Climate_ aponta uma boa manutenabilidade.

![Code Climate](../../../../assets/design-patterns/Pax/CodeClimate.png)

Este resultado leva em conta fatores como:

- Quantidade de argumentos de uma função
- Complexidade lógica
- Tamanho do arquivo
- Replicação de código
- Complexidade de métodos
- Quantidade de métodos
- Tamanho dos métodos
- Estruturas com muitos _if_ e _switch_
- Retorno dos métodos
