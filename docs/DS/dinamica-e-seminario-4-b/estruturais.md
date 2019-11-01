# GoF's Estruturais

Os **GoF**'s (_Gang of Four_) são padrões de _design_ que visão prover soluções para problemas comum no desenvolvimento de _software_. No caso de _programação orientada à objetos_, os GoF's se propõem a solucionar problemas de interação e geração de objetos, que podem ser aplicados a contexto de problemas reais.São ferramentas poderosas no desenvolvimento de _softwares_.

Os **Padrões de Design Estruturais**(_Structural Patterns_) estão preocupados com como classes e objetos são unidos para formar estruturas maiores. Classes estruturais usam herança para compor interfaces de implementação.

## Histórico de Revisões

|    Data    | Versão |                     Descrição                     |            Autor(es)             |
| :--------: | :----: | :-----------------------------------------------: | :------------------------------: |
| 21/10/2019 |  0.1   |           Cria a estrutura do documento           |          Rogério Júnior          |
| 21/10/2019 |  0.2   |      Adiciona definição de GoF's Estruturais      |          Rogério Júnior          |
| 24/10/2019 |  0.3   |             Adiciona definição Facade             |          Fabiana Ribas           |
| 24/10/2019 |  0.4   |             Adiciona serviço Category             |          Fabiana Ribas           |
| 24/10/2019 |  0.5   |             Padronizando o documento              | Rogério Júnior e Youssef Muhamad |
| 24/10/2019 |  0.6   |      Adição dos patterns do serviço de Chat       | Rogério Júnior e Youssef Muhamad |
| 24/10/2019 |  0.7   | Refinando algumas descrições e citações de GRASPs |           Marcos Nery            |

<!-- ## Adapter

[Descrição]

## Bridge

[Descrição]

## Composite

[Descrição] -->

## Decorator

O Decorator é um padrão de projeto estrutural que permite, a partir de uma base, anexar novos comportamentos aos objetos. Isso é feito tendo a base como um envelopamento do restante, que por conseguinte sempre será executado em adição ao resto. Isso contribui para a manutenção dos GRASPS de alta coesão e do especialista.

- [User](docs/DS/dinamica-e-seminario-4-b/servicos/User.md#Decorator)

## Facade

Sendo mais um exemplo do GRASP de invensão pura o facade fornece uma interface simplificada para uma biblioteca, uma estrutura ou qualquer outro conjunto complexo de classes. De tal forma que toda a comunicação fica centralizada nessa interface e é ela que delega as chamadas para os métodos apropriados a resolvê-las. Isso ajuda a manter o baixo acoplamento, pois é apenas a interface dele que ficará responsável por saber quem deve tratar qual chamada.

- [Category](docs/DS/dinamica-e-seminario-4-b/servicos/Category.md#Facade)
- [User](docs/DS/dinamica-e-seminario-4-b/servicos/User.md#Facade)
- [Chat](docs/DS/dinamica-e-seminario-4-b/servicos/Chat.md#facade)
- [Pax](docs/DS/dinamica-e-seminario-4-b/servicos/Pax.md#facade)

<!-- ## Flyweight

[Descrição] -->

## Proxy

Proxy permite prover um substituto ou espaço reservado para outro objeto. Faz o controle de acesso ao objeto original, permitindo que possa realizar algumas coisa antes ou depois da requisição passar por ele.

- [Chat](docs/DS/dinamica-e-seminario-4-b/servicos/Chat.md#proxy)

## Referências

- GAMMA, Erich et al. **Design Patterns**: Elements of Reusable Object-Oriented Software. 1. ed. Massachusetts: Addison-Wesley Professional, 2009. 426 p. ISBN 0-201-63361-2.

- CARR, Richard. **Gang of Four Design Patterns**. [S. l.], 2009. Disponível em: http://www.blackwasp.co.uk/gofpatterns.aspx. Acesso em: 21 out. 2019.

- Refactoring Guru. **Design Patterns**. [S. l.], 2019. Disponível em: https://refactoring.guru/design-patterns. Acesso em: 21 out. 2019.
