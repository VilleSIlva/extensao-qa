# Relatório de Bugs

**Software:** Sifit

**QA responsável:**  Ville Nunes Figueiredo da Silva

**Data:** 13.10.26

---

### 🐞 **Bug 01: Mensagem de erro incorreta ao tentar realizar login com campos vazios**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-001 | Ao clicar no botão "Entrar" na página de login com os campos de nome de usuário e senha vazios, o sistema exibe a mensagem "O nome de usuário e senha não correspondem", a mesma apresentada quando são informadas credenciais inválidas, em vez de indicar que os campos obrigatórios devem ser preenchidos. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a página de login do SIFIT. |
| 2. Manter os campos de nome de usuário e senha vazios. |
| 3. Clicar no botão "Entrar". |
| 4. Verificar a mensagem de erro exibida pelo sistema. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar que os campos de nome de usuário e senha são obrigatórios, orientando o usuário a preenchê-los. | O sistema exibe a mensagem "O nome de usuário e senha não correspondem", utilizada também para tentativas de login com credenciais inválidas. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Windows 11. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Login / Autenticação de usuário | C01-CT03: Tentativa de acesso com campos obrigatórios vazios |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/3ebcc976-9012-471d-a577-6177221fd267)

---

### 🐞 **Bug 02: Quantidade de alunos em risco diverge entre as telas**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-002 | A quantidade de alunos em risco de evasão é diferente em cada local: o card da Página Inicial e o "Radar de Evasão" exibem 3 alunos, o bloco "Inteligência de Retenção" exibe 4 alunos em médio risco e o Dashboard exibe 0 "Alunos em risco". Além disso, o Radar informa último treino "Há 15 dias" para alunos que nunca registraram visita. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a Página Inicial do SIFIT. |
| 2. Observar o card "alunos em risco de evasão" e o bloco "Inteligência de Retenção". |
| 3. Clicar em "Ver detalhes" do card de risco e observar o "Radar de Evasão". |
| 4. Acessar o menu "Dashboard" e observar o indicador "Alunos em risco". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| A quantidade de alunos em risco deve ser a mesma em todas as telas. | As telas exibem 3, 4 e 0 alunos em risco. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Página Inicial / Dashboard / Inteligência | C02-CT02: Radar de evasão / C03-CT03: Indicador de alunos em risco do Dashboard |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo C02-CT02](https://jam.dev/c/5d2ad698-91fa-4d9f-a9f0-64f26dc274dc) · [Vídeo C03-CT03](https://jam.dev/c/a0888ff3-82b8-458c-afb0-b9aecdd5df18) |

---

### 🐞 **Bug 03: Quantidade de clientes ausentes diverge entre a Página Inicial e a tela de Clientes**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-003 | A Página Inicial exibe 4 clientes ausentes (Rafael Santos, Jerome Lionel, Steven Kaiki e Lila, todos sem visitas registradas), enquanto o indicador "Ausentes" da tela de Clientes exibe 0. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a Página Inicial do SIFIT. |
| 2. Observar o card "Clientes Ausentes". |
| 3. Acessar a tela de Clientes. |
| 4. Observar o indicador "Ausentes". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| As duas telas devem exibir a mesma quantidade de clientes ausentes. | A Página Inicial exibe 4 e a tela de Clientes exibe 0. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Página Inicial / Clientes | C02-CT03: Clientes ausentes |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/7cde0ad8-fe3a-4a3b-9a14-0805dca3875b) |

---

### 🐞 **Bug 04: Lista de desistências vazia, embora o total informe 3 desistências**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-004 | Ao clicar no card "Desistências no Período", que exibe 3, a janela exibe a mensagem "Nenhuma desistência encontrada no período." e, logo abaixo, "Total de desistências: 3". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a Página Inicial do SIFIT. |
| 2. Observar o card "Desistências no Período". |
| 3. Clicar no card. |
| 4. Verificar a lista e o total exibidos. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| A janela deve listar as 3 desistências do período. | A janela informa que não há desistências, mas exibe o total de 3. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Página Inicial / Desistências | C02-CT05: Desistências no período |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/9b8a90d6-7d67-426f-8c6b-48eb4b8e1296) |

---

### 🐞 **Bug 05: Título e navegação do Dashboard exibem "Despesas Fixas"**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-005 | Ao acessar o menu "Dashboard", a tela exibe o título "Despesas Fixas" e a navegação "Início > Despesas Fixas", embora o conteúdo seja o Dashboard e o menu "Dashboard" esteja selecionado. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar o SIFIT autenticado. |
| 2. Clicar no menu "Dashboard". |
| 3. Verificar o título e a navegação no topo da tela. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O título e a navegação devem exibir "Dashboard". | O título e a navegação exibem "Despesas Fixas". |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Dashboard | C03-CT01: Acesso ao Dashboard |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/fbc8ddfc-e244-413c-995b-c8bee8733105) |

---

### 🐞 **Bug 06: Títulos das seções e dos gráficos do Dashboard ilegíveis**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-006 | No modo claro, os títulos das seções ("Clientes", "Matrículas", "Contas a Receber", "Cancelamentos" e "Avaliações") são exibidos em branco sobre fundo claro, e os títulos dos gráficos (ex.: "FREQUÊNCIA", "POR MÊS") são exibidos em cinza-escuro (rgb 31, 41, 55) sobre o fundo azul-marinho dos cartões (rgb 23, 43, 77), ficando praticamente invisíveis. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar o SIFIT autenticado no modo claro. |
| 2. Clicar no menu "Dashboard". |
| 3. Observar os títulos das seções e dos gráficos. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| Os títulos devem estar legíveis, com contraste adequado em relação ao fundo. | Os títulos ficam praticamente invisíveis. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Dashboard / Gráficos | C03-CT02: Legibilidade dos gráficos do Dashboard |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/72ff4074-832d-451e-908c-674402829bf3) |

---

### 🐞 **Bug 07: Erro ao cadastrar cliente com dados válidos**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-007 | Ao preencher todos os campos obrigatórios (e também os opcionais) com dados válidos e clicar em "Cadastrar Cliente", o sistema exibe a mensagem "Erro ao criar cliente." e o cliente não é cadastrado. A API retorna erro 500 com a mensagem "Erro interno inesperado.". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Crítica | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de clientes do SIFIT. |
| 2. Clicar no botão "Novo Cliente". |
| 3. Preencher Nome ("Teste Ville Nunes"), Status ("Ativo"), Sexo e Data de Nascimento válidos. |
| 4. Clicar no botão "Cadastrar Cliente". |
| 5. Verificar a mensagem exibida pelo sistema. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve cadastrar o cliente, exibir mensagem de sucesso e apresentá-lo na listagem. | O sistema exibe o modal "Erro - Erro ao criar cliente." e o cliente não é cadastrado. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Clientes / Cadastro de cliente | C04-CT08: Cadastro de cliente com dados válidos |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/e21003f6-a3e5-4f6f-9ea2-755f25b7ff91) |

---

### 🐞 **Bug 08: Busca por código não retorna clientes sem matrícula**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-008 | Ao pesquisar pelo código de um cliente que não possui matrícula (ex.: 406 e 408), a listagem retorna vazia, embora o cliente exista e apareça na listagem padrão. Para clientes com matrícula (ex.: 398), a busca funciona. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de clientes do SIFIT. |
| 2. Informar o código "408" no campo "Código". |
| 3. Clicar no botão "Buscar". |
| 4. Verificar a listagem exibida. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve exibir o cliente que possui o código informado. | A tela de clientes fica totalmente em branco após clicar em "Buscar", embora o cliente 408 esteja cadastrado e ativo. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Clientes / Busca por código | C04-CT04: Busca de cliente pelo código |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/e36fb928-6b21-4210-b361-cc99a1358cf9) |

---

### 🐞 **Bug 09: Paginação exibe páginas vazias com filtro aplicado**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-009 | Com o filtro "Status" em "Ativo" (padrão da tela), a listagem apresenta 5 clientes, porém a paginação exibe 3 páginas. Ao clicar nas páginas "2" e "3", a tabela é exibida vazia. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de clientes do SIFIT. |
| 2. Manter o filtro "Status" em "Ativo". |
| 3. Observar a quantidade de páginas exibida na paginação. |
| 4. Clicar nas páginas "2" e "3". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| A paginação deve exibir somente a quantidade de páginas correspondente aos registros filtrados. | A paginação exibe 3 páginas e as páginas 2 e 3 são apresentadas vazias. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Clientes / Paginação | C04-CT05: Paginação da listagem filtrada |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/a38cb135-f8d3-43d6-8385-f821247140da) |

---

### 🐞 **Bug 10: Listagem não respeita a quantidade de registros por página**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-010 | Com a opção "50" registros por página selecionada e o filtro "Status" em "Todos", a primeira página exibe todos os 126 clientes cadastrados, enquanto a página 2 exibe 50 clientes. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de clientes do SIFIT. |
| 2. Selecionar "Todos" no filtro "Status". |
| 3. Clicar no botão "Buscar". |
| 4. Contar a quantidade de clientes exibidos na primeira página. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| A primeira página deve exibir no máximo 50 clientes. | A primeira página exibe todos os clientes cadastrados (125 no momento da gravação). |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Clientes / Paginação | C04-CT06: Quantidade de registros por página |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/7e9313e8-1a42-4e1f-99be-f22711d0d555) |

---

### 🐞 **Bug 11: Ausência de mensagem quando a busca não encontra clientes**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-011 | Ao pesquisar um nome que não está cadastrado, o sistema exibe apenas a tabela vazia, sem nenhuma mensagem informando que nenhum cliente foi encontrado. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de clientes do SIFIT. |
| 2. Informar um nome inexistente no campo "Nome". |
| 3. Clicar no botão "Buscar". |
| 4. Verificar a listagem exibida. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve exibir uma mensagem como "Nenhum cliente encontrado". | O sistema exibe somente o cabeçalho da tabela, sem registros e sem mensagem. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Clientes / Busca por nome | C04-CT03: Busca de cliente com nome inexistente |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/1400615a-e41d-4ab8-95d5-5a68bd56510d) |

---

### 🐞 **Bug 12: Erro ao salvar alterações dos dados do cliente**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-012 | Ao alterar os dados de um cliente existente (ex.: nome ou status) e clicar em "Salvar Alterações", o sistema exibe a mensagem "Erro ao criar cliente." e as alterações não são salvas. A API de atualização retorna erro 500 com a mensagem "Erro interno inesperado.". Além disso, a mensagem exibida menciona "criar" em uma operação de alteração. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Crítica | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de clientes do SIFIT. |
| 2. Clicar no botão "Visualizar" de um cliente (ex.: código 405). |
| 3. Clicar no botão "Alterar dados". |
| 4. Alterar o nome para "Teste Ville Nunes" ou o status para "Inativo". |
| 5. Clicar no botão "Salvar Alterações". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve salvar as alterações, exibir mensagem de sucesso e apresentar os dados atualizados na listagem. | O sistema exibe o modal "Erro - Erro ao criar cliente." e o cliente permanece com os dados anteriores. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Clientes / Alteração e inativação de cliente | C04-CT10: Alteração dos dados do cliente |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/ef0c7a28-0a2f-4bb6-9c78-3fc0995ec51f) |

---

### 🐞 **Bug 13: Erro no servidor ao acessar cliente excluído**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-013 | Ao acessar pela URL a tela de visualização ou alteração de um cliente que foi excluído (ex.: /visualizar-cliente/407), o sistema exibe o modal "Erro no servidor - Erro interno inesperado." e, na tela de alteração, carrega o formulário vazio com o botão "Cadastrar Cliente". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar o SIFIT autenticado. |
| 2. Acessar a URL /visualizar-cliente/407 (cliente excluído). |
| 3. Verificar a mensagem exibida pelo sistema. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar que o cliente não foi encontrado e redirecionar para a listagem de clientes. | O sistema exibe "Erro no servidor - Erro interno inesperado." (erro 500). |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Clientes / Visualização de cliente | C04-CT09: Visualização dos dados do cliente |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/132ddc8a-ed22-488c-9527-d95562c4b9d8) |

---

### 🐞 **Bug 14: Coluna "Alunos", ranking e receita estimada dos planos exibem valores zerados**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-014 | Na tela de planos, a coluna "Alunos" exibe 0 para todos os planos e o indicador "Receita Estimada" exibe R$ 0,00, embora o indicador "Alunos em Planos" mostre 2 e o ranking mostre o plano "Treino Livre" com 1 aluno. No ranking, a mensalidade do "Treino Livre" é exibida como R$ 0,00, embora o plano custe R$ 52,00. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de planos do SIFIT. |
| 2. Observar o indicador "Alunos em Planos" e o ranking "Planos com mais alunos". |
| 3. Observar a coluna "Alunos" do plano "Treino Livre" na listagem. |
| 4. Observar o indicador "Receita Estimada". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| A coluna "Alunos", o ranking e a receita estimada devem refletir as matrículas ativas (ex.: Treino Livre com 1 aluno e mensalidade R$ 52,00). | A coluna "Alunos" exibe 0, a receita estimada exibe R$ 0,00 e a mensalidade no ranking exibe R$ 0,00. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Planos / Listagem e indicadores | C05-CT02: Exibição da quantidade de alunos e da receita dos planos |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/a5ed20f9-d1e4-4e37-90ce-9941e6799792) |

---

### 🐞 **Bug 15: Busca por código retorna planos cujo código apenas contém o valor informado**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-015 | Ao pesquisar o código "1", a listagem retorna os planos #1, #11, #16, #41 e #51, ou seja, todos os planos cujo código contém o dígito "1", em vez de somente o plano #1. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de planos do SIFIT. |
| 2. Informar "1" no campo "Código". |
| 3. Clicar no botão "Buscar". |
| 4. Verificar os planos exibidos. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve exibir somente o plano de código #1. | O sistema exibe os planos #1, #11, #16, #41 e #51. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Planos / Busca por código | C05-CT04: Busca de plano pelo código |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/ec3ca053-5d62-438d-aa52-034d12e49b9a) |

---

### 🐞 **Bug 16: Erro interno com exposição de SQL ao salvar plano sem grupo**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-016 | Ao salvar um plano informando apenas o nome, o sistema exibe a mensagem genérica "Erro ao salvar plano". A API retorna erro 500 com a mensagem do banco de dados "SQLSTATE[23000]: Integrity constraint violation: 1048 Column 'grupo_id' cannot be null", o que indica ausência de validação do campo "Grupo" e expõe detalhes internos do banco de dados. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de planos do SIFIT. |
| 2. Clicar no botão "Novo Plano". |
| 3. Informar apenas o nome "Plano Teste Ville". |
| 4. Clicar no botão "Salvar Plano". |
| 5. Verificar a mensagem exibida e a resposta da API no DevTools (aba Network). |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar que o campo "Grupo" é obrigatório, sem erro interno e sem expor detalhes do banco de dados. | O sistema exibe "Erro ao salvar plano" e a API retorna erro 500 com a instrução SQL que falhou. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Planos / Cadastro de plano | C05-CT05: Cadastro de plano sem grupo |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/fa85a065-f8b6-45aa-989b-d65a05e2eb66) |

---

### 🐞 **Bug 17: Sistema permite cadastrar plano com quantidade de parcelas negativa**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-017 | O campo "Parcelas" aceita valores negativos e o plano é salvo normalmente com "-3" parcelas. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de planos do SIFIT. |
| 2. Clicar no botão "Novo Plano". |
| 3. Informar o nome "Plano Teste Ville Negativo" e um grupo. |
| 4. Informar "-3" no campo "Parcelas". |
| 5. Clicar no botão "Salvar Plano". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve impedir o cadastro e informar que a quantidade de parcelas deve ser maior que zero. | O plano é cadastrado com "-3" parcelas. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Planos / Cadastro de plano | C05-CT06: Cadastro de plano com quantidade de parcelas negativa |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/1a785e1d-5f84-4b11-9c13-50be1961a7f4) |

---

### 🐞 **Bug 18: Inativação do plano não é salva**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-018 | Ao alterar o status de um plano para "Inativo" e clicar em "Salvar Plano", o sistema envia o status "inativo" e a API responde com sucesso, porém o plano permanece "ATIVO" na listagem e ao ser reaberto. As demais alterações (nome e valor) são salvas normalmente. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de planos do SIFIT. |
| 2. Clicar no botão "Visualizar" de um plano ativo (ex.: "Plano Teste Ville Editado"). |
| 3. Selecionar "Inativo" no campo "Status". |
| 4. Clicar no botão "Salvar Plano". |
| 5. Verificar o status do plano na listagem. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O plano deve constar com status "INATIVO". | O plano permanece com status "ATIVO". |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Planos / Alteração de plano | C05-CT09: Inativação do plano |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/9f76f60c-600d-4c55-b9ae-8eb8069889e9) |

---

### 🐞 **Bug 19: Planos inativos são exibidos no cadastro de matrícula**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-019 | No campo "Modalidade" da tela "Cadastrar Matrícula", são exibidos planos com status "INATIVO" (ex.: "AVA" e "Teste Final"), permitindo matricular clientes em planos que não estão mais em vigor. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de planos do SIFIT e identificar planos inativos (ex.: "AVA"). |
| 2. Acessar a tela "Cadastrar Matrícula". |
| 3. Abrir o campo "Modalidade". |
| 4. Verificar se os planos inativos são exibidos. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| Somente planos ativos devem ser exibidos no campo "Modalidade". | Os planos inativos "AVA" e "Teste Final" são exibidos como opção. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Planos / Matrículas | C05-CT10: Plano inativo indisponível para matrícula |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/96013002-d0e4-4057-8dc1-383ef6437707) |

---

### 🐞 **Bug 20: Desconto não é aplicado ao valor total da matrícula**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-020 | Ao informar um desconto no cadastro da matrícula, o campo "Valor Total" não é recalculado. Na tela "Visualizar Matrícula", o campo "Desconto" exibe o valor da parcela (R$ 52,00) em vez do desconto informado, inclusive quando o desconto é 0. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de matrículas do SIFIT. |
| 2. Clicar em "Cadastrar Matrícula". |
| 3. Selecionar o cliente e a modalidade "Treino Livre" (R$ 52,00). |
| 4. Informar "10" no campo "Desconto" e verificar o "Valor Total". |
| 5. Salvar a matrícula e clicar em "Visualizar" na listagem. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O valor total deve ser R$ 42,00 e a visualização deve exibir desconto de R$ 10,00. | O valor total permanece R$ 52,00 e a visualização exibe "Desconto 52,00". |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Matrículas / Cadastro e visualização | C06-CT08: Cadastro de matrícula com desconto / C06-CT10: Visualização dos dados da matrícula |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 21: Mensagem incorreta ao cadastrar matrícula para cliente com matrícula ativa**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-021 | Ao tentar cadastrar uma matrícula para um cliente que já possui matrícula ativa, o sistema impede o cadastro, porém exibe a mensagem genérica "Erro ao Cadastrar com Assinatura". O motivo real ("Já existe matrícula ativa") é retornado pela API, mas não é exibido ao usuário. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela "Cadastrar Matrícula" do SIFIT. |
| 2. Selecionar um cliente que já possui matrícula ativa (ex.: Steven Kaiki). |
| 3. Preencher modalidade, tipo de pagamento e dia de vencimento. |
| 4. Clicar no botão "Salvar". |
| 5. Verificar a mensagem exibida pelo sistema. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar que o cliente já possui matrícula ativa. | O sistema exibe a mensagem "Erro ao Cadastrar com Assinatura". |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Matrículas / Cadastro de matrícula | C06-CT09: Cadastro de matrícula para cliente com matrícula ativa |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 22: Paginação não permite acessar matrículas além da primeira página**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-022 | Com a opção "50" registros por página, a listagem exibe 50 matrículas e apenas a página "1", com o botão "Próxima" desabilitado. Ao alterar para "100" registros por página, são exibidas 84 matrículas, ou seja, 34 matrículas ficam inacessíveis com a configuração padrão. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de matrículas do SIFIT. |
| 2. Manter a opção "50" registros por página. |
| 3. Verificar a paginação e o botão "Próxima". |
| 4. Alterar para "100" registros por página e contar as matrículas exibidas. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| A paginação deve exibir 2 páginas e permitir acessar as 84 matrículas. | A paginação exibe somente a página 1 e o botão "Próxima" fica desabilitado. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Matrículas / Paginação | C06-CT04: Paginação da listagem de matrículas |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 23: Erro no servidor ao excluir matrícula, embora a exclusão seja efetivada**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-023 | Ao confirmar a exclusão de uma matrícula, o sistema exibe o modal "Erro no servidor - Erro interno inesperado." (API retorna erro 500), porém a matrícula é removida da listagem. O usuário é informado de uma falha em uma operação que foi realizada. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de matrículas do SIFIT. |
| 2. Clicar no botão "Deletar" (lixeira) de uma matrícula. |
| 3. Confirmar a mensagem "Deseja deletar essa matrícula?". |
| 4. Verificar a mensagem exibida e a listagem. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve excluir a matrícula e exibir mensagem de sucesso. | O sistema exibe "Erro no servidor - Erro interno inesperado.", mas a matrícula é excluída. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Matrículas / Exclusão de matrícula | C06-CT12: Exclusão de matrícula |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 24: Mensagem de validação permanece após selecionar o tipo de pagamento**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-024 | Após tentar salvar a matrícula sem tipo de pagamento, a mensagem "Selecione o Tipo de Pagamento" é exibida abaixo do campo e permanece na tela mesmo depois que o tipo de pagamento é selecionado e a matrícula é salva. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela "Cadastrar Matrícula" do SIFIT. |
| 2. Selecionar cliente e modalidade, sem tipo de pagamento. |
| 3. Clicar no botão "Salvar". |
| 4. Selecionar o tipo de pagamento "Pix". |
| 5. Verificar a mensagem abaixo do campo "Tipo Pagamento". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| A mensagem de validação deve desaparecer quando o campo for preenchido. | A mensagem "Selecione o Tipo de Pagamento" permanece exibida. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Matrículas / Cadastro de matrícula | C06-CT06: Cadastro de matrícula sem tipo de pagamento |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 25: Ausência de mensagem quando a busca não encontra matrículas**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-025 | Ao pesquisar um nome que não possui matrícula, o sistema exibe apenas a tabela vazia, sem nenhuma mensagem informando que nenhuma matrícula foi encontrada. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de matrículas do SIFIT. |
| 2. Informar um nome inexistente no campo "Nome". |
| 3. Clicar no botão "Buscar". |
| 4. Verificar a listagem exibida. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve exibir uma mensagem como "Nenhuma matrícula encontrada". | O sistema exibe somente o cabeçalho da tabela, sem registros e sem mensagem. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Matrículas / Busca por nome | C06-CT03: Busca de matrícula com nome inexistente |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 26: Matrícula cadastrada não gera conta a receber**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-026 | Após cadastrar matrículas no plano "Treino Livre" (R$ 52,00) para os clientes Jerome Lionel (matrícula 240, com 1 parcela confirmada em "Escolher") e Steven Kaiki (matrícula 239), nenhuma conta a receber de R$ 52,00 foi gerada, mesmo pesquisando o período de 2020 a 2030 por vencimento e por recebimento. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Cadastrar uma matrícula no plano "Treino Livre" para um cliente sem matrícula ativa. |
| 2. Confirmar a quantidade de parcelas na janela "Quantidade Parcelas" (botão "Escolher"). |
| 3. Acessar a tela de contas a receber. |
| 4. Pesquisar o nome do cliente com período de 01/01/2020 a 31/12/2030. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| Deve existir uma conta a receber de R$ 52,00 referente à parcela da matrícula. | Nenhuma conta a receber referente à matrícula é exibida. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Contas a Receber / Matrículas | C07-CT12: Geração de conta a receber a partir da matrícula |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 27: Indicador "Contas Atrasadas" diverge do filtro de contas vencidas**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-027 | O indicador "Contas Atrasadas" exibe 2, porém ao filtrar a listagem pelo status "Vencido" nenhuma conta é exibida. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de contas a receber do SIFIT. |
| 2. Observar o indicador "Contas Atrasadas". |
| 3. Selecionar "Vencido" no filtro "Status". |
| 4. Clicar no botão "Buscar". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| A listagem deve exibir as 2 contas atrasadas indicadas no indicador. | A listagem não exibe nenhuma conta. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Contas a Receber / Indicadores e filtros | C07-CT05: Consistência do indicador de contas atrasadas |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 28: Recebimento é registrado sem tipo de pagamento**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-028 | Ao efetuar o recebimento de uma conta sem selecionar o tipo de pagamento, o sistema registra o recebimento normalmente. Na visualização da conta, o campo "Tipo de Pagamento" fica vazio, o que prejudica o controle financeiro e o fechamento de caixa. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de contas a receber do SIFIT. |
| 2. Clicar em "Visualizar" de uma conta pendente. |
| 3. Clicar em "Efetuar Recebimento". |
| 4. Não selecionar o tipo de pagamento e clicar em "Salvar". |
| 5. Confirmar a mensagem "O caixa aberto não é de hoje, deseja continuar?". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve exigir a seleção do tipo de pagamento antes de registrar o recebimento. | O recebimento é registrado com o tipo de pagamento vazio. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Contas a Receber / Recebimento | C07-CT09: Recebimento de conta sem tipo de pagamento |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 29: Recebimento aceita valor maior que o valor a receber sem alerta**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-029 | Ao efetuar o recebimento de uma conta de R$ 75,50 informando o valor recebido de R$ 100,00, o sistema registra o recebimento sem nenhum alerta sobre a diferença de valores. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de contas a receber do SIFIT. |
| 2. Clicar em "Visualizar" de uma conta pendente de R$ 75,50. |
| 3. Clicar em "Efetuar Recebimento". |
| 4. Informar o valor recebido de R$ 100,00, o tipo de pagamento e o local de recebimento. |
| 5. Clicar em "Salvar" e confirmar a mensagem do caixa. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve alertar sobre a divergência ou impedir o recebimento acima do valor da conta. | O recebimento é registrado com R$ 100,00 sem nenhum alerta. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Contas a Receber / Recebimento | C07-CT10: Recebimento com valor maior que o valor a receber |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 30: Ausência de mensagem quando a busca não encontra contas a receber**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-030 | Ao pesquisar um nome de cliente inexistente, o sistema exibe apenas a tabela vazia, sem nenhuma mensagem informando que nenhuma conta foi encontrada. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de contas a receber do SIFIT. |
| 2. Informar um nome inexistente no campo "Nome do cliente". |
| 3. Clicar no botão "Buscar". |
| 4. Verificar a listagem exibida. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve exibir uma mensagem como "Nenhuma conta encontrada". | O sistema exibe somente o cabeçalho da tabela, sem registros e sem mensagem. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Contas a Receber / Busca | C07-CT03: Busca de conta com nome inexistente |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 31: Busca por código inexistente ou parcial retorna todos os fornecedores**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-031 | Ao pesquisar um código que não existe (ex.: "999") ou parte de um código (ex.: "29"), a listagem exibe todos os 8 fornecedores cadastrados, como se nenhum filtro tivesse sido aplicado. A busca funciona somente com o código exato (ex.: "394"). |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de fornecedores do SIFIT. |
| 2. Informar "999" no campo "Código". |
| 3. Clicar no botão "Buscar". |
| 4. Verificar os fornecedores exibidos. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| A listagem não deve exibir fornecedores e o sistema deve informar que nenhum fornecedor foi encontrado. | A listagem exibe todos os 8 fornecedores cadastrados. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Fornecedores / Busca por código | C08-CT04: Busca de fornecedor com código inexistente |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 32: Erro ao cadastrar fornecedor com dados válidos**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-032 | Ao salvar um novo fornecedor, o sistema exibe a mensagem "Erro ao salvar fornecedor." e o fornecedor não é cadastrado. A API retorna erro 500 ("Erro interno inesperado.") tanto com todos os campos preenchidos quanto informando apenas o nome. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de fornecedores do SIFIT. |
| 2. Clicar no botão "Novo Fornecedor". |
| 3. Informar o nome "Fornecedor Teste Ville" e os demais dados válidos. |
| 4. Clicar no botão "Salvar". |
| 5. Verificar a mensagem exibida. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve cadastrar o fornecedor e exibir mensagem de sucesso. | O sistema exibe "Erro ao salvar fornecedor." e o fornecedor não é cadastrado. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Fornecedores / Cadastro | C08-CT06: Cadastro de fornecedor com dados válidos |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 33: Erro interno com exposição de SQL ao alterar fornecedor**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-033 | Ao alterar qualquer dado de um fornecedor existente (nome ou status) e clicar em "Salvar", o sistema exibe "Erro no servidor - Ocorreu um erro interno no servidor." e a alteração não é salva. A API retorna erro 500 com a mensagem do banco de dados "SQLSTATE[23000]: Integrity constraint violation: 1048 Column 'tipo_pessoa' cannot be null". O problema ocorre com os fornecedores 299 (Jao) e 394 (Copel). Além disso, salvar com o nome vazio não é validado na tela e também gera o erro do servidor. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de fornecedores do SIFIT. |
| 2. Clicar no botão "Visualizar" do fornecedor "Jao". |
| 3. Clicar no ícone de edição. |
| 4. Alterar o nome para "Jao Teste Ville". |
| 5. Clicar no botão "Salvar". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve salvar a alteração e exibir o nome atualizado na listagem. | O sistema exibe "Erro no servidor" e o fornecedor permanece com o nome "Jao". |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Fornecedores / Alteração | C08-CT08: Alteração dos dados do fornecedor |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 34: Check-ins realizados não aparecem na tela de Presenças**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-034 | Após realizar 3 check-ins no dia (Jerome Lionel, Lila e Steven Kaiki), a tela de Presenças exibe "Total no período 0" e a mensagem "Nenhuma presença encontrada", tanto no período da semana quanto no atalho "Hoje". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de check-in do SIFIT. |
| 2. Realizar o check-in manual de um cliente. |
| 3. Acessar o menu "Presenças". |
| 4. Clicar no atalho "Hoje". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| A tela de Presenças deve listar os check-ins realizados no dia. | A tela exibe "Nenhuma presença encontrada" e total 0. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Check-in / Presenças | C09-CT10: Exibição dos check-ins na tela de Presenças |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 35: Check-in permanece "Pendente" e não há retorno ao registrar entrada novamente**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-035 | Após o check-in, o cliente permanece com status "Pendente" na listagem, com o botão "Registrar entrada" disponível, e o indicador "Presentes agora" continua em 0. Ao clicar novamente em "Registrar entrada", a API responde "Cliente ja possui check-in aberto.", mas nenhuma mensagem é exibida ao usuário. Na janela de check-in manual, o mesmo cliente ainda aparece como "Cliente liberado para realizar o check-in.". Não existe opção para registrar a saída. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de check-in do SIFIT. |
| 2. Realizar o check-in manual do cliente "Jerome Lionel". |
| 3. Observar o status na listagem e o indicador "Presentes agora". |
| 4. Clicar no botão "Registrar entrada" da linha do cliente. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O cliente deve constar como presente, o indicador deve ser atualizado e uma nova tentativa deve informar que já existe check-in aberto. | O status permanece "Pendente", "Presentes agora" fica em 0 e a nova tentativa não exibe nenhuma mensagem. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Check-in / Listagem | C09-CT07: Status do check-in e indicador "Presentes agora" / C09-CT08: Check-in duplicado |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 36: Horário de entrada do check-in exibido com 3 horas a mais**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-036 | O check-in realizado às 18:11 (horário exibido no relógio da própria tela) é apresentado na coluna "Entrada" como 21:11, ou seja, com 3 horas de diferença, o que indica a exibição do horário em UTC em vez do horário de Brasília. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de check-in do SIFIT e observar o horário no topo da tela. |
| 2. Realizar o check-in manual de um cliente. |
| 3. Observar o horário exibido na coluna "Entrada". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| A coluna "Entrada" deve exibir o horário local do check-in (ex.: 18:11). | A coluna "Entrada" exibe 21:11. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Check-in / Listagem | C09-CT03: Check-in manual de cliente com matrícula ativa |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 37: Cliente sem matrícula ativa é liberado para check-in**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-037 | Ao selecionar no check-in manual a cliente "Lila", que não possui matrícula ativa (consta como "Sem Matrícula" na tela de Clientes), o sistema exibe "Cliente liberado para realizar o check-in." e registra a entrada normalmente. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de check-in do SIFIT. |
| 2. Clicar em "Check-in manual". |
| 3. Pesquisar e selecionar a cliente "Lila" (sem matrícula ativa). |
| 4. Clicar em "Registrar entrada". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar que a cliente não possui matrícula ativa e bloquear o check-in. | O sistema libera e registra o check-in. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Check-in / Regras de acesso | C09-CT04: Check-in de cliente sem matrícula ativa |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 38: Ausência de mensagens no check-in manual e na entrada rápida**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-038 | Ao registrar um check-in com sucesso (manual ou pela entrada rápida), nenhuma mensagem de confirmação é exibida, embora a API retorne "Checkin criado com sucesso!". Ao clicar em "Realizar check-in" com o campo "Código do cliente" vazio, nada acontece e nenhuma orientação é exibida. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de check-in do SIFIT. |
| 2. Manter o campo "Código do cliente" vazio e clicar em "Realizar check-in". |
| 3. Informar o código de um cliente ativo (ex.: 406) e clicar em "Realizar check-in". |
| 4. Observar as mensagens exibidas. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve solicitar o código quando o campo estiver vazio e confirmar o check-in realizado. | Nenhuma mensagem é exibida nos dois casos. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Check-in / Entrada rápida e manual | C09-CT06: Entrada rápida sem código / C09-CT03: Check-in manual de cliente com matrícula ativa |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 39: Indicadores da tela de check-in com valores fixos ou incorretos**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-039 | O indicador "Check-ins hoje" exibe a comparação "18% vs ontem" mesmo com 0 check-ins no dia e mantém o mesmo valor após novos check-ins. Com 1 check-in no dia e 4 clientes ativos, a "Taxa de frequência" exibe 100% em vez de 25%. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de check-in do SIFIT sem check-ins no dia e observar o indicador "Check-ins hoje". |
| 2. Realizar o check-in de 1 cliente. |
| 3. Observar os indicadores "Check-ins hoje" e "Taxa de frequência". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| Os indicadores devem ser calculados a partir dos check-ins realizados (ex.: taxa de 25%). | A comparação permanece "18% vs ontem" e a taxa exibe 100%. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Check-in / Indicadores | C09-CT09: Indicadores da tela de check-in |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 40: Erro ao salvar avaliação realizada**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-040 | Ao clicar em "Fazer Avaliação", informar altura (1,75) e peso (80) e clicar em "Salvar", o sistema exibe "Erro ao salvar avaliação" e a avaliação permanece "PENDENTE". A API retorna erro 500 ("Erro interno inesperado."). O mesmo ocorre ao salvar sem medidas, caso em que o sistema também não orienta o preenchimento dos campos. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de avaliações do SIFIT. |
| 2. Cadastrar uma avaliação para o aluno "Steven Kaiki". |
| 3. Clicar em "Fazer Avaliação" na linha da avaliação. |
| 4. Informar altura "1,75" e peso "80". |
| 5. Clicar no botão "Salvar". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve salvar a avaliação e alterar o status para "REALIZADO". | O sistema exibe "Erro ao salvar avaliação" e a avaliação permanece pendente. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Avaliações / Fazer avaliação | C10-CT10: Registro da avaliação realizada |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 41: Alteração de data e hora da avaliação não é salva**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-041 | Na janela "Alterar Data / Hora", ao informar a nova data (26/10/2026) e a nova hora (11:00) e clicar em "Salvar", nenhuma requisição é enviada, nenhuma mensagem é exibida e a avaliação permanece com a data e a hora originais. O mesmo ocorre com os campos vazios. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de avaliações do SIFIT. |
| 2. Clicar no botão "Alterar" de uma avaliação pendente. |
| 3. Informar a nova data "26/10/2026" e a nova hora "11:00". |
| 4. Clicar no botão "Salvar". |
| 5. Verificar a data e a hora na listagem. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve salvar a nova data e hora e confirmar a alteração. | Nada acontece e a avaliação mantém a data e a hora originais. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Avaliações / Alteração de data e hora | C10-CT08: Alteração da data e hora da avaliação |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 42: Cadastro de avaliação aceita hora inválida e retorna erro interno**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-042 | O campo de hora aceita valores inexistentes, como "25:99". Ao salvar, o sistema exibe a mensagem genérica "Erro ao cadastrar Avaliação." e a API retorna erro 500, em vez de informar que a hora é inválida. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de avaliações do SIFIT. |
| 2. Clicar em "Cadastrar Avaliação". |
| 3. Selecionar o aluno "Lila" e o personal "Gabriella". |
| 4. Informar a hora "25:99". |
| 5. Clicar no botão "Salvar". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar que a hora é inválida antes de enviar o cadastro. | O sistema exibe "Erro ao cadastrar Avaliação." (erro 500). |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Avaliações / Cadastro | C10-CT06: Cadastro de avaliação com hora inválida |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 43: IMC exibido sem formatação**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-043 | Ao informar altura 1,75 e peso 80 na tela "Fazer Avaliação", o campo "IMC" exibe "26.122448979591837", com ponto como separador decimal e sem arredondamento. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de avaliações do SIFIT. |
| 2. Clicar em "Fazer Avaliação" de uma avaliação pendente. |
| 3. Informar altura "1,75" e peso "80". |
| 4. Observar o campo "IMC". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O IMC deve ser exibido como "26,12". | O IMC é exibido como "26.122448979591837". |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Avaliações / Fazer avaliação | C10-CT09: Cálculo do IMC |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 44: Erro ao salvar alterações da turma**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-044 | Ao clicar em "Editar" de qualquer turma e em "Salvar", o sistema exibe "Erro ao salvar turma." e a API retorna erro 500 ("Erro interno inesperado."). O erro ocorre ao alterar nome, horário ou status e até ao salvar sem nenhuma alteração (testado nas turmas #10 e #11). |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de turmas do SIFIT. |
| 2. Clicar no botão "Editar" da turma "Turma do Ville". |
| 3. Clicar no botão "Salvar" sem alterar nenhum campo. |
| 4. Verificar a mensagem exibida. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve salvar a turma e exibir mensagem de sucesso. | O sistema exibe "Erro ao salvar turma." e nenhuma alteração é salva. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Turmas / Alteração | C11-CT10: Alteração de turma |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 45: Cadastro de turma aceita hora final anterior à hora inicial**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-045 | O sistema permite cadastrar uma turma com hora inicial 11:00 e hora final 10:00. A turma é salva e exibida na listagem com o horário "11:00:00 - 10:00:00". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de turmas do SIFIT. |
| 2. Clicar em "Cadastrar Turma". |
| 3. Informar o nome "Turma Teste Ville Horario", o plano "Treino Livre" e o dia Seg. |
| 4. Informar a hora inicial 11:00 e a hora final 10:00. |
| 5. Clicar no botão "Salvar". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar que a hora final deve ser maior que a hora inicial. | A turma é cadastrada com o horário "11:00:00 - 10:00:00". |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Turmas / Cadastro | C11-CT09: Cadastro de turma com hora final anterior à inicial |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 46: "Gerar aulas" do SifitBox não informa o resultado**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-046 | Ao clicar em "Gerar aulas" na tela do SifitBox, nenhuma mensagem é exibida. A API retorna "criadas: 0", mas o usuário não é informado se aulas foram geradas, nem o motivo de nenhuma aula ter sido criada. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar o menu "SifitBox". |
| 2. Clicar no botão "Gerar aulas". |
| 3. Observar o retorno exibido ao usuário. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar quantas aulas foram geradas ou o motivo de nenhuma aula ter sido gerada. | Nenhuma mensagem é exibida e a tela continua com "Nenhuma aula encontrada no periodo.". |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| SifitBox / Aulas | C11-CT13: Geração de aulas do SifitBox |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 47: Fechamento de caixa não é salvo após "Buscar Contas"**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-047 | Na janela "Fechamento de Caixa", após selecionar o local e clicar em "Buscar Contas", o botão "Salvar" não executa nenhuma ação: nenhuma requisição é enviada e o caixa permanece "ABERTO". O fechamento só é salvo quando o usuário não busca as contas (ver BUG-048). |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de caixas do SIFIT. |
| 2. Clicar em "Visualizar" de um caixa aberto. |
| 3. Selecionar o local de contas e clicar em "Buscar Contas". |
| 4. Clicar no botão "Salvar". |
| 5. Verificar o status do caixa na listagem. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O caixa deve ser fechado com os totais conferidos. | Nada acontece e o caixa permanece aberto. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Caixas / Fechamento | C12-CT10: Fechamento de caixa com conferência das contas |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 48: Caixa pode ser fechado sem a conferência das contas**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-048 | Embora a janela oriente "Confira o periodo, busque as contas e valide os totais antes de salvar", ao clicar em "Salvar" sem buscar as contas o caixa é fechado com todos os totais zerados (entradas, saídas e total). |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de caixas do SIFIT. |
| 2. Clicar em "Visualizar" de um caixa aberto. |
| 3. Clicar no botão "Salvar" sem clicar em "Buscar Contas". |
| 4. Verificar o status do caixa na listagem. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve exigir a busca e a conferência das contas antes do fechamento. | O caixa é fechado com os totais zerados. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Caixas / Fechamento | C12-CT11: Fechamento de caixa sem buscar as contas |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 49: Sistema permite abrir mais de um caixa no mesmo local**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-049 | Com um caixa já aberto no local "Teste2", foi possível abrir um segundo caixa no mesmo local e na mesma data (caixas #29 e #30). O sistema passou a ter 5 caixas abertos para apenas 4 locais. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de caixas do SIFIT. |
| 2. Abrir um caixa no local "Teste2". |
| 3. Clicar novamente em "Abrir Caixa" e selecionar o local "Teste2". |
| 4. Clicar no botão "Salvar". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar que já existe um caixa aberto para o local. | Um segundo caixa é aberto no mesmo local. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Caixas / Abertura | C12-CT08: Abertura de caixa duplicado no mesmo local |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 50: Erro interno ao abrir caixa sem local de contas**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-050 | Ao clicar em "Salvar" na janela "Abrir Caixa" sem selecionar o local de contas, o sistema exibe "Erro no servidor - Erro interno inesperado." (erro 500), em vez de informar que o local é obrigatório. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de caixas do SIFIT. |
| 2. Clicar em "Abrir Caixa". |
| 3. Não selecionar o local de contas. |
| 4. Clicar no botão "Salvar". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar que o local de contas é obrigatório. | O sistema exibe "Erro no servidor". |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Caixas / Abertura | C12-CT06: Abertura de caixa sem local |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 51: Indicador "Caixas Fechados" é reduzido ao abrir um caixa**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-051 | Com 3 caixas abertos e 17 fechados, ao abrir um novo caixa o indicador "Caixas Fechados" passa para 16 e, ao abrir outro, para 15, embora nenhum caixa tenha sido reaberto. Após fechar os 2 caixas de teste, o indicador volta a 17, quando deveria ser 19. O valor parece ser calculado como 20 menos a quantidade de caixas abertos. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de caixas do SIFIT e anotar os indicadores. |
| 2. Abrir um novo caixa. |
| 3. Observar os indicadores "Caixas Abertos" e "Caixas Fechados". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| "Caixas Abertos" deve aumentar em 1 e "Caixas Fechados" deve permanecer igual. | "Caixas Fechados" diminui em 1 a cada caixa aberto. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Caixas / Indicadores | C12-CT09: Indicadores de caixas abertos e fechados |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 52: Listagem inicial de caixas ignora o período exibido no filtro**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-052 | Ao acessar a tela, o filtro exibe o período de 01/10/2026 a 31/10/2026, mas a listagem mostra todos os 20 caixas (de 2022 a 2026) e o indicador "Registros no Periodo" exibe 20. Somente após clicar em "Buscar" o período é aplicado e a listagem passa a exibir 1 caixa. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de caixas do SIFIT. |
| 2. Observar o período exibido nos filtros e as datas dos caixas listados. |
| 3. Clicar no botão "Buscar" sem alterar os filtros. |
| 4. Comparar a quantidade de caixas exibidos. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| A listagem inicial deve exibir somente os caixas do período exibido nos filtros. | A listagem inicial exibe todos os caixas, fora do período. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Caixas / Listagem | C12-CT02: Listagem inicial conforme o período exibido |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 53: Não é possível registrar o pagamento de conta a pagar**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-053 | Não existe opção para registrar o pagamento de uma conta pendente: a linha da listagem possui apenas os botões "Visualizar" e "Deletar", e a janela "Visualizar Conta a Pagar" possui apenas o botão "Fechar". Assim, as contas permanecem "PENDENTE" indefinidamente. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de contas a pagar do SIFIT. |
| 2. Cadastrar uma conta pendente para o fornecedor "Centrion Web". |
| 3. Procurar na linha da conta uma opção de pagamento. |
| 4. Clicar em "Visualizar" e procurar uma opção de pagamento. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve permitir registrar o pagamento e alterar o status para "PAGO". | Não há nenhuma opção para registrar o pagamento. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Contas a Pagar / Pagamento | C13-CT08: Registro do pagamento da conta |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 54: Indicadores "Total a Pagar" e "Valor Restante" exibem zero**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-054 | Com contas pendentes listadas (ex.: R$ 200,00 da conta 24 e R$ 50,00 da conta de teste), os indicadores "Total a Pagar" e "Valor Restante" permanecem em 0, enquanto "Contas Listadas" é atualizado corretamente. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de contas a pagar do SIFIT. |
| 2. Observar as contas pendentes listadas no período. |
| 3. Observar os indicadores "Total a Pagar" e "Valor Restante". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| Os indicadores devem exibir a soma dos valores das contas pendentes. | Os indicadores exibem 0. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Contas a Pagar / Indicadores | C13-CT04: Indicadores de valores a pagar |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 55: Cadastro de conta a pagar sem validação dos campos obrigatórios**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-055 | Ao salvar uma nova conta a pagar vazia, sem fornecedor ou sem valor, o sistema não informa quais campos devem ser preenchidos: a requisição é enviada e o sistema exibe a mensagem genérica "Erro ao salvar conta a pagar" (erro 500). |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de contas a pagar do SIFIT. |
| 2. Clicar em "Nova Conta". |
| 3. Clicar no botão "Salvar" sem preencher fornecedor e valor. |
| 4. Verificar a mensagem exibida. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar que fornecedor e valor são obrigatórios. | O sistema exibe "Erro ao salvar conta a pagar" (erro 500). |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Contas a Pagar / Cadastro | C13-CT05: Cadastro de conta a pagar com campos obrigatórios vazios |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 56: Erro no servidor exibido após excluir conta a pagar**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-056 | Ao confirmar a exclusão de uma conta a pagar, a conta é excluída, mas em seguida o sistema exibe "Erro no servidor - Erro interno inesperado.", pois tenta carregar novamente a conta que acabou de ser removida. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de contas a pagar do SIFIT. |
| 2. Clicar em "Deletar" de uma conta de teste. |
| 3. Confirmar a mensagem "Deseja deletar esta conta?". |
| 4. Verificar a mensagem exibida. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve excluir a conta e exibir mensagem de sucesso. | A conta é excluída, mas o sistema exibe "Erro no servidor". |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Contas a Pagar / Exclusão | C13-CT09: Exclusão de conta a pagar |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 57: Visualização da conta a pagar exibe códigos internos e campos vazios**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-057 | Na janela "Visualizar Conta a Pagar", o campo "Codigo" fica vazio, o tipo é exibido como "DESPESA_FORNECEDOR", a categoria e o tipo de documento são exibidos pelo código interno (ex.: "Categoria 3", "Tipo 1") e a data de emissão é exibida no formato "2026-10-25". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de contas a pagar do SIFIT. |
| 2. Clicar em "Visualizar" de uma conta. |
| 3. Observar os campos exibidos. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| A visualização deve exibir o código da conta, a categoria e o tipo pelo nome e as datas no formato dd/mm/aaaa. | São exibidos códigos internos, campo de código vazio e data no formato aaaa-mm-dd. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Contas a Pagar / Visualização | C13-CT07: Visualização da conta a pagar |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 58: Despesa fixa aceita valor negativo e erro interno com valor em texto**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-058 | O campo "Valor" da despesa fixa não possui validação: o valor "-100" é aceito e a despesa é cadastrada com "-R$ 100,00"; ao informar "abc", o sistema exibe a mensagem genérica "Erro ao salvar despesa fixa" (erro 500). |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de despesas fixas do SIFIT. |
| 2. Clicar em "Nova Despesa". |
| 3. Informar o nome "Despesa Teste Ville Negativa" e o valor "-100". |
| 4. Clicar no botão "Salvar Despesa". |
| 5. Verificar a despesa na listagem. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve aceitar somente valores numéricos maiores que zero. | A despesa é cadastrada com valor negativo. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Despesas Fixas / Cadastro | C13-CT13: Cadastro de despesa fixa com valor negativo |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 59: Ficha de treino não pode ser aberta nem salva**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-059 | Após criar a ficha, a tela de montagem dos treinos é exibida, mas ao clicar em "Salvar Ficha" o sistema exibe "Erro no servidor - Erro interno inesperado." (erro 500). Ao clicar em "Visualizar" na listagem, o sistema também exibe "Erro no servidor". A API de consulta da ficha retorna o erro do banco de dados "SQLSTATE[42S22]: Column not found: 1054 Unknown column 'f.descanso_padrao' in 'field list'", indicando uma coluna inexistente no banco. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Cadastrar um objetivo em "Objetivos Treino" (pré-requisito). |
| 2. Acessar "Ficha de Treino" e clicar em "Cadastrar Ficha". |
| 3. Selecionar o aluno, o personal e o objetivo e clicar em "Criar Nova Ficha". |
| 4. Clicar em "Adicionar Treino" e depois em "Salvar Ficha". |
| 5. Voltar à listagem e clicar em "Visualizar" da ficha. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve salvar os treinos e permitir abrir a ficha cadastrada. | O sistema exibe "Erro no servidor" ao salvar e ao visualizar a ficha. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Fichas de Treino / Montagem e visualização | C14-CT05: Montagem e salvamento dos treinos da ficha / C14-CT06: Visualização da ficha de treino |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 60: Mensagem genérica ao criar ficha sem objetivo do treino**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-060 | Ao criar a ficha sem objetivo, o sistema exibe apenas "Erro ao salvar Ficha.". A API retorna a mensagem correta "Escolha o objetivo do treino.", mas ela não é exibida ao usuário. Além disso, o campo "Objetivo" não apresenta opções quando não há objetivos cadastrados, sem orientar o usuário a cadastrá-los em "Objetivos Treino". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar "Ficha de Treino" e clicar em "Cadastrar Ficha". |
| 2. Selecionar o aluno "Steven Kaiki" e o personal "Santhago". |
| 3. Não selecionar o objetivo (campo sem opções). |
| 4. Clicar em "Criar Nova Ficha". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar "Escolha o objetivo do treino." e orientar o cadastro de objetivos. | O sistema exibe "Erro ao salvar Ficha.". |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Fichas de Treino / Cadastro | C14-CT03: Cadastro de ficha sem objetivo |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 61: Exclusão de ficha de treino retorna comandos SQL na resposta da API**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-061 | Ao excluir uma ficha de treino, a exclusão é realizada, porém a resposta da API contém o comando SQL executado e os parâmetros ("DELETE FROM ficha_treino WHERE id = 1 AND empresa_id = ..."), expondo detalhes internos do banco de dados. A falha é visível no DevTools (aba Network). |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar "Ficha de Treino". |
| 2. Abrir o DevTools do navegador na aba "Network". |
| 3. Clicar em "Deletar" de uma ficha de teste e confirmar. |
| 4. Verificar a resposta da requisição "deletar-ficha". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| A API deve retornar apenas o resultado da operação, sem expor comandos SQL. | A resposta da API contém o comando SQL executado. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Fichas de Treino / Exclusão | C14-CT07: Exclusão de ficha de treino |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 62: Sistema permite cadastrar exercício duplicado no mesmo grupo**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-062 | Foi possível cadastrar duas vezes o exercício "Exercício Teste Ville" no grupo "Peitoral", sem nenhum aviso. O total de exercícios passou de 6 para 7. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de exercícios do SIFIT. |
| 2. Clicar em "Adicionar" no grupo "Peitoral" e cadastrar "Exercício Teste Ville". |
| 3. Repetir o cadastro com o mesmo nome no mesmo grupo. |
| 4. Verificar o grupo "Peitoral". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar que o exercício já está cadastrado no grupo. | O exercício é cadastrado em duplicidade. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Exercícios / Cadastro | C14-CT11: Cadastro de exercício duplicado |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 63: Sistema permite cadastrar lead duplicado**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-063 | Foi possível cadastrar duas vezes o lead "Lead Teste Ville" com o mesmo e-mail (lead.ville@teste.com) e o mesmo telefone ((44) 99999-0000), sem nenhum aviso. Os dois registros passam a constar na listagem (códigos 6 e 7). |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de prospecção do SIFIT. |
| 2. Cadastrar o lead "Lead Teste Ville" com e-mail e telefone. |
| 3. Clicar novamente em "Adicionar Lead" e informar o mesmo nome, e-mail e telefone. |
| 4. Clicar no botão "Salvar Lead". |
| 5. Verificar a listagem. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar que já existe um lead com o mesmo e-mail ou telefone. | O lead é cadastrado em duplicidade. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Prospecção / Cadastro de lead | C15-CT10: Cadastro de lead duplicado |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 64: Erro interno ao cadastrar colaborador sem selecionar Status e Sexo**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-064 | Na tela "Novo Colaborador", os campos "Status" e "Sexo" exibem "Ativo" e "Masculino", mas não possuem valor selecionado. Ao salvar sem alterar esses campos (mesmo com os demais dados válidos), o sistema exibe "Erro no servidor - Erro interno inesperado." (erro 500). O cadastro só funciona quando o usuário seleciona explicitamente Status e Sexo. Com o formulário vazio, o sistema também exibe o erro 500 em vez de indicar os campos obrigatórios. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de colaboradores e clicar em "Novo Colaborador". |
| 2. Preencher nome, data de nascimento, CPF, e-mail, login, senha e celular válidos. |
| 3. Não alterar os campos "Status" e "Sexo" (exibindo "Ativo" e "Masculino"). |
| 4. Clicar no botão "Salvar". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve cadastrar o colaborador com os valores exibidos ou informar os campos obrigatórios. | O sistema exibe "Erro no servidor" (erro 500). |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Colaboradores / Cadastro | C16-CT06: Cadastro de colaborador sem alterar Status e Sexo / C16-CT04: Cadastro de colaborador com campos vazios |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 65: Busca de colaborador por código inexistente exibe linha vazia**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-065 | Ao pesquisar o código "999" na tela de colaboradores, a listagem exibe uma linha vazia contendo apenas "/", em vez de informar que nenhum colaborador foi encontrado. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de colaboradores do SIFIT. |
| 2. Informar "999" no campo "Código". |
| 3. Clicar no botão "Buscar". |
| 4. Verificar a listagem exibida. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar que nenhum colaborador foi encontrado. | A listagem exibe uma linha vazia com "/". |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Colaboradores / Busca | C16-CT03: Busca de colaborador com código inexistente |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 66: Alteração de colaborador retorna comandos SQL na resposta da API**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-066 | Ao salvar a alteração de um colaborador, a alteração é realizada, porém a resposta da API contém o comando SQL executado ("UPDATE pessoas SET nome = :nome, cpf = :cpf, ...") e seus parâmetros, expondo detalhes internos do banco de dados. A falha é visível no DevTools (aba Network). |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar o perfil de um colaborador e clicar em "Editar". |
| 2. Abrir o DevTools do navegador na aba "Network". |
| 3. Alterar o nome e clicar em "Salvar". |
| 4. Verificar a resposta da requisição "atualizar/colaborador". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| A API deve retornar apenas o resultado da operação, sem expor comandos SQL. | A resposta da API contém o comando SQL executado. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Colaboradores / Alteração | C16-CT07: Alteração de colaborador |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 67: Funções não podem ser alteradas nem excluídas**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-067 | Na tela de funções, a janela aberta pelo botão "Visualizar" exibe todos os campos somente para leitura, com os botões "Fechar" e "Voltar", e a listagem não possui botão de exclusão. Assim, uma função cadastrada com erro (ex.: duplicada) não pode ser corrigida nem removida. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de funções do SIFIT. |
| 2. Clicar em "Visualizar" de uma função. |
| 3. Tentar alterar o nome da função. |
| 4. Procurar na listagem uma opção para excluir a função. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve permitir alterar e excluir funções. | Os campos são somente leitura e não há opção de exclusão. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Funções / Alteração e exclusão | C16-CT16: Alteração e exclusão de função |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 68: Sistema permite cadastrar função duplicada**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-068 | Foi possível cadastrar duas vezes a função "Função Teste Ville" (códigos #9 e #10), sem nenhum aviso. Como funções não podem ser excluídas (BUG-067), a duplicidade não pode ser corrigida. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de funções do SIFIT. |
| 2. Cadastrar a função "Função Teste Ville". |
| 3. Clicar novamente em "Nova Função" e informar o mesmo nome. |
| 4. Clicar no botão "Salvar Função". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar que a função já existe. | A função é cadastrada em duplicidade. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Funções / Cadastro | C16-CT15: Cadastro de função duplicada |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 69: Produto do tipo Pontuação não pode ser cadastrado**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-069 | Ao selecionar o tipo "Pontuação", o campo "Preço" é substituído pelo campo "Pontuação". Ao salvar o produto com 100 pontos, o sistema exibe "Erro ao salvar produto" e a API retorna o erro do banco de dados "Data truncated for column 'valor' at row 1", pois o valor é enviado vazio. Assim, nenhum produto de troca por pontos pode ser cadastrado. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de produtos do SIFIT e clicar em "Novo". |
| 2. Informar o nome "Produto Teste Ville Pontos". |
| 3. Selecionar o tipo "Pontuação" e informar 100 no campo "Pontuação". |
| 4. Clicar no botão "Salvar". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve cadastrar o produto do tipo Pontuação com 100 pontos. | O sistema exibe "Erro ao salvar produto" e o produto não é cadastrado. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Produtos / Cadastro | C17-CT07: Cadastro de produto do tipo Pontuação |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 70: Cadastro de produto sem validação e com erro do banco de dados**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-070 | Ao salvar um produto com os campos vazios, a tela não indica os campos obrigatórios e exibe apenas "Erro ao salvar produto". A API retorna o erro do banco de dados "Data truncated for column 'valor' at row 1", expondo detalhes internos. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de produtos do SIFIT e clicar em "Novo". |
| 2. Manter os campos vazios. |
| 3. Clicar no botão "Salvar". |
| 4. Verificar a mensagem exibida e a resposta da API no DevTools. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar que nome e preço são obrigatórios, sem expor erros do banco de dados. | O sistema exibe "Erro ao salvar produto" e a API retorna o erro do banco. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Produtos / Cadastro | C17-CT04: Cadastro de produto com campos vazios |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 71: Sistema permite cadastrar produto com preço negativo**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-071 | O campo "Preço" aceita valores negativos: o produto "Produto Teste Ville Negativo" foi cadastrado com o preço "-50" e exibido na listagem como "R$ -50". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de produtos do SIFIT e clicar em "Novo". |
| 2. Informar o nome "Produto Teste Ville Negativo" e o preço "-50". |
| 3. Clicar no botão "Salvar". |
| 4. Verificar o produto na listagem. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar que o preço deve ser maior que zero. | O produto é cadastrado com preço negativo. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Produtos / Cadastro | C17-CT05: Cadastro de produto com preço negativo |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 72: Valores dos produtos exibidos sem formatação monetária**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-072 | Na listagem de produtos, os valores são exibidos sem separador de milhar, sem casas decimais fixas e com ponto como separador decimal, por exemplo "R$ 1550", "R$ 7000.99" e "R$ 49.9". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a tela de produtos do SIFIT. |
| 2. Observar a coluna "Valor / Pontos". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| Os valores devem ser exibidos como "R$ 1.550,00", "R$ 7.000,99" e "R$ 49,90". | Os valores são exibidos como "R$ 1550", "R$ 7000.99" e "R$ 49.9". |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Produtos / Listagem | C17-CT08: Exibição do valor dos produtos |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 73: Anamneses aplicadas não aparecem na listagem**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-073 | Após finalizar a anamnese do aluno Steven Kaiki (a API confirma a gravação com o código 11), a tela de fichas de anamnese continua exibindo "Nenhuma ficha encontrada" e todos os indicadores em 0. A consulta da listagem é enviada com o parâmetro "id": null e retorna lista vazia. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar "Fichas Anamnese" e clicar em "Nova Anamnese". |
| 2. Selecionar o aluno "Steven Kaiki" e o modelo "Triplet". |
| 3. Clicar em "Iniciar" e em "Finalizar Anamnese". |
| 4. Verificar a listagem e os indicadores. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| A anamnese deve constar na listagem e os indicadores devem ser atualizados. | A listagem exibe "Nenhuma ficha encontrada" e os indicadores permanecem em 0. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Fichas de Anamnese / Listagem | C18-CT07: Listagem das anamneses aplicadas |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 74: Perguntas do modelo de anamnese não são exibidas**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-074 | O modelo "Triplet" informa "1 perguntas", mas ao clicar em "Iniciar" o assistente vai direto para a etapa "Revisar e Finalizar", sem exibir a pergunta. A anamnese é finalizada e gravada com a lista de respostas vazia e status "concluida". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar "Fichas Anamnese" e clicar em "Nova Anamnese". |
| 2. Selecionar o aluno "Steven Kaiki". |
| 3. Selecionar o modelo "Triplet" (1 pergunta) e clicar em "Iniciar". |
| 4. Verificar se a pergunta é exibida. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| A pergunta do modelo deve ser exibida para resposta antes da revisão. | O assistente pula para "Revisar e Finalizar" sem exibir a pergunta. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Fichas de Anamnese / Aplicação | C18-CT05: Exibição das perguntas do modelo |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 75: Assistente de anamnese avança sem aluno e falha com erro interno**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-075 | Ao clicar em "Próxima" sem selecionar aluno, o assistente avança para a escolha do modelo. Ao concluir o fluxo, o sistema exibe "Erro no servidor - Erro interno inesperado." (erro 500), pois a anamnese é enviada sem aluno. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar "Fichas Anamnese" e clicar em "Nova Anamnese". |
| 2. Não selecionar aluno e clicar em "Próxima". |
| 3. Selecionar o modelo "Triplet", clicar em "Iniciar" e em "Finalizar Anamnese". |
| 4. Verificar as mensagens exibidas. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve impedir o avanço e informar que é necessário selecionar um aluno. | O assistente avança e a finalização exibe "Erro no servidor". |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Fichas de Anamnese / Aplicação | C18-CT02: Avançar sem selecionar aluno |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |

---

### 🐞 **Bug 76: Nome do aluno não é exibido na escolha do modelo de anamnese**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-076 | Na etapa "Selecionar Modelo", o texto é exibido como "Escolha o modelo de anamnese a aplicar para .", sem o nome do aluno selecionado, embora o aluno seja exibido no cabeçalho das etapas seguintes. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar "Fichas Anamnese" e clicar em "Nova Anamnese". |
| 2. Selecionar o aluno "Steven Kaiki". |
| 3. Observar o texto da etapa "Selecionar Modelo". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O texto deve exibir "Escolha o modelo de anamnese a aplicar para Steven Kaiki.". | O texto é exibido sem o nome do aluno. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Linux. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Fichas de Anamnese / Aplicação | C18-CT04: Exibição do aluno na escolha do modelo |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]() |
