# Tarefa 01

Para nossa primeira tarefa, vamos iniciar criando um branch a partir da main do repositório, cada tarefa deve ser desenvolvida criando um branch para o seu desenvolvimento

Em seguida em uma pasta chamada “projeto” realize a criação de um projeto de uma WEB API na tecnologia que escolheu com o nome Quiron.Api

Para isso após a criação da API em branco devemos ter a seguinte estrutura

projeto<br/>
| -  Quiron.Api<br/>
| -  Quiron.sln<br/>

Como optei pelo C#, ao criar meu projeto defini o nome da solução como Quiron e o nome do projeto como Quiron.Api, utilizei as versões mais recentes disponíveis no momento do .NET e dos pacotes padrões com os quais o projeto já nasce

O próximo passo e criar uma pasta dentro da nossa solução chamada “1-Presentation” esta pasta servira para conter os projetos referentes a camada de apresentação da nossa API, aqueles projeto que vão ser podemos dizer o frontend da nossa aplicação, que por hora será apenas o Quiron.Api, pois o mesmo será responsável por expor as rotas pelas quais será possível consumir nossa aplicação

Em seguida crie mais 4 pastas:<br/>

<b>2-Domain</b> <i>(vai conter os projetos da camada de domínio, responsável por guardar nossas classes, interfaces e tipos para que estejam disponíveis em todos os projetos que vão compor nossa solução)</i><br/>
<b>3-Application</b> <i>(vai conter os projetos da camada de aplicação, ou seja, o core de negócio do nosso projeto, contendo regras, validações e utilitários)</i><br/>
<b>4-Infra</b> <i>(vai conter os projetos da camada de infraestrutura, ou seja, acesso a dados, possibilitando a persistência e leitura de informações em um banco de dados)</i><br/>
<b>5-Test</b> <i>(Vai conter os projetos da camada de testes unitários da nossa aplicação)</i><br/>

Apos a criação das pastas, o projeto Quiron.Api deve ser movido para a pasta 1-Presentation

Esta separação em camadas definindo responsabilidades nos possibilita reutilizar recursos com facilidade e manter uma organização, gerando uma separação das responsabilidades

Em seguida vamos criar novos projetos do tipo Class Library (no C#), que são repositórios de código podendo ser utilizados em outros projetos casso necessário, facilitando o reaproveitamento e no casso da camada de aplicação a cobertura de nosso core de negócio com testes unitários

Crie os projetos para que nossa arquitetura fique da seguinte forma:

projeto<br/>
| - 1-Presentation<br/>
| - | - Quiron.Api<br/>
| - 2-Domain<br/>
| - | - Quiron.Domain<br/>
| - 3-Application<br/>
| - | - Quiron.Service<br/>
| - 4-Infra<br/>
| - | - Quiron.Data.EF<br/>
| - 5-Test<br/>
| - | - Quiron.NUnitTest<br/>
| - Quiron.sln<br/>

<b>Observação:</b> O projeto Quiron.NUnitTest não é apenas um Class Library, o mesmo é um projeto de testes unitários criado para usar NUnit, caso use outra tecnologia lembre dessa premissa

# Objetivo da tarefa:

Criação de um projeto seguindo a arquitetura proposta entendendo cada parte da mesma para poder iniciar o desenvolvimento.<br/>
A API deve estar buildando e podendo ser executada, em seguida deve ser realizado um commit no branch criado e feito um merge no fast forced com a sua main, em seguida o branch pode ser apagado (Lembre de fazer o merge com apenas um commit no branch)