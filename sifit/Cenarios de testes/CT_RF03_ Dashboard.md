## Cenário 03: Acesso e visualização do Dashboard.

### Caso de Teste 01: Acesso ao Dashboard.

| ID | Descrição |
| :--- | :--- |
| C03-CT01 | Verificar se a tela do Dashboard é aberta com o título e a navegação corretos. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos autenticados no SIFIT |
| **QUANDO** clicarmos no menu "Dashboard" |
| **ENTÃO** a tela deverá exibir o título "Dashboard" e a navegação "Início > Dashboard" |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir o Dashboard com título e navegação correspondentes à tela. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 02: Legibilidade dos gráficos do Dashboard.

| ID | Descrição |
| :--- | :--- |
| C03-CT02 | Verificar se os títulos das seções e dos gráficos do Dashboard estão legíveis. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela do Dashboard no modo claro |
| **QUANDO** observarmos as seções "Clientes", "Matrículas", "Contas a Receber", "Cancelamentos" e "Avaliações" |
| **ENTÃO** os títulos das seções e dos gráficos (ex.: "FREQUÊNCIA", "POR MÊS") deverão estar visíveis e legíveis |

| **Critérios de aceitação** |
| :--- |
| Os títulos devem ter contraste suficiente em relação ao fundo. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 03: Indicador de alunos em risco do Dashboard.

| ID | Descrição |
| :--- | :--- |
| C03-CT03 | Verificar se o indicador "Alunos em risco" do Dashboard é coerente com a Página Inicial. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e a Página Inicial deve indicar alunos em risco de evasão. |

| **Passos** |
| :--- |
| **DADO** que a Página Inicial exibe "3 alunos em risco de evasão" |
| **QUANDO** acessarmos a tela do Dashboard |
| **ENTÃO** o indicador "Alunos em risco" do bloco "Inteligência Sifit" deverá exibir a mesma quantidade |

| **Critérios de aceitação** |
| :--- |
| Os indicadores de risco devem ser iguais em todas as telas. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 04: Acesso à Inteligência pelo Dashboard.

| ID | Descrição |
| :--- | :--- |
| C03-CT04 | Verificar se o botão "Ver Inteligência" direciona para os resultados da Inteligência Sifit. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela do Dashboard |
| **QUANDO** clicarmos no botão "Ver Inteligência" |
| **ENTÃO** deveremos ser direcionados à tela de resultados da Inteligência Sifit |

| **Critérios de aceitação** |
| :--- |
| O botão deve direcionar para a tela correta. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |
