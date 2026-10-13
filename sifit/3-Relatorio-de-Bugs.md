# Relatório de Bugs

**Software:** Sifit

**QA responsável:**  Ville Nunes Figueiredo da Silva

**Data:** 13.10.26

---

### 🐞 **Bug 01: Mensagem de erro incorreta ao tentar realizar login com campos vazios**

| **ID** | **Descrição** |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-001 | Ao clicar no botão "Entrar" na página de login com os campos de nome de usuário e senha vazios, o sistema exibe a mensagem "O nome de usuário e senha não correspondem", a mesma apresentada quando são informadas credenciais inválidas, em vez de indicar que os campos obrigatórios devem ser preenchidos. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| --------------------- | -------------------------- | ---------- |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| -------------------------------------------------------------- |
| 1. Acessar a página de login do SIFIT. |
| 2. Manter os campos de nome de usuário e senha vazios. |
| 3. Clicar no botão "Entrar". |
| 4. Verificar a mensagem de erro exibida pelo sistema. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| O sistema deve informar que os campos de nome de usuário e senha são obrigatórios, orientando o usuário a preenchê-los. | O sistema exibe a mensagem "O nome de usuário e senha não correspondem", utilizada também para tentativas de login com credenciais inválidas. |

| **Ambiente** |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Windows 11. |
| Navegador Google Chrome. |
| Sistema SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| -------------------------- | ------------------------------------------ |
| Login / Autenticação de usuário | C01-CT03: Tentativa de acesso com campos obrigatórios vazios |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/3ebcc976-9012-471d-a577-6177221fd267)  