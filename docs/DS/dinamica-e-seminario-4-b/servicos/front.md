# [Front-End](https://github.com/pax-app/Frontend)

Esse serviço se encontra toda a interface que os usuários do aplicativo vai interagir.

## Padrões usádos:

### Factory Method
O Flutter tem uma arquitetura chamada BLoC (Business Logic Component), o qual tem
a função de separar a logica de negócio da UI através do uso de Streams. Em suma, stream 
é uma fonte de eventos assíncronos.

> Em termos práticos, essa arquitetura BLoC pode ser comparada com o padrão de projeto ‘factory method’.

<iframe
  src="https://carbon.now.sh/embed/?bg=rgba(255%2C255%2C255%2C0)&t=dracula&wt=none&l=auto&ds=true&dsyoff=0px&dsblur=25px&wc=false&wa=true&pv=41px&ph=50px&ln=true&fl=1&fm=Hack&fs=14px&lh=177%25&si=false&es=1x&wm=false&code=class%2520GeneralCategoryBloc%2520implements%2520BlocBase%2520%257B%250A%2520%2520List%253CGeneralCategory%253E%2520apiGeneralCategories%2520%253D%2520List%253CGeneralCategory%253E()%253B%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%250A%2520%250A%2520%2520final%2520_outGeneralCategoryController%2520%253D%250A%2520%2520%2520%2520%2520%2520BehaviorSubject%253CList%253CGeneralCategory%253E%253E()%253B%250A%2520%2520Stream%2520get%2520outGeneralCategories%2520%253D%253E%2520_outGeneralCategoryController.stream%253B%250A%2520%250A%2520%2520GeneralCategoryBloc()%2520async%2520%257B%250A%2520%2520%2520%2520apiGeneralCategories%2520%253D%2520await%2520Api.getGeralCateories()%253B%250A%2520%2520%2520%2520_outGeneralCategoryController.sink.add(apiGeneralCategories)%253B%250A%2520%2520%257D%250A%250A%2520%2520%2540override%250A%2520%2520void%2520dispose()%2520%257B%250A%2520%2520%2520%2520_outGeneralCategoryController.close()%253B%250A%2520%2520%257D%250A%257D"
  style="transform:scale(1); width:100%; height:580px; border:0; overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

**Acesso ao padrão:** [GeralCategoryBloc](https://github.com/pax-app/Frontend/blob/devel/lib/blocs/general_category_bloc.dart)

### State

O Flutter por default vem com a arqitetura Lifting State Up (Vanilla), o qual 
é uma derivação do state. Todas as variáveis dentro da classe fazem parte do estado do widget.
Nisso, quando alguma delas é alterada no setState(), toda a aplicação é renderizada.

<iframe
  src="https://carbon.now.sh/embed/?bg=rgba(171%2C%20184%2C%20195%2C%201)&t=dracula&wt=none&l=auto&ds=true&dsyoff=0px&dsblur=25px&wc=false&wa=true&pv=56px&ph=56px&ln=true&fl=1&fm=Hack&fs=14px&lh=177%25&si=false&es=2x&wm=false&code=onChanged%253A(double%2520newLowerValue%252C%2520double%2520newUpperValue)%2520%257B%250A%2520%2509setState(()%2520%257B%250A%2520%2520%2520%2520%2520%2520_lowerValue%2520%253D%2520newLowerValue%253B%250A%2520%2520%2520%2520%2520%2520_upperValue%2520%253D%2520newUpperValue%253B%250A%2509%257D)%253B%250A%257D"
  style="transform:scale(1); width:100%; height:580px; border:0; overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

**Acesso ao padrão:** [BecameProviderScreen](https://github.com/pax-app/Frontend/blob/e17214d9cbd13c0a9801042e556069c6cf8d616c/lib/screens/became_provider_screen/became_provider_screen.dart)

### Singleton

### Strategy

### Observer

### Decorator

[Porque usou esse padrão / Porque não usou outro]


### [⬅](docs/DS/dinamica-e-seminario-4-b/criacionais.md#factory-method)