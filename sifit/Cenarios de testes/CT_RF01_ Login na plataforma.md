## Cenário 01: Autenticação de usuário na plataforma SIFIT.

### Caso de Teste 01: Login realizado com credenciais válidas.

| ID | Descrição |
| :--- | :--- |
| C01-CT01 | Verificar se o acesso à plataforma é permitido ao informar um usuário e uma senha válidos. |

| **Pré-condições** |
| :--- |
| O usuário deve possuir credenciais válidas e estar cadastrado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que acessamos a página de login do SIFIT |
| **E** informamos um nome de usuário válido no campo correspondente |
| **E** digitamos a senha correta no campo de senha |
| **QUANDO** acionarmos o botão "Entrar" |
| **ENTÃO** deveremos ser direcionados à página principal do sistema |

| **Critérios de aceitação** |
| :--- |
| O sistema deve autenticar o usuário e apresentar a página principal corretamente. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/636f8f34-e2d1-432d-a7b0-dead44c3b654)      |

---

### Caso de Teste 02: Tentativa de acesso com senha incorreta.

| ID | Descrição |
| :--- | :--- |
| C01-CT02 | Verificar se o sistema impede o acesso quando uma senha incorreta é informada. |

| **Pré-condições** |
| :--- |
| Deve existir um usuário cadastrado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de autenticação do SIFIT |
| **E** inserimos um nome de usuário cadastrado |
| **E** informamos uma senha incorreta |
| **QUANDO** clicarmos no botão "Entrar" |
| **ENTÃO** o sistema deverá apresentar uma mensagem informando que as credenciais são inválidas |

| **Critérios de aceitação** |
| :--- |
| O sistema deve negar o acesso e exibir uma mensagem de erro indicando que os dados informados são inválidos. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/52fc8c29-5fb9-4cfb-b930-d0b60ff19640)      |

---

### Caso de Teste 03: Tentativa de acesso com campos obrigatórios vazios.

| ID | Descrição |
| :--- | :--- |
| C01-CT03 | Verificar se o sistema impede a autenticação quando os campos obrigatórios não são preenchidos. |

| **Pré-condições** |
| :--- |
| Nenhuma. |

| **Passos** |
| :--- |
| **DADO** que acessamos a página de login do SIFIT |
| **E** mantemos os campos de usuário e senha vazios |
| **QUANDO** pressionarmos o botão "Entrar" |
| **ENTÃO** o sistema deverá apresentar mensagens de erro |

| **Critérios de aceitação** |
| :--- |
| Deve exibir uma mensagem de erro, impedindo o envio do formulário até que os dados necessários sejam informados. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/3ebcc976-9012-471d-a577-6177221fd267)      |

---

### Caso de Teste 04: Login com espaços extras nas credenciais válidas.

| ID | Descrição |
| :--- | :--- |
| C01-CT04 | Verificar se o acesso é permitido quando usuário e senha válidos são informados com espaços no início ou no fim dos campos. |

| **Pré-condições** |
| :--- |
| O usuário deve possuir credenciais válidas e não haver sessão ativa. |

| **Passos** |
| :--- |
| **DADO** que acessamos a página de login do SIFIT |
| **E** informamos um nome de usuário válido com espaços no início ou no fim |
| **E** digitamos a senha correta com espaços no início ou no fim |
| **QUANDO** acionarmos o botão "Entrar" |
| **ENTÃO** deveremos ser direcionados à página principal do sistema |

| **Critérios de aceitação** |
| :--- |
| Espaços apenas nas pontas dos campos não devem impedir o login de credenciais válidas. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/51531b19-254b-468b-ad89-7487194fc22a)      |

---

### Caso de Teste 05: Persistência da sessão com "Manter conectado".

| ID | Descrição |
| :--- | :--- |
| C01-CT05 | Verificar se a sessão permanece ativa ao retornar ao SIFIT quando a opção "Manter conectado" é marcada. |

| **Pré-condições** |
| :--- |
| O usuário deve possuir credenciais válidas. |

| **Passos** |
| :--- |
| **DADO** que acessamos a página de login do SIFIT |
| **E** informamos usuário e senha válidos |
| **E** marcamos a opção "Manter conectado" |
| **QUANDO** acionarmos o botão "Entrar" e abrirmos o SIFIT novamente |
| **ENTÃO** a sessão deverá continuar ativa, sem solicitar as credenciais outra vez |

| **Critérios de aceitação** |
| :--- |
| Ao retornar ao sistema, o usuário deve continuar autenticado. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/0e862f82-e4d0-49df-9406-0ff970332873)      |

---

### Caso de Teste 06: Acesso ao Dashboard sem sessão válida.

| ID | Descrição |
| :--- | :--- |
| C01-CT06 | Verificar se o sistema impede o acesso direto ao endereço /dashboard quando não há sessão válida. |

| **Pré-condições** |
| :--- |
| Não deve haver sessão ativa no navegador. |

| **Passos** |
| :--- |
| **DADO** que estamos na tela de login, sem sessão válida |
| **QUANDO** informarmos o endereço /dashboard na barra de endereços |
| **ENTÃO** o sistema deverá retornar à tela de login sem exibir o Dashboard |

| **Critérios de aceitação** |
| :--- |
| A área autenticada não deve ser exibida pelo endereço direto quando não há sessão válida. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/0e862f82-e4d0-49df-9406-0ff970332873)      |

---

### Caso de Teste 07: Acesso à recuperação de senha.

| ID | Descrição |
| :--- | :--- |
| C01-CT07 | Verificar se o link "Esqueci minha senha" inicia o fluxo de recuperação de senha. |

| **Pré-condições** |
| :--- |
| Nenhuma. |

| **Passos** |
| :--- |
| **DADO** que acessamos a página de login do SIFIT |
| **QUANDO** clicarmos no link "Esqueci minha senha" |
| **ENTÃO** o sistema deverá abrir a tela de recuperação de senha |

| **Critérios de aceitação** |
| :--- |
| O sistema deve direcionar o usuário ao fluxo de recuperação de senha. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/c647a93a-812e-418f-8f05-d080e188b70f)      |

---

### Caso de Teste 08: Tentativa de acesso com usuário inexistente.

| ID | Descrição |
| :--- | :--- |
| C01-CT08 | Verificar se o sistema impede o acesso quando é informado um usuário não cadastrado. |

| **Pré-condições** |
| :--- |
| Nenhuma. |

| **Passos** |
| :--- |
| **DADO** que acessamos a página de login do SIFIT |
| **E** informamos o usuário "usuario_inexistente_qa" |
| **E** informamos a senha "senhaerrada" |
| **QUANDO** clicarmos no botão "Entrar" |
| **ENTÃO** o sistema deverá apresentar uma mensagem informando que as credenciais são inválidas |

| **Critérios de aceitação** |
| :--- |
| O sistema deve negar o acesso, exibir a mensagem de erro e manter o usuário na tela de login. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/461b0484-4a78-4535-81d5-c3542770ff27)      |

---

### Caso de Teste 09: Logout e acesso a tela interna.

| ID | Descrição |
| :--- | :--- |
| C01-CT09 | Verificar se, após sair do sistema, as telas internas deixam de ser acessíveis. |

| **Pré-condições** |
| :--- |
| O usuário deve estar autenticado na plataforma SIFIT. |

| **Passos** |
| :--- |
| **DADO** que estamos autenticados no SIFIT |
| **E** abrimos o menu do usuário e clicamos em "Sair do sistema" |
| **QUANDO** acessarmos diretamente o endereço /clientes |
| **ENTÃO** deveremos ser direcionados à tela de login |

| **Critérios de aceitação** |
| :--- |
| A sessão deve ser encerrada e as telas internas devem exigir novo login. |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/06bd8930-85a1-4de6-8889-eb73d57b799d)      |
