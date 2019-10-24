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
  src="https://carbon.now.sh/embed/?bg=rgba(171%2C%20184%2C%20195%2C0)&t=dracula&wt=none&l=auto&ds=true&dsyoff=0px&dsblur=25px&wc=false&wa=true&pv=56px&ph=56px&ln=true&fl=1&fm=Hack&fs=14px&lh=177%25&si=false&es=2x&wm=false&code=onChanged%253A(double%2520newLowerValue%252C%2520double%2520newUpperValue)%2520%257B%250A%2520%2509setState(()%2520%257B%250A%2520%2520%2520%2520%2520%2520_lowerValue%2520%253D%2520newLowerValue%253B%250A%2520%2520%2520%2520%2520%2520_upperValue%2520%253D%2520newUpperValue%253B%250A%2509%257D)%253B%250A%257D"
  style="transform:scale(1); width:100%; height:300px; border:0; overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

**Acesso ao padrão:** [BecameProviderScreen](https://github.com/pax-app/Frontend/blob/e17214d9cbd13c0a9801042e556069c6cf8d616c/lib/screens/became_provider_screen/became_provider_screen.dart)

### Singleton

No Front-End, usamos a classe Api como um singleton para fazer toda a comunição do front com o gateway. 

<iframe
  src="https://carbon.now.sh/embed/?bg=rgba(171%2C%20184%2C%20195%2C0)&t=dracula&wt=none&l=auto&ds=true&dsyoff=0px&dsblur=25px&wc=false&wa=true&pv=56px&ph=56px&ln=true&fl=1&fm=Hack&fs=14px&lh=177%25&si=false&es=2x&wm=false&code=class%2520Api%2520%257B%250A%2520%2520static%2520String%2520url%2520%253D%2520%2522http%253A%252F%252F172.18.0.1%253A5001%252Fauth%252Flogin%2522%253B%250A%2520%2520Future%253Cint%253E%2520logIn()%2520async%2520%257B%250A%2520%2520%2520%2520final%2520email%2520%253D%2520_emailController.value%253B%250A%2520%2520%2520%2520final%2520password%2520%253D%2520_passwordController.value%253B%250A%2520%2520%2520%2520Map%253CString%252C%2520String%253E%2520body%2520%253D%2520%257B'email'%253A%2520email%252C%2520'password'%253A%2520password%257D%253B%250A%2520%2520%2520%2520Map%253CString%252C%2520String%253E%2520header%2520%253D%2520%257B'content-type'%253A%2520'application%252Fjson'%257D%253B%250A%250A%2520%2520%2520%2520var%2520jsonBody%2520%253D%2520json.encode(body)%253B%250A%2520%2520%2520%2520final%2520response%2520%253D%2520await%2520http.post(%250A%2520%2520%2520%2520%2520%2520url%252C%250A%2520%2520%2520%2520%2520%2520headers%253A%2520header%252C%250A%2520%2520%2520%2520%2520%2520body%253A%2520jsonBody%252C%250A%2520%2520%2520%2520)%253B%250A%2520%2520%2520%2520if%2520(response.statusCode%2520%253D%253D%2520200)%2520%257B%250A%2520%2520%2520%2520%2520%2520final%2520responseJson%2520%253D%2520json.decode(response.body)%253B%250A%250A%2520%2520%2520%2520%2520%2520saveCurrentLogin(responseJson)%253B%250A%2520%2520%2520%2520%257D%250A%2520%2520%2520%2520return%2520response.statusCode%253B%250A%2520%2520%257D%250A%257D"
  style="transform:scale(1); width:100%; height:680px; border:0; overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

**Acesso ao padrão:** [Api](https://github.com/pax-app/Frontend/blob/142_faixas_de_preco/lib/services/api.dart)

### Strategy

No Front usamos uma lógica o qual teria uma página base, isto é, um página que teria tudo que uma página deveria ter. Nisso, dependendo do o que é passado para ela como parâmetro, ela 
se adaptaria aos argumentos. 

<iframe
  src="https://carbon.now.sh/embed/?bg=rgba(171%2C%20184%2C%20195%2C0)&t=dracula&wt=none&l=auto&ds=true&dsyoff=0px&dsblur=25px&wc=false&wa=true&pv=56px&ph=56px&ln=true&fl=1&fm=Hack&fs=14px&lh=177%25&si=false&es=2x&wm=false&code=class%2520BaseScreen%2520extends%2520StatelessWidget%2520%257B%250A%2520%2520final%2520String%2520pageTitle%252C%2520appBarTitle%253B%250A%2520%2520final%2520Widget%2520body%252C%2520drawer%253B%250A%2520%2520final%2520bool%2520padding%253B%250A%2520%2520BaseScreen(this.appBarTitle%252C%2520this.pageTitle%252C%2520this.body%252C%2520this.drawer%252C%250A%2520%2520%2520%2520%2520%2520%257Bthis.padding%2520%253D%2520true%257D)%253B%250A%250A%2520%2520%2540override%250A%2520%2520Widget%2520build(BuildContext%2520context)%2520%257B%250A%2520%2520%2520%2520%252F%252FN%25C3%25A3o%2520h%25C3%25A1%2520o%2520c%25C3%25B3digo%2520do%2520componente%2520para%2520melhor%2520visualizar%2520a%2520classe%250A%2520%2520%2520%2520return%2520componente()%253B%250A%2520%2520%257D%250A%257D"
  style="transform:scale(1); width:100%; height:480px; border:0; overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

**Acesso ao padrão:** [BaseScreen](https://github.com/pax-app/Frontend/blob/142_faixas_de_preco/lib/components/base_screen/base_screen.dart)

### Observer
O Flutter usa uma classe StreamBuilder a qual fica observando a alteração de alguma variável
do bloc e com isso, renderiza a tela de acordo com a alteração.

<iframe
  src="https://carbon.now.sh/embed/?bg=rgba(171%2C%20184%2C%20195%2C0)&t=dracula&wt=none&l=auto&ds=true&dsyoff=0px&dsblur=25px&wc=false&wa=true&pv=56px&ph=56px&ln=true&fl=1&fm=Hack&fs=14px&lh=177%25&si=false&es=2x&wm=false&code=child%253A%2520StreamBuilder(%250A%2520%2520%2520%2520stream%253A%2520_firestore%250A%2520%2520%2520%2520%2520%2520%2520%2520.collection(chat_id)%250A%2520%2520%2520%2520%2520%2520%2520%2520.orderBy('date_time_sent'%252C%2520descending%253A%2520true)%250A%2520%2520%2520%2520%2520%2520%2520%2520.snapshots()%252C%250A%2520%2520%2520%2520builder%253A%2520(context%252C%2520snapshot)%2520%257B%250A%2520%2520%2520%2520%2520%2520%252F%252F%2520Strategy%250A%2520%2520%2520%2520%2520%2520if%2520(!snapshot.hasData)%250A%2520%2520%2520%2520%2520%2520%2520%2520return%2520Center(child%253A%2520CircularProgressIndicator())%253B%250A%250A%2520%2520%2520%2520%2520%2520if%2520(snapshot.data.documents.length%2520%253C%253D%25200)%2520%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520return%2520Center(%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520child%253A%2520Text(%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520'Inicie%2520a%2520conversa%2520%253A)'%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520style%253A%2520Theme.of(context).textTheme.title%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520)%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520)%253B%250A%2520%2520%2520%2520%2520%2520%257D%250A%250A%2520%2520%2520%2520%2520%2520return%2520ChatList(%250A%2520%2520%2520%2520%2520%2520%2520%2520snapshot%253A%2520snapshot.data.documents%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520isProvider%253A%2520isProvider%252C%250A%2520%2520%2520%2520%2520%2520)%253B%250A%2520%2520%2520%2520%257D%252C%250A%2520%2520)%252C%250A)%252C"
  style="transform:scale(1); width:100%; height:780px; border:0; overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

**Acesso ao padrão:** [ChatScreen](https://github.com/pax-app/Frontend/blob/e17214d9cbd13c0a9801042e556069c6cf8d616c/lib/screens/chat_screen/chat_screen.dart)

### Memento

O Flutter usa o padrão memento na pilha de navegação.

<iframe
  src="https://carbon.now.sh/embed/?bg=rgba(171%2C%20184%2C%20195%2C0)&t=dracula&wt=none&l=auto&ds=true&dsyoff=0px&dsblur=25px&wc=false&wa=true&pv=56px&ph=56px&ln=true&fl=1&fm=Hack&fs=14px&lh=177%25&si=false&es=2x&wm=false&code=Navigator.of(context).push(%250A%2509MaterialPageRoute(%250A%2509%2509builder%253A%2520(context)%2520%253D%253E%2520BaseScreen(%250A%2520%2520%2520%2520%2520%2520%2520%2520%2509%2522%2522%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520%2509%2522%2522%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520%2509EditPerfilTab()%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520%2509null%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520)%252C%250A%2520%2520%2520%2520)%252C%250A)%253B"
  style="transform:scale(1); width:100%; height:400px; border:0; overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

**Acesso ao padrão:** [ConfigScreen](https://github.com/pax-app/Frontend/blob/e17214d9cbd13c0a9801042e556069c6cf8d616c/lib/screens/config_screen/config_screen.dart)

### [⬅](docs/DS/dinamica-e-seminario-4-b/criacionais.md#factory-method)