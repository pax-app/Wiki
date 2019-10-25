# [Front-End](https://github.com/pax-app/Frontend)

Camada da aplicação responsável pela interação com o usuário.

## Padrões usados:

### Factory Method

O _Flutter_ possui uma arquitetura chamada BLoC (_Business Logic Component_), a qual tem
a função de separar a lógica de negócio da UI através do uso de _Streams_. Em suma, _stream_
é uma fonte de eventos assíncronos.

> Em termos práticos, essa arquitetura BLoC pode ser comparada com o padrão de projeto ‘factory method’.

![Factory](../../../../assets/Patterns/Frontend/factory_method.svg)

Arquivo: [general_category_bloc.dart](https://github.com/pax-app/Frontend/blob/devel/lib/blocs/general_category_bloc.dart)

### [⬅](docs/DS/dinamica-e-seminario-4-b/criacionais.md#factory-method)

### State

O Flutter por default vem com a arqitetura Lifting State Up (Vanilla), o qual
é uma derivação do state. Todas as variáveis dentro da classe fazem parte do estado do widget.
Nisso, quando alguma delas é alterada no setState(), toda a aplicação é renderizada.

![State](../../../../assets/Patterns/Frontend/state.svg)

Arquivo: [became_provider_screen.dart](https://github.com/pax-app/Frontend/blob/e17214d9cbd13c0a9801042e556069c6cf8d616c/lib/screens/became_provider_screen/became_provider_screen.dart)

### [⬅](docs/DS/dinamica-e-seminario-4-b/comportamentais.md#state)

### Singleton

No Front-End, usamos a classe Api como um singleton para fazer toda a comunição do front com o gateway, além de utilizar o singleton para lidar com informações de autenticação e utilizar o singleton nativo do flutter.

![](../../../../assets/Patterns/Front/singleton_api.svg)
![](../../../../assets/Patterns/Front/singleton_usuario.svg)
![](../../../../assets/Patterns/Front/singleton_preferences.svg)

Arquivos:

- [api.dart](https://github.com/pax-app/Frontend/blob/142_faixas_de_preco/lib/services/api.dart)
- [loggedUser.dart](https://github.com/pax-app/Frontend/blob/142_faixas_de_preco/lib/services/loggedUser.dart)
- [shared_preferences.dart](https://github.com/flutter/plugins/blob/6deda07662e420d747896a886518fd2855451fde/packages/shared_preferences/lib/shared_preferences.dart)

### [⬅](docs/DS/dinamica-e-seminario-4-b/criacionais.md#singleton)

### Strategy

A BaseScreen é o padrão que toda tela deve seguir, ela possui o contexto para o resto da página _Widget_ body, e como toda tela no flutter herda de _Widget_ existe a garantia de que esse contexto sempre existirá.

![Strategy](../../../../assets/Patterns/Frontend/strategy.svg)

Arquivo: [base_screen.dart](https://github.com/pax-app/Frontend/blob/142_faixas_de_preco/lib/components/base_screen/base_screen.dart)

### [⬅](docs/DS/dinamica-e-seminario-4-b/comportamentais.md#strategy)

### Memento

O Flutter usa o padrão memento na pilha de navegação.

![Memento](../../../../assets/Patterns/Frontend/memento.svg)

Arquivo: [config_screen.dart](https://github.com/pax-app/Frontend/blob/e17214d9cbd13c0a9801042e556069c6cf8d616c/lib/screens/config_screen/config_screen.dart)

### [⬅](docs/DS/dinamica-e-seminario-4-b/comportamentais.md#memento)

### Observer

No Chat da aplicação está sendo utilizado a classe _StreamBuilder_, que espera uma _Stream_ para para fazer a _subscription_ na entidade que pode ser observada. Neste caso o que será observado é a instância do firestore(um banco de dados do Firebase que reage a mudanças), sempre que o _StreamBuilder_ receber modificações via _notify_ do firestore será executado o método passado para o parâmetro _builder_, que neste caso é o método de _update_.

![Observable](../../../../assets/Patterns/Frontend/stream_observable.svg)

O método _update_ abaixo é responsável por atualizar esta classe com base nas novas informações recebidas via _Stream_

![update](../../../../assets/Patterns/Frontend/observer_update.svg)

Arquivo: [chat_screen.dart](https://github.com/pax-app/Frontend/blob/e17214d9cbd13c0a9801042e556069c6cf8d616c/lib/screens/chat_screen/chat_screen.dart)

### [⬅](docs/DS/dinamica-e-seminario-4-b/comportamentais.md#observer)
