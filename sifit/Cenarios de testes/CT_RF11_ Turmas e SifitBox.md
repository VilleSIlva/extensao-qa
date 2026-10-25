## Cenário 11: Turmas e SifitBox na plataforma SIFIT.

### Caso de Teste 01: Acesso à listagem de turmas.

| ID | Descrição |
| :--- | :--- |
| C11-CT01 | Verificar se a tela de turmas é exibida com os filtros, os indicadores e a listagem. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos autenticados no SIFIT |
| **QUANDO** acessarmos o menu "Turmas" |
| **ENTÃO** a tela deverá exibir os filtros, os indicadores (Turmas cadastradas, Turmas ativas, Com personal e Aula experimental) e a listagem de turmas |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir a tela de turmas com todos os seus componentes carregados. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 02: Busca de turma pelo nome.

| ID | Descrição |
| :--- | :--- |
| C11-CT02 | Verificar se a busca pelo nome retorna as turmas correspondentes. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir turma cadastrada com o nome pesquisado. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de turmas |
| **E** informamos "teste" no campo "Nome" |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** a listagem deverá exibir somente as turmas que contêm "Teste" no nome |

| **Critérios de aceitação** |
| :--- |
| O sistema deve filtrar a listagem pelo nome informado, sem diferenciar letras maiúsculas e minúsculas. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 03: Busca de turma inexistente.

| ID | Descrição |
| :--- | :--- |
| C11-CT03 | Verificar se o sistema informa que nenhuma turma foi encontrada. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de turmas |
| **E** informamos "999" no campo "Código" |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** o sistema deverá apresentar a mensagem "Nenhuma turma encontrada" |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir uma mensagem informativa quando a busca não retornar resultados. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 04: Limpar filtros.

| ID | Descrição |
| :--- | :--- |
| C11-CT04 | Verificar se o botão "Limpar filtros" remove os filtros aplicados. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que pesquisamos "teste" no campo "Nome" |
| **QUANDO** clicarmos no botão "Limpar filtros" |
| **ENTÃO** o campo "Nome" deverá ser limpo e todas as turmas deverão ser exibidas |

| **Critérios de aceitação** |
| :--- |
| O sistema deve remover os filtros e exibir a listagem completa. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 05: Cadastro de turma sem nome.

| ID | Descrição |
| :--- | :--- |
| C11-CT05 | Verificar se o sistema impede o cadastro da turma sem nome. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que abrimos a janela "Cadastrar Turma" |
| **E** mantemos o campo "Nome" vazio |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** o sistema deverá apresentar o aviso "Informe o nome da turma." |

| **Critérios de aceitação** |
| :--- |
| O sistema deve impedir o cadastro até que o nome seja informado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 06: Cadastro de turma sem plano.

| ID | Descrição |
| :--- | :--- |
| C11-CT06 | Verificar se o sistema impede o cadastro da turma sem plano. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que abrimos a janela "Cadastrar Turma" |
| **E** informamos apenas o nome "Turma Teste Ville" |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** o sistema deverá apresentar o aviso "Selecione um plano." |

| **Critérios de aceitação** |
| :--- |
| O sistema deve impedir o cadastro até que um plano seja selecionado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 07: Cadastro de turma sem dias da semana.

| ID | Descrição |
| :--- | :--- |
| C11-CT07 | Verificar se o sistema impede o cadastro da turma sem dias de aula. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que abrimos a janela "Cadastrar Turma" |
| **E** informamos o nome "Turma Teste Ville" e o plano "Treino Livre" |
| **E** não selecionamos nenhum dia da semana |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** o sistema deverá apresentar o aviso "Selecione ao menos um dia da semana." |

| **Critérios de aceitação** |
| :--- |
| O sistema deve impedir o cadastro até que ao menos um dia seja selecionado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 08: Cadastro de turma com dados válidos.

| ID | Descrição |
| :--- | :--- |
| C11-CT08 | Verificar se a turma é cadastrada ao informar os dados corretamente. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que abrimos a janela "Cadastrar Turma" |
| **E** informamos o nome "Turma Teste Ville", o plano "Treino Livre", o horário das 18:00 às 19:00 e os dias Seg, Qua e Sex |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** a turma deverá constar na listagem com status "ATIVO" |

| **Critérios de aceitação** |
| :--- |
| O sistema deve cadastrar a turma e exibi-la na listagem. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 09: Cadastro de turma com hora final anterior à inicial.

| ID | Descrição |
| :--- | :--- |
| C11-CT09 | Verificar se o sistema impede o cadastro de turma com horário inválido. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que abrimos a janela "Cadastrar Turma" |
| **E** informamos o nome "Turma Teste Ville Horario", o plano "Treino Livre" e o dia Seg |
| **E** informamos a hora inicial 11:00 e a hora final 10:00 |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** o sistema deverá informar que a hora final deve ser maior que a hora inicial |

| **Critérios de aceitação** |
| :--- |
| O sistema deve validar o horário da turma. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 10: Alteração de turma.

| ID | Descrição |
| :--- | :--- |
| C11-CT10 | Verificar se as alterações de uma turma são salvas. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir turma cadastrada. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de turmas |
| **E** clicamos no botão "Editar" da turma "Turma do Ville" |
| **QUANDO** clicarmos no botão "Salvar" |
| **ENTÃO** o sistema deverá salvar a turma e exibir mensagem de sucesso |

| **Critérios de aceitação** |
| :--- |
| O sistema deve salvar as alterações da turma. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 11: Exclusão de turma.

| ID | Descrição |
| :--- | :--- |
| C11-CT11 | Verificar se a turma é excluída ao confirmar a exclusão. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir turma de teste cadastrada. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de turmas |
| **E** clicamos no botão "Deletar" da turma "Turma Teste Ville" |
| **QUANDO** confirmarmos a mensagem "Deseja deletar esta turma?" |
| **ENTÃO** a turma não deverá mais constar na listagem |

| **Critérios de aceitação** |
| :--- |
| O sistema deve solicitar confirmação e excluir a turma. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 12: Acesso às aulas do SifitBox.

| ID | Descrição |
| :--- | :--- |
| C11-CT12 | Verificar se a tela de aulas do SifitBox é exibida com o período e as ações. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos autenticados no SIFIT |
| **QUANDO** acessarmos o menu "SifitBox" |
| **ENTÃO** a tela deverá exibir o período, os botões "Buscar" e "Gerar aulas" e as aulas do período ou a mensagem "Nenhuma aula encontrada no periodo." |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir a tela de aulas do SifitBox. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 13: Geração de aulas do SifitBox.

| ID | Descrição |
| :--- | :--- |
| C11-CT13 | Verificar se o sistema informa o resultado da geração de aulas. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de aulas do SifitBox |
| **QUANDO** clicarmos no botão "Gerar aulas" |
| **ENTÃO** o sistema deverá informar quantas aulas foram geradas no período |

| **Critérios de aceitação** |
| :--- |
| O sistema deve informar ao usuário o resultado da geração de aulas. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |
