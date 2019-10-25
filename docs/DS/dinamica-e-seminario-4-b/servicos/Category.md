# [Category](https://github.com/pax-app/Category)

Camada da aplicação responsável pelas categorias gerais e de serviço disponíveis no sistema.

## Padrões usados:

### Strategy

O Strategy é um _Design Pattern_ comportamental que permite definir uma família de algoritmos, colocar cada um deles em uma classe separada e tornar seus objetos intercambiáveis.

É frequentemente usado em várias estruturas para fornecer aos usuários uma maneira de alterar o comportamento de uma classe sem estendê-lo.

O Strategy foi utilizado como forma de usar diferentes variações do método de retorno da API de acordo com cada tipo de categoria definida.

<img src="https://i.imgur.com/oPSgBlQ.png">

**Arquivo:** [models.py](https://github.com/pax-app/Category/blob/devel/project/api/models.py)

### Facade

O Facade é especialmente útil ao trabalhar com bibliotecas e APIs complexas.

Facade pode ser reconhecida em uma classe que possui uma interface simples, mas delega a maior parte do trabalho para outras classes. Geralmente, as fachadas gerenciam o ciclo de vida completo dos objetos que à usam.

<img src="https://i.imgur.com/P0ypUkk.png">

**Arquivo:** [init.py](https://github.com/pax-app/Category/blob/devel/project/__init__.py)

<img src="https://i.imgur.com/4NwwZhh.png">

**Arquivo:** [views.py](https://github.com/pax-app/Category/blob/devel/project/api/views.py)

## Padrões não usados:

### Composite

De início, foi uma possíbilidade a utilização do _Design Pattern_ Composite, porém, sua aplicação em uma representação de árvore das categorias foi descartada por aumentar a complexidade, e o entendimento do código, por enquanto.
