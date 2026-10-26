## Cenário 04: Gestão de clientes na plataforma SIFIT.

### Caso de Teste 01: Acesso à listagem de clientes.

| ID | Descrição |
| :--- | :--- |
| C04-CT01 | Verificar se a tela de clientes é exibida corretamente com os filtros, os indicadores e a listagem. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos autenticados no SIFIT |
| **QUANDO** acessarmos o menu "Clientes" |
| **ENTÃO** a tela deverá exibir os filtros de busca, os indicadores (Clientes Cadastrados, Clientes Ativos, Sem Matrículas e Ausentes) e a listagem de clientes |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir a tela de clientes com todos os seus componentes carregados corretamente. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/b1c527ff-d8b0-4c51-a962-a32348beab98)      |

---

### Caso de Teste 02: Busca de cliente pelo nome.

| ID | Descrição |
| :--- | :--- |
| C04-CT02 | Verificar se a busca pelo nome retorna os clientes correspondentes, inclusive com nome parcial. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir cliente cadastrado com o nome pesquisado. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de clientes |
| **E** informamos o nome completo ou parte do nome de um cliente no campo "Nome" |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** a listagem deverá exibir apenas os clientes cujo nome corresponde à pesquisa |

| **Critérios de aceitação** |
| :--- |
| O sistema deve filtrar a listagem pelo nome informado, sem diferenciar letras maiúsculas e minúsculas. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/1a48e93b-6754-48a9-8b3e-302281e1b967)      |

---

### Caso de Teste 03: Busca de cliente com nome inexistente.

| ID | Descrição |
| :--- | :--- |
| C04-CT03 | Verificar se o sistema informa que nenhum cliente foi encontrado ao pesquisar um nome inexistente. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de clientes |
| **E** informamos no campo "Nome" um nome que não está cadastrado |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** o sistema deverá apresentar uma mensagem informando que nenhum cliente foi encontrado |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir uma mensagem informativa em vez de apenas uma tabela vazia. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/1400615a-e41d-4ab8-95d5-5a68bd56510d)      |

---

### Caso de Teste 04: Busca de cliente pelo código.

| ID | Descrição |
| :--- | :--- |
| C04-CT04 | Verificar se a busca pelo código retorna o cliente correspondente. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir cliente cadastrado com o código pesquisado. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de clientes |
| **E** informamos o código de um cliente cadastrado no campo "Código" |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** a listagem deverá exibir o cliente que possui o código informado |

| **Critérios de aceitação** |
| :--- |
| O sistema deve retornar o cliente correspondente ao código informado, independentemente de possuir matrícula. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/e36fb928-6b21-4210-b361-cc99a1358cf9)      |

---

### Caso de Teste 05: Paginação da listagem filtrada.

| ID | Descrição |
| :--- | :--- |
| C04-CT05 | Verificar se a quantidade de páginas corresponde ao número de clientes retornados pelo filtro. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de clientes com o filtro "Status" em "Ativo" |
| **E** a listagem exibe menos clientes do que o limite por página |
| **QUANDO** observarmos a paginação e clicarmos nas páginas "2" e "3" |
| **ENTÃO** deverá existir apenas uma página, sem páginas vazias |

| **Critérios de aceitação** |
| :--- |
| A paginação deve refletir a quantidade de registros do filtro aplicado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/a38cb135-f8d3-43d6-8385-f821247140da)      |

---

### Caso de Teste 06: Quantidade de registros por página.

| ID | Descrição |
| :--- | :--- |
| C04-CT06 | Verificar se a listagem respeita a quantidade de registros por página selecionada. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existirem mais de 50 clientes cadastrados. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de clientes com a opção "50" registros por página |
| **E** selecionamos a opção "Todos" no filtro "Status" |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** a primeira página deverá exibir no máximo 50 clientes |

| **Critérios de aceitação** |
| :--- |
| O sistema deve limitar a listagem à quantidade de registros por página selecionada. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/7e9313e8-1a42-4e1f-99be-f22711d0d555)      |

---

### Caso de Teste 07: Cadastro de cliente com campos obrigatórios vazios.

| ID | Descrição |
| :--- | :--- |
| C04-CT07 | Verificar se o sistema impede o cadastro quando os campos obrigatórios não são preenchidos. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que acessamos a tela "Cadastrar Cliente" pelo botão "Novo Cliente" |
| **E** mantemos os campos obrigatórios (Nome, Status, Sexo e Data de Nascimento) vazios |
| **QUANDO** clicarmos no botão "Cadastrar Cliente" |
| **ENTÃO** o sistema deverá apresentar mensagem de erro indicando os campos obrigatórios |

| **Critérios de aceitação** |
| :--- |
| O sistema deve impedir o cadastro e orientar o usuário a preencher os campos obrigatórios. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/b2527661-b09d-4792-b31d-a0e24e09bdc0)      |

---

### Caso de Teste 08: Cadastro de cliente com dados válidos.

| ID | Descrição |
| :--- | :--- |
| C04-CT08 | Verificar se o cliente é cadastrado ao informar todos os dados corretamente. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela "Cadastrar Cliente" |
| **E** informamos o nome "Teste Ville Nunes", o status "Ativo", o sexo e uma data de nascimento válida |
| **QUANDO** clicarmos no botão "Cadastrar Cliente" |
| **ENTÃO** o sistema deverá exibir mensagem de sucesso e o cliente deverá constar na listagem |

| **Critérios de aceitação** |
| :--- |
| O sistema deve cadastrar o cliente e exibi-lo na listagem de clientes. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/e21003f6-a3e5-4f6f-9ea2-755f25b7ff91)      |

---

### Caso de Teste 09: Visualização dos dados do cliente.

| ID | Descrição |
| :--- | :--- |
| C04-CT09 | Verificar se a tela de detalhes do cliente é exibida ao clicar em "Visualizar". |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir cliente cadastrado. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de clientes |
| **QUANDO** clicarmos no botão "Visualizar" (lupa) de um cliente |
| **ENTÃO** deveremos ser direcionados à tela "Visualizar Cliente" com os dados do cliente selecionado |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir os dados, o desempenho, a matrícula e a situação financeira do cliente selecionado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/aa6dbfa6-1c39-4d8a-b536-86d4b806198e)      |

---

### Caso de Teste 10: Alteração dos dados do cliente.

| ID | Descrição |
| :--- | :--- |
| C04-CT10 | Verificar se as alterações nos dados do cliente são salvas corretamente. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir cliente cadastrado. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela "Visualizar Cliente" |
| **E** clicamos no botão "Alterar dados" |
| **E** alteramos o nome do cliente para "Teste Ville Nunes" |
| **QUANDO** clicarmos no botão "Salvar Alterações" |
| **ENTÃO** o sistema deverá exibir mensagem de sucesso e a listagem deverá apresentar o nome atualizado |

| **Critérios de aceitação** |
| :--- |
| O sistema deve salvar as alterações e exibi-las na listagem e nos detalhes do cliente. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/ef0c7a28-0a2f-4bb6-9c78-3fc0995ec51f)      |

---

### Caso de Teste 11: Cancelamento da exclusão de cliente.

| ID | Descrição |
| :--- | :--- |
| C04-CT11 | Verificar se o sistema solicita confirmação antes de excluir um cliente e mantém o registro ao cancelar. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir cliente cadastrado. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de clientes |
| **E** clicamos no botão "Deletar" (X) de um cliente |
| **QUANDO** o sistema exibir a mensagem "Deseja deletar este cliente?" e clicarmos em "Cancelar" |
| **ENTÃO** o cliente deverá permanecer na listagem |

| **Critérios de aceitação** |
| :--- |
| O sistema deve solicitar confirmação antes da exclusão e não remover o cliente quando a ação for cancelada. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/a0153288-ba95-4015-852c-17228345f666)      |
