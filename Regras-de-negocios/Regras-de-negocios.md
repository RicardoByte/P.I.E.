## Regras de Negócio (RN)

*Definem as políticas, condições, restrições obrigatórias e lógicas de validação que o sistema deve aplicar para que as funcionalidades operem corretamente e com segurança.*


| ID | Regra | Descrição | Origem/Referência |
| :--- | :--- | :--- | :--- |
| **RN01** | Restrição de Acesso Acadêmico | O acesso aos dados do Google Sala de Aula somente é permitido após a autenticação bem-sucedida via protocolo OAuth da conta Google do usuário. | Derivado do RF06 / RNF06 |
| **RN02** | Salvamento Automático Obrigatório | O sistema não deve possuir um botão manual de "Salvar" para o Bloco de Notas. A camada de lógica deve interceptar as mudanças e salvar automaticamente as anotações no armazenamento local. | Derivado do RF04 |
| **RN03** | Prioridade e Interceptação de !bangs | Antes de executar qualquer pesquisa, o sistema deve verificar a string digitada. Se iniciar com um comando '!bang' mapeado (ex: !yt), o sistema aborta a pesquisa padrão e executa o redirecionamento imediato para a URL do serviço correspondente. | Derivado do RF10 |
| **RN04** | Fallback de Pesquisa Padrão | Caso o termo inserido na barra de pesquisa não contenha um comando '!bang' ou seja uma pesquisa simples, o sistema deve direcionar a busca para o motor de pesquisa definido como padrão pelo usuário (ex: Google ou DuckDuckGo). | Derivado do RF09 |
| **RN05** | Privacidade e Isolamento de Dados | Sendo um sistema sem servidor próprio, é estritamente proibido o envio de dados locais (Anotações, Calendário e Atalhos) para APIs externas de terceiros. Toda a persistência deve ficar restrita à Browser Storage API. | Derivado do RNF04 |
| **RN06** | Classificação de Status de Atividades | As informações consumidas do Google Classroom API devem ser obrigatoriamente filtradas e exibidas na interface em três categorias distintas de status: Abertas, Pendentes e Concluídas. | Derivado do RF07 |
| **RN07** | Sincronismo do Bloco de Notas Global | Como o bloco de notas pode ser aberto em qualquer página do navegador, qualquer inserção de dados na extensão minimizada deve refletir em tempo real (ou no próximo carregamento) na visão geral da página inicial do P.I.E. | Derivado do RF03 |