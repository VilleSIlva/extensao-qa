## 📦 **Requisitos Funcionais Detalhados para Testes Manuais**



### 🔐 **RF01 - Autenticação de Usuário**

  * O sistema deve permitir que o usuário realize login com nome de usuário e senha válidos.

  * O sistema deve exibir mensagens de erro em caso de login inválido.

---


### 🏠 **RF02 - Página Inicial**

  * O sistema deve exibir, após o login, a Página Inicial com o resumo da academia: indicadores de clientes, matrículas, risco de evasão, financeiro em aberto e ações recomendadas.

  * Os indicadores da Página Inicial devem ser coerentes com as demais telas e permitir acessar o detalhamento de cada informação.

---


### 📊 **RF03 - Dashboard**

  * O sistema deve exibir o Dashboard com os gráficos de clientes, matrículas, contas a receber, cancelamentos e avaliações, além dos indicadores da Inteligência Sifit.

---


### 👥 **RF04 - Gestão de Clientes**

  * O sistema deve permitir listar, buscar (por código e nome) e filtrar (por plano, personal, status e situação) os clientes cadastrados.

  * O sistema deve permitir cadastrar um novo cliente, validando os campos obrigatórios (Nome, Status, Sexo e Data de Nascimento).

  * O sistema deve permitir visualizar, alterar, inativar e excluir clientes, solicitando confirmação antes da exclusão.

---


### 💳 **RF05 - Gestão de Planos**

  * O sistema deve permitir listar, buscar (por código e nome) e filtrar (por status) os planos, exibindo a quantidade de alunos e a receita estimada.

  * O sistema deve permitir cadastrar planos com grupo, tipo de cobrança, parcelas e valores, validando os campos obrigatórios.

  * O sistema deve permitir visualizar, alterar, inativar e excluir planos, e somente planos ativos devem estar disponíveis para matrícula.

---


### 📝 **RF06 - Gestão de Matrículas**

  * O sistema deve permitir listar e buscar (por código e nome) as matrículas cadastradas.

  * O sistema deve permitir cadastrar uma matrícula vinculando cliente, plano e forma de pagamento, validando os campos obrigatórios e impedindo mais de uma matrícula ativa por cliente.

  * O sistema deve permitir visualizar, cancelar e excluir matrículas, solicitando confirmação antes do cancelamento e da exclusão.

---


### 💰 **RF07 - Contas a Receber**

  * O sistema deve permitir listar, buscar (por código e nome do cliente) e filtrar (por status, tipo de data e período) as contas a receber, exibindo indicadores financeiros do mês.

  * O sistema deve permitir cadastrar contas a receber, validando cliente e valor, e gerar automaticamente as contas referentes às parcelas das matrículas.

  * O sistema deve permitir visualizar, efetuar o recebimento (com tipo de pagamento e local de recebimento) e excluir contas a receber.

---


### 🚚 **RF08 - Gestão de Fornecedores**

  * O sistema deve permitir listar e buscar (por código e nome) os fornecedores cadastrados.

  * O sistema deve permitir cadastrar, visualizar, alterar e excluir fornecedores, validando o nome como campo obrigatório e solicitando confirmação antes da exclusão.

---


### ✅ **RF09 - Check-in e Presenças**

  * O sistema deve permitir registrar o check-in de clientes de forma manual (busca por nome, código, CPF ou telefone) e pela entrada rápida (código do cliente), liberando somente clientes com matrícula ativa.

  * O sistema deve exibir os check-ins do dia, os clientes presentes e os indicadores de frequência, e registrar os check-ins na tela de Presenças.

---


### 📏 **RF10 - Avaliações**

  * O sistema deve permitir listar, buscar (por código e nome) e filtrar (por status) as avaliações físicas.

  * O sistema deve permitir agendar avaliações (aluno, personal, data e hora), alterar a data e a hora, registrar a avaliação realizada com cálculo automático do IMC e excluir avaliações.

---


### 🏋️ **RF11 - Turmas e SifitBox**

  * O sistema deve permitir listar, buscar (por código e nome) e filtrar (por status) as turmas.

  * O sistema deve permitir cadastrar, alterar e excluir turmas, validando nome, plano, dias da semana e horário.

  * O sistema deve permitir consultar e gerar as aulas do SifitBox por período, informando o resultado ao usuário.

---


### 🏦 **RF12 - Caixas**

  * O sistema deve permitir listar e filtrar (por período e status) os caixas, exibindo a quantidade de caixas abertos, fechados e locais de caixa.

  * O sistema deve permitir abrir um caixa por local de contas e fechá-lo somente após a busca e a conferência das contas do período.

---


### 💸 **RF13 - Contas a Pagar e Despesas Fixas**

  * O sistema deve permitir listar, buscar (por código e fornecedor/colaborador) e filtrar (por tipo de data, período e status) as contas a pagar, exibindo os valores a pagar e restantes.

  * O sistema deve permitir cadastrar, visualizar, registrar o pagamento e excluir contas a pagar, validando os campos obrigatórios.

  * O sistema deve permitir cadastrar, alterar, inativar e excluir despesas fixas com valor e recorrência, aceitando somente valores positivos.

---


### 💪 **RF14 - Fichas de Treino e Exercícios**

  * O sistema deve permitir cadastrar fichas de treino para os alunos (aluno, personal, período e objetivo), montar os treinos com exercícios da biblioteca, visualizar e excluir fichas.

  * O sistema deve manter a biblioteca de exercícios organizada por grupo muscular, permitindo cadastrar, alterar e excluir exercícios sem duplicidade.

---


### 🎯 **RF15 - Prospecção**

  * O sistema deve permitir cadastrar, buscar (por nome, e-mail, telefone ou código), filtrar (por estágio), alterar e excluir leads, acompanhando sua evolução pelos estágios Novo Contato, Interessado, Fez Aula Experimental, Proposta e Fechado, sem permitir leads duplicados.

---


### 🧑‍💼 **RF16 - Colaboradores e Funções**

  * O sistema deve permitir cadastrar, buscar, alterar, inativar e excluir colaboradores, além de vincular funções a cada colaborador.

  * O sistema deve permitir cadastrar, filtrar, alterar e excluir funções (internas ou externas, personal e avaliador), sem duplicidade, e definir as permissões de acesso de cada função.

---


### 🛍️ **RF17 - Produtos**

  * O sistema deve permitir cadastrar, buscar, filtrar (por status e tipo), alterar, inativar e excluir produtos de venda (com preço positivo) e de troca por pontos (com pontuação), exibindo os valores no formato monetário brasileiro.

---


### 🩺 **RF18 - Fichas de Anamnese**

  * O sistema deve permitir aplicar anamneses aos alunos por meio de um assistente (seleção do aluno, escolha do modelo, resposta às perguntas e finalização), exibindo as fichas aplicadas na listagem com busca, filtro de status e indicadores.

---
