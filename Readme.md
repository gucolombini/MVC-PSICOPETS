https://drive.google.com/file/d/1kBmNRUgVe29VUy1KYJ4TgElrfUaXveAl/view?usp=sharing

- Nome do Projeto: PsicoPatas
- Descrição: Website com objetivo de receber respostas de formulários e exibir essas respostas para pesquisadores de forma efetiva.
- Arquitetura: MVC (Model-View-Controller)
- Ferramenta de Diagramação: draw.io

## Modelos
- Users: Encarregado de receber e entregar os dados sobre os usuários em relação ao login, gravando e lendo os dados encriptografados na base de dados (Registra cada usuário com um Id distinto).
- Forms 1, 2, 3: Encarregados de entregar as perguntas e receber as respostas dos formulários dos usuários e gravá-las na base de dados.
- Forms 1, 2, 3 Dados: Encarregados de ler as respostas e outros dados registradas na base de dados para usos de pesquisa.

## Controladores
- Users: Procura dados para login ou grava dados para cadastro.
- Formulários: Procura e lista as perguntas de acordo com o formulário escolhido, grava as respostas recebidas.
- Dashboard: Procura, lista, e faz cálculos com os dados já gravados.

## Views
- Página de Login: Exibe campo de email e senha. Os dados preenchidos são enviados para o controlador de Users, que entregam uma resposta caso o login tenha sucedido ou não.
- Página de Cadastro: Exibe campo de email, nome e senha, que são então enviados para o controlador de Users, que grava essas informações.
- Página de Formulário: Exibe as perguntas que o controlados dos Forms enviou, com campos de resposta condizentes e alguma respostas pré-definidas. Quando completado o formulário, as respostas são enviadas ao controlador dos Forms, que as grava na base de dados junto com uma identificação do usuário (diferente do Id de login!).
- Página do Pesquisador: Exibe uma dashboard com diversas maneiras de visualizar os dados, com diversos gráficos que permitem maior facilidade na compreensão dos dados obtidos.

## Infraestrutura
- Para gerenciar a base de dados, vamos fazer uso do PostgreSQL, pois é o mais utilizado no mercado, e é muito versátil.
- Para fazer deploy do website, vamos usar o Render, por ser confiável e fácil de usar.
- A framework do site está sendo desenvolvida com o Sails.js, pois permite o desenvolvimento por meio da arquitetura MVC.