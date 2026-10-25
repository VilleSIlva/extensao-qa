## Cenário 02: Acesso e visualização da Página Inicial.

### Caso de Teste 01: Acesso à Página Inicial.

| ID | Descrição |
| :--- | :--- |
| C02-CT01 | Verificar se a Página Inicial é exibida após o login com a saudação, a data e os indicadores. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que realizamos o login no SIFIT |
| **QUANDO** formos direcionados à Página Inicial |
| **ENTÃO** deverão ser exibidos a saudação ao usuário, a data atual e os indicadores da academia |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir a Página Inicial com todos os seus componentes carregados. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 02: Radar de evasão.

| ID | Descrição |
| :--- | :--- |
| C02-CT02 | Verificar se a quantidade de alunos em risco é a mesma no card, no "Radar de Evasão" e no bloco "Inteligência de Retenção". |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na Página Inicial |
| **E** observamos o card "alunos em risco de evasão" e o bloco "Inteligência de Retenção" |
| **QUANDO** clicarmos em "Ver detalhes" do card de risco |
| **ENTÃO** a quantidade de alunos em risco deverá ser a mesma no card, no "Radar de Evasão" e no bloco de retenção |

| **Critérios de aceitação** |
| :--- |
| Os indicadores de risco de evasão devem ser coerentes entre si. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 03: Clientes ausentes.

| ID | Descrição |
| :--- | :--- |
| C02-CT03 | Verificar se a quantidade de clientes ausentes da Página Inicial é coerente com a tela de Clientes. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na Página Inicial |
| **E** observamos o card "Clientes Ausentes" |
| **QUANDO** acessarmos a tela de Clientes |
| **ENTÃO** o indicador "Ausentes" deverá exibir a mesma quantidade |

| **Critérios de aceitação** |
| :--- |
| A quantidade de clientes ausentes deve ser igual nas duas telas. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 04: Clientes sem matrícula.

| ID | Descrição |
| :--- | :--- |
| C02-CT04 | Verificar se o card "Sem Matrículas" exibe a lista de clientes sem matrícula ativa. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na Página Inicial |
| **QUANDO** clicarmos no card "Sem Matrículas" |
| **ENTÃO** deverá ser exibida a lista de clientes sem matrícula ativa, com a mesma quantidade do card |

| **Critérios de aceitação** |
| :--- |
| A lista deve apresentar a mesma quantidade informada no card. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 05: Desistências no período.

| ID | Descrição |
| :--- | :--- |
| C02-CT05 | Verificar se o card "Desistências no Período" lista as matrículas canceladas. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existirem matrículas canceladas no período. |

| **Passos** |
| :--- |
| **DADO** que estamos na Página Inicial e o card "Desistências no Período" exibe 3 |
| **QUANDO** clicarmos no card "Desistências no Período" |
| **ENTÃO** deverão ser listadas as 3 desistências, com código, nome, data e motivo |

| **Critérios de aceitação** |
| :--- |
| A lista de desistências deve corresponder ao total informado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 06: Financeiro em aberto.

| ID | Descrição |
| :--- | :--- |
| C02-CT06 | Verificar se o detalhe do valor em aberto exibe as mensalidades pendentes. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existirem mensalidades pendentes. |

| **Passos** |
| :--- |
| **DADO** que estamos na Página Inicial |
| **QUANDO** clicarmos em "Ver detalhes" do card "em aberto" |
| **ENTÃO** deverá ser exibida a janela "Financeiro em Aberto" com as mensalidades pendentes |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir o detalhamento das mensalidades em aberto. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 07: Ação "Cobrar agora".

| ID | Descrição |
| :--- | :--- |
| C02-CT07 | Verificar se o botão "Cobrar agora" das ações recomendadas inicia a cobrança dos alunos com pagamento em aberto. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir aluno com pagamento em aberto. |

| **Passos** |
| :--- |
| **DADO** que estamos na Página Inicial |
| **E** a ação recomendada exibe "Cobrar 1 alunos com pagamento em aberto" |
| **QUANDO** clicarmos no botão "Cobrar agora" |
| **ENTÃO** o sistema deverá exibir a lista de alunos a cobrar ou as opções de cobrança |

| **Critérios de aceitação** |
| :--- |
| O botão deve executar uma ação visível ao usuário. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 08: Links de navegação da Página Inicial.

| ID | Descrição |
| :--- | :--- |
| C02-CT08 | Verificar se os links da Página Inicial direcionam para as telas corretas. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na Página Inicial |
| **QUANDO** clicarmos em "Ver avaliações", "Ver análise completa" e "Ver todos" (Últimas entradas) |
| **ENTÃO** deveremos ser direcionados, respectivamente, às telas de Avaliações pendentes, Inteligência & Automação e Presenças |

| **Critérios de aceitação** |
| :--- |
| Cada link deve direcionar para a tela correspondente. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |
