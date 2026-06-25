## JavaScript (ES6+) e HTML/CSS

A escolha do **JavaScript (ES6+)**, juntamente com **HTML5 e CSS3**, deve-se ao fato de serem as tecnologias nativas para o desenvolvimento de aplicações web e extensões de navegador. Como o PIE será executado diretamente em navegadores baseados em Chromium e Firefox, essas tecnologias garantem compatibilidade, desempenho e integração direta com os recursos disponibilizados pelos navegadores.

O **HTML5** é responsável pela estruturação dos elementos da interface, permitindo organizar componentes como o bloco de notas, calendário, barra de pesquisa e painel de atividades acadêmicas.

O **CSS3** é utilizado para a estilização da interface, possibilitando a criação de um design moderno, responsivo e minimalista, atendendo ao requisito de usabilidade (RNF03).

Já o **JavaScript ES6+** fornece os recursos necessários para implementar toda a lógica da extensão, incluindo:

* Manipulação dinâmica da interface;
* Gerenciamento de eventos do usuário;
* Comunicação com APIs externas;
* Armazenamento e recuperação de dados;
* Processamento da lógica dos comandos **!bangs**;
* Atualização automática dos componentes da página.

Além disso, os recursos modernos do ES6+, como *arrow functions*, *modules*, *async/await*, *destructuring* e *classes*, tornam o código mais organizado, legível e fácil de manter.

### Principais vantagens

* Compatibilidade nativa com navegadores Chromium e Firefox;
* Não exige instalação de runtimes adicionais;
* Excelente integração com APIs do navegador;
* Grande comunidade e documentação;
* Facilidade de manutenção e evolução do projeto.

---

## React

O **React** foi escolhido como framework para a construção da interface do PIE devido à sua arquitetura baseada em componentes reutilizáveis.

Como a página inicial da extensão será composta por diversos widgets independentes, como:

* Bloco de notas;
* Calendário;
* Barra de pesquisa;
* Lista de atividades do Google Sala de Aula.

O React permite que cada funcionalidade seja desenvolvida como um componente isolado, facilitando o desenvolvimento, os testes e futuras manutenções.

Além disso, o React utiliza o conceito de **Virtual DOM**, que reduz a quantidade de atualizações necessárias na interface, proporcionando maior desempenho e contribuindo para o atendimento do requisito de carregamento rápido (RNF02).

Outro benefício importante é o gerenciamento eficiente de estados, permitindo atualizar automaticamente informações na tela sem a necessidade de recarregar a página.

### Principais vantagens

* Desenvolvimento baseado em componentes reutilizáveis;
* Melhor organização e manutenção do código;
* Atualizações eficientes da interface através do Virtual DOM;
* Facilidade para gerenciar múltiplos widgets simultaneamente;
* Grande ecossistema e ampla adoção no mercado;
* Escalabilidade para futuras funcionalidades.

---

## Chrome/Browser Storage API

A **Browser Storage API** (Chrome Storage API e Firefox Storage API) foi escolhida como mecanismo de persistência de dados do PIE.

Por se tratar de uma extensão de navegador focada em produtividade pessoal, não há necessidade de manter um servidor ou banco de dados remoto para armazenar informações simples, como:

* Anotações do bloco de notas;
* Eventos do calendário;
* Preferências do usuário;
* Atalhos personalizados.

A utilização da Storage API permite armazenar esses dados diretamente no navegador do usuário, reduzindo custos de infraestrutura e aumentando a velocidade de acesso às informações.

Essa tecnologia também é fundamental para atender à regra de negócio **RN02**, que determina que as anotações sejam salvas automaticamente sempre que houver alterações, evitando perda de dados caso o navegador seja fechado inesperadamente.

Além disso, a API foi desenvolvida especificamente para extensões de navegador, oferecendo melhor integração e segurança em comparação ao uso de alternativas como LocalStorage.

### Principais vantagens

* Armazenamento local sem necessidade de servidor externo;
* Maior desempenho no acesso aos dados;
* Persistência das informações entre sessões;
* Integração nativa com extensões Chromium e Firefox;
* Menor custo de desenvolvimento e manutenção;
* Atendimento direto à regra RN02 de salvamento automático.

---

## Google Classroom API (OAuth)

A **Google Classroom API** foi escolhida para possibilitar a integração do PIE com o Google Sala de Aula, permitindo que o estudante visualize suas atividades diretamente na página inicial do navegador.

Por meio dessa API, a extensão poderá consultar:

* Atividades pendentes;
* Atividades abertas;
* Atividades concluídas;
* Informações das turmas vinculadas à conta do usuário.

O acesso às informações ocorre utilizando o protocolo **OAuth 2.0**, adotado pela Google como mecanismo oficial de autenticação e autorização.

Essa abordagem garante que o sistema tenha acesso apenas aos dados autorizados pelo usuário, atendendo à regra de negócio **RN01**, que exige consentimento prévio para leitura das informações acadêmicas.

### Principais vantagens

* Integração oficial com o Google Sala de Aula;
* Acesso seguro aos dados acadêmicos;
* Autenticação padronizada via OAuth 2.0;
* Garantia de privacidade e controle pelo usuário;
* Atualização automática das atividades;
* Atendimento à regra RN01 de autorização obrigatória.

