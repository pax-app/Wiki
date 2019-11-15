# [User](https://github.com/pax-app/User)

Microsserviço responsável por toda interação do usuário, como login, registro.

## Histórico de Revisões

|    Data    | Versão |      Descrição       |  Autor(es)  |
| :--------: | :----: | :------------------: | :---------: |
| 25/10/2019 |  1.0   | Criação do documento | Lucas Dutra |

## Padrões usados

### Decorator

O _decorator_, no contexto do serviço de usuários, é utilizado para implementar uma função que tem como foco alterar o comportamento de determinadas rotas. Assim, executando a validação do _token_ e requerindo a presença do mesmo naquelas rotas que forem agregadas com o _decorator_.

![Decorator](../../../../assets/design-patterns/User/Decorator.png)

Arquivo: [auth_utils.py](https://github.com/pax-app/User/blob/devel/project/api/utils/auth_utils.py)

### [⬅](docs/DS/dinamica-e-seminario-4-b/estruturais.md#decorator)

### Facade

O padrão de faixada é implementado por padrão em uma ferramenta do _Micro-Framework_ _Flask_ chamada _Blueprint_. Isso acontece pois, essa estrutura, tem como papel destribuir para as rotas uma _URL_ base e ao mesmo tempo, ao instanciá-la, cria-se um vínculo da rota que faz uso dessa _Blueprint_ com todas as outras que implementam ela.

![Facade](../../../../assets/design-patterns/User/Facade.png)

Arquivo: [init.py](https://github.com/pax-app/User/blob/devel/project/__init__.py)

### [⬅](docs/DS/dinamica-e-seminario-4-b/estruturais.md#facade)

### Factory method

O Application Factory, é uma evolução do design _Pattern Factory_, sendo essa evolução proposta em plataformas emergentes orientadas à convenção, e adaptada à tecnologia de Micro-framework _Flask_. Por um lado é um padrão emergente, mas por outro tem em sua base o original conceito de fábrica do padrão de projeto GoF.

Este padrão é aplicado na criação da instância de um _app_ proveniente da biblioteca padrão do _Flask_.

![ApplicationFactory](../../../../assets/design-patterns/User/ApplicationFactory.png)

Arquivo: [init.py](https://github.com/pax-app/User/blob/devel/project/__init__.py)

### [⬅](docs/DS/dinamica-e-seminario-4-b/criacionais.md#factory-method)

### Iterator

Os iterators, por mais que sua implementação purista não esteja presente, a abstração feita pela linguagem de programação _Python_ atráves dos loops como _for_, _while_, está implentada no serviço de Usuários.

A aplicação deste padrão é dada no ato de percorrer listas de dicionários para adicionarmos valores a cada um deles.

![Iterator](../../../../assets/design-patterns/User/Iterator.png)

Arquivo: [creation_utils.py](https://github.com/pax-app/User/blob/devel/project/api/utils/creation_utils.py)

### [⬅](docs/DS/dinamica-e-seminario-4-b/comportamentais.md#iterator)

### Singleton

O Singleton foi utilizado para garantirmos a instância única da aplicação com o banco de dados.

![Singleton](../../../../assets/design-patterns/User/Singleton.png)

Arquivo: [database_singleton.py](https://github.com/pax-app/User/blob/devel/database_singleton.py)

### [⬅](docs/DS/dinamica-e-seminario-4-b/criacionais.md#singleton)

### Strategy

Utilizamos do Strategy para implementar a diferenciação entre duas rotas que, previamente, eram muito semelhantes. Assim, refatoramos o comportamento das mesmas de acordo com o padrão, possuindo assim uma estratégia para ordenação de prestadores de serviço por menor preço e por maior nota na avaliação de seu serviço.

![Strategy](../../../../assets/design-patterns/User/Strategy.png)

Arquivo: [display_strategy.py](https://github.com/pax-app/User/blob/devel/project/api/utils/display_strategy.py)

### [⬅](docs/DS/dinamica-e-seminario-4-b/comportamentais.md#strategy)

## Controle de Manutenabilidade

Antes da implementações fizemos uso da ferramenta _Code Climate_ para mensurar a manutenabilidade do código deste microsserviço.

![Code Climate](../../../../assets/design-patterns/User/Before.jpg)

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

Após a refatoração o resultado foi de imensa melhora da avaliação do serviço, principalmente no arquivo _views.py_ onde, previamente, continha toda lógica aninhada.

![Code Climate](../../../../assets/design-patterns/User/After.png)

O arquivo _views.py_ subiu de nota "D" para nota "A" com base nos critérios de avaliação e, além disso, teve sua quantidade de linhas diminuída em quase 100.
![Code Climate](../../../../assets/design-patterns/User/After-views.jpg)
