# [Front-End](https://github.com/pax-app/Frontend)

Camada da aplicação responsável pela interação com o usuário.

## Padrões usados:

### Factory Method

O _Flutter_ possui uma arquitetura chamada BLoC (_Business Logic Component_), a qual tem
a função de separar a lógica de negócio da UI através do uso de _Streams_. Em suma, _stream_
é uma fonte de eventos assíncronos.

> Em termos práticos, essa arquitetura BLoC pode ser comparada com o padrão de projeto Factory Method.

<iframe
  src="https://carbon.now.sh/embed/?bg=rgba(255%2C255%2C255%2C0)&t=dracula&wt=none&l=auto&ds=true&dsyoff=0px&dsblur=25px&wc=false&wa=true&pv=56px&ph=56px&ln=true&fl=1&fm=Hack&fs=14px&lh=177%25&si=false&es=4x&wm=false&code=class%2520GeneralCategoryBloc%2520implements%2520BlocBase%2520%257B%250A%2509List%253CGeneralCategory%253E%2520apiGeneralCategories%2520%253D%2520List%253CGeneralCategory%253E()%253B%250A%2509final%2520_outGeneralCategoryController%2520%253D%2520BehaviorSubject%253CList%253CGeneralCategory%253E%253E()%253B%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%250A%2520%2520%2509Stream%2520get%2520outGeneralCategories%2520%253D%253E%2520_outGeneralCategoryController.stream%253B%250A%250A%2520%2520%2520%2520GeneralCategoryBloc()%2520async%2520%257B%250A%2520%2520%2520%2520%2520%2520apiGeneralCategories%2520%253D%2520await%2520Api.getGeneralCategories()%253B%250A%2520%2520%2520%2520%2520%2520_outGeneralCategoryController.sink.add(apiGeneralCategories)%253B%250A%2520%2520%2520%2520%257D%250A%2520%2520%250A%2520%2520%2509%2540override%250A%2520%2520%2509void%2520dispose()%2520%257B%250A%2520%2520%2520%2520%2520_outGeneralCategoryController.close()%253B%250A%2520%2520%2520%2520%257D%2520%250A%257D"
  style="transform:scale(1); width:115%; height:550px; border:0; overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

**Arquivo:** [general_category_bloc.dart](https://github.com/pax-app/Frontend/blob/devel/lib/blocs/general_category_bloc.dart)

### State

### Singleton

### Strategy

### Observer

### Decorator

[Porque usou esse padrão / Porque não usou outro]

### [⬅](docs/DS/dinamica-e-seminario-4-b/criacionais.md#factory-method)
