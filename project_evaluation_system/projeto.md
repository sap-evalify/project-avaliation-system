# PROJETO DE SOFTWARE: SISTEMA DE AVALIAÇÃO DE PROJETOS

## *Stakeholders*

| NOME | CARGO | E-MAIL |
|:---|:---|:---|
| José Vinicius | Desenvolvedor / Aluno | martines.jose@estudante.ifro.edu.br |
| Carlos Eduardo | Desenvolvedor / Aluno | - |
| Luiz Guilhermy | Desenvolvedor / Aluno | moretti.luiz@estudante.ifro.edu.br |
| Professores Orientadores | Cliente / Orientação | - |

---

# Sumário

* [RESUMO DO PROJETO](#resumo-do-projeto)
* [INTRODUÇÃO](#introdução)
  * [PROPÓSITO DESTE DOCUMENTO](#propósito-deste-documento)
  * [CONCEPÇÃO DO SISTEMA](#concepção-do-sistema)
* [DESCRIÇÃO GERAL](#descrição-geral)
  * [USUÁRIOS DO SISTEMA](#usuários-do-sistema)
  * [ABRANGÊNCIA E SISTEMAS SIMILARES](#abrangência-e-sistemas-similares)
  * [SUPOSIÇÕES E DEPENDÊNCIAS](#suposições-e-dependências)
* [ESTUDO DE VIABILIDADE](#estudo-de-viabilidade)
* [METODOLOGIA ADOTADA NO DESENVOLVIMENTO](#metodologia-adotada-no-desenvolvimento)
* [REQUISITOS DO SOFTWARE](#requisitos-do-software)
  * [REQUISITOS FUNCIONAIS](#requisitos-funcionais)
  * [REQUISITOS NÃO FUNCIONAIS](#requisitos-não-funcionais)
* [PROTOTIPAGEM](#prototipagem)
* [DIAGRAMA DE ATIVIDADES](#diagrama-de-atividades)
* [DIAGRAMA DE SEQUÊNCIA](#diagrama-de-sequência)
* [DIAGRAMA DE CLASSES](#diagrama-de-classes)
* [DIAGRAMA DE CASOS DE USO](#diagrama-de-casos-de-uso)
  * [ESPECIFICAÇÃO DOS CASOS DE USO](#descrição--especificação-dos-casos-de-uso)
* [REFERÊNCIAS](#referências)

---

# RESUMO DO PROJETO

| ITEM | DETALHES |
|:---|:---|
| **NOME** | Sistema de Gestão e Avaliação de Projetos |
| **Líder do Projeto** | [José Martines] |
| **PRINCIPAL OBJETIVO** | Centralizar a gestão de projetos acadêmicos e implementar um sistema de avaliação 360° (Peer-to-Peer) para mensurar o desempenho individual e coletivo. |
| **BENEFÍCIOS ESPERADOS** | Visão unificada do progresso para professores; feedback justo e desenvolvimento de soft skills para alunos; centralização de artefatos e notas. |
| **INÍCIO E TÉRMINO PREVISTOS** | 2025 |

---

# INTRODUÇÃO

Este projeto tem como objetivo desenvolver uma plataforma web para o gerenciamento de projetos acadêmicos no âmbito do IFRO Campus Vilhena. O sistema visa solucionar a dificuldade de acompanhamento de múltiplas equipes, a subjetividade nas avaliações e a falta de canais estruturados para feedback entre alunos.

## PROPÓSITO DESTE DOCUMENTO

Este documento tem como propósito especificar os requisitos funcionais e não funcionais, bem como documentar a modelagem do sistema (diagramas e casos de uso), servindo como guia para o desenvolvimento, testes e validação do software.

## CONCEPÇÃO DO SISTEMA

Métodos utilizados para a obtenção dos requisitos do sistema:

* Análise das dores atuais na gestão de projetos da disciplina Fábrica de Software.
* Levantamento de histórias de usuário com perfis de Aluno e Professor.
* Definição de MVP (*Minimum Viable Product*) baseado em prioridades essenciais.

---

# DESCRIÇÃO GERAL

## Usuários do sistema

| USUÁRIO | DESCRIÇÃO |
|:---|:---|
| **Administrador** | Responsável por gerenciar usuários, perfis e configurações globais do sistema. |
| **Professor (Gestor)** | Cria projetos, define milestones, visualiza dashboards, relatórios e gerencia as notas das equipes. |
| **Aluno (Membro/Avaliador)** | Visualiza projetos, submete artefatos, visualiza suas notas e realiza a avaliação 360° dos colegas de equipe. |

## Abrangência e Sistemas Similares

* Moodle (Ambiente acadêmico)

## Suposições e dependências

Os usuários acessarão a plataforma via navegadores web modernos (Chrome, Firefox, Edge). O sistema depende de conexão com a internet para sincronização de dados e notificações. Requer suporte a HTTPS para segurança dos dados.

---

# ESTUDO DE VIABILIDADE

O sistema é viável pois utiliza tecnologias web padrão e ataca um problema real do ambiente acadêmico: a dificuldade de mensurar a participação individual em trabalhos de grupo. A implementação da avaliação Peer-to-Peer traz um valor pedagógico significativo sem alto custo de infraestrutura.

---

# METODOLOGIA ADOTADA NO DESENVOLVIMENTO

Utilizamos uma abordagem ágil, com o backlog do produto organizado em Histórias de Usuário e priorizado utilizando a técnica MoSCoW (Essencial, Importante, Desejável). O desenvolvimento é guiado por entregas de valor (MVP), focando primeiro no ciclo de vida do projeto e gestão de acessos.

---

# REQUISITOS DO SOFTWARE

A especificação segue as recomendações da norma IEEE Std-830-1998.

## Requisitos Funcionais

A tabela a seguir contém a relação dos Requisitos Funcionais elicitados:

| IDENTIFICADOR | NOME | DESCRIÇÃO | PRIORIDADE |
|:---|:---|:---|:---|
| **RF01** | Gerenciar Usuário | O sistema deve permitir o cadastro de diferentes perfis de usuários (Admin, Professor, Aluno). | Essencial |
| **RF02** | Gerenciamento de Projetos | O sistema deve permitir cadastrar novos projetos com título, descrição, datas e responsável. | Essencial |
| **RF03** | Relatórios de Projetos | O sistema deve gerar relatórios consolidados sobre status, prazos e notas. | Essencial |
| **RF04** | Autenticação e Autorização | Login, logout e recuperação de senha, com restrição de acesso por perfil. | Essencial |
| **RF05** | Dashboard | Painel inicial com métricas de projetos, avaliações pendentes e gráficos. | Essencial |
| **RF06** | Visualização de Projetos | Lista paginada e filtrável de projetos com status resumido. | Essencial |
| **RF07** | Detalhes do Projeto | Visualização completa de equipe, líderes, artefatos e milestones. | Essencial |
| **RF08** | Edição de Projeto | Permitir edição de dados do projeto, alteração de líderes e artefatos. | Essencial |
| **RF09** | Avaliação de Equipe (Peer-to-Peer) | Membros avaliam pares usando critérios pré-definidos (0-5) e comentários. | Essencial |
| **RF10** | Criação de Milestones/Critérios | Cadastro de marcos de entrega e critérios de avaliação associados. | Essencial |
| **RF11** | Gerenciamento de Notas | Exibição de notas (Individual, Grupo, 360°) com filtros. | Essencial |
| **RF12** | Busca e Filtro | Busca textual e filtros avançados em listas de projetos e usuários. | Essencial |
| **RF13** | Edição de Perfil | Usuário edita seus dados pessoais e altera senha. | Essencial |
| **RF14** | Notificações | Alertas sobre prazos e novas atribuições. | Importante |
| **RF15** | Excluir Projeto | Permitir exclusão de projetos existentes. | Importante |

## Requisitos Não Funcionais

A tabela a seguir contém a relação com os Requisitos Não Funcionais identificados:

| IDENTIFICADOR | NOME | DESCRIÇÃO |
|:---|:---|:---|
| **RNF01** | Performance | Carregamento de páginas não deve exceder 3 segundos. |
| **RNF02** | Usabilidade | Interface intuitiva para diferentes níveis de experiência. |
| **RNF03** | Segurança | Criptografia de senhas e uso de HTTPS. |
| **RNF04** | Confiabilidade | Disponibilidade de 99.5%. |
| **RNF05** | Escalabilidade | Suportar aumento de usuários sem degradação. |
| **RNF06** | Manutenibilidade | Código documentado e modular (Code Review). |
| **RNF07** | Compatibilidade | Funcional em navegadores modernos e responsivo. |
| **RNF08** | Audibilidade | Logs de ações críticas (cadastro, edição, exclusão). |
| **RNF09** | Acessibilidade | Seguir padrões WCAG 2.1 AA. |

---

# PROTOTIPAGEM

## Interface Dashboard e Projetos
*(Inserir aqui as imagens do Dashboard, Lista de Projetos e Detalhes)*

## Interface de Avaliação 360°
*(Inserir aqui as imagens do Modal de Avaliação de Pares)*

## Interface Administrativa
*(Inserir aqui as imagens de Gestão de Usuários e Login)*

---

# DIAGRAMA DE ATIVIDADES
*(Inserir aqui o diagrama de atividade de Cadastro de Projetos)*

---

# DIAGRAMA DE SEQUÊNCIA
*(Inserir aqui os diagramas de sequência de Login, Avaliação, etc.)*

---

# DIAGRAMA DE CLASSES
*(Inserir aqui o Diagrama de Classes)*

**Principais Classes Identificadas:**

* **Usuário:** `id`, `nome`, `email`, `senha`, `avatar_url`, `data_cadastro`, `função` (Representa os atores do sistema).
* **Projeto:** `id`, `nome_projeto`, `descricao`, `semestre`, `data_criacao`, `status` (Entidade central).
* **Time:** `id`, `nome_time`, `id_criador` (Agrupamento de alunos).
* **Avaliação:** `id`, `milestone`, `artefatos`, `valor`, `data_registro` (Registros de feedback e notas).

---

# DIAGRAMA DE CASOS DE USO
*(Inserir aqui o Diagrama de Caso de Uso final corrigido)*

## Descrição / Especificação dos Casos de Uso

### UC-01 - Realizar Avaliação Peer-to-Peer (RF09)

| UC-01 - Realizar Avaliação Peer-to-Peer | |
|:---|:---|
| **Descrição/Objetivo:** | Permite que um aluno avalie os membros de sua equipe com base em critérios de soft skills (colaboração, iniciativa, etc.). |
| **Atores:** | Aluno, Sistema |
| **Pré-condições:** | O aluno deve estar logado e pertencer a uma equipe com período de avaliação aberto. |
| **Pós-condições:** | Avaliação registrada e status de pendência removido. |
| **FLUXO PRINCIPAL:** | 1. Aluno acessa a área de avaliações pendentes ou o detalhe do projeto.<br>2. O sistema exibe o modal de Avaliação 360° com a lista de colegas.<br>3. Aluno seleciona um colega.<br>4. Aluno atribui notas (1-5) para os critérios.<br>5. Aluno insere comentários qualitativos (opcional).<br>6. Aluno clica em "Enviar Avaliação".<br>7. O sistema salva a avaliação e atualiza o progresso. |
| **EXCEÇÕES:** | **A1: Cancelar Avaliação:** O aluno clica em cancelar e os dados não salvos são descartados. |

### UC-02 - Cadastrar Projeto (RF02)

| UC-02 - Cadastrar Projeto | |
|:---|:---|
| **Descrição/Objetivo:** | O Professor cria um novo projeto definindo escopo, equipe e critérios. |
| **Atores:** | Professor, Sistema |
| **Pré-condições:** | Professor autenticado no sistema. |
| **Pós-condições:** | Projeto criado com status "Em andamento". |
| **FLUXO PRINCIPAL:** | 1. Professor clica em "Novo Projeto".<br>2. Sistema exibe formulário de cadastro (Etapa 1).<br>3. Professor insere Nome, Semestre e Descrição.<br>4. Professor avança para Etapa 2 e adiciona os alunos à equipe.<br>5. Professor avança para Etapa 3 e define Milestones/Critérios.<br>6. Professor clica em "Salvar".<br>7. Sistema valida dados e cria o projeto. |
| **EXCEÇÕES:** | **A1: Dados Inválidos:** Se campos obrigatórios estiverem vazios, o sistema exibe alerta. |

### UC-03 - Gerar Relatórios (RF03)

| UC-03 - Gerar Relatórios | |
|:---|:---|
| **Descrição/Objetivo:** | Exportar dados consolidados do dashboard para análise externa. |
| **Atores:** | Professor, Sistema |
| **Pré-condições:** | Professor logado na tela de Dashboard. |
| **Pós-condições:** | Arquivo (PDF/CSV) baixado no dispositivo do usuário. |
| **FLUXO PRINCIPAL:** | 1. Professor clica em "Exportar" no Dashboard.<br>2. Sistema exibe modal de configuração de relatório.<br>3. Professor seleciona formato (PDF/Excel), período e seções desejadas.<br>4. Professor clica em "Gerar Relatório".<br>5. Sistema processa os dados e inicia o download do arquivo. |

### UC-04 - Gerenciar Usuários (RF01)

| UC-04 - Gerenciar Usuários | |
|:---|:---|
| **Descrição/Objetivo:** | O Administrador gerencia o cadastro e acesso dos usuários. |
| **Atores:** | Administrador, Sistema |
| **Pré-condições:** | Administrador autenticado. |
| **Pós-condições:** | Usuário criado, editado ou desativado. |
| **FLUXO PRINCIPAL:** | 1. Administrador acessa lista de usuários.<br>2. Clica em "Novo Usuário".<br>3. Preenche Nome, E-mail, Função (Admin/Prof/Aluno) e Grupo.<br>4. Clica em "Criar Usuário".<br>5. Sistema valida unicidade do e-mail e salva o registro. |
| **EXCEÇÕES:** | **A1: E-mail Duplicado:** Se o e-mail já existir, sistema exibe erro. |

### UC-05 - Realizar Login (RF04)

| UC-05 - Realizar Login | |
|:---|:---|
| **Descrição/Objetivo:** | Permite que o usuário acesse o sistema utilizando suas credenciais. |
| **Atores:** | Usuário (Todos), Sistema |
| **Pós-condições:** | Usuário autenticado e redirecionado para o Dashboard. |
| **FLUXO PRINCIPAL:** | 1. Usuário acessa a página de login.<br>2. O sistema solicita e-mail e senha.<br>3. Usuário informa as credenciais e clica em "Entrar".<br>4. O sistema valida as credenciais.<br>5. O sistema redireciona o usuário para o Dashboard. |
| **EXCEÇÕES:** | **A1: Credenciais Inválidas:** Mensagem de erro exibida. |

### UC-06 - Visualizar Dashboard (RF05)

| UC-06 - Visualizar Dashboard | |
|:---|:---|
| **Descrição/Objetivo:** | Apresentar métricas, gráficos e notificações relevantes. |
| **Atores:** | Professor, Sistema |
| **FLUXO PRINCIPAL:** | 1. Professor acessa a página inicial.<br>2. Sistema carrega os cards de métricas.<br>3. Sistema exibe gráfico de "Tempo médio de conclusão".<br>4. Sistema lista as notificações pendentes.<br>5. Professor visualiza o calendário e ranking. |

### UC-07 - Editar Projeto (RF08)

| UC-07 - Editar Projeto | |
|:---|:---|
| **Descrição/Objetivo:** | Permite atualizar informações de um projeto existente. |
| **Atores:** | Professor, Sistema |
| **FLUXO PRINCIPAL:** | 1. Professor clica em "Editar" no card do projeto.<br>2. Sistema carrega o formulário preenchido.<br>3. Professor altera as informações necessárias.<br>4. Professor clica em "Salvar Alterações".<br>5. Sistema valida e atualiza o registro. |

### UC-08 - Visualizar Notas (RF11)

| UC-08 - Visualizar Notas | |
|:---|:---|
| **Descrição/Objetivo:** | Exibir resultados consolidados das avaliações. |
| **Atores:** | Professor, Aluno, Sistema |
| **FLUXO PRINCIPAL:** | 1. Usuário acessa a página de "Notas".<br>2. Sistema exibe a aba "Visão Geral" com a nota final.<br>3. Usuário clica na aba "Nota Individual" para ver critérios específicos.<br>4. Usuário clica na aba "Nota Grupo" para ver critérios colaborativos. |

### UC-09 - Editar Perfil (RF13)

| UC-09 - Editar Perfil | |
|:---|:---|
| **Descrição/Objetivo:** | Permitir atualização de dados pessoais e senha. |
| **Atores:** | Usuário (Todos), Sistema |
| **FLUXO PRINCIPAL:** | 1. Usuário acessa "Configurações" > "Meu Perfil".<br>2. Usuário edita campos permitidos (Nome, Foto).<br>3. Para troca de senha, preenche "Nova Senha" e "Confirmação".<br>4. Usuário clica em "Salvar". |

### UC-10 - Excluir Projeto (RF15)

| UC-10 - Excluir Projeto | |
|:---|:---|
| **Descrição/Objetivo:** | Remover permanentemente um projeto e seus dados. |
| **Atores:** | Professor, Sistema |
| **FLUXO PRINCIPAL:** | 1. Professor clica em "Excluir" no menu do projeto.<br>2. Sistema exibe modal de confirmação.<br>3. Professor confirma a ação.<br>4. Sistema remove o projeto e seus artefatos. |

### UC-11 - Listar e Filtrar Projetos (RF06, RF12)

| UC-11 - Listar e Filtrar Projetos | |
|:---|:---|
| **Descrição/Objetivo:** | Localizar projetos através de lista paginada e filtros. |
| **Atores:** | Usuário, Sistema |
| **FLUXO PRINCIPAL:** | 1. Usuário clica no menu "Projetos".<br>2. Sistema exibe lista de cards.<br>3. Usuário utiliza busca textual ou filtros de status.<br>4. Sistema atualiza a lista com os resultados. |

### UC-12 - Detalhar Projeto (RF07)

| UC-12 - Detalhar Projeto | |
|:---|:---|
| **Descrição/Objetivo:** | Visualizar todas as informações de um projeto em uma tela. |
| **Atores:** | Usuário, Sistema |
| **FLUXO PRINCIPAL:** | 1. Usuário clica em um projeto.<br>2. Sistema exibe Visão Geral, Equipe, Milestones e Artefatos.<br>3. (Opcional) Professor pode rotular um líder de equipe nesta tela. |

### UC-13 - Definir Estrutura de Avaliação (RF10)

| UC-13 - Definir Estrutura de Avaliação | |
|:---|:---|
| **Descrição/Objetivo:** | Cadastro de Milestones e critérios de avaliação. |
| **Atores:** | Professor, Sistema |
| **FLUXO PRINCIPAL:** | 1. Professor clica em "Adicionar Milestone".<br>2. Informa Nome, Data e Descrição.<br>3. Associa critérios de avaliação e artefatos esperados.<br>4. Sistema salva a estrutura. |

### UC-14 - Receber Notificações (RF14)

| UC-14 - Receber Notificações | |
|:---|:---|
| **Descrição/Objetivo:** | Informar sobre prazos e eventos críticos. |
| **Atores:** | Usuário, Sistema |
| **FLUXO PRINCIPAL:** | 1. Sistema detecta evento gatilho.<br>2. Envia notificação visual e e-mail.<br>3. Usuário clica na notificação e é redirecionado. |

### UC-15 - Duplicar Projeto (RF15)



### UC-15 - Gerenciar Artefatos de Entrega

| UC-15 - Gerenciar Artefatos de Entrega | |
|:---|:---|
| **Descrição/Objetivo:** | Upload e gestão de arquivos de entrega. |
| **Atores:** | Aluno, Professor, Sistema |
| **FLUXO PRINCIPAL:** | 1. Usuário acessa Detalhes > "Artefatos".<br>2. Clica em "Fazer Upload" ou insere Link.<br>3. Associa a um Milestone.<br>4. Sistema armazena o artefato. |

### UC-16 - Definir Critérios de Avaliação (360º)

| UC-16 - Definir Critérios de Avaliação | |
|:---|:---|
| **Descrição/Objetivo:** | Configurar critérios de avaliação Peer-to-Peer. |
| **Atores:** | Professor, Administrador, Sistema |
| **FLUXO PRINCIPAL:** | 1. Professor acessa "Gestão de Avaliações".<br>2. Cria novo conjunto de critérios (ex: Soft Skills).<br>3. Define escala de pontuação.<br>4. Salva o conjunto. |

---

# REFERÊNCIAS

Esta subseção apresenta as referências aos documentos utilizados.

* [UML Specification](https://www.omg.org/spec/UML/2.5/About-UML/)
* [IEEE Std 830-1998 - Recommended Practice for Software Requirements Specifications](https://ieeexplore.ieee.org/document/720574)

[ [VOLTAR AO INÍCIO](#projeto-de-software-sistema-de-avaliação-de-projetos) ]