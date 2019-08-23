# Brainstorm



## Histórico de Revisões

|    Data    | Versão |                Descrição                 |   Autor(es)   |
| :--------: | :----: | :--------------------------------------: | :-----------: |
| 22/08/2019 |  1.0   | Adicionado V1 da documentação do brainstorm |  Gabriel Albino  |


## Metodologia
### Primeira Etapa - Elicitação de ideias
O brainstorm foi realizado pelos membros do grupo para elicitação de funcionalidades importantes para o aplicativo a partir dos artefatos de elicitação anteriores. No inicio do brainstorm foram definidas duas métricas para nortear as funcionalidades: 
* aplicativo seria focado no contrantante, isto é, em quem busca o serviço
* Tanto o contratante como o contratado usarão o mesmo sistema, não haverá separação de apps.

Com isso em vista os membros começaram a elicitar e explicar as funcionalidades que o app deveria ter, que foram:

| Funcionalidade	| Observação	|		
|---------------------------------------------------------|--------------------------------------------------------------------------------------------|				
| Chat	| Chat para o prestador se comunicar com o contratante	|		
| Lista de serviços	| Lista de serviços disponíves no app	|		
| Sistema de avaliação	| Sistema de avaliação onde o contratante avalia o contratado e vice-versa	|		
| Recomendação baseada na localização	| Usuários prestadores de serviço que estão perto da cidade do contratante aparecem primeiro |			
| Recomendação baseada na avaliação	| Usuários prestadores de serviço com boa avaliação aparecem primeiro	|		
| Lista de favoritos	| Lista de serviços utilizado com frequência	|		
| Histórico de serviços	| Histórico de serviços já prestado por aquele prestador	|		
| Lista de prestadores de serviço	| Lista de prestadores de serviço disponíveis no APP	|		
| Pagamento IN-APP	| Pagamento direto pelo APP	|		
| Perfil de Usuário	| Perfil do usuário com avaliações e informações	|		
| Prestador "Validado"	| Prestador de serviço com o perfil completo recebe um selo	|		
| Perfil "Normal" e "Premium" para prestadores de serviço | Prestador de serviço que paga taxa mensal recebe um selo	|			
| Categorização de serviços	| Serviços são categorizados por temas	|		
| Nívels de complitude do perfil	| Gameficação para incentivar os usuários a preencherem completamente o perfil	|		
| Ver prestadores de serviço no mapa	| Ver a localização dos prestadores de serviço	|		
| Cadastro de pequenas empresas	| Cadastrar pequenas empresas prestadoras de serviço no app	|


![Foto 1](https://i.imgur.com/MNNe0NA.png)

### Segunda Etapa - Compactação de ideias

Após a elicitação inicial foi feito o merge de algumas funcionalidades em outras que tinham um nível de similaridade elevado, resultando na seguinte lista: 

|Funcionalidade                                         |Observação                                                                                   |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------|
|Chat                                                   |Chat para o prestador se comunicar com o contratante                                         |
|Lista de serviços                                      |Lista de serviços disponíves no app                                                          |
|Sistema de avaliação                                   |Sistema de avaliação onde o contratante avalia o contratado e vice-versa                     |
|Sistema de report                                      |Usuários podem reportar um serviço prestado                                                  |
|Recomendação                                           |Usuários prestadores de serviço com boa avaliação e com localização próxima aparecem primeiro|
|Lista de favoritos                                     |Lista de serviços utilizado com frequência                                                   |
|Histórico de serviços                                  |Histórico de serviços já prestado por aquele prestador                                       |
|Lista de prestadores de serviço                        |Lista de prestadores de serviço disponíveis no APP                                           |
|Pagamento IN-APP                                       |Pagamento direto pelo APP                                                                    |
|Perfil de Usuário                                      |Perfil do usuário com avaliações e informações                                               |
|Prestador "Validado"                                   |Prestador de serviço com o perfil completo recebe um selo                                    |
|Perfil "Normal" e "Premium" para prestadores de serviço|Prestador de serviço que paga taxa mensal recebe um selo                                     |
|Categorização de serviços                              |Serviços são categorizados por temas                                                         |
|Nívels de complitude do perfil                         |Gamificação para incentivar os usuários a preencherem completamente o perfil                 |
|Ver prestadores de serviço no mapa                     |Ver a localização dos prestadores de serviço                                                 |

![Imagem 2](https://i.imgur.com/7xJ0K7m.png)

### Terceira Etapa - Escolha de ideias

Após isso os membros votaram nas funcionalidades, cada membro tinha 3 pontos positivos e 1 ponto negativo para distribuir, justificando o ponto.

A tabela com o resultado final e as justificativas encontram-se abaixo:

|Funcionalidade                                         |Observação                                                                                   |Votos positivos|Votos Negativos|Votos positivos do PO|Justificativas                                                                              |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------|---------------|---------------|---------------------|--------------------------------------------------------------------------------------------|
|Chat                                                   |Chat para o prestador se comunicar com o contratante                                         |8              |0              |2                    |  Vai evitar evasão do usuário, pois evita troca de número pessoal                          |
|Lista de serviços                                      |Lista de serviços disponíves no app                                                          |               |0              |0                    |  Entendeu-se como uma funcionalidade core do aplicativo, não necessitando votos.           |
|Sistema de avaliação                                   |Sistema de avaliação onde o contratante avalia o contratado e vice-versa                     |6              |0              |1                    |  A availiação vai ajudar a garantir a confiabilidade do serviço prestado                   |
|Sistema de report                                      |Usuários podem reportar um serviço prestado                                                  |1              |0              |0                    |  Funcionalidade importante para evitar com que ocorram golpes                              |
|Recomendação                                           |Usuários prestadores de serviço com boa avaliação e com localização próxima aparecem primeiro|2              |0              |1                    |  Funcionalidade que daria impacto e valor à avaliação                                      |
|Lista de favoritos                                     |Lista de serviços utilizado com frequência                                                   |               |1              |0                    |  Uma funcionalidade que seria importante, porém não é fundamental para o aplicativo        |
|Histórico de serviços                                  |Histórico de serviços já prestado por aquele prestador                                       |1              |0              |1                    |  Importante para que o contratante veja as avaliações anteriores dos prestadores de serviço|
|Lista de prestadores de serviço                        |Lista de prestadores de serviço disponíveis no APP                                           |0              |1              |0                    |  Uma funcionalidade que seria importante, porém não é fundamental para o aplicativo        |
|Pagamento IN-APP                                       |Pagamento direto pelo APP                                                                    |4              |0              |1                    |  Garante uma segurança maior para o prestador de serviço e para o contratante              |
|Perfil de Usuário                                      |Perfil do usuário com avaliações e informações                                               |1              |0              |0                    |  Garante uma segurança maior para o prestador de serviço e para o contratante              |
|Prestador "Validado"                                   |Prestador de serviço com o perfil completo recebe um selo                                    |4              |0              |0                    |  Garante uma segurança maior para o prestador de serviço e para o contratante              |
|Perfil "Normal" e "Premium" para prestadores de serviço|Prestador de serviço que paga taxa mensal recebe um selo                                     |2              |0              |0                    |  Garante uma segurança maior para o prestador de serviço e para o contratante              |
|Categorização de serviços                              |Serviços são categorizados por temas                                                         |1              |0              |0                    |  Garante uma melhor organização e interface do app                                         |
|Nívels de complitude do perfil                         |Gameficação para incentivar os usuários a preencherem completamente o perfil                 |0              |3              |0                    |  Uma funcionalidade que seria importante, porém não é fundamental para o aplicativo        |
|Ver prestadores de serviço no mapa                     |Ver a localização dos prestadores de serviço                                                 |0              |4              |0                    |  Não foi julgada como uma funcionalidade fundamental                                       |


![Imagem 3](https://i.imgur.com/o5P1fvO.png)


## Requisitos Elicitados

### Requisitos Funcionais
* O sistema deve possuir um chat 
* O sistema deve ter uma lista de serviços disponíveis para contratação
* O sistema deve ter um sistema de avaliação em estrelas
* O sistema deve possuir um sistema para usuários reportaram serviços contratados ou prestados
* O sistema deverá exibir os pretadores de serviço com boa avaliação e próximos com prioridade
* O sistema deverá permitir com que o usuário marque um serviço como favorito
* O sistema deverá ter a lista de serviços prestados ou contratados anteriormente, assim como sua avaliação.
* O sistema deverá possuir uma lista com todos os prestadores de serviço cadastrados
* O sistema deverá possuir opção de pagamento pelo app
* O usuário deverá ter um perfil com informações e informações sobre ele
* O sistema deverá diferenciar prestadores de serviço com o perfil completamente preenchido dos demais
* O sistema deverá possuir conta premium, dando destaque ao prestador de serviço que possuir o serviço.
* O sistema deverá organizar os serviços prestados por categoria.
* O sistema deverá ter gameficação para incentivar o usuário a preencher todas as informações do perfil
* O sistema deverá exibir a localização do prestador de serviço
