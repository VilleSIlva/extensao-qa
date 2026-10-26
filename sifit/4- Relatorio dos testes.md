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
| 191                     | 114            | 77             | 76               |

---

## 🔍 **Cobertura por Módulo**

| Código RF | Módulo                    | Casos Testados | Casos Passaram | Bugs encontrados | Bug(s) Associado(s)                                |
| --------- | ------------------------- | -------------- | -------------- | ---------------- | -------------------------------------------------- |
| RF01      | Autenticação de Usuário   | 3              | 2              | 1                | BUG-001 |
| RF02      | Página Inicial            | 7              | 4              | 3                | BUG-002, BUG-003, BUG-004 |
| RF03      | Dashboard                 | 4              | 1              | 3                | BUG-002, BUG-005, BUG-006 |
| RF04      | Gestão de Clientes        | 11             | 5              | 7                | BUG-007, BUG-008, BUG-009, BUG-010, BUG-011, BUG-012, BUG-013 |
| RF05      | Gestão de Planos          | 11             | 5              | 6                | BUG-014, BUG-015, BUG-016, BUG-017, BUG-018, BUG-019 |
| RF06      | Gestão de Matrículas      | 12             | 6              | 6                | BUG-020, BUG-021, BUG-022, BUG-023, BUG-024, BUG-025 |
| RF07      | Contas a Receber          | 12             | 7              | 5                | BUG-026, BUG-027, BUG-028, BUG-029, BUG-030 |
| RF08      | Gestão de Fornecedores    | 9              | 6              | 3                | BUG-031, BUG-032, BUG-033 |
| RF09      | Check-in e Presenças      | 11             | 4              | 6                | BUG-034, BUG-035, BUG-036, BUG-037, BUG-038, BUG-039 |
| RF10      | Avaliações                | 11             | 7              | 4                | BUG-040, BUG-041, BUG-042, BUG-043 |
| RF11      | Turmas e SifitBox         | 13             | 10             | 3                | BUG-044, BUG-045, BUG-046 |
| RF12      | Caixas                    | 11             | 5              | 6                | BUG-047, BUG-048, BUG-049, BUG-050, BUG-051, BUG-052 |
| RF13      | Contas a Pagar e Despesas Fixas | 16       | 10             | 6                | BUG-053, BUG-054, BUG-055, BUG-056, BUG-057, BUG-058 |
| RF14      | Fichas de Treino e Exercícios | 13         | 9              | 4                | BUG-059, BUG-060, BUG-061, BUG-062 |
| RF15      | Prospecção                | 12             | 11             | 1                | BUG-063 |
| RF16      | Colaboradores e Funções   | 17             | 12             | 5                | BUG-064, BUG-065, BUG-066, BUG-067, BUG-068 |
| RF17      | Produtos                  | 11             | 7              | 4                | BUG-069, BUG-070, BUG-071, BUG-072 |
| RF18      | Fichas de Anamnese        | 7              | 3              | 4                | BUG-073, BUG-074, BUG-075, BUG-076 |

---

## 🐞 **Resumo dos Bugs Reportados**

| ID      | Título                                                                | Severidade | Status |
| ------- | --------------------------------------------------------------------- | ---------- | ------ |
| BUG-001 | Mensagem de erro incorreta ao tentar realizar login com campos vazios | Média      | Aberto |
| BUG-002 | Quantidade de alunos em risco diverge entre as telas                  | Média      | Aberto |
| BUG-003 | Quantidade de clientes ausentes diverge entre a Página Inicial e a tela de Clientes | Média | Aberto |
| BUG-004 | Lista de desistências vazia, embora o total informe 3 desistências    | Média      | Aberto |
| BUG-005 | Título e navegação do Dashboard exibem "Despesas Fixas"              | Baixa      | Aberto |
| BUG-006 | Títulos das seções e dos gráficos do Dashboard ilegíveis              | Média      | Aberto |
| BUG-007 | Erro ao cadastrar cliente com dados válidos                           | Crítica    | Aberto |
| BUG-008 | Busca por código não retorna clientes sem matrícula                   | Média      | Aberto |
| BUG-009 | Paginação exibe páginas vazias com filtro aplicado                    | Média      | Aberto |
| BUG-010 | Listagem não respeita a quantidade de registros por página            | Baixa      | Aberto |
| BUG-011 | Ausência de mensagem quando a busca não encontra clientes             | Baixa      | Aberto |
| BUG-012 | Erro ao salvar alterações dos dados do cliente                        | Crítica    | Aberto |
| BUG-013 | Erro no servidor ao acessar cliente excluído                          | Baixa      | Aberto |
| BUG-014 | Coluna "Alunos", ranking e receita estimada dos planos exibem valores zerados | Média | Aberto |
| BUG-015 | Busca por código retorna planos cujo código apenas contém o valor informado | Baixa | Aberto |
| BUG-016 | Erro interno com exposição de SQL ao salvar plano sem grupo           | Média      | Aberto |
| BUG-017 | Sistema permite cadastrar plano com quantidade de parcelas negativa   | Média      | Aberto |
| BUG-018 | Inativação do plano não é salva                                       | Alta       | Aberto |
| BUG-019 | Planos inativos são exibidos no cadastro de matrícula                 | Média      | Aberto |
| BUG-020 | Desconto não é aplicado ao valor total da matrícula                   | Média      | Aberto |
| BUG-021 | Mensagem incorreta ao cadastrar matrícula para cliente com matrícula ativa | Baixa | Aberto |
| BUG-022 | Paginação não permite acessar matrículas além da primeira página      | Média      | Aberto |
| BUG-023 | Erro no servidor ao excluir matrícula, embora a exclusão seja efetivada | Média    | Aberto |
| BUG-024 | Mensagem de validação permanece após selecionar o tipo de pagamento   | Baixa      | Aberto |
| BUG-025 | Ausência de mensagem quando a busca não encontra matrículas           | Baixa      | Aberto |
| BUG-026 | Matrícula cadastrada não gera conta a receber                         | Alta       | Aberto |
| BUG-027 | Indicador "Contas Atrasadas" diverge do filtro de contas vencidas    | Média      | Aberto |
| BUG-028 | Recebimento é registrado sem tipo de pagamento                        | Média      | Aberto |
| BUG-029 | Recebimento aceita valor maior que o valor a receber sem alerta       | Baixa      | Aberto |
| BUG-030 | Ausência de mensagem quando a busca não encontra contas a receber     | Baixa      | Aberto |
| BUG-031 | Busca por código inexistente ou parcial retorna todos os fornecedores | Baixa      | Aberto |
| BUG-032 | Erro ao cadastrar fornecedor com dados válidos                        | Alta       | Aberto |
| BUG-033 | Erro interno com exposição de SQL ao alterar fornecedor               | Alta       | Aberto |
| BUG-034 | Check-ins realizados não aparecem na tela de Presenças                | Alta       | Aberto |
| BUG-035 | Check-in permanece "Pendente" e não há retorno ao registrar entrada novamente | Média | Aberto |
| BUG-036 | Horário de entrada do check-in exibido com 3 horas a mais            | Média      | Aberto |
| BUG-037 | Cliente sem matrícula ativa é liberado para check-in                  | Alta       | Aberto |
| BUG-038 | Ausência de mensagens no check-in manual e na entrada rápida          | Baixa      | Aberto |
| BUG-039 | Indicadores da tela de check-in com valores fixos ou incorretos       | Baixa      | Aberto |
| BUG-040 | Erro ao salvar avaliação realizada                                    | Alta       | Aberto |
| BUG-041 | Alteração de data e hora da avaliação não é salva                     | Média      | Aberto |
| BUG-042 | Cadastro de avaliação aceita hora inválida e retorna erro interno     | Baixa      | Aberto |
| BUG-043 | IMC exibido sem formatação                                            | Baixa      | Aberto |
| BUG-044 | Erro ao salvar alterações da turma                                    | Alta       | Aberto |
| BUG-045 | Cadastro de turma aceita hora final anterior à hora inicial           | Média      | Aberto |
| BUG-046 | "Gerar aulas" do SifitBox não informa o resultado                     | Baixa      | Aberto |
| BUG-047 | Fechamento de caixa não é salvo após "Buscar Contas"                 | Alta       | Aberto |
| BUG-048 | Caixa pode ser fechado sem a conferência das contas                   | Média      | Aberto |
| BUG-049 | Sistema permite abrir mais de um caixa no mesmo local                 | Média      | Aberto |
| BUG-050 | Erro interno ao abrir caixa sem local de contas                       | Média      | Aberto |
| BUG-051 | Indicador "Caixas Fechados" é reduzido ao abrir um caixa             | Baixa      | Aberto |
| BUG-052 | Listagem inicial de caixas ignora o período exibido no filtro         | Baixa      | Aberto |
| BUG-053 | Não é possível registrar o pagamento de conta a pagar                 | Alta       | Aberto |
| BUG-054 | Indicadores "Total a Pagar" e "Valor Restante" exibem zero           | Média      | Aberto |
| BUG-055 | Cadastro de conta a pagar sem validação dos campos obrigatórios       | Média      | Aberto |
| BUG-056 | Erro no servidor exibido após excluir conta a pagar                   | Baixa      | Aberto |
| BUG-057 | Visualização da conta a pagar exibe códigos internos e campos vazios  | Baixa      | Aberto |
| BUG-058 | Despesa fixa aceita valor negativo e erro interno com valor em texto  | Média      | Aberto |
| BUG-059 | Ficha de treino não pode ser aberta nem salva                         | Alta       | Aberto |
| BUG-060 | Mensagem genérica ao criar ficha sem objetivo do treino               | Média      | Aberto |
| BUG-061 | Exclusão de ficha de treino retorna comandos SQL na resposta da API   | Média      | Aberto |
| BUG-062 | Sistema permite cadastrar exercício duplicado no mesmo grupo          | Baixa      | Aberto |
| BUG-063 | Sistema permite cadastrar lead duplicado                              | Baixa      | Aberto |
| BUG-064 | Erro interno ao cadastrar colaborador sem selecionar Status e Sexo    | Média      | Aberto |
| BUG-065 | Busca de colaborador por código inexistente exibe linha vazia         | Baixa      | Aberto |
| BUG-066 | Alteração de colaborador retorna comandos SQL na resposta da API      | Média      | Aberto |
| BUG-067 | Funções não podem ser alteradas nem excluídas                         | Média      | Aberto |
| BUG-068 | Sistema permite cadastrar função duplicada                            | Baixa      | Aberto |
| BUG-069 | Produto do tipo Pontuação não pode ser cadastrado                     | Alta       | Aberto |
| BUG-070 | Cadastro de produto sem validação e com erro do banco de dados        | Média      | Aberto |
| BUG-071 | Sistema permite cadastrar produto com preço negativo                  | Média      | Aberto |
| BUG-072 | Valores dos produtos exibidos sem formatação monetária                | Baixa      | Aberto |
| BUG-073 | Anamneses aplicadas não aparecem na listagem                          | Alta       | Aberto |
| BUG-074 | Perguntas do modelo de anamnese não são exibidas                      | Alta       | Aberto |
| BUG-075 | Assistente de anamnese avança sem aluno e falha com erro interno      | Média      | Aberto |
| BUG-076 | Nome do aluno não é exibido na escolha do modelo de anamnese          | Baixa      | Aberto |

---

## 📈 **Gráfico de Resultado (Texto Alternativo)**

**Casos por status:**

* ✅ Passaram: 114
* ❌ Falharam: 77

**Severidade dos bugs:**

* 🟥 Crítica: 2
* 🟧 Alta: 14
* 🟨 Média: 34
* 🟩 Baixa: 26

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
  * [CT_RF14 - Fichas de treino e exercícios](Cenarios%20de%20testes/CT_RF14_%20Fichas%20de%20treino%20e%20exerc%C3%ADcios.md)
  * [CT_RF15 - Prospecção](Cenarios%20de%20testes/CT_RF15_%20Prospec%C3%A7%C3%A3o.md)
  * [CT_RF16 - Colaboradores e funções](Cenarios%20de%20testes/CT_RF16_%20Colaboradores%20e%20fun%C3%A7%C3%B5es.md)
  * [CT_RF17 - Produtos](Cenarios%20de%20testes/CT_RF17_%20Produtos.md)
  * [CT_RF18 - Fichas de anamnese](Cenarios%20de%20testes/CT_RF18_%20Fichas%20de%20anamnese.md)
* 🐛 [Relatório de Bugs com Evidências em Vídeo](3-Relatorio-de-Bugs.md)
* 📹 Evidências em vídeo hospedadas no [Jam.dev](https://jam.dev)

---

## ✅ **Conclusão**

A execução dos testes manuais no SIFIT demonstrou **bom funcionamento da autenticação** e das principais telas de listagem, busca e visualização, mas **apresentou falhas críticas** que impedem o cadastro e a alteração de registros em módulos centrais da academia.

Na **Página Inicial** e no **Dashboard**, as telas carregam e a navegação funciona, mas os **indicadores são inconsistentes entre as telas** (alunos em risco, clientes ausentes e desistências — BUG-002, BUG-003 e BUG-004), o que reduz a confiança do gestor nos números exibidos. O Dashboard também apresenta **título incorreto** e **gráficos com títulos ilegíveis** (BUG-005 e BUG-006).

No módulo de **Clientes**, a listagem, a busca por nome, os filtros e a visualização funcionam, mas **não é possível cadastrar nem alterar clientes** (BUG-007 e BUG-012), o que bloqueia **processos-chave** da academia, como a entrada de novos alunos e a inativação de alunos que saíram.

No módulo de **Planos**, o cadastro, a edição e a exclusão funcionam, mas **não é possível inativar um plano** (BUG-018) e **planos inativos continuam disponíveis para matrícula** (BUG-019). Os **indicadores de alunos e receita estão zerados** (BUG-014), e o cadastro **aceita parcelas negativas** (BUG-017) e **expõe mensagens do banco de dados** quando o grupo não é informado (BUG-016).

No módulo de **Matrículas**, o cadastro, a busca e o cancelamento funcionam, mas o **desconto não é aplicado ao valor total** (BUG-020), o que pode gerar cobranças incorretas, e a **paginação esconde parte das matrículas** (BUG-022). A exclusão é efetivada, mas o sistema informa erro ao usuário (BUG-023).

No módulo de **Contas a Receber**, a busca, os filtros, o cadastro manual, o recebimento e a exclusão funcionam, e os indicadores do mês são atualizados corretamente. Porém, **as matrículas cadastradas não geraram contas a receber** (BUG-026), o que compromete a cobrança dos alunos, e **o recebimento pode ser registrado sem tipo de pagamento** (BUG-028), prejudicando o fechamento de caixa.

No módulo de **Fornecedores**, a listagem, a busca por nome e a visualização funcionam, mas, assim como em Clientes, **não é possível cadastrar nem alterar fornecedores** (BUG-032 e BUG-033), e a alteração expõe mensagens do banco de dados.

No módulo de **Check-in e Presenças**, o check-in é gravado e o código inexistente é tratado, mas **os check-ins não aparecem na tela de Presenças** (BUG-034), **clientes sem matrícula ativa são liberados** (BUG-037), o status permanece "Pendente" sem opção de saída (BUG-035) e o horário é exibido com 3 horas a mais (BUG-036).

No módulo de **Avaliações**, a busca, os filtros, o agendamento e a exclusão funcionam, mas **não é possível registrar a avaliação realizada** (BUG-040) nem **alterar a data e a hora** de uma avaliação agendada (BUG-041), o que impede o acompanhamento físico dos alunos.

No módulo de **Turmas e SifitBox**, a busca, os filtros, as validações do cadastro, o cadastro e a exclusão funcionam, mas **nenhuma turma pode ser alterada** (BUG-044) e o cadastro **aceita horário com fim anterior ao início** (BUG-045).

No módulo de **Caixas**, a busca, os filtros, a paginação e a abertura funcionam, mas **o fechamento com conferência das contas não é salvo** (BUG-047), enquanto **o fechamento sem conferência é aceito com totais zerados** (BUG-048), e **é possível abrir mais de um caixa no mesmo local** (BUG-049). Essas falhas comprometem o controle financeiro diário da academia.

No módulo de **Contas a Pagar e Despesas Fixas**, a busca, os filtros e o cadastro de contas funcionam, e as despesas fixas podem ser cadastradas, alteradas, inativadas e excluídas. Porém, **não existe opção para registrar o pagamento de uma conta a pagar** (BUG-053), **os indicadores de valores a pagar ficam zerados** (BUG-054) e o cadastro não valida os campos obrigatórios (BUG-055).

No módulo de **Fichas de Treino e Exercícios**, a biblioteca de exercícios funciona (cadastro, alteração e exclusão) e a ficha pode ser criada, mas **a ficha não pode ser salva nem aberta depois de criada** (BUG-059), devido a uma coluna inexistente no banco de dados, o que impede o uso das fichas de treino pelos alunos.

O módulo de **Prospecção** apresentou o melhor resultado entre os módulos testados: busca, filtros, cadastro, alteração de estágio, exclusão e indicadores funcionam corretamente, com apenas a ausência de controle de leads duplicados (BUG-063).

No módulo de **Colaboradores e Funções**, a busca, o cadastro (quando Status e Sexo são selecionados), a alteração, a inativação, o vínculo de funções, a exclusão de colaboradores e as permissões das funções funcionam. Porém, **o cadastro falha com os valores padrão exibidos em Status e Sexo** (BUG-064), **as funções não podem ser alteradas nem excluídas** (BUG-067) e a alteração de colaborador expõe comandos SQL (BUG-066).

No módulo de **Produtos**, a busca, os filtros e o cadastro, alteração, inativação e exclusão de produtos de venda funcionam, mas **produtos do tipo Pontuação não podem ser cadastrados** (BUG-069), o cadastro aceita preço negativo (BUG-071) e os valores são exibidos sem formatação monetária (BUG-072).

No módulo de **Fichas de Anamnese**, o assistente localiza o aluno e grava a anamnese, mas **as perguntas do modelo não são exibidas** (BUG-074) e **as anamneses aplicadas não aparecem na listagem** (BUG-073), o que torna o módulo inutilizável para o acompanhamento de saúde dos alunos.

Também foram encontradas falhas de **busca e paginação** (BUG-008, BUG-009 e BUG-010) e de **mensagens ao usuário** (BUG-001, BUG-011, BUG-013, BUG-021, BUG-024 e BUG-025), que prejudicam a **experiência do usuário**, mas não impedem o uso do sistema.

Recomenda-se priorizar a correção dos bugs críticos e reexecutar os casos C04-CT08 e C04-CT10 (cadastro e alteração de clientes) após a correção, incluindo as validações de CPF e data de nascimento no cadastro, que não puderam ser avaliadas enquanto o cadastro estiver indisponível.

🔍 Identificação da Causa Raiz (Root Cause Analysis)
A identificação da causa raiz é uma etapa essencial no processo de garantia de qualidade (QA), pois busca entender por que um defeito ocorreu, indo além dos sintomas visíveis do problema. Essa análise ajuda a evitar recorrência de falhas, melhorando a qualidade do software a longo prazo.

Ao encontrar um bug, o QA não deve apenas registrá-lo, mas também investigar sua origem. A causa raiz pode estar em erros de lógica no código, falhas de validação, má comunicação entre equipes, requisitos mal definidos ou até inconsistências no ambiente de teste. Ferramentas como 5 Porquês, Diagrama de Ishikawa ou análise de logs podem ser utilizadas para essa investigação.

Identificar corretamente a causa raiz permite que os desenvolvedores corrijam o erro de forma precisa e que o time evite retrabalhos, contribuindo para entregas mais estáveis, eficientes e com menor custo.

Com base na análise das requisições feitas pelo navegador (DevTools), foram levantadas as seguintes hipóteses de causa raiz para os bugs encontrados:

* **BUG-002, BUG-003 e BUG-004:** cada tela calcula os indicadores com regras ou consultas diferentes (ex.: "ausente" na Página Inicial considera quem nunca visitou, e a tela de Clientes não), o que indica a ausência de uma regra única de cálculo.
* **BUG-006:** o console do navegador registra o erro "Invalid scale configuration for scale: yAxes", indicando configuração desatualizada da biblioteca de gráficos, e as cores dos títulos não foram ajustadas ao tema dos cartões.
* **BUG-007 e BUG-012:** as rotas de cadastro e de atualização de cliente retornam erro 500 ("Erro interno inesperado.") mesmo com dados válidos, o que indica uma falha comum no back-end, como erro de persistência no banco de dados ou de tratamento dos campos enviados.
* **BUG-008:** a busca por código funciona apenas para clientes com matrícula. A hipótese foi confirmada durante os testes de matrículas: após matricular a cliente 408, ela passou a ser encontrada pela busca por código, o que indica que a consulta depende do vínculo com a matrícula.
* **BUG-009 e BUG-010:** a quantidade de páginas parece ser calculada sobre o total de clientes, sem considerar o filtro aplicado, e o limite por página não é aplicado no primeiro carregamento.
* **BUG-013:** o sistema não trata o caso de cliente inexistente e retorna erro 500 em vez de uma mensagem de "cliente não encontrado".
* **BUG-016 e BUG-017:** o back-end não valida os campos do plano antes de gravar no banco de dados; o erro de restrição do banco é devolvido diretamente na resposta da API.
* **BUG-018:** o status "inativo" é enviado corretamente pela tela, mas não é gravado, o que indica que a rota de atualização ignora o campo de status.
* **BUG-020:** o campo "Desconto" exibido na visualização recebe o valor da parcela, o que sugere que o campo errado é gravado ou lido, e o valor total não é recalculado na tela de cadastro.
* **BUG-021 e BUG-023:** a API retorna o motivo correto ("Já existe matrícula ativa") ou realiza a operação, mas a tela exibe uma mensagem genérica de erro, indicando falha no tratamento das respostas da API.
* **BUG-022:** a quantidade de páginas não é calculada a partir do total de matrículas, impedindo a navegação além da primeira página.
* **BUG-026:** a matrícula é gravada (a API retorna o código da matrícula), mas nenhuma conta a receber é criada; a geração das parcelas pode depender de uma etapa posterior não concluída ou estar falhando de forma silenciosa.
* **BUG-028 e BUG-029:** o formulário de recebimento não valida os campos antes do envio e o back-end aceita os dados sem validação.
* **BUG-032 e BUG-033:** a atualização do fornecedor não envia o campo "tipo_pessoa" (Física/Jurídica), que é obrigatório no banco de dados; o mesmo padrão de erro 500 no cadastro e na alteração ocorre em Clientes (BUG-007 e BUG-012), o que sugere uma falha comum nas rotas de gravação de cadastros.
* **BUG-034 a BUG-037:** o check-in é gravado em uma tabela própria (a API retorna o código do check-in), mas não gera o registro de presença nem atualiza o status; o horário é armazenado em UTC e exibido sem conversão para o fuso de Brasília; a liberação do check-in não consulta a situação da matrícula do cliente.
* **BUG-040 a BUG-042:** a rota de registro da avaliação retorna erro 500 mesmo com dados válidos, o botão "Salvar" da alteração de data e hora não dispara nenhuma requisição e os campos de hora não são validados na tela antes do envio.
* **BUG-044 e BUG-045:** a rota de atualização de turma retorna erro 500 mesmo sem alterações, o que indica falha no back-end independente dos dados enviados; o horário não é validado nem na tela nem no back-end.
* **BUG-047 a BUG-051:** o fluxo de fechamento não valida se as contas foram conferidas e deixa de enviar o fechamento após a busca das contas; a abertura não verifica se já existe caixa aberto para o local nem valida o local antes do envio; o indicador de caixas fechados é calculado sobre um total fixo, e não sobre a quantidade real de caixas.
* **BUG-053 a BUG-058:** a tela de contas a pagar não implementa a ação de pagamento nem calcula os indicadores de valores; os formulários de contas a pagar e despesas fixas não validam os campos na tela e o back-end aceita valores negativos ou devolve erro 500 para dados inválidos.
* **BUG-059 e BUG-061:** o banco de dados de homologação não possui a coluna "descanso_padrao" utilizada pela consulta da ficha, o que indica migração de banco não aplicada no ambiente; a rota de exclusão devolve a saída de depuração do SQL na resposta.
* **BUG-064:** os campos de seleção exibem a primeira opção visualmente, mas o valor vinculado ao formulário permanece vazio, e o back-end não valida esses campos antes de gravar; o mesmo padrão de erro 500 em cadastros ocorre em Clientes (BUG-007) e Fornecedores (BUG-032).
* **BUG-061 e BUG-066:** as rotas de exclusão de ficha e de atualização de colaborador devolvem a saída de depuração do SQL, o que indica modo de depuração ativo no back-end de homologação.
* **BUG-069 e BUG-070:** o back-end grava o campo "valor" mesmo para produtos de pontuação e não trata o valor vazio, devolvendo o erro do banco de dados ("Data truncated for column 'valor'") na resposta.
* **BUG-073 a BUG-075:** a listagem consulta as fichas com o parâmetro "id" nulo; o assistente não carrega as perguntas do modelo e não valida o aluno antes de avançar, enviando a anamnese sem respostas ou sem aluno.
