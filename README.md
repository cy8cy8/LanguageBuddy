# LanguageBuddy

**Introdução**

Este projeto inicial detalhado descreve a criação de um site para adicionar e gerenciar flashcards utilizando TypeScript, Next.js e PostgreSQL. O objetivo principal é fornecer aos usuários uma ferramenta robusta e eficiente para aprimorar seus estudos através de flashcards interativos e personalizados.

**Tecnologias**

* **Front-end:**
    * TypeScript: Linguagem de programação que adiciona tipagem estática ao JavaScript, proporcionando maior confiabilidade e robustez ao código.
    * Next.js: Framework React para renderização do lado do servidor e outras funcionalidades avançadas.
* **Back-end:**
    * PostgreSQL: Banco de dados relacional robusto e escalável, ideal para armazenar os dados do sistema.

**Arquitetura do Sistema**

A arquitetura do sistema segue os princípios de separação de camadas e inversão de controle, promovendo modularidade, testabilidade e flexibilidade para futuras expansões.

* **Camada de Apresentação:** Responsável pela interface do usuário (UI) e pela interação com o usuário. Desenvolverá componentes reutilizáveis e interfaces intuitivas utilizando bibliotecas, como por exemplo React Bootstrap ou Material UI.
* **Camada de Negócio:** Implementará as regras de negócio do sistema, encapsulando a lógica de manipulação dos dados e validando as operações realizadas pelos usuários.
* **Camada de Dados:** Fornecerá acesso aos dados armazenados no banco de dados PostgreSQL, utilizando drivers como TypeORM ou Sequelize para mapear objetos às tabelas do banco de dados (isso ainda pode ser alterado no decorrer do projeto).

**Modelo de Dados**

O modelo de dados relacional do sistema é composto por entidades inter-relacionadas, definidas como:

* **Entidade Usuário:**
    * `id_usuario` (chave primária): Identificador único do usuário.
    * `nome`: Nome completo do usuário.
    * `email`: Endereço de email do usuário.
    * `senha`: Senha de acesso do usuário (armazenada com criptografia robusta).
* **Entidade Lista:**
    * `id_lista` (chave primária): Identificador único da lista.
    * `id_usuario` (chave estrangeira): Referência ao usuário que criou a lista.
    * `nome`: Nome da lista de flashcards.
    * `descricao`: Descrição opcional da lista.
* **Entidade Flashcard:**
    * `id_flashcard` (chave primária): Identificador único do flashcard.
    * `id_lista` (chave estrangeira): Referência à lista à qual o flashcard pertence.
    * `frente`: Conteúdo textual na frente do flashcard.
    * `verso`: Conteúdo textual no verso do flashcard.
    * `data_criacao`: Data e hora da criação do flashcard.
    * `data_ultima_revisao`: Data e hora da última revisão do flashcard.
    * `acertos`: Número de vezes que o flashcard foi respondido corretamente.
    * `erros`: Número de vezes que o flashcard foi respondido incorretamente.
* **Entidade Estatística:**
    * `id_estatistica` (chave primária): Identificador único da estatística.
    * `id_usuario` (chave estrangeira): Referência ao usuário da estatística.
    * `id_lista` (chave estrangeira): Referência à lista da estatística.
    * `data_estatistica`: Data e hora da geração da estatística.
    * `taxa_acerto`: Porcentagem de acertos nos flashcards da lista na data especificada.

**Arquivo de Protótipo:**

Um arquivo de protótipo foi criado para ilustrar a interface do usuário do sistema, incluindo telas para criação de contas, listas, flashcards e revisão de flashcards, que serão adicionadas ao projeto ao decorrer do desenvolvimento.

![Protótipo 01](images/protótipo01.png)

**Funcionalidades do Sistema**

O sistema oferecerá diversas funcionalidades para auxiliar os usuários em seus estudos:

* **Autenticação e Gerenciamento de Usuários:**
    * Cadastro de novos usuários com nome, email e senha.
    * Autenticação de usuários com email e senha.
    * Recuperação de senha em caso de esquecimento.
* **Gerenciamento de Listas:**
    * Criação, edição e exclusão de listas de flashcards.
    * Visualização de listas com seus flashcards associados.
    * Ordenação e filtragem de listas de acordo com critérios específicos.
* **Gerenciamento de Flashcards:**
    * Criação, edição e exclusão de flashcards em listas específicas.
    * Adição de imagens e outros recursos multimídia aos flashcards (opcional).
    * Formatação do texto

* **Próximos Passos:**

* Implementar o backend com PostgreSQL, criando as tabelas e as funcionalidades de CRUD (Criar, Ler, Atualizar e Deletar) para os dados.
* Implementar o frontend com Next.js, criando os componentes para as telas do site e conectando-os ao backend.
* Desenvolver o modo de revisão de flashcards, permitindo que os usuários pratiquem e melhorem seu aprendizado.
* Implementar o sistema de estatísticas, permitindo que os usuários acompanhem seu progresso.
* Testar o sistema para garantir que esteja funcionando corretamente e livre de bugs.

**Observações:**

* Este projeto inicial é um ponto de partida para o desenvolvimento do sistema de flashcards.
* As funcionalidades e o design do sistema podem ser modificados e aprimorados de acordo com as necessidades dos usuários.
* É importante seguir boas práticas de desenvolvimento de software para garantir a qualidade e a sustentabilidade do código.

**Recursos Adicionais:**

* [TypeScript](https://www.typescriptlang.org/)
* [Next.js](https://nextjs.org/)
* [PostgreSQL](https://www.postgresql.org/)
* [Documentação do PostgreSQL](https://www.postgresql.org/docs/current/)

**Contribuição:**

Este projeto está aberto à contribuição de outros desenvolvedores. Se você tiver interesse em contribuir, por favor, entre em contato.
