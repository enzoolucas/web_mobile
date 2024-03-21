# Aula 3 - 20/03

- Padrões Arquiteturais: definem a Estrutura, Interações e Organização dos Componentes de Software, facilitando a comunicação entre devs e garantindo escalabilidade, manutenção e reutilização de código.

Padrões existentes: 1 Monolítico, 2 Microserviços, 3 Modelo-Visão-Controlador (MVC)
1 - Formada por módulos que mesmo agindo separadamente continuam ligados transoformando o conjunto em um único sistema.
Falicidade para criar soluções únicas, interligando todas as funcionalidades do sistema.
Problemas: escalabilidade, agregação de tecnologias, demora de aprendizado para novatos, aumento da complexidade de acordo com o tamanho, depende de componentes de código, falta de flexibilidade e dificuldade para colocar em produção

2 - Separação dos Elementos de Funcionalidades, colocados em serviços separados tornando-os autônomos e independentes  que se comunicam por meio de APIs.
Cada funcionalidade é separada em serviços bem definidos que podem ou não complementar outra funcionalidade.
Dificuldade: Necessidade Desenvolvedores qualificados.
    
    ![Untitled](Aula%203%20-%2020%2003%206a1cd8ffccd143b4a7fd3f779aefc1ee/Untitled.png)
    
    3 - MVC é um padrão de arquitetura de software que Separa a Representação da Informação da Interação do usuário com ele. Alterações feitas no layout não afetam a manipulção de dados, e estes poderão ser reorganizados sem alterar o layout. Provê a Separação das tarefas de acesso aos dados e lógica de negócio, lógica de apresentação e de interação com o utilizador, introduzindo um componente entre dois: o controlador
    Padrão arquitetural MVC:
       a. Modelo: Consiste nos dados da aplicação, regras de negócios, lógica e funções
       b. Visão: Qualquer saída de representação dos dados como uma tabela ou diagrama, é    possível ter várias visões do mesmo dado
       c. Controlador: Faz a mediação da entrada convertendo-a em comandos para modelo ou  visão, as ideias centrais são a reusabilidade e separação de conceitos.
    
    ![Untitled](Aula%203%20-%2020%2003%206a1cd8ffccd143b4a7fd3f779aefc1ee/Untitled%201.png)
    
    Model View Template (MTV)
    Model: representa a camda de acesso aos dados pelo acesso ao banco
    Template: camada de apresentação da informação que lida com a interface
    View: camada usada pra implementar a lógica de negócios e interagir com um modelo para transportar dados e renderizar um template.
    
    ![Untitled](Aula%203%20-%2020%2003%206a1cd8ffccd143b4a7fd3f779aefc1ee/Untitled%202.png)
    
- Mapeamento Objeto Relacional - ORM
Técnica de desenvolvimento utilizada para reduzir a demanda de trabalho em programa orientada a objetos ao se utilizar bancos de dados relacionais.
As tabelas do banco de dados são representadas através de classes e os registros de cada tabela são representados como instancias das classes correspondentes.
O programador não precisa se preocupar com os comandos SQL, ele usa a interface de programação simples que faz todo o trabalho de persistência.
Não é necessária uma correspondência entra as tabelas de dados e as classes do programa.
A relação entre as tabelas onde originam os dados e o objeto que disponibiliza é configurada pelo programador, isolando o código do programa das alterações à organização dos dados nas tabelas do banco de dados.
A forma como este mapeamento é configurado depende da ferramenta utilizada, exemplo: programador que use Hibernate na linguagem Java pode usar XML ou sistema de anotações que a linguagem providencia. Em outros casos o mapeamento é feito diretamente no código através da herança de classes especiais como é o caso do ORM do Django e do SqlAlchemy na linguagem python.
Algumas ferramentas gráficas podem ser usadas pra gerar o código que representa o modelo do banco, como o ORM Pony também na linguagem python.