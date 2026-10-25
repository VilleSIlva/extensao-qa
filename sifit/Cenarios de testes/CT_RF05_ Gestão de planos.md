## Cenário 05: Gestão de planos na plataforma SIFIT.

### Caso de Teste 01: Acesso à listagem de planos.

| ID | Descrição |
| :--- | :--- |
| C05-CT01 | Verificar se a tela de planos é exibida com os filtros, os indicadores, o ranking e a listagem. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos autenticados no SIFIT |
| **QUANDO** acessarmos o menu "Planos" |
| **ENTÃO** a tela deverá exibir os filtros de busca, os indicadores (Planos, Ativos, Alunos em Planos e Receita Estimada), o ranking e a listagem de planos |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir a tela de planos com todos os seus componentes carregados corretamente. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 02: Exibição da quantidade de alunos e da receita dos planos.

| ID | Descrição |
| :--- | :--- |
| C05-CT02 | Verificar se a coluna "Alunos", o ranking e o indicador "Receita Estimada" refletem as matrículas ativas. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existirem matrículas ativas (ex.: plano "Treino Livre", R$ 52,00, com 2 alunos). |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de planos |
| **QUANDO** observarmos a coluna "Alunos" do plano "Treino Livre", o ranking e o indicador "Receita Estimada" |
| **ENTÃO** a coluna deverá exibir 2 alunos, o ranking deverá exibir a mensalidade de R$ 52,00 e a receita estimada deverá ser maior que zero |

| **Critérios de aceitação** |
| :--- |
| Os indicadores, o ranking e a listagem devem apresentar valores consistentes com as matrículas ativas. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 03: Busca de plano pelo nome.

| ID | Descrição |
| :--- | :--- |
| C05-CT03 | Verificar se a busca pelo nome retorna os planos correspondentes, inclusive com nome parcial. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir plano cadastrado com o nome pesquisado. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de planos |
| **E** informamos "treino" no campo "Nome do plano" |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** a listagem deverá exibir apenas os planos que contêm "Treino" no nome |

| **Critérios de aceitação** |
| :--- |
| O sistema deve filtrar a listagem pelo nome informado, sem diferenciar letras maiúsculas e minúsculas. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 04: Busca de plano pelo código.

| ID | Descrição |
| :--- | :--- |
| C05-CT04 | Verificar se a busca pelo código retorna somente o plano com o código informado. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir plano cadastrado com o código pesquisado. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de planos |
| **E** informamos "1" no campo "Código" |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** a listagem deverá exibir somente o plano de código #1 |

| **Critérios de aceitação** |
| :--- |
| O sistema deve retornar apenas o plano cujo código é igual ao informado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 05: Cadastro de plano sem grupo.

| ID | Descrição |
| :--- | :--- |
| C05-CT05 | Verificar se o sistema valida o campo "Grupo" antes de salvar o plano. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que abrimos o formulário "Novo Plano" |
| **E** informamos apenas o nome "Plano Teste Ville" |
| **QUANDO** clicarmos no botão "Salvar Plano" |
| **ENTÃO** o sistema deverá informar que o campo "Grupo" é obrigatório |

| **Critérios de aceitação** |
| :--- |
| O sistema deve validar o grupo e exibir uma mensagem clara, sem erro interno. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 06: Cadastro de plano com quantidade de parcelas negativa.

| ID | Descrição |
| :--- | :--- |
| C05-CT06 | Verificar se o sistema impede o cadastro de plano com quantidade de parcelas negativa. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que abrimos o formulário "Novo Plano" |
| **E** informamos o nome "Plano Teste Ville Negativo" e um grupo |
| **E** informamos "-3" no campo "Parcelas" |
| **QUANDO** clicarmos no botão "Salvar Plano" |
| **ENTÃO** o sistema deverá informar que a quantidade de parcelas é inválida |

| **Critérios de aceitação** |
| :--- |
| O sistema deve aceitar somente quantidade de parcelas maior que zero. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 07: Cadastro de plano com dados válidos.

| ID | Descrição |
| :--- | :--- |
| C05-CT07 | Verificar se o plano é cadastrado ao informar todos os dados corretamente. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que abrimos o formulário "Novo Plano" |
| **E** informamos o nome "Plano Teste Ville", o grupo "Treino Livre" e a cobrança "Mensalidade recorrente" |
| **E** informamos 1 parcela, valor mensal de R$ 99,90 e valor de matrícula de R$ 10,00 |
| **QUANDO** clicarmos no botão "Salvar Plano" |
| **ENTÃO** o plano deverá constar na listagem com status "ATIVO" e valor R$ 99,90 |

| **Critérios de aceitação** |
| :--- |
| O sistema deve cadastrar o plano e exibi-lo na listagem. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 08: Alteração dos dados do plano.

| ID | Descrição |
| :--- | :--- |
| C05-CT08 | Verificar se as alterações nos dados do plano são salvas corretamente. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir plano cadastrado. |

| **Passos** |
| :--- |
| **DADO** que estamos visualizando o plano "Plano Teste Ville" |
| **E** alteramos o nome para "Plano Teste Ville Editado" e o valor mensal para R$ 89,90 |
| **QUANDO** clicarmos no botão "Salvar Plano" |
| **ENTÃO** a listagem deverá exibir o nome e o valor atualizados |

| **Critérios de aceitação** |
| :--- |
| O sistema deve salvar as alterações e exibi-las na listagem. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 09: Inativação do plano.

| ID | Descrição |
| :--- | :--- |
| C05-CT09 | Verificar se o plano é inativado ao alterar o seu status para "Inativo". |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir plano ativo. |

| **Passos** |
| :--- |
| **DADO** que estamos visualizando o plano "Plano Teste Ville Editado" |
| **E** selecionamos "Inativo" no campo "Status" |
| **QUANDO** clicarmos no botão "Salvar Plano" |
| **ENTÃO** o plano deverá constar com status "INATIVO" na listagem |

| **Critérios de aceitação** |
| :--- |
| O sistema deve atualizar o status do plano para inativo. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 10: Plano inativo indisponível para matrícula.

| ID | Descrição |
| :--- | :--- |
| C05-CT10 | Verificar se planos inativos não são exibidos como opção no cadastro de matrícula. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existirem planos inativos (ex.: "AVA" e "Teste Final"). |

| **Passos** |
| :--- |
| **DADO** que existem planos com status "INATIVO" |
| **QUANDO** acessarmos a tela "Cadastrar Matrícula" e abrirmos o campo "Modalidade" |
| **ENTÃO** somente os planos ativos deverão ser exibidos |

| **Critérios de aceitação** |
| :--- |
| O sistema não deve permitir matricular clientes em planos inativos. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 11: Exclusão de plano.

| ID | Descrição |
| :--- | :--- |
| C05-CT11 | Verificar se o plano é excluído ao confirmar a exclusão. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir plano sem alunos matriculados. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de planos |
| **E** clicamos no botão "Deletar" (X) do plano "Plano Teste Ville Negativo" |
| **QUANDO** confirmarmos a mensagem "Deseja deletar o Plano?" |
| **ENTÃO** o plano não deverá mais constar na listagem |

| **Critérios de aceitação** |
| :--- |
| O sistema deve solicitar confirmação e excluir o plano. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |
