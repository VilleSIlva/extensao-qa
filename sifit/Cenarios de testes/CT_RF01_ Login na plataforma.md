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
| [Vídeo](https://jam.dev/c/02a61d44-1616-4bb4-9a18-60c2053eade0)      |

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
