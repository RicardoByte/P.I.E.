### Planejamento de Sprints

| Sprint | Duração | Requisitos Funcionais | Tarefas | Prioridade |
| :--- | :--- | :--- | :--- | :--- |
| *Sprint 1* | 1 semana | Estruturação Base e RF01 – Gerenciar Bloco de Notas. | Configurar o projeto da extensão utilizando JavaScript (ES6+), HTML/CSS e React para a interface; desenvolver a interface do bloco de notas para ser aberto em qualquer aba e visível na página inicial; implementar o salvamento automático de alterações via Chrome/Browser Storage API (RN02), garantindo persistência local sem servidor externo. | Essencial |
| *Sprint 2* | 1 semana | RF03 – Motor de Busca com !Bangs. | Desenvolver a barra de pesquisa unificada com suporte a motores web variados e pesquisa interna; implementar a lógica de processamento de comandos de atalho (!bangs, como !yt ou !r), garantindo que o comando seja interceptado antes do motor padrão para direcionar o usuário ao site correspondente (RN03). | Essencial |
| *Sprint 3* | 1 semana | RF04 – Acompanhamento de Calendário. | Construir o componente de calendário interativo para a página inicial; desenvolver e testar as funções que permitem ao usuário adicionar, editar, excluir e acompanhar eventos e datas acadêmicas importantes. | Importante |
| *Sprint 4* | 1 semana | RF02 – Integração Google Sala de Aula. | Implementar o fluxo de autenticação OAuth para obter permissão de leitura da conta Google do usuário (RN01); consumir a Google Classroom API para buscar e listar na interface as atividades abertas, pendentes e concluídas do estudante. | Importante |
