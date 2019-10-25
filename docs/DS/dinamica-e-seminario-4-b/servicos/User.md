# [User](https://github.com/pax-app/User)

Microsserviço responsável por toda interação do usuário, como login, registro.

## Padrões usados:

### Factory method

O Application Factory, é uma evolução do design _Pattern Factory_, sendo essa evolução proposta em plataformas emergentes orientadas à convenção, e adaptada à tecnologia de Micro-framework _Flask_. Por um lado é um padrão emergente, mas por outro tem em sua base o original conceito de fábrica do padrão de projeto GoF.

Este padrão é aplicado na criação da instância de um _app_ proveniente da biblioteca padrão do _Flask_.

![ApplicationFactory](../../../../assets/design-patterns/User/ApplicationFactory.png)

**Acesso ao padrão:** [init.py](https://github.com/pax-app/User/blob/devel/project/__init__.py)

### Decorator

O _decorator_, no contexto do serviço de usuários, é utilizado para implementar uma função que tem como foco alterar o comportamento de determinadas rotas. Assim, executando a validação e requerindo a presença do mesmo naquelas rotas que forem agregadas com o _decorator_.

![Decorator](../../../../assets/design-patterns/User/Decorator.png)

**Acesso ao padrão:** [auth_utils.py](https://github.com/pax-app/User/blob/devel/project/api/utils/auth_utils.py)

### Facade

O padrão de faixada é implementado por padrão em uma ferramenta do _Micro-Framework_ _Flask_ chamada _Blueprint_. Isso acontece pois, essa estrutura, tem como papel destribuir para as rotas uma _URL_ base e ao mesmo tempo, ao instanciá-la, cria-se um vínculo da rota que faz uso dessa _Blueprint_ com todas as outras que implementam ela.

![Facade](../../../../assets/design-patterns/User/Facade.png)

**Acesso ao padrão:** [init.py](https://github.com/pax-app/User/blob/devel/project/__init__.py)

### Iterator

### Singleton

### Strategy
