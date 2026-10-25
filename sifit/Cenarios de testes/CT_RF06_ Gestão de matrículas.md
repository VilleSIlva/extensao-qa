## Cenário 06: Gestão de matrículas na plataforma SIFIT.

### Caso de Teste 01: Acesso à listagem de matrículas.

| ID | Descrição |
| :--- | :--- |
| C06-CT01 | Verificar se a tela de matrículas é exibida com os filtros, os indicadores e a listagem. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos autenticados no SIFIT |
| **QUANDO** acessarmos o menu "Matrículas" |
| **ENTÃO** a tela deverá exibir os filtros de busca, os indicadores (Matrículas Ativas, Recorrentes, Não Renovadas e Cadastradas este Mês) e a listagem de matrículas |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir a tela de matrículas com todos os seus componentes carregados corretamente. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 02: Busca de matrícula pelo nome do cliente.

| ID | Descrição |
| :--- | :--- |
| C06-CT02 | Verificar se a busca pelo nome retorna as matrículas do cliente, inclusive com nome parcial. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir matrícula cadastrada para o cliente pesquisado. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de matrículas |
| **E** informamos o nome completo ou parte do nome do cliente no campo "Nome" |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** a listagem deverá exibir apenas as matrículas do cliente pesquisado |

| **Critérios de aceitação** |
| :--- |
| O sistema deve filtrar a listagem pelo nome informado, sem diferenciar letras maiúsculas e minúsculas. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 03: Busca de matrícula com nome inexistente.

| ID | Descrição |
| :--- | :--- |
| C06-CT03 | Verificar se o sistema informa que nenhuma matrícula foi encontrada ao pesquisar um nome inexistente. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de matrículas |
| **E** informamos no campo "Nome" um nome que não possui matrícula |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** o sistema deverá apresentar uma mensagem informando que nenhuma matrícula foi encontrada |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir uma mensagem informativa em vez de apenas uma tabela vazia. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 04: Paginação da listagem de matrículas.

| ID | Descrição |
| :--- | :--- |
| C06-CT04 | Verificar se é possível acessar todas as matrículas cadastradas por meio da paginação. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existirem mais de 50 matrículas cadastradas. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de matrículas com a opção "50" registros por página |
| **QUANDO** observarmos a paginação e clicarmos no botão "Próxima" |
| **ENTÃO** deveremos ser direcionados à página 2 com as demais matrículas |

| **Critérios de aceitação** |
| :--- |
| A paginação deve permitir acessar todas as matrículas cadastradas. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 05: Cadastro de matrícula sem cliente selecionado.

| ID | Descrição |
| :--- | :--- |
| C06-CT05 | Verificar se o sistema impede o cadastro da matrícula quando nenhum cliente é selecionado. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que acessamos a tela "Cadastrar Matrícula" pelo botão "Cadastrar Matrícula" |
| **E** não selecionamos nenhum cliente |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** o sistema deverá apresentar a mensagem "Selecione o cliente!" |

| **Critérios de aceitação** |
| :--- |
| O sistema deve impedir o cadastro até que um cliente seja selecionado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 06: Cadastro de matrícula sem tipo de pagamento.

| ID | Descrição |
| :--- | :--- |
| C06-CT06 | Verificar se o sistema impede o cadastro da matrícula quando o tipo de pagamento não é selecionado. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir cliente cadastrado. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela "Cadastrar Matrícula" |
| **E** selecionamos um cliente e uma modalidade |
| **E** não selecionamos o tipo de pagamento |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** o sistema deverá apresentar a mensagem "Selecione o Tipo de Pagamento" |

| **Critérios de aceitação** |
| :--- |
| O sistema deve impedir o cadastro até que o tipo de pagamento seja selecionado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 07: Cadastro de matrícula com dados válidos.

| ID | Descrição |
| :--- | :--- |
| C06-CT07 | Verificar se a matrícula é cadastrada ao informar todos os dados corretamente. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir cliente sem matrícula ativa. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela "Cadastrar Matrícula" |
| **E** selecionamos o cliente, a modalidade "Treino Livre" e o tipo de pagamento "Pix" |
| **E** informamos o dia de vencimento e a observação "Teste Ville Nunes" |
| **QUANDO** clicarmos no botão "Salvar" e confirmarmos a quantidade de parcelas em "Escolher" |
| **ENTÃO** o sistema deverá exibir a mensagem "Matrícula salva!" e a matrícula deverá constar na listagem com status "ATIVO" |

| **Critérios de aceitação** |
| :--- |
| O sistema deve cadastrar a matrícula e exibi-la na listagem. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 08: Cadastro de matrícula com desconto.

| ID | Descrição |
| :--- | :--- |
| C06-CT08 | Verificar se o desconto informado é aplicado ao valor total da matrícula. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir cliente sem matrícula ativa. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela "Cadastrar Matrícula" com cliente e modalidade "Treino Livre" (R$ 52,00) selecionados |
| **E** informamos o valor "10" no campo "Desconto" |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** o valor total deverá ser R$ 42,00 e a matrícula deverá exibir desconto de R$ 10,00 |

| **Critérios de aceitação** |
| :--- |
| O sistema deve aplicar o desconto e calcular corretamente o valor total. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 09: Cadastro de matrícula para cliente com matrícula ativa.

| ID | Descrição |
| :--- | :--- |
| C06-CT09 | Verificar se o sistema impede uma nova matrícula para cliente que já possui matrícula ativa, informando o motivo. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir cliente com matrícula ativa. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela "Cadastrar Matrícula" |
| **E** selecionamos um cliente que já possui matrícula ativa |
| **E** preenchemos os demais campos corretamente |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** o sistema deverá informar que o cliente já possui matrícula ativa |

| **Critérios de aceitação** |
| :--- |
| O sistema deve impedir a matrícula duplicada e exibir uma mensagem clara com o motivo. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 10: Visualização dos dados da matrícula.

| ID | Descrição |
| :--- | :--- |
| C06-CT10 | Verificar se os dados da matrícula são exibidos corretamente ao clicar em "Visualizar". |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir matrícula cadastrada. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de matrículas |
| **QUANDO** clicarmos no botão "Visualizar" (lupa) de uma matrícula |
| **ENTÃO** o sistema deverá exibir os dados gerais, os dados da matrícula, os valores e a observação conforme o cadastro |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir os dados da matrícula iguais aos informados no cadastro. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 11: Cancelamento de matrícula.

| ID | Descrição |
| :--- | :--- |
| C06-CT11 | Verificar se a matrícula é cancelada ao confirmar o cancelamento. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir matrícula ativa. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de matrículas |
| **E** clicamos no botão "Cancelar" (X) de uma matrícula ativa |
| **E** informamos o motivo do cancelamento e clicamos em "Cancelar Matrícula" |
| **QUANDO** confirmarmos a mensagem "Deseja cancelar essa matrícula?" |
| **ENTÃO** a matrícula deverá constar com status "CANCELADO" na listagem |

| **Critérios de aceitação** |
| :--- |
| O sistema deve atualizar o status da matrícula para cancelado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 12: Exclusão de matrícula.

| ID | Descrição |
| :--- | :--- |
| C06-CT12 | Verificar se a matrícula é excluída ao confirmar a exclusão. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir matrícula cadastrada. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de matrículas |
| **E** clicamos no botão "Deletar" (lixeira) de uma matrícula |
| **QUANDO** confirmarmos a mensagem "Deseja deletar essa matrícula?" |
| **ENTÃO** o sistema deverá exibir mensagem de sucesso e a matrícula não deverá mais constar na listagem |

| **Critérios de aceitação** |
| :--- |
| O sistema deve excluir a matrícula e informar o sucesso da operação. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |
