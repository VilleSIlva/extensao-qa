## Cenário 17: Gestão de produtos na plataforma SIFIT.

### Caso de Teste 01: Acesso à listagem de produtos.

| ID | Descrição |
| :--- | :--- |
| C17-CT01 | Verificar se a tela de produtos é exibida com os filtros, os indicadores e a listagem. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos autenticados no SIFIT |
| **QUANDO** acessarmos o menu "Produtos" |
| **ENTÃO** a tela deverá exibir os filtros (Código, Nome, Status e Tipo), os indicadores e a listagem de produtos |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir a tela de produtos com todos os seus componentes carregados. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 02: Busca de produto pelo nome.

| ID | Descrição |
| :--- | :--- |
| C17-CT02 | Verificar se a busca pelo nome retorna os produtos correspondentes. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existirem produtos cadastrados. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de produtos |
| **E** informamos "gamer" no campo "Nome do produto" |
| **QUANDO** clicarmos no botão de busca |
| **ENTÃO** a listagem deverá exibir somente o produto "Notebook Gamer" |

| **Critérios de aceitação** |
| :--- |
| O sistema deve filtrar os produtos pelo nome, sem diferenciar letras maiúsculas e minúsculas. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 03: Busca de produto inexistente.

| ID | Descrição |
| :--- | :--- |
| C17-CT03 | Verificar se o sistema informa que nenhum produto foi encontrado. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de produtos |
| **E** informamos um nome inexistente no campo "Nome do produto" |
| **QUANDO** clicarmos no botão de busca |
| **ENTÃO** o sistema deverá apresentar a mensagem "Nenhum produto encontrado." |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir uma mensagem informativa quando a busca não retornar resultados. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 04: Cadastro de produto com campos vazios.

| ID | Descrição |
| :--- | :--- |
| C17-CT04 | Verificar se o sistema orienta o preenchimento dos campos obrigatórios. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que abrimos a janela "Novo" produto |
| **E** mantemos os campos vazios |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** o sistema deverá informar que nome e preço são obrigatórios |

| **Critérios de aceitação** |
| :--- |
| O sistema deve validar os campos obrigatórios antes de enviar o cadastro. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 05: Cadastro de produto com preço negativo.

| ID | Descrição |
| :--- | :--- |
| C17-CT05 | Verificar se o sistema impede o cadastro de produto com preço negativo. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que abrimos a janela "Novo" produto |
| **E** informamos o nome "Produto Teste Ville Negativo" e o preço "-50" |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** o sistema deverá informar que o preço deve ser maior que zero |

| **Critérios de aceitação** |
| :--- |
| O sistema deve aceitar somente preços positivos. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 06: Cadastro de produto para venda.

| ID | Descrição |
| :--- | :--- |
| C17-CT06 | Verificar se o produto do tipo "Venda" é cadastrado e os indicadores são atualizados. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que abrimos a janela "Novo" produto |
| **E** informamos o nome "Produto Teste Ville", a descrição "Teste Ville Nunes", o tipo "Venda" e o preço |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** o produto deverá constar na listagem e os indicadores "Total de produtos", "Ativos" e "Para venda" deverão aumentar em 1 |

| **Critérios de aceitação** |
| :--- |
| O sistema deve cadastrar o produto e atualizar os indicadores. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 07: Cadastro de produto do tipo Pontuação.

| ID | Descrição |
| :--- | :--- |
| C17-CT07 | Verificar se o produto do tipo "Pontuação" é cadastrado com a quantidade de pontos. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que abrimos a janela "Novo" produto |
| **E** informamos o nome "Produto Teste Ville Pontos" e selecionamos o tipo "Pontuação" |
| **E** informamos 100 no campo "Pontuação" |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** o produto deverá constar na listagem com o tipo "Pontuação" e 100 pontos |

| **Critérios de aceitação** |
| :--- |
| O sistema deve cadastrar produtos de troca por pontos. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 08: Exibição do valor dos produtos.

| ID | Descrição |
| :--- | :--- |
| C17-CT08 | Verificar se os valores dos produtos são exibidos no formato monetário brasileiro. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existirem produtos cadastrados. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de produtos |
| **QUANDO** observarmos a coluna "Valor / Pontos" dos produtos "Notebook" e "Notebook Gamer" |
| **ENTÃO** os valores deverão ser exibidos como "R$ 1.550,00" e "R$ 7.000,99" |

| **Critérios de aceitação** |
| :--- |
| Os valores devem ser exibidos com separador de milhar e duas casas decimais. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 09: Alteração de produto.

| ID | Descrição |
| :--- | :--- |
| C17-CT09 | Verificar se os dados do produto podem ser alterados. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir o produto "Produto Teste Ville". |

| **Passos** |
| :--- |
| **DADO** que clicamos em "Visualizar" do produto "Produto Teste Ville" |
| **E** alteramos o nome para "Produto Teste Ville Editado" e o preço |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** a listagem deverá exibir o nome e o preço atualizados |

| **Critérios de aceitação** |
| :--- |
| O sistema deve salvar as alterações do produto. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 10: Inativação de produto.

| ID | Descrição |
| :--- | :--- |
| C17-CT10 | Verificar se o produto é inativado e os indicadores são atualizados. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir produto de teste ativo. |

| **Passos** |
| :--- |
| **DADO** que clicamos em "Visualizar" do produto de teste |
| **E** selecionamos "Inativo" no campo "Status" |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** o produto deverá constar como "Inativo", o indicador "Inativos" deverá aumentar em 1 e o filtro "Inativo" deverá exibi-lo |

| **Critérios de aceitação** |
| :--- |
| O sistema deve inativar o produto e atualizar os indicadores. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 11: Exclusão de produto.

| ID | Descrição |
| :--- | :--- |
| C17-CT11 | Verificar se o produto é excluído ao confirmar a exclusão. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir produto de teste. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de produtos |
| **E** clicamos no botão "Deletar" do produto de teste |
| **QUANDO** confirmarmos a mensagem "Deseja deletar o produto?" |
| **ENTÃO** o produto não deverá mais constar na listagem |

| **Critérios de aceitação** |
| :--- |
| O sistema deve solicitar confirmação e excluir o produto. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |
