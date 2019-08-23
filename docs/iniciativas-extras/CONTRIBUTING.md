# Guia de Contribuição  

## Como contribuir?

Para contribuir com o projeto é muito fácil e cada pouquinho conta! Basta seguir os seguintes passos:

* *Fork* do repositório (apenas para usuários externos)
* Criar [*issues*](CONTRIBUTING.md#política-de-issues)
* Criar [*branchs*](CONTRIBUTING.md#política-de-branches)
* Seguir a política de [*commits*](CONTRIBUTING.md#política-de-commits)
* Submeter [*Pull Request*](CONTRIBUTING.md#política-de-merges-e-pull-requests)


### Política de Issues

As *issues* devem possuir título, descrição, no mínimo um assinante responsável, *labels*,  *milestone*(a *sprint* que deve ser concluída).

Para criação de issue o [template Issue](ISSUE_TEMPLATE.md) deve ser seguido.

### Política de Branches  

#### *master*

A branch *master* é a branch de produção, onde ficará a versão estável do projeto. Ela estará bloqueada para commits e para pushs.
Veja a política de merges no tópico [Merges para *master*](CONTRIBUTING.md#merges-para-master).

#### *development*

A branch *development* é a branch de desenvolvimento, onde o trabalho das outras branchs será unificado e onde será criada uma versão estável para mesclar com a *master*.
Assim como a *master* ela está bloqueada para commits e pushs.
Veja a política de merges no tópico [Merges para development](CONTRIBUTING.md#merges-para-development)
merges para *development*</a> .

#### Nome das Branches  

As branchs de desenvolvimento de features serão criadas a partir da branch *development* com a nomenclatura padrão da lingua inglesa `x_issue_name`, onde o `x` representa o código de rastreio da issue.

### Política de Commits

Os commits devem ser feitos usando o parâmetro `-s` para indicar sua assinatura no commit e em inglês.

```
git commit -s
```
A issue em questão deve ser citada no commit, para isso, basta adicionar `#<issue_number>`.

```
 #5 Adding contribuition guide
```

** \*\*Por padrão, o caracter `#` define uma linha de comentário no arquivo da mensagem do commit. Para resolver este problema, use o commando:**
```
git config --local core.commentChar '!'
```

Igualmente, para commits em dupla deve ser usado o comando `-s` , e deve ser adicionado a assinatura da sua dupla.

```
git commit -s
```
Comentário do commit:
```
#5 Adding contribuition guide

Signed-off-by: Alex Turner <alex.turner@gmail.com>
```

Para que ambos envolvidos no commit sejam incluidos como contribuintes no gráfico de commits do GitHub, basta incluir a instrução `Co-authored-by:` na mensagem:

```
#5 Adding contribuition guide

Signed-off-by: Alex Turner <alex.turner@gmail.com>
Co-authored-by: Matthew Helders <matt.helders@gmail.com>
```


Para commits que encerram a resolução de uma issue, deve-se iniciar a mensagem do commit com `Fix #<issue_number> <mensagem>`, para que a issue seja [encerrada automaticamente](https://help.github.com/articles/closing-issues-using-keywords/) quando mesclada na `master`.

Exemplo de comentário do commit:
```
Fix #5 Setting project's contribuition guide
```

Para commits que incluem uma pequena mudança em uma issue que já teve sua resolução encerrada, deve-se iniciar a mensagem do commit com `HOTFIX #<issue_number> <message>`

Exemplo de comentário do commit:
```
HOTFIX #5 Updating project's contribuition guide
```

### Política de Merges e Pull Requests

#### Pull Requests

Pull requests devem ser feitos para a branch *master* seguindo as regras e os passos do tópico [*Merges para master*](CONTRIBUTING.md#merges-para-master). No conteúdo do pull request deve haver uma descrição clara do que foi feito.

Deve ser seguido o [template Pull Request](PULL_REQUEST_TEMPLATE.md).

##### Work in Progress

Caso haja a necessidade de atualizar a branch *master* antes de concluir a issue, o nome do pull request deve conter WIP:<X_nome_da_branch> para que a branch não seja deletada.

#### Merges para *master*
Os merges para *master* deverão ser feitos quando a funcionalidade ou refatoração estiverem de acordo com os seguintes aspectos:  

- Funcionalidade ou refatoração concluída;
- Funcionalidade revisada por algum outro membro.

Para fazer um merge para *master* os passos a serem seguidos são:  
- `git checkout branch_de_trabalho`;
- `git pull --rebase origin master`;
- `git push origin branch_de_trabalho`;
- Abrir pull request via interface GitHub;
- Aguardar Code Review


##### Code Review
O code review deve ser feito por um ou mais membros da equipe que não participaram das modificações.
Após pelo menos uma aprovação de Code Review,Pull Request poderá ser aceito;

Para aceitar o Pull Request, deve-se usar a opção *merge* no Github.

