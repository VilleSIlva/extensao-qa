# ✅ **Relatório Final de Execução de Testes - SIFIT**

**Sistema testado:** SIFIT - Sistema para Academias (ambiente de homologação)
**Responsável:** Ville Nunes Figueiredo da Silva
**Data de execução:** 13/10/2026 a 25/10/2026
**Ambiente:** Homologação

* Sistema operacional: Windows 11 / Linux
* Navegador: Google Chrome 155.0.8059.84
* URL: [https://sifitalfa.centrion.com.br](https://sifitalfa.centrion.com.br)

---

## 📊 **Resumo da Execução**

| Total de Casos de Teste | Casos Passaram | Casos Falharam | Bugs Registrados |
| ----------------------- | -------------- | -------------- | ---------------- |
| 132                     | 72             | 60             | 59               |

---

## 🔍 **Cobertura por Módulo**

| Código RF | Módulo                    | Casos Testados | Casos Passaram | Bugs encontrados | Bug(s) Associado(s)                                |
| --------- | ------------------------- | -------------- | -------------- | ---------------- | -------------------------------------------------- |
| RF01      | Autenticação de Usuário   | 3              | 2              | 1                | BUG-001 |
| RF02      | Página Inicial            | 8              | 4              | 4                | BUG-002, BUG-003, BUG-004, BUG-005 |
| RF03      | Dashboard                 | 4              | 1              | 3                | BUG-002, BUG-006, BUG-007 |
| RF04      | Gestão de Clientes        | 11             | 5              | 7                | BUG-008, BUG-009, BUG-010, BUG-011, BUG-012, BUG-013, BUG-014 |
| RF05      | Gestão de Planos          | 11             | 5              | 6                | BUG-015, BUG-016, BUG-017, BUG-018, BUG-019, BUG-020 |
| RF06      | Gestão de Matrículas      | 12             | 6              | 6                | BUG-021, BUG-022, BUG-023, BUG-024, BUG-025, BUG-026 |
| RF07      | Contas a Receber          | 12             | 7              | 5                | BUG-027, BUG-028, BUG-029, BUG-030, BUG-031 |
| RF08      | Gestão de Fornecedores    | 9              | 6              | 3                | BUG-032, BUG-033, BUG-034 |
| RF09      | Check-in e Presenças      | 11             | 4              | 6                | BUG-035, BUG-036, BUG-037, BUG-038, BUG-039, BUG-040 |
| RF10      | Avaliações                | 11             | 7              | 4                | BUG-041, BUG-042, BUG-043, BUG-044 |
| RF11      | Turmas e SifitBox         | 13             | 10             | 3                | BUG-045, BUG-046, BUG-047 |
| RF12      | Caixas                    | 11             | 5              | 6                | BUG-048, BUG-049, BUG-050, BUG-051, BUG-052, BUG-053 |
| RF13      | Contas a Pagar e Despesas Fixas | 16       | 10             | 6                | BUG-054, BUG-055, BUG-056, BUG-057, BUG-058, BUG-059 |

---

## 🐞 **Resumo dos Bugs Reportados**

| ID      | Título                                                                | Severidade | Status |
| ------- | --------------------------------------------------------------------- | ---------- | ------ |
| BUG-001 | Mensagem de erro incorreta ao tentar realizar login com campos vazios | Média      | Aberto |
| BUG-002 | Quantidade de alunos em risco diverge entre as telas                  | Média      | Aberto |
| BUG-003 | Quantidade de clientes ausentes diverge entre a Página Inicial e a tela de Clientes | Média | Aberto |
| BUG-004 | Lista de desistências vazia, embora o total informe 3 desistências    | Média      | Aberto |
| BUG-005 | Botão "Cobrar agora" não executa nenhuma ação                         | Média      | Aberto |
| BUG-006 | Título e navegação do Dashboard exibem "Despesas Fixas"              | Baixa      | Aberto |
| BUG-007 | Títulos das seções e dos gráficos do Dashboard ilegíveis              | Média      | Aberto |
| BUG-008 | Erro ao cadastrar cliente com dados válidos                           | Crítica    | Aberto |
| BUG-009 | Busca por código não retorna clientes sem matrícula                   | Média      | Aberto |
| BUG-010 | Paginação exibe páginas vazias com filtro aplicado                    | Média      | Aberto |
| BUG-011 | Listagem não respeita a quantidade de registros por página            | Baixa      | Aberto |
| BUG-012 | Ausência de mensagem quando a busca não encontra clientes             | Baixa      | Aberto |
| BUG-013 | Erro ao salvar alterações dos dados do cliente                        | Crítica    | Aberto |
| BUG-014 | Erro no servidor ao acessar cliente excluído                          | Baixa      | Aberto |
| BUG-015 | Coluna "Alunos", ranking e receita estimada dos planos exibem valores zerados | Média | Aberto |
| BUG-016 | Busca por código retorna planos cujo código apenas contém o valor informado | Baixa | Aberto |
| BUG-017 | Erro interno com exposição de SQL ao salvar plano sem grupo           | Média      | Aberto |
| BUG-018 | Sistema permite cadastrar plano com quantidade de parcelas negativa   | Média      | Aberto |
| BUG-019 | Inativação do plano não é salva                                       | Alta       | Aberto |
| BUG-020 | Planos inativos são exibidos no cadastro de matrícula                 | Média      | Aberto |
| BUG-021 | Desconto não é aplicado ao valor total da matrícula                   | Média      | Aberto |
| BUG-022 | Mensagem incorreta ao cadastrar matrícula para cliente com matrícula ativa | Baixa | Aberto |
| BUG-023 | Paginação não permite acessar matrículas além da primeira página      | Média      | Aberto |
| BUG-024 | Erro no servidor ao excluir matrícula, embora a exclusão seja efetivada | Média    | Aberto |
| BUG-025 | Mensagem de validação permanece após selecionar o tipo de pagamento   | Baixa      | Aberto |
| BUG-026 | Ausência de mensagem quando a busca não encontra matrículas           | Baixa      | Aberto |
| BUG-027 | Matrícula cadastrada não gera conta a receber                         | Alta       | Aberto |
| BUG-028 | Indicador "Contas Atrasadas" diverge do filtro de contas vencidas    | Média      | Aberto |
| BUG-029 | Recebimento é registrado sem tipo de pagamento                        | Média      | Aberto |
| BUG-030 | Recebimento aceita valor maior que o valor a receber sem alerta       | Baixa      | Aberto |
| BUG-031 | Ausência de mensagem quando a busca não encontra contas a receber     | Baixa      | Aberto |
| BUG-032 | Busca por código inexistente ou parcial retorna todos os fornecedores | Baixa      | Aberto |
| BUG-033 | Erro ao cadastrar fornecedor com dados válidos                        | Alta       | Aberto |
| BUG-034 | Erro interno com exposição de SQL ao alterar fornecedor               | Alta       | Aberto |
| BUG-035 | Check-ins realizados não aparecem na tela de Presenças                | Alta       | Aberto |
| BUG-036 | Check-in permanece "Pendente" e não há retorno ao registrar entrada novamente | Média | Aberto |
| BUG-037 | Horário de entrada do check-in exibido com 3 horas a mais            | Média      | Aberto |
| BUG-038 | Cliente sem matrícula ativa é liberado para check-in                  | Alta       | Aberto |
| BUG-039 | Ausência de mensagens no check-in manual e na entrada rápida          | Baixa      | Aberto |
| BUG-040 | Indicadores da tela de check-in com valores fixos ou incorretos       | Baixa      | Aberto |
| BUG-041 | Erro ao salvar avaliação realizada                                    | Alta       | Aberto |
| BUG-042 | Alteração de data e hora da avaliação não é salva                     | Média      | Aberto |
| BUG-043 | Cadastro de avaliação aceita hora inválida e retorna erro interno     | Baixa      | Aberto |
| BUG-044 | IMC exibido sem formatação                                            | Baixa      | Aberto |
| BUG-045 | Erro ao salvar alterações da turma                                    | Alta       | Aberto |
| BUG-046 | Cadastro de turma aceita hora final anterior à hora inicial           | Média      | Aberto |
| BUG-047 | "Gerar aulas" do SifitBox não informa o resultado                     | Baixa      | Aberto |
| BUG-048 | Fechamento de caixa não é salvo após "Buscar Contas"                 | Alta       | Aberto |
| BUG-049 | Caixa pode ser fechado sem a conferência das contas                   | Média      | Aberto |
| BUG-050 | Sistema permite abrir mais de um caixa no mesmo local                 | Média      | Aberto |
| BUG-051 | Erro interno ao abrir caixa sem local de contas                       | Média      | Aberto |
| BUG-052 | Indicador "Caixas Fechados" é reduzido ao abrir um caixa             | Baixa      | Aberto |
| BUG-053 | Listagem inicial de caixas ignora o período exibido no filtro         | Baixa      | Aberto |
| BUG-054 | Não é possível registrar o pagamento de conta a pagar                 | Alta       | Aberto |
| BUG-055 | Indicadores "Total a Pagar" e "Valor Restante" exibem zero           | Média      | Aberto |
| BUG-056 | Cadastro de conta a pagar sem validação dos campos obrigatórios       | Média      | Aberto |
| BUG-057 | Erro no servidor exibido após excluir conta a pagar                   | Baixa      | Aberto |
| BUG-058 | Visualização da conta a pagar exibe códigos internos e campos vazios  | Baixa      | Aberto |
| BUG-059 | Despesa fixa aceita valor negativo e erro interno com valor em texto  | Média      | Aberto |

---

## 📈 **Gráfico de Resultado (Texto Alternativo)**

**Casos por status:**

* ✅ Passaram: 72
* ❌ Falharam: 60

**Severidade dos bugs:**

* 🟥 Crítica: 2
* 🟧 Alta: 10
* 🟨 Média: 27
* 🟩 Baixa: 20

---

## 📁 **Evidências e Documentos**

* ✔️ [Análise de Requisitos](1-Analise%20de%20requisitos.md)
* ✔️ [Plano de Testes](2-plano%20de%20testes.md)
* ✔️ Casos de Teste:
  * [CT_RF01 - Login na plataforma](Cenarios%20de%20testes/CT_RF01_%20Login%20na%20plataforma.md)
  * [CT_RF02 - Página inicial](Cenarios%20de%20testes/CT_RF02_%20P%C3%A1gina%20inicial.md)
  * [CT_RF03 - Dashboard](Cenarios%20de%20testes/CT_RF03_%20Dashboard.md)
  * [CT_RF04 - Gestão de clientes](Cenarios%20de%20testes/CT_RF04_%20Gest%C3%A3o%20de%20clientes.md)
  * [CT_RF05 - Gestão de planos](Cenarios%20de%20testes/CT_RF05_%20Gest%C3%A3o%20de%20planos.md)
  * [CT_RF06 - Gestão de matrículas](Cenarios%20de%20testes/CT_RF06_%20Gest%C3%A3o%20de%20matr%C3%ADculas.md)
  * [CT_RF07 - Contas a receber](Cenarios%20de%20testes/CT_RF07_%20Contas%20a%20receber.md)
  * [CT_RF08 - Gestão de fornecedores](Cenarios%20de%20testes/CT_RF08_%20Gest%C3%A3o%20de%20fornecedores.md)
  * [CT_RF09 - Check-in e presenças](Cenarios%20de%20testes/CT_RF09_%20Check-in%20e%20presen%C3%A7as.md)
  * [CT_RF10 - Avaliações](Cenarios%20de%20testes/CT_RF10_%20Avalia%C3%A7%C3%B5es.md)
  * [CT_RF11 - Turmas e SifitBox](Cenarios%20de%20testes/CT_RF11_%20Turmas%20e%20SifitBox.md)
  * [CT_RF12 - Caixas](Cenarios%20de%20testes/CT_RF12_%20Caixas.md)
  * [CT_RF13 - Contas a pagar e despesas fixas](Cenarios%20de%20testes/CT_RF13_%20Contas%20a%20pagar%20e%20despesas%20fixas.md)
* 🐛 [Relatório de Bugs com Evidências em Vídeo](3-Relatorio-de-Bugs.md)
* 📹 Evidências em vídeo hospedadas no [Jam.dev](https://jam.dev)

---

## ✅ **Conclusão**

A execução dos testes manuais no SIFIT demonstrou **bom funcionamento da autenticação** e das principais telas de listagem, busca e visualização, mas **apresentou falhas críticas** que impedem o cadastro e a alteração de registros em módulos centrais da academia.

Na **Página Inicial** e no **Dashboard**, as telas carregam e a navegação funciona, mas os **indicadores são inconsistentes entre as telas** (alunos em risco, clientes ausentes e desistências — BUG-002, BUG-003 e BUG-004), o que reduz a confiança do gestor nos números exibidos. O Dashboard também apresenta **título incorreto** e **gráficos com títulos ilegíveis** (BUG-006 e BUG-007).

No módulo de **Clientes**, a listagem, a busca por nome, os filtros e a visualização funcionam, mas **não é possível cadastrar nem alterar clientes** (BUG-008 e BUG-013), o que bloqueia **processos-chave** da academia, como a entrada de novos alunos e a inativação de alunos que saíram.

No módulo de **Planos**, o cadastro, a edição e a exclusão funcionam, mas **não é possível inativar um plano** (BUG-019) e **planos inativos continuam disponíveis para matrícula** (BUG-020). Os **indicadores de alunos e receita estão zerados** (BUG-015), e o cadastro **aceita parcelas negativas** (BUG-018) e **expõe mensagens do banco de dados** quando o grupo não é informado (BUG-017).

No módulo de **Matrículas**, o cadastro, a busca e o cancelamento funcionam, mas o **desconto não é aplicado ao valor total** (BUG-021), o que pode gerar cobranças incorretas, e a **paginação esconde parte das matrículas** (BUG-023). A exclusão é efetivada, mas o sistema informa erro ao usuário (BUG-024).

No módulo de **Contas a Receber**, a busca, os filtros, o cadastro manual, o recebimento e a exclusão funcionam, e os indicadores do mês são atualizados corretamente. Porém, **as matrículas cadastradas não geraram contas a receber** (BUG-027), o que compromete a cobrança dos alunos, e **o recebimento pode ser registrado sem tipo de pagamento** (BUG-029), prejudicando o fechamento de caixa.

No módulo de **Fornecedores**, a listagem, a busca por nome e a visualização funcionam, mas, assim como em Clientes, **não é possível cadastrar nem alterar fornecedores** (BUG-033 e BUG-034), e a alteração expõe mensagens do banco de dados.

No módulo de **Check-in e Presenças**, o check-in é gravado e o código inexistente é tratado, mas **os check-ins não aparecem na tela de Presenças** (BUG-035), **clientes sem matrícula ativa são liberados** (BUG-038), o status permanece "Pendente" sem opção de saída (BUG-036) e o horário é exibido com 3 horas a mais (BUG-037).

No módulo de **Avaliações**, a busca, os filtros, o agendamento e a exclusão funcionam, mas **não é possível registrar a avaliação realizada** (BUG-041) nem **alterar a data e a hora** de uma avaliação agendada (BUG-042), o que impede o acompanhamento físico dos alunos.

No módulo de **Turmas e SifitBox**, a busca, os filtros, as validações do cadastro, o cadastro e a exclusão funcionam, mas **nenhuma turma pode ser alterada** (BUG-045) e o cadastro **aceita horário com fim anterior ao início** (BUG-046).

No módulo de **Caixas**, a busca, os filtros, a paginação e a abertura funcionam, mas **o fechamento com conferência das contas não é salvo** (BUG-048), enquanto **o fechamento sem conferência é aceito com totais zerados** (BUG-049), e **é possível abrir mais de um caixa no mesmo local** (BUG-050). Essas falhas comprometem o controle financeiro diário da academia.

No módulo de **Contas a Pagar e Despesas Fixas**, a busca, os filtros e o cadastro de contas funcionam, e as despesas fixas podem ser cadastradas, alteradas, inativadas e excluídas. Porém, **não existe opção para registrar o pagamento de uma conta a pagar** (BUG-054), **os indicadores de valores a pagar ficam zerados** (BUG-055) e o cadastro não valida os campos obrigatórios (BUG-056).

Também foram encontradas falhas de **busca e paginação** (BUG-009, BUG-010 e BUG-011) e de **mensagens ao usuário** (BUG-001, BUG-012, BUG-014, BUG-022, BUG-025 e BUG-026), que prejudicam a **experiência do usuário**, mas não impedem o uso do sistema.

Recomenda-se priorizar a correção dos bugs críticos e reexecutar os casos C04-CT08 e C04-CT10 (cadastro e alteração de clientes) após a correção, incluindo as validações de CPF e data de nascimento no cadastro, que não puderam ser avaliadas enquanto o cadastro estiver indisponível.

🔍 Identificação da Causa Raiz (Root Cause Analysis)
A identificação da causa raiz é uma etapa essencial no processo de garantia de qualidade (QA), pois busca entender por que um defeito ocorreu, indo além dos sintomas visíveis do problema. Essa análise ajuda a evitar recorrência de falhas, melhorando a qualidade do software a longo prazo.

Ao encontrar um bug, o QA não deve apenas registrá-lo, mas também investigar sua origem. A causa raiz pode estar em erros de lógica no código, falhas de validação, má comunicação entre equipes, requisitos mal definidos ou até inconsistências no ambiente de teste. Ferramentas como 5 Porquês, Diagrama de Ishikawa ou análise de logs podem ser utilizadas para essa investigação.

Identificar corretamente a causa raiz permite que os desenvolvedores corrijam o erro de forma precisa e que o time evite retrabalhos, contribuindo para entregas mais estáveis, eficientes e com menor custo.

Com base na análise das requisições feitas pelo navegador (DevTools), foram levantadas as seguintes hipóteses de causa raiz para os bugs encontrados:

* **BUG-002, BUG-003 e BUG-004:** cada tela calcula os indicadores com regras ou consultas diferentes (ex.: "ausente" na Página Inicial considera quem nunca visitou, e a tela de Clientes não), o que indica a ausência de uma regra única de cálculo.
* **BUG-007:** o console do navegador registra o erro "Invalid scale configuration for scale: yAxes", indicando configuração desatualizada da biblioteca de gráficos, e as cores dos títulos não foram ajustadas ao tema dos cartões.
* **BUG-008 e BUG-013:** as rotas de cadastro e de atualização de cliente retornam erro 500 ("Erro interno inesperado.") mesmo com dados válidos, o que indica uma falha comum no back-end, como erro de persistência no banco de dados ou de tratamento dos campos enviados.
* **BUG-009:** a busca por código funciona apenas para clientes com matrícula. A hipótese foi confirmada durante os testes de matrículas: após matricular a cliente 408, ela passou a ser encontrada pela busca por código, o que indica que a consulta depende do vínculo com a matrícula.
* **BUG-010 e BUG-011:** a quantidade de páginas parece ser calculada sobre o total de clientes, sem considerar o filtro aplicado, e o limite por página não é aplicado no primeiro carregamento.
* **BUG-014:** o sistema não trata o caso de cliente inexistente e retorna erro 500 em vez de uma mensagem de "cliente não encontrado".
* **BUG-017 e BUG-018:** o back-end não valida os campos do plano antes de gravar no banco de dados; o erro de restrição do banco é devolvido diretamente na resposta da API.
* **BUG-019:** o status "inativo" é enviado corretamente pela tela, mas não é gravado, o que indica que a rota de atualização ignora o campo de status.
* **BUG-021:** o campo "Desconto" exibido na visualização recebe o valor da parcela, o que sugere que o campo errado é gravado ou lido, e o valor total não é recalculado na tela de cadastro.
* **BUG-022 e BUG-024:** a API retorna o motivo correto ("Já existe matrícula ativa") ou realiza a operação, mas a tela exibe uma mensagem genérica de erro, indicando falha no tratamento das respostas da API.
* **BUG-023:** a quantidade de páginas não é calculada a partir do total de matrículas, impedindo a navegação além da primeira página.
* **BUG-027:** a matrícula é gravada (a API retorna o código da matrícula), mas nenhuma conta a receber é criada; a geração das parcelas pode depender de uma etapa posterior não concluída ou estar falhando de forma silenciosa.
* **BUG-029 e BUG-030:** o formulário de recebimento não valida os campos antes do envio e o back-end aceita os dados sem validação.
* **BUG-033 e BUG-034:** a atualização do fornecedor não envia o campo "tipo_pessoa" (Física/Jurídica), que é obrigatório no banco de dados; o mesmo padrão de erro 500 no cadastro e na alteração ocorre em Clientes (BUG-008 e BUG-013), o que sugere uma falha comum nas rotas de gravação de cadastros.
* **BUG-035 a BUG-038:** o check-in é gravado em uma tabela própria (a API retorna o código do check-in), mas não gera o registro de presença nem atualiza o status; o horário é armazenado em UTC e exibido sem conversão para o fuso de Brasília; a liberação do check-in não consulta a situação da matrícula do cliente.
* **BUG-041 a BUG-043:** a rota de registro da avaliação retorna erro 500 mesmo com dados válidos, o botão "Salvar" da alteração de data e hora não dispara nenhuma requisição e os campos de hora não são validados na tela antes do envio.
* **BUG-045 e BUG-046:** a rota de atualização de turma retorna erro 500 mesmo sem alterações, o que indica falha no back-end independente dos dados enviados; o horário não é validado nem na tela nem no back-end.
* **BUG-048 a BUG-052:** o fluxo de fechamento não valida se as contas foram conferidas e deixa de enviar o fechamento após a busca das contas; a abertura não verifica se já existe caixa aberto para o local nem valida o local antes do envio; o indicador de caixas fechados é calculado sobre um total fixo, e não sobre a quantidade real de caixas.
* **BUG-054 a BUG-059:** a tela de contas a pagar não implementa a ação de pagamento nem calcula os indicadores de valores; os formulários de contas a pagar e despesas fixas não validam os campos na tela e o back-end aceita valores negativos ou devolve erro 500 para dados inválidos.
