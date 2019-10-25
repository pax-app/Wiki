# GoF's Comportamentais

Os **GoF**'s (_Gang of Four_) são padrões de _design_ que visão prover soluções para problemas comum no desenvolvimento de _software_. No caso de _programação orientada à objetos_, os GoF's se propõem a solucionar problemas de interação e geração de objetos, que podem ser aplicados a contexto de problemas reais.São ferramentas poderosas no desenvolvimento de _softwares_.

Os **Padrões de Design Comportamentais** (_Behavioral Patterns_) se preocupam dos algoritmos e tarefas entre objetos. Não são responsáveis apenas pelo comportamento entre os objetos, mas também pela sua comunicação. Esses padrões se caracterizam por cuidar de fluxos complexos que são difíceis de acompanhar em tempo real e permitem que o desenvolvedor se preocupe somente com o jeito que os objetos estão interconectados.

## Histórico de Revisões

|    Data    | Versão |                         Descrição                          |            Autor(es)             |
| :--------: | :----: | :--------------------------------------------------------: | :------------------------------: |
| 21/10/2019 |  0.1   |               Cria a estrutura do documento                |          Rogério Júnior          |
| 21/10/2019 |  0.2   |        Adiciona definição de GoF's Comportamentais         |          Rogério Júnior          |
| 23/10/2019 |  0.3   |              Adicionando serviço de FrontEnd               |           Ésio Freitas           |
| 24/10/2019 |  0.4   |              Adicionando serviço de Category               |          Fabiana Ribas           |
| 24/10/2019 |  0.5   | Adiciona definição para Mediator e Chain of responsibility |           Marcos Nery            |
| 24/10/2019 |  0.6   |                   Melhorando descrições                    |           Marcos Nery            |
| 24/10/2019 |  0.7   |                  Padronizando o documento                  | Rogério Júnior e Youssef Muhamad |
| 24/10/2019 |  0.8   |           Adição dos patterns do serviço de Chat           | Rogério Júnior e Youssef Muhamad |
| 24/10/2019 |  0.9   |         Melhorando explicações no uso dos patterns         | Rogério Júnior e Youssef Muhamad |
| 24/10/2019 |  1.0 |         Melhorando algumas descrições e adicionando citações de GRASPs        | Marcos Nery |


<!-- ## Command

[Descrição] -->

## Iterator

O iterador é um padrão de projeto comportamental que permite atravessar elementos de uma coleção sem expor sua representação subjacente (lista, pilha, árvore, etc.). Esse padrão ajuda portanto a garantir os GRASPs de alta coesão e do especialista, já que algoritmos de ordenação e outras coisas do tipo, que não fazem realmente parte da responsabilidade de algumas classes mas que precisam ser implementados para resolver os problemas dela, podem ser passados para classes separadas.

- [User](docs/DS/dinamica-e-seminario-4-b/servicos/User.md#Iterator)

## Mediator

Padrão que visa diminuir a dependência desorganizada entre objetos/serviços estabelecendo uma interface que se responsabiliza por gerir toda a comunicação de um sistema, redirecionado as chamadas que chegam a ele para as camadas que serão responsáveis por trata-las, podendo também haver algum tipo de tratamento adicional na própria passagem da requisição ou da sua resposta. Vindo da invenção pura, esse padrão contribuí para o baixo acoplamento e para alta coesão.

- [API Gateway](docs/DS/dinamica-e-seminario-4-b/servicos/Gateway.md#mediator)

## Observer

Observer é um padrão de design comportamental que permite definir um mecanismo de inscrição para notificar vários objetos sobre quaisquer eventos que ocorram no objeto que estão observando.

- [Front-End](docs/DS/dinamica-e-seminario-4-b/servicos/front.md#Observer)

## Strategy

Strategy é um padrão de design comportamental que permite definir uma família de algoritmos, colocar cada um deles em uma classe separada e tornar seus objetos intercambiáveis. O Strategy contribui para o cumprimento dos GRASPs Alta coesão e especialista, já que cada estratégia é separada em sua própria classe e contém apenas o que lhe é de competência. Também pode ser enquadrado como um caso de implementação do respeito ao GRASP de variações protegidas.

- [Category](docs/DS/dinamica-e-seminario-4-b/servicos/Category.md#Strategy)
- [Front-End](docs/DS/dinamica-e-seminario-4-b/servicos/front.md#Strategy)
- [User](docs/DS/dinamica-e-seminario-4-b/servicos/User.md#Strategy)

<!-- ## Template Method

[Descrição]

## Visitor

[Descrição] -->

## Memento

Memento é um padrão de design comportamental que permite salvar e restaurar o estado anterior de um objeto sem revelar os detalhes de sua implementação.

- [Front-End](docs/DS/dinamica-e-seminario-4-b/servicos/front.md#Memento)

## Chain of Responsibility

Nesse padrão cada chamada passa por uma cadeia de funções, cada uma delas trata do que é de sua competência e em sequência passa a chamada para próxima função da cadeia, até que finalmente uma delas decide que a requisição foi totalmente tratada e então encerra o caminho e retorna o resultado. Dessa forma, o padrão contribuí para GRASPs como o o baixo acoplamento, alta coesão e utilização do especialista.

- [API Gateway](docs/DS/dinamica-e-seminario-4-b/servicos/Gateway.md#chain-of-responsibility)
- [Chat](docs/DS/dinamica-e-seminario-4-b/servicos/Chat.md#chain-of-responsibility)

## State

State é um padrão de design comportamental que permite que um objeto altere seu comportamento quando seu estado interno for alterado. Quase como se o objeto tivesse mudado de classe. Esse padrão ajuda a manter os GRASPs de alta coesão e especialista, já que o que é referente a cada um dos estados pode ser representado em classes diferentes.

- [Front-End](docs/DS/dinamica-e-seminario-4-b/servicos/front.md#State)

## Referências

- GAMMA, Erich et al. **Design Patterns**: Elements of Reusable Object-Oriented Software. 1. ed. Massachusetts: Addison-Wesley Professional, 2009. 426 p. ISBN 0-201-63361-2.

- CARR, Richard. **Gang of Four Design Patterns**. [S. l.], 2009. Disponível em: http://www.blackwasp.co.uk/gofpatterns.aspx. Acesso em: 21 out. 2019.

- Refactoring Guru. **Design Patterns**. [S. l.], 2019. Disponível em: https://refactoring.guru/design-patterns. Acesso em: 21 out. 2019.
