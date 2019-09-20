# Plano de Gerenciamento de Configuração de Software

### Histórico de Revisão

| Data     | Versão | Descrição            | Autor(es)     |
| -------- | ------ | -------------------- | ------------- |
| 19/09/19 | 1.0    | Criação do Documento | Felipe Campos |

## 1 - Introdução

Neste documento, será descrito o planejamento dos principais itens relevantes em relação a Gerência de Configuração. Esse documento busca definir as Políticas de Configurações que serão utilizadas ao longo do desenvolvimento e manutenção do projeto.

## 3 - Tecnologias

## 3.1 - Node.js

### 3.1.1 - Ambiente de Desenvolvimento

O Ambiente de desenvolvimento node.js foi construído utilizando ferramentas para prover conforto e produtividade para o desenvolvedor.

- ## Ferramentas

  - [Visual Studio Code]()
  - [ESLint](https://eslint.org)
  - [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) (Extensão do VSCode)
  - [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) (Extensão do VSCode)
  - [EditorConfig](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig) (Extensão do VSCode)
  - [Docker](https://www.docker.com/)
  - [Docker](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker) (Extensão do VSCode)
  - [Docker Compose](https://docs.docker.com/compose/gettingstarted/)

- ### Visual Studio Code

  Editor de texto que atende perfeitamente as necessidades do desenvolvedor node.js, foi escolhido por ser o padrão da comunidade, alem de sua grande quantidade de extensões que facilitam o processo de desenvolvimento.

- ### ESLint

  O ESLint é uma ferramenta de análise de código estático para identificar padrões problemáticos encontrados no código JavaScript. Escolhido para padronizar o guia de estilo do código. A extensão do VSCode facilita a padronização.

- ### Prettier

  O Prettier é um code formatter que tem por finalidade "forçar" um padrão de código. Ele realiza isso analisando o seu código e alterando-o de acordo com regras pré-definidas. Escolhido por sua integração simples VSCode e ao ESLint.

- ### EditorConfig

  O EditorConfig ajuda a manter o estilo de código consistente para vários desenvolvedores que trabalham no mesmo projeto em vários editores e IDEs. Escolhido para que não haja nenhum erro caso algum desenvolvedor queira utilizar outro editor de texto ou IDE.

- ### Docker

  O Docker fornece uma camada adicional de abstração e automação de virtualização de nível de sistema operacional no Windows e no Linux. Escolhido para empacotar todas as dependências necessárias para o desenvolvimento e funcionamento da aplicação.
  A extensão do VSCode auxilia no build de imagens e na composição de containers.

- ### Docker Compose

  Docker Compose é o orquestrador de containers da Docker. Escolhido para realizar a composição dos containers necessários para o desenvolvimento da aplicação.

- ## Instalação do Ambiente de Desenvolvimento em Ambiente Linux

  - ### Visual Studio Code

  https://code.visualstudio.com/download

- ### ESLint

  O ESLint será instalado dentro do container Docker, sendo dispensável a instalação local. Dessa forma, é necessária apenas a instalação da extensão para o VSCode.

  https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint

- ### Prettier

  https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode

  Após a instalação, são necessárias algumas configurações adicionais:

  - No VSCode, utiliza Ctrl + Shifr + P para abrir a barra de comandos, e pesquise por
    "Preferences: Open Settings (JSON)".
  - Ao abrir o arquivo _settings.json_, adicione as seguintes linhas:

          "editor.formatOnSave": true,
          "prettier.eslintIntegration": true,

  - Salve o arquivo _settings.json_

- ### EditorConfig

  https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig

- ### Docker

  Execute no terminal, os seguintes comandos;

        $ wget -qO- https://get.docker.com/ | sh
        $ sudo usermod -aG docker seu_usuario_aqui

  Não esqueça de utilizar o usuário do sistema operacional no lugar de _seu_usuario_aqui_.

- ### Docker Compose

  Execute no terminal, os seguintes comandos;

        $ sudo curl -L https://github.com/docker/compose/releases/download/1.25.0-rc2/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
        $ sudo chmod +x /usr/local/bin/docker-compose

- ## Execução do Ambiente de Desenvolvimento em Ambiente Linux

  Clone algum dos repositórios baseados em node.js:

        $ git clone https://github.com/pax-app/Pax_Gateway

  Abra o VSCode dentro do repositório:

        $ cd Pax_Gateway
        $ code .

  Com o botão direito, clique no arquivo _Dockerfile_, e execute o comando _Build Image_.

  Em seguida, clique com o botão direito no arquivo _docker-compose.yaml_, e execute o comando _Compose Up_, ou, execute no terminal

        $ docker-compose up

## 3.2 - Flask

## 3.3 - Flutter
