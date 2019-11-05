# GoF's Criacionais

Os **GoF**'s (_Gang of Four_) são padrões de _design_ que visão prover soluções para problemas comum no desenvolvimento de _software_. No caso de _programação orientada à objetos_, os GoF's se propõem a solucionar problemas de interação e geração de objetos, que podem ser aplicados a contexto de problemas reais.São ferramentas poderosas no desenvolvimento de _softwares_.

Os **Padrões de Design Criacionais** (Creational Patterns) abstraem a instanciação de objetos. Eles ajudam a criar um sistema independente de como seus objetos são criados, compostos e representados.

## Histórico de Revisões

|    Data    | Versão |                          Descrição                           |            Autor(es)             |
| :--------: | :----: | :----------------------------------------------------------: | :------------------------------: |
| 21/10/2019 |  0.1   |                Cria a estrutura do documento                 |          Rogério Júnior          |
| 21/10/2019 |  0.2   |           Adiciona definição de GoF's Criacionais            |          Rogério Júnior          |
| 22/10/2019 |  0.3   | Adiciona definição de Factory Method e o serviço de FrontEnd |           Ésio Freitas           |
| 23/10/2019 |  0.4   |               Adicionando serviço de FrontEnd                |           Ésio Freitas           |
| 24/10/2019 |  0.5   |                   Padronizando o documento                   | Rogério Júnior e Youssef Muhamad |
| 24/10/2019 |  0.6   |            Adição dos patterns do serviço de Chat            | Rogério Júnior e Youssef Muhamad |
| 24/10/2019 |  0.7   |     Melhoria de algumas descrições e abordagem de GRASPS     |           Marcos Nery            |

## Factory Method

É um padrão de projeto que permite às classes delegar para subclasses decidirem os tipos de objetos que serão criados, isso é feito através da criação de objetos que chamam o método fabrica especificado numa interface e implementado por um classe filha ou implementado numa classe abstrata e opcionalmente sobrescrito por classes derivadas. Esse padrão ajuda a garantir os grasps de baixo acoplamento e creator.

- [Front-End](docs/DS/dinamica-e-seminario-4-b/servicos/front.md#factory-method)
- [User](docs/DS/dinamica-e-seminario-4-b/servicos/User.md#factory-method)
- [Pax](docs/DS/dinamica-e-seminario-4-b/servicos/Pax.md#factory-method)

<!-- ## Abstract Factory

[Descrição]

## Builder

[Descrição]

## Prototype

[Descrição] -->

## Singleton

Singleton é um padrão de design criacional que permite garantir que uma classe tenha apenas uma instância, enquanto fornece um ponto de acesso global a essa instância. Garantindo dessa forma que o dado objeto seja inicializado apenas uma vez.

- [API Gateway](docs/DS/dinamica-e-seminario-4-b/servicos/Gateway.md#Singleton)
- [Chat](docs/DS/dinamica-e-seminario-4-b/servicos/Chat.md#singleton)
- [Front-End](docs/DS/dinamica-e-seminario-4-b/servicos/front.md#Singleton)
- [User](docs/DS/dinamica-e-seminario-4-b/servicos/User.md#Singleton)
- [Pax](docs/DS/dinamica-e-seminario-4-b/servicos/Pax.md#Singleton)

<!-- ## Multiton

[Descrição]

## Object Pool

[Descrição] -->

## Referências

- GAMMA, Erich et al. **Design Patterns**: Elements of Reusable Object-Oriented Software. 1. ed. Massachusetts: Addison-Wesley Professional, 2009. 426 p. ISBN 0-201-63361-2.

- CARR, Richard. **Gang of Four Design Patterns**. [S. l.], 2009. Disponível em: http://www.blackwasp.co.uk/gofpatterns.aspx. Acesso em: 21 out. 2019.

- Refactoring Guru. **Design Patterns**. [S. l.], 2019. Disponível em: https://refactoring.guru/design-patterns. Acesso em: 21 out. 2019.
