## Cenário 09: Check-in e presenças na plataforma SIFIT.

### Caso de Teste 01: Acesso à tela de check-in.

| ID | Descrição |
| :--- | :--- |
| C09-CT01 | Verificar se a tela de check-in é exibida com os indicadores, a listagem, a entrada rápida e o check-in manual. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos autenticados no SIFIT |
| **QUANDO** acessarmos o menu "Check-in" |
| **ENTÃO** a tela deverá exibir os indicadores do dia, a listagem de check-ins, a "Entrada rápida" e o botão "Check-in manual" |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir a tela de check-in com todos os seus componentes carregados. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 02: Check-in manual sem cliente selecionado.

| ID | Descrição |
| :--- | :--- |
| C09-CT02 | Verificar se o sistema impede o registro de entrada manual sem cliente selecionado. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que abrimos a janela "Check-in manual" |
| **E** não pesquisamos nenhum cliente |
| **QUANDO** tentarmos clicar no botão "Registrar entrada" |
| **ENTÃO** o botão deverá estar desabilitado |

| **Critérios de aceitação** |
| :--- |
| O sistema não deve permitir registrar entrada sem um cliente selecionado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 03: Check-in manual de cliente com matrícula ativa.

| ID | Descrição |
| :--- | :--- |
| C09-CT03 | Verificar se o check-in manual é registrado com mensagem de confirmação e horário correto. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir cliente com matrícula ativa (ex.: Jerome Lionel). |

| **Passos** |
| :--- |
| **DADO** que abrimos a janela "Check-in manual" |
| **E** pesquisamos e selecionamos o cliente "Jerome Lionel" |
| **QUANDO** clicarmos no botão "Registrar entrada" |
| **ENTÃO** o sistema deverá exibir mensagem de sucesso e o check-in deverá constar na listagem com o horário atual |

| **Critérios de aceitação** |
| :--- |
| O sistema deve registrar o check-in, confirmar a operação e exibir o horário local correto. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 04: Check-in de cliente sem matrícula ativa.

| ID | Descrição |
| :--- | :--- |
| C09-CT04 | Verificar se o sistema impede o check-in de cliente que não possui matrícula ativa. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existir cliente sem matrícula ativa (ex.: Lila). |

| **Passos** |
| :--- |
| **DADO** que abrimos a janela "Check-in manual" |
| **E** pesquisamos e selecionamos a cliente "Lila", que não possui matrícula ativa |
| **QUANDO** observarmos a situação exibida e clicarmos em "Registrar entrada" |
| **ENTÃO** o sistema deverá informar que a cliente não possui matrícula ativa e bloquear o check-in |

| **Critérios de aceitação** |
| :--- |
| O sistema deve liberar o check-in somente para clientes com matrícula ativa. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 05: Entrada rápida com código inexistente.

| ID | Descrição |
| :--- | :--- |
| C09-CT05 | Verificar se o sistema informa quando o código informado na entrada rápida não pertence a nenhum cliente. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de check-in |
| **E** informamos "99999" no campo "Código do cliente" da "Entrada rápida" |
| **QUANDO** clicarmos no botão "Realizar check-in" |
| **ENTÃO** o sistema deverá apresentar a mensagem "Cliente nao encontrado para esta empresa." |

| **Critérios de aceitação** |
| :--- |
| O sistema deve informar que o cliente não foi encontrado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 06: Entrada rápida sem código.

| ID | Descrição |
| :--- | :--- |
| C09-CT06 | Verificar se o sistema orienta o usuário quando a entrada rápida é acionada sem código. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de check-in |
| **E** mantemos o campo "Código do cliente" vazio |
| **QUANDO** clicarmos no botão "Realizar check-in" |
| **ENTÃO** o sistema deverá solicitar o preenchimento do código do cliente |

| **Critérios de aceitação** |
| :--- |
| O sistema deve exibir uma mensagem orientando o preenchimento do código. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 07: Status do check-in e indicador "Presentes agora".

| ID | Descrição |
| :--- | :--- |
| C09-CT07 | Verificar se, após o check-in, o cliente passa a constar como presente. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e ter realizado o check-in de um cliente. |

| **Passos** |
| :--- |
| **DADO** que realizamos o check-in do cliente "Jerome Lionel" |
| **QUANDO** observarmos a listagem e o indicador "Presentes agora" |
| **ENTÃO** o status do cliente deverá ser "Presente" e o indicador "Presentes agora" deverá exibir 1 |

| **Critérios de aceitação** |
| :--- |
| O sistema deve atualizar o status do check-in e a quantidade de presentes. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 08: Check-in duplicado.

| ID | Descrição |
| :--- | :--- |
| C09-CT08 | Verificar se o sistema informa quando o cliente já possui check-in aberto. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e o cliente deve possuir check-in aberto. |

| **Passos** |
| :--- |
| **DADO** que o cliente "Jerome Lionel" já possui check-in aberto |
| **QUANDO** clicarmos no botão "Registrar entrada" da linha do cliente na listagem |
| **ENTÃO** o sistema deverá informar que o cliente já possui check-in aberto |

| **Critérios de aceitação** |
| :--- |
| O sistema deve impedir o check-in duplicado e informar o motivo ao usuário. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 09: Indicadores da tela de check-in.

| ID | Descrição |
| :--- | :--- |
| C09-CT09 | Verificar se os indicadores refletem os check-ins realizados. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado, existirem 4 clientes ativos e 1 check-in no dia. |

| **Passos** |
| :--- |
| **DADO** que existe 1 check-in no dia e 4 clientes ativos |
| **QUANDO** observarmos os indicadores "Check-ins hoje" e "Taxa de frequência" |
| **ENTÃO** a comparação com o dia anterior e a taxa de frequência (25%) deverão ser calculadas a partir dos check-ins realizados |

| **Critérios de aceitação** |
| :--- |
| Os indicadores devem ser calculados com base nos dados reais. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 10: Exibição dos check-ins na tela de Presenças.

| ID | Descrição |
| :--- | :--- |
| C09-CT10 | Verificar se os check-ins realizados no dia são exibidos na tela de Presenças. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado e existirem check-ins realizados no dia. |

| **Passos** |
| :--- |
| **DADO** que realizamos 3 check-ins no dia |
| **E** acessamos o menu "Presenças" |
| **QUANDO** clicarmos no atalho "Hoje" |
| **ENTÃO** o "Total no período" deverá ser 3 e as presenças deverão ser listadas |

| **Critérios de aceitação** |
| :--- |
| A tela de Presenças deve exibir todos os check-ins realizados. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |

---

### Caso de Teste 11: Atalhos de período da tela de Presenças.

| ID | Descrição |
| :--- | :--- |
| C09-CT11 | Verificar se os atalhos "Hoje", "Esta semana" e "Este mês" ajustam o período da busca. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de Presenças |
| **QUANDO** clicarmos nos atalhos "Hoje", "Esta semana" e "Este mês" |
| **ENTÃO** as datas e o indicador "Dias no período" deverão ser atualizados conforme o atalho |

| **Critérios de aceitação** |
| :--- |
| Cada atalho deve aplicar o período correspondente. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo]()      |
