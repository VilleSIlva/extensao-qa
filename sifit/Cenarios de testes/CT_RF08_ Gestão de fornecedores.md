## Cenário 08: Gestão de fornecedores na plataforma SIFIT.

### Caso de Teste 01: Acesso à listagem de fornecedores.

| ID | Descrição |
| :--- | :--- |
| C08-CT01 | Verificar se a tela de fornecedores é exibida com os filtros, os indicadores e a listagem. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos autenticados no SIFIT |
| **QUANDO** acessarmos o menu "Fornecedores" |
| **ENTÃO** a tela deverá exibir os filtros de busca, os indicadores (Fornecedores Cadastrados e Fornecedores Ativos) e a listagem de fornecedores |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir a tela de fornecedores com todos os seus componentes carregados. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 02: Busca de fornecedor pelo nome.

| ID | Descrição |
| :--- | :--- |
| C08-CT02 | Verificar se a busca pelo nome retorna os fornecedores correspondentes, inclusive com nome parcial. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir fornecedor cadastrado com o nome pesquisado. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de fornecedores |
| **E** informamos "pesado" no campo "Nome" |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** a listagem deverá exibir somente o fornecedor "Peso Pesado" |

| **Critérios de aceitação** |
| :--- |
| O sistema deve filtrar a listagem pelo nome informado, sem diferenciar letras maiúsculas e minúsculas. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 03: Busca de fornecedor pelo código.

| ID | Descrição |
| :--- | :--- |
| C08-CT03 | Verificar se a busca pelo código retorna o fornecedor correspondente. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir fornecedor cadastrado com o código pesquisado. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de fornecedores |
| **E** informamos "394" no campo "Código" |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** a listagem deverá exibir somente o fornecedor "Copel" |

| **Critérios de aceitação** |
| :--- |
| O sistema deve retornar o fornecedor correspondente ao código informado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 04: Busca de fornecedor com código inexistente.

| ID | Descrição |
| :--- | :--- |
| C08-CT04 | Verificar se o sistema informa que nenhum fornecedor foi encontrado ao pesquisar um código inexistente. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de fornecedores |
| **E** informamos "999" no campo "Código" |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** a listagem não deverá exibir fornecedores e o sistema deverá informar que nenhum fornecedor foi encontrado |

| **Critérios de aceitação** |
| :--- |
| O sistema não deve exibir fornecedores que não correspondem ao código pesquisado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 05: Cadastro de fornecedor com campos obrigatórios vazios.

| ID | Descrição |
| :--- | :--- |
| C08-CT05 | Verificar se o sistema impede o cadastro quando o nome do fornecedor não é informado. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que abrimos o formulário "Novo Fornecedor" |
| **E** mantemos todos os campos vazios |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** o sistema deverá apresentar a mensagem "Informe o nome do fornecedor." |

| **Critérios de aceitação** |
| :--- |
| O sistema deve impedir o cadastro até que o nome seja informado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 06: Cadastro de fornecedor com dados válidos.

| ID | Descrição |
| :--- | :--- |
| C08-CT06 | Verificar se o fornecedor é cadastrado ao informar os dados corretamente. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que abrimos o formulário "Novo Fornecedor" |
| **E** informamos o nome "Fornecedor Teste Ville", um CNPJ válido, telefone, e-mail, estado "Paraná" e cidade "Umuarama" |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** o sistema deverá exibir mensagem de sucesso e o fornecedor deverá constar na listagem com status "ATIVO" |

| **Critérios de aceitação** |
| :--- |
| O sistema deve cadastrar o fornecedor e exibi-lo na listagem. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 07: Visualização dos dados do fornecedor.

| ID | Descrição |
| :--- | :--- |
| C08-CT07 | Verificar se os dados do fornecedor são exibidos ao clicar em "Visualizar". |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir fornecedor cadastrado. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de fornecedores |
| **QUANDO** clicarmos no botão "Visualizar" (lupa) do fornecedor "Jao" |
| **ENTÃO** deverá ser exibida a janela "Visualizar Fornecedor" com os dados principais, documentos, contato e endereço |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir os dados do fornecedor selecionado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 08: Alteração dos dados do fornecedor.

| ID | Descrição |
| :--- | :--- |
| C08-CT08 | Verificar se as alterações nos dados do fornecedor são salvas corretamente. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir fornecedor cadastrado. |

| **Passos** |
| :--- |
| **DADO** que estamos visualizando o fornecedor "Jao" |
| **E** clicamos no ícone de edição |
| **E** alteramos o nome para "Jao Teste Ville" |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** a listagem deverá exibir o nome atualizado |

| **Critérios de aceitação** |
| :--- |
| O sistema deve salvar as alterações e exibi-las na listagem. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 09: Cancelamento da exclusão de fornecedor.

| ID | Descrição |
| :--- | :--- |
| C08-CT09 | Verificar se o sistema solicita confirmação antes de excluir um fornecedor e mantém o registro ao cancelar. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir fornecedor cadastrado. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de fornecedores |
| **E** clicamos no botão "Deletar" (X) de um fornecedor |
| **QUANDO** o sistema exibir a mensagem "Deseja deletar este fornecedor?" e clicarmos em "Cancelar" |
| **ENTÃO** o fornecedor deverá permanecer na listagem |

| **Critérios de aceitação** |
| :--- |
| O sistema deve solicitar confirmação e não excluir o fornecedor quando a ação for cancelada. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |
