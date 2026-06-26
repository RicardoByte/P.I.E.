Com base no material fornecido, aqui estão os requisitos funcionais e não funcionais estruturados para o repositório do projeto P.I.E.:

# 📋 Documentação de Requisitos - P.I.E. (Página Inicial do Estudante)

O P.I.E. (Página Inicial do Estudante) consiste em uma extensão de navegador que substitui a página inicial por um conjunto de ferramentas e utilidades com foco no estudo e na organização de conteúdos acadêmicos. O sistema adota uma arquitetura em camadas para separar a interface gráfica, a lógica de negócio e os serviços externos.

## ⚙️ Requisitos Funcionais (RF)

*Descrevem as ações que o sistema deve ser capaz de executar e as funcionalidades disponíveis para o usuário.*

| ID | Funcionalidade | Descrição |
| --- | --- | --- |
| **RF01** | Substituição da Página Inicial | A extensão deve substituir a página inicial (homepage) do navegador por um conjunto de ferramentas focadas no usuário.

 |
| **RF02** | Atalhos Rápidos | O sistema deve exibir atalhos rápidos para o acesso a páginas de pesquisa e conteúdo acadêmico.

 |
| **RF03** | Bloco de Notas | O sistema deve disponibilizar um bloco de notas embutido para anotações, que pode ser aberto em qualquer página do navegador. As anotações do bloco de notas devem poder ser vistas como uma visão geral na página inicial.

 |
| **RF04** | Salvamento Automático | A camada de lógica de negócio deve salvar automaticamente as anotações locais do usuário, respeitando a regra RN02.

 |
| **RF05** | Calendário de Eventos | O sistema deve possuir um calendário para a adição e o acompanhamento de eventos e datas importantes. A camada de lógica deve gerenciar os eventos registrados neste calendário.

 |
| **RF06** | Autenticação Google | O sistema deve controlar a autenticação do usuário utilizando o OAuth da conta Google (regra RN01) para conceder o acesso aos dados do Google Sala de Aula.

 |
| **RF07** | Integração Google Classroom | O sistema deve exibir um widget na página inicial integrado ao Google Sala de Aula para listar as atividades abertas, pendentes e concluídas.

 |
| **RF08** | Pesquisa Interna | O sistema deve possuir uma barra de pesquisa capaz de encontrar notas, eventos, datas e matérias do próprio usuário.

 |
| **RF09** | Pesquisa Externa (Motores de Busca) | A barra de pesquisa deve permitir buscas externas no motor de pesquisa desejado (como Google, DuckDuckGO, Bing, Yandex, Wikipedia, etc.).

 |
| **RF10** | Suporte a Comandos !bangs | O sistema deve permitir a utilização de sintaxe de pesquisa avançada e !bangs (ex: !yt para pesquisar no YouTube ou !r para o Reddit) para realizar pesquisas diretas em sites específicos. A camada de lógica deve processar os comandos '!bangs' antes de executar a pesquisa padrão, conforme a regra RN03.

 |

---

## 🛠️ Requisitos Não Funcionais (RNF)

*Definem as restrições, padrões de arquitetura e os atributos de qualidade e segurança do sistema.*

| ID | Categoria | Descrição |
| --- | --- | --- |
| **RNF01** | Compatibilidade de Navegador | A extensão deve funcionar adequadamente em navegadores variantes de Chromium e Firefox.

 |
| **RNF02** | Tecnologias Front-end | A camada de apresentação (interface) da página inicial deve ser construída utilizando React, juntamente com as tecnologias HTML5 e CSS3.

 |
| **RNF03** | Tecnologias de Lógica | A camada de controle interno e lógica de negócio deve ser implementada utilizando a linguagem JavaScript (ES6+).

 |
| **RNF04** | Persistência de Dados Local | O armazenamento de dados (anotações, eventos do calendário, atalhos e preferências) deve ser realizado localmente, utilizando a Browser Storage API (Chrome Storage ou Firefox Storage). O projeto não deve utilizar um servidor próprio de banco de dados.

 |
| **RNF05** | Disponibilidade Offline de Dados | Os dados de armazenamento persistidos pela Browser Storage API devem permanecer disponíveis de forma local mesmo após o fechamento e reabertura do navegador.

 |
| **RNF06** | Privacidade e Segurança API | A comunicação e o acesso à Google Classroom API só podem ser efetuados após a devida autenticação, garantindo que o usuário só consiga acessar as suas próprias informações acadêmicas autorizadas.

 |
