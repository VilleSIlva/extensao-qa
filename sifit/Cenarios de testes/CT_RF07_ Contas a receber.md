## Cenário 07: Contas a receber na plataforma SIFIT.

### Caso de Teste 01: Acesso à tela de contas a receber.

| ID | Descrição |
| :--- | :--- |
| C07-CT01 | Verificar se a tela de contas a receber é exibida com os filtros, os indicadores e a listagem do mês. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos autenticados no SIFIT |
| **QUANDO** acessarmos o menu "Contas a Receber" |
| **ENTÃO** a tela deverá exibir os filtros, os indicadores (Entradas, Saídas, Líquido, Previsto para o Mês, Recebido no Mês, Pendentes no Mês e Contas Atrasadas) e as contas do mês atual |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir a tela com indicadores coerentes com as contas listadas. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 02: Busca de conta pelo nome do cliente.

| ID | Descrição |
| :--- | :--- |
| C07-CT02 | Verificar se a busca pelo nome do cliente retorna as contas correspondentes. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir conta cadastrada para o cliente pesquisado. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de contas a receber |
| **E** informamos "lila" no campo "Nome do cliente" |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** a listagem deverá exibir apenas as contas da cliente Lila |

| **Critérios de aceitação** |
| :--- |
| O sistema deve filtrar as contas pelo nome do cliente, sem diferenciar letras maiúsculas e minúsculas. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 03: Busca de conta com nome inexistente.

| ID | Descrição |
| :--- | :--- |
| C07-CT03 | Verificar se o sistema informa que nenhuma conta foi encontrada ao pesquisar um nome inexistente. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de contas a receber |
| **E** informamos um nome inexistente no campo "Nome do cliente" |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** o sistema deverá apresentar uma mensagem informando que nenhuma conta foi encontrada |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir uma mensagem informativa em vez de apenas uma tabela vazia. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 04: Filtro de contas por status.

| ID | Descrição |
| :--- | :--- |
| C07-CT04 | Verificar se o filtro "Status" exibe somente as contas com o status selecionado. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existirem contas pendentes e recebidas. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de contas a receber |
| **E** selecionamos "Pendente" no filtro "Status" |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** a listagem deverá exibir somente contas com status "PENDENTE" |

| **Critérios de aceitação** |
| :--- |
| O sistema deve filtrar corretamente a listagem conforme o status selecionado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 05: Consistência do indicador de contas atrasadas.

| ID | Descrição |
| :--- | :--- |
| C07-CT05 | Verificar se a quantidade do indicador "Contas Atrasadas" corresponde às contas exibidas no filtro "Vencido". |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e o indicador "Contas Atrasadas" deve exibir valor maior que zero. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de contas a receber e o indicador "Contas Atrasadas" exibe 2 |
| **E** selecionamos "Vencido" no filtro "Status" |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** a listagem deverá exibir as 2 contas atrasadas |

| **Critérios de aceitação** |
| :--- |
| O indicador e o filtro de contas vencidas devem apresentar informações consistentes. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 06: Cadastro de conta com campos obrigatórios vazios.

| ID | Descrição |
| :--- | :--- |
| C07-CT06 | Verificar se o sistema impede o cadastro da conta quando nenhum cliente é selecionado. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que abrimos o formulário "Nova Conta" |
| **E** mantemos os campos vazios |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** o sistema deverá apresentar a mensagem "Selecione o cliente." |

| **Critérios de aceitação** |
| :--- |
| O sistema deve impedir o cadastro até que o cliente seja selecionado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 07: Cadastro de conta com dados válidos.

| ID | Descrição |
| :--- | :--- |
| C07-CT07 | Verificar se a conta é cadastrada e os indicadores são atualizados. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir cliente cadastrado. |

| **Passos** |
| :--- |
| **DADO** que abrimos o formulário "Nova Conta" |
| **E** selecionamos a cliente "Lila", o status "Pendente", o título "Teste Ville Nunes" e o valor R$ 75,50 |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** a conta deverá constar na listagem com status "PENDENTE" e o indicador "Previsto para o Mês" deverá aumentar em R$ 75,50 |

| **Critérios de aceitação** |
| :--- |
| O sistema deve cadastrar a conta e atualizar os indicadores. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 08: Recebimento de conta pendente.

| ID | Descrição |
| :--- | :--- |
| C07-CT08 | Verificar se a baixa (recebimento) de uma conta pendente é registrada corretamente. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado, existir conta pendente e um caixa aberto. |

| **Passos** |
| :--- |
| **DADO** que estamos visualizando uma conta pendente |
| **E** clicamos em "Efetuar Recebimento" |
| **E** selecionamos o tipo de pagamento "Dinheiro" e o local "Caixa Academia" |
| **QUANDO** clicarmos em "Salvar" e confirmarmos a mensagem do caixa |
| **ENTÃO** a conta deverá constar com status "RECEBIDO" e o indicador "Recebido no Mês" deverá ser atualizado |

| **Critérios de aceitação** |
| :--- |
| O sistema deve registrar o recebimento e atualizar o status e os indicadores. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 09: Recebimento de conta sem tipo de pagamento.

| ID | Descrição |
| :--- | :--- |
| C07-CT09 | Verificar se o sistema impede o recebimento quando o tipo de pagamento não é selecionado. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado, existir conta pendente e um caixa aberto. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela "Efetuar Recebimento" de uma conta pendente |
| **E** não selecionamos o tipo de pagamento |
| **QUANDO** clicarmos em "Salvar" |
| **ENTÃO** o sistema deverá informar que o tipo de pagamento é obrigatório |

| **Critérios de aceitação** |
| :--- |
| O sistema deve impedir o recebimento até que o tipo de pagamento seja selecionado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 10: Recebimento com valor maior que o valor a receber.

| ID | Descrição |
| :--- | :--- |
| C07-CT10 | Verificar se o sistema alerta quando o valor recebido é maior que o valor a receber. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado, existir conta pendente e um caixa aberto. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela "Efetuar Recebimento" de uma conta de R$ 75,50 |
| **E** informamos o valor recebido de R$ 100,00 |
| **QUANDO** clicarmos em "Salvar" |
| **ENTÃO** o sistema deverá alertar que o valor recebido é maior que o valor a receber |

| **Critérios de aceitação** |
| :--- |
| O sistema deve impedir ou alertar o recebimento com valor divergente. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 11: Exclusão de conta a receber.

| ID | Descrição |
| :--- | :--- |
| C07-CT11 | Verificar se a conta é excluída ao confirmar a exclusão. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir conta cadastrada. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de contas a receber |
| **E** clicamos no botão "Deletar" de uma conta |
| **QUANDO** confirmarmos a mensagem "Deseja deletar esta conta?" |
| **ENTÃO** a conta não deverá mais constar na listagem e os indicadores deverão ser atualizados |

| **Critérios de aceitação** |
| :--- |
| O sistema deve solicitar confirmação, excluir a conta e atualizar os indicadores. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 12: Geração de conta a receber a partir da matrícula.

| ID | Descrição |
| :--- | :--- |
| C07-CT12 | Verificar se o cadastro de uma matrícula gera a conta a receber correspondente. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir cliente sem matrícula ativa. |

| **Passos** |
| :--- |
| **DADO** que cadastramos uma matrícula no plano "Treino Livre" (R$ 52,00) e confirmamos 1 parcela em "Escolher" |
| **QUANDO** acessarmos a tela de contas a receber e pesquisarmos o cliente em um período amplo |
| **ENTÃO** deverá existir uma conta a receber de R$ 52,00 referente à matrícula |

| **Critérios de aceitação** |
| :--- |
| O sistema deve gerar automaticamente as contas a receber das parcelas da matrícula. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |
