# SAI – Sistema de Alerta Inteligente

**Projeto Final – Etapa 3 | Sprint Review 2 + Sprint Planning 3**
**Desenvolvimento Ágil com Scrum**

**Instituto Federal de São Paulo – Campus São João da Boa Vista**
Curso: Tecnologia em Sistemas para Internet
Professor: Gaio Belitardo de Oliveira

**Integrantes:**
- Alexandro de Oliveira dos Santos
- André Frigo Lima
- Danilo Rodrigues Alves de Sousa
- Rafael Torres de Araujo
- Victor Emanuel de Souza

São João da Boa Vista – SP, 2026

---

## 1. Sprint Review — Sprint 2

**Data da Review:** 02/06/2026
**Duração da Sprint:** 7 dias
**Objetivo da Sprint 2:** Modelar as User Stories classificadas como *Should Have* na matriz de priorização.

### 1.1 Itens entregues (Done)

| ID | Funcionalidade | Entregável UML | Status |
|----|----------------|----------------|--------|
| US05 | Avisos de rotas afetadas | Diagrama de Sequência + Diagrama de Contexto atualizado | ✅ Concluído |
| US06 | Relatórios operacionais | Diagrama de Casos de Uso (extensão) | ✅ Concluído |
| US10 | Histórico de alertas | Diagrama de Classes (extensão) + Diagrama de Atividades | ✅ Concluído |
| DOCS | Repositório GitHub atualizado com diagramas da Sprint 1 | Arquivos .md publicados no GitHub | ✅ Concluído |

### 1.2 Itens não entregues

| ID | Funcionalidade | Motivo | Destino |
|----|----------------|--------|---------|
| US07 | Alertas via WhatsApp/SMS | Escopo técnico mais amplo que o estimado; integração com APIs externas requer validação de requisitos adicionais | Remanejado para Sprint 3 |

### 1.3 Retrospectiva (Retrospective)

**O que funcionou bem:**
- Divisão clara de responsabilidades entre os integrantes por User Story.
- Uso do GitHub Projects facilitou a visualização do progresso da Sprint.
- Diagramas em Mermaid permitiram revisão rápida diretamente no repositório.

**O que pode melhorar:**
- Iniciar a modelagem mais cedo na semana para evitar concentração de entregas no final da Sprint.
- Alinhar melhor o nível de detalhamento dos diagramas entre os integrantes antes de começar.

**Ação de melhoria para Sprint 3:**
- Realizar uma reunião de kick-off no primeiro dia da Sprint para alinhar padrão de modelagem e critério de pronto.

---

## 2. Sprint Planning — Sprint 3

**Data do Planning:** 02/06/2026
**Duração da Sprint:** 7 dias
**Meta da Sprint 3:** Refinar e integrar todos os modelos UML produzidos nas Sprints anteriores, garantindo rastreabilidade completa entre User Stories e diagramas, e entregar o documento final consolidado do projeto.

### 2.1 Backlog da Sprint 3

| Rank | ID | Tarefa | Responsável | Esforço (1–5) |
|------|----|--------|-------------|---------------|
| 1 | US07 | Modelagem dos alertas via WhatsApp/SMS (Diagrama de Sequência + Componentes) | Victor Emanuel | 4 |
| 2 | REV01 | Revisão geral de todos os diagramas UML (consistência e completude) | Alexandro | 3 |
| 3 | REV02 | Integração dos modelos: tabela de rastreabilidade US → Diagrama | André Frigo | 2 |
| 4 | REV03 | Diagrama de Pacotes / Arquitetura completa do sistema | Danilo | 3 |
| 5 | REV04 | Documento final consolidado (Etapas 1, 2 e 3 unificadas) | Rafael | 3 |
| 6 | REV05 | Preparação da apresentação e defesa do projeto | Todos | 2 |

### 2.2 Definição de Pronto (DoD) — Sprint 3

- [ ] US07: Diagrama de Sequência e Diagrama de Componentes publicados no repositório.
- [ ] REV01: Todos os diagramas revisados e sem inconsistências entre si.
- [ ] REV02: Tabela de rastreabilidade US ↔ Diagrama publicada no README.
- [ ] REV03: Diagrama de Pacotes validado e publicado.
- [ ] REV04: Documento final em formato .docx e .md no repositório GitHub.
- [ ] REV05: Slides de apresentação prontos e ensaiados.

### 2.3 Distribuição de tarefas

```
Alexandro  → REV01 (revisão geral dos diagramas)
André      → REV02 (rastreabilidade US → Diagramas)
Danilo     → REV03 (Diagrama de Pacotes / Arquitetura)
Rafael     → REV04 (documento final consolidado)
Victor     → US07  (alertas WhatsApp/SMS)
Todos      → REV05 (apresentação — últimos 2 dias da Sprint)
```

---

## 3. Diagramas da Sprint 2

### 3.1 Diagrama de Sequência — US05: Avisos de Rotas Afetadas

```mermaid
sequenceDiagram
    autonumber
    actor Operador as Operador
    participant Sistema as SAI (Backend)
    participant Mapa as Modulo Mapa
    actor Motorista as Motorista

    Operador->>Sistema: confirmarAlerta(idAlerta, gravidade)
    Sistema->>Sistema: identificarRotasAfetadas(areaRisco)
    Sistema->>Mapa: atualizarRotas(rotasAfetadas)
    Mapa-->>Sistema: confirmacaoAtualizacao()
    Sistema->>Motorista: enviarAvisoRota(mensagem, rotasAfetadas)
    Motorista-->>Sistema: confirmarRecebimento()
```

---

### 3.2 Diagrama de Atividades — US10: Histórico de Alertas

```mermaid
flowchart TD
    A([Início]) --> B[Operador acessa o sistema]
    B --> C[Seleciona 'Histórico de Alertas']
    C --> D[Sistema busca alertas no banco de dados]
    D --> E{Existem registros?}
    E -- Não --> F[Exibir mensagem: nenhum alerta registrado]
    E -- Sim --> G[Exibir lista de alertas paginada]
    G --> H[Operador filtra por data, área ou gravidade]
    H --> I[Sistema aplica filtros e atualiza lista]
    I --> J{Operador deseja exportar?}
    J -- Sim --> K[Gerar relatório PDF ou CSV]
    K --> L([Fim])
    J -- Não --> L
    F --> L
```

---

### 3.3 Extensão do Diagrama de Classes — US10 + US06

```mermaid
classDiagram
    direction TB

    class Alerta {
        +int id
        +DateTime dataHora
        +String descricao
        +GravidadeAlerta gravidade
        +StatusAlerta status
        +gerar() void
        +classificarGravidade(gravidade) void
        +fechar() void
    }

    class HistoricoAlerta {
        +int id
        +int alertaId
        +DateTime dataConsulta
        +String filtrosAplicados
        +buscarPorPeriodo(inicio, fim) List~Alerta~
        +buscarPorGravidade(gravidade) List~Alerta~
        +exportar(formato) Arquivo
    }

    class RelatorioOperacional {
        +int id
        +DateTime dataGeracao
        +String periodo
        +TipoRelatorio tipo
        +gerar() void
        +exportarPDF() Arquivo
        +exportarCSV() Arquivo
    }

    class TipoRelatorio {
        <<enumeration>>
        OCORRENCIAS_POR_PERIODO
        ALERTAS_POR_GRAVIDADE
        AREAS_MAIS_AFETADAS
    }

    HistoricoAlerta "N" --> "1" Alerta : referencia
    RelatorioOperacional --> TipoRelatorio : possui
    RelatorioOperacional "1" --> "N" Alerta : consolida
```

---

## 4. Tabela de Rastreabilidade (Parcial — atualizar na Sprint 3)

| User Story | Diagrama de Contexto | Casos de Uso | Sequência | Classes | Atividades |
|------------|:-------------------:|:------------:|:---------:|:-------:|:----------:|
| US01 – Painel operacional | ✅ | ✅ | ✅ | ✅ | — |
| US02 – Alertas automáticos | ✅ | ✅ | ✅ | ✅ | — |
| US03 – Cadastro de áreas | ✅ | ✅ | — | ✅ | — |
| US04 – Mapa interativo | ✅ | ✅ | — | — | — |
| US08 – Classificação por gravidade | — | ✅ | ✅ | ✅ | — |
| US09 – Controle de usuários | — | ✅ | — | ✅ | — |
| US05 – Rotas afetadas | ✅ | — | ✅ | — | — |
| US06 – Relatórios operacionais | — | ✅ | — | ✅ | — |
| US10 – Histórico de alertas | — | — | — | ✅ | ✅ |
| US07 – WhatsApp/SMS | — | — | — | — | — |

> Legenda: ✅ = modelado | — = pendente (Sprint 3)
