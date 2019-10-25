# [Chat](https://github.com/pax-app/Chat)

O serviço de chat é responsável pelo gerênciamento das salas de chat entre o usuário e o provedor. Se encarrega da comunicação direta com a banco de dados de forma a inserir, consultar e deletar as informações. Provem _endpoints_ que permitem a comunicação entre o sistema.

## Class Database

O _Singleton_ é de extrema importância, neste caso, para que a instância de conexão com o Banco seja única e acessível por todo os módulos do serviço que a importar. O _JavaScript_ tem um jeito simples de fazer isso que é o _export default new ClasseDesejada()_ que faz com que o todas as vezes que essa instância for chamada, ela será a mesma em qualquer lugar.

![Class Database](../../../../assets/Patterns/Chat/database.svg)

Arquivo: [database/index.js](https://github.com/pax-app/Chat/blob/devel/src/database/index.js#L7)

### [⬅](docs/DS/dinamica-e-seminario-4-b/criacionais.md#singleton)

## Chat List

O _Chain of Responsibility_ foi implementado para que possa ser feita a validação dos _schema_ recebidos via requisição, atuando como um _middleware_. Caso a validação ocorra com sucesso ele chama a _controller_ responsável pela requisição.

![Chat List](../../../../assets/Patterns/Chat/chat_list.svg)

![Routes](../../../../assets/Patterns/Chat/routes_list.svg)

Arquivos:

- [ChatList.js](https://github.com/pax-app/Chat/blob/devel/src/app/validators/ChatList.js#L3)
- [Routes.js](https://github.com/pax-app/Chat/blob/devel/src/routes.js#L9)

### [⬅](docs/DS/dinamica-e-seminario-4-b/comportamentais.md#chain-of-responsibility)
