## 🧪 **Plano de Testes - SIFIT (Sistema para Academias)**

### 📌 1. **Identificação**

* **Nome do Projeto**: SIFIT - Sistema de Gestão de Academias
* **Versão Avaliada**: Ambiente de homologação (alfa)
* **Ambiente de Testes**: [https://sifitalfa.centrion.com.br](https://sifitalfa.centrion.com.br)
* **Tipo de Teste**: Teste Funcional Manual
* **Data do Documento**: 25/10/2026
* **Responsável**: Ville Nunes Figueiredo da Silva

---

### 🎯 2. **Objetivo**

Realizar a verificação manual dos principais requisitos funcionais do SIFIT, com foco na validação dos fluxos críticos da academia (cadastro de clientes, planos, matrículas e cobranças), das mensagens de erro, do comportamento esperado e da coerência das informações exibidas entre as telas.

---

### 🧩 3. **Escopo**

**Incluído (já executado):**

* Autenticação de usuário (Login)
* Página Inicial
* Dashboard
* Gestão de clientes
* Gestão de planos
* Gestão de matrículas
* Contas a receber
* Gestão de fornecedores
* Check-in e Presenças
* Avaliações
* Turmas e SifitBox
* Caixas
* Contas a pagar e Despesas fixas

**Incluído (pendente de execução):**

* Fichas de treino e Exercícios
* Prospecção
* Colaboradores e Funções
* Produtos
* Fichas de anamnese
* Relatórios
* Cadastros auxiliares (Grupos, Tipos de pagamento, Bandeiras, Modelos de contrato, Grupos musculares, Objetivos de treino e Tipos de documentos)

**Excluído:**

* Integração com a Pagar.me (envolve cobranças reais)
* Envio de mensagens pelo WhatsApp (ex.: "Cobrar todos no WhatsApp" e "Enviar mensagem"), pois envia mensagens a pessoas reais
* Aplicativo mobile do aluno
* Testes de performance, carga e segurança

---

### 🔧 4. **Ferramentas Utilizadas**

* Navegador Google Chrome
* Ferramentas de inspeção do navegador (DevTools), para analisar as respostas da API
* Jam.dev (gravação das evidências em vídeo)
* Markdown (registro dos casos de teste, bugs e relatórios)

---

### 🧪 5. **Técnicas de Teste**

* Particionamento de equivalência
* Análise de valor limite (ex.: valores negativos e zerados)
* Caminho feliz (Happy Path)
* Testes negativos (campos obrigatórios vazios e dados inválidos)
* Testes exploratórios
* Verificação de consistência entre telas (indicadores e totais)

---

### 📄 6. **Critérios de Aceitação**

* Todos os casos de teste devem passar com sucesso, conforme o resultado esperado.
* Nenhuma falha crítica deve estar presente em funcionalidades principais.
* Mensagens de erro e validações devem ser claras e consistentes.
* Os indicadores devem apresentar os mesmos valores em todas as telas.

---

### 🚦 7. **Critérios de Saída (Exit Criteria)**

* Todos os testes do escopo foram executados.
* Falhas foram registradas, analisadas e reexecutadas se necessário.
* Documentação de evidências de sucesso e falhas está completa.

---

### ⏱️ 8. **Cronograma Estimado**

| Atividade                                    | Data Início | Data Fim   | Situação     |
| -------------------------------------------- | ----------- | ---------- | ------------ |
| Planejamento de Testes                       | 13/10/2026  | 13/10/2026 | ✅ Concluído |
| Criação de Casos de Teste (RF01 a RF08)      | 13/10/2026  | 25/10/2026 | ✅ Concluído |
| Execução dos Testes Manuais (RF01 a RF08)    | 13/10/2026  | 25/10/2026 | ✅ Concluído |
| Registro e Report de Bugs (RF01 a RF08)      | 13/10/2026  | 25/10/2026 | ✅ Concluído |
| Gravação das evidências em vídeo             | 26/10/2026  | 30/10/2026 | ⏳ Pendente  |
| Criação e execução dos testes (RF09 a RF20)  | 26/10/2026  | 13/11/2026 | ⏳ Pendente  |
| Reteste dos bugs corrigidos                  | A definir   | A definir  | ⏳ Pendente  |
| Encerramento e Evidências                    | 16/11/2026  | 16/11/2026 | ⏳ Pendente  |

---

### 📋 9. **Módulos a Serem Testados**

A sequência segue o fluxo de uso do sistema: acesso, visão geral, cadastro do aluno, contratação, cobrança e, por fim, as rotinas de apoio.

| Código RF | Módulo                                   | Prioridade | Situação      |
| --------- | ---------------------------------------- | ---------- | ------------- |
| RF01      | Login                                    | Alta       | ✅ Executado  |
| RF02      | Página Inicial                           | Média      | ✅ Executado  |
| RF03      | Dashboard                                | Média      | ✅ Executado  |
| RF04      | Gestão de Clientes                       | Alta       | ✅ Executado  |
| RF05      | Gestão de Planos                         | Alta       | ✅ Executado  |
| RF06      | Gestão de Matrículas                     | Alta       | ✅ Executado  |
| RF07      | Contas a Receber                         | Alta       | ✅ Executado  |
| RF08      | Gestão de Fornecedores                   | Baixa      | ✅ Executado  |
| RF09      | Check-in e Presenças                     | Alta       | ✅ Executado  |
| RF10      | Avaliações                               | Média      | ✅ Executado  |
| RF11      | Turmas e SifitBox                        | Média      | ✅ Executado  |
| RF12      | Caixas                                   | Alta       | ✅ Executado  |
| RF13      | Contas a Pagar e Despesas Fixas          | Alta       | ✅ Executado  |
| RF14      | Fichas de Treino e Exercícios            | Média      | ⏳ Pendente   |
| RF15      | Prospecção                               | Média      | ⏳ Pendente   |
| RF16      | Colaboradores e Funções                  | Média      | ⏳ Pendente   |
| RF17      | Produtos                                 | Baixa      | ⏳ Pendente   |
| RF18      | Fichas de Anamnese                       | Baixa      | ⏳ Pendente   |
| RF19      | Relatórios                               | Média      | ⏳ Pendente   |
| RF20      | Cadastros Auxiliares                     | Baixa      | ⏳ Pendente   |

**Resumo:** 13 de 20 módulos executados, com 132 casos de teste e 59 bugs registrados até o momento.

---

### 🐞 10. **Gestão de Defeitos**

* Bugs serão documentados com:

  * Título
  * Descrição
  * Passos para reproduzir
  * Comportamento esperado e comportamento obtido
  * Evidência (vídeo)
  * Gravidade (Crítica, Alta, Média, Baixa)
* Ferramenta: [Relatório de Bugs](3-Relatorio-de-Bugs.md) em Markdown

---

### 📌 11. **Riscos Identificados**

| Risco                                                                 | Impacto | Mitigação                                                            |
| --------------------------------------------------------------------- | ------- | -------------------------------------------------------------------- |
| Sistema fora do ar ou instável                                        | Alto    | Tentar novamente após intervalo                                      |
| Ambiente compartilhado: outros usuários alteram ou excluem dados      | Médio   | Identificar os registros de teste com "Ville" no nome e conferir os dados antes de gravar |
| Cadastro e alteração de clientes e fornecedores indisponíveis (BUG-008, BUG-013, BUG-033 e BUG-034) | Alto | Usar registros já existentes e reexecutar os testes após a correção |
| Ações que enviam mensagens ou cobranças reais (WhatsApp e Pagar.me)  | Alto    | Manter essas ações fora do escopo                                    |
| Testes limitados a um único usuário (perfil administrador)            | Médio   | Documentar esse limite no escopo                                     |

---

### 📁 12. **Entregáveis**

* [Análise de Requisitos](1-Analise%20de%20requisitos.md)
* Plano de Testes (este documento)
* Casos de Teste (pasta [Cenarios de testes](Cenarios%20de%20testes))
* Evidências de Execução (vídeos no Jam.dev)
* [Registro de Bugs](3-Relatorio-de-Bugs.md)
* [Relatório Final de Execução](4-%20Relatorio%20dos%20testes.md)
