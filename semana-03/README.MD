# Consultoria Técnica – Chaos-IT
**Base conceitual:** Modelo Espiral (Boehm) e CMMI – conforme Sommerville

---

## 1. Contextualização

A Chaos-IT apresenta falhas recorrentes em seus projetos, evidenciadas pela queda de um sistema de drones, causada principalmente pela ausência de processos estruturados e pela negligência na análise de riscos.

---

## 2. Parte 1 – Modelo Espiral de Boehm

### 2.1 Importância da Análise de Riscos

O Modelo Espiral é caracterizado por ciclos iterativos que integram, de forma obrigatória, a análise sistemática de riscos.

A aplicação desse modelo teria evitado a falha do projeto de drones pelos seguintes fatores:

- Identificação antecipada de riscos técnicos (falhas de sensores, comunicação e software)
- Validação progressiva por meio de prototipação
- Correção iterativa de defeitos ao longo do desenvolvimento
- Tomada de decisão baseada em avaliação técnica estruturada

**Conclusão:**  
A ausência de análise de riscos resultou na materialização de falhas previsíveis. O uso do Modelo Espiral teria mitigado esses riscos antes da operação em ambiente real.

---

### 2.2 Aplicação ao Projeto de IA Subaquática

#### Representação do ciclo

![Modelo Espiral](./diagramas/espiral.png)

---

### 2.3 Detalhamento dos Quadrantes

#### Planejamento
- Definição dos objetivos do ciclo
- Levantamento de requisitos do sistema
- Estimativa de custos, recursos e prazos

#### Análise de Riscos
- Identificação de riscos técnicos e operacionais:
  - Comunicação subaquática limitada
  - Comportamento imprevisível da IA
  - Falhas estruturais de hardware
- Avaliação de impacto e probabilidade
- Definição de estratégias de mitigação (simulações, redundância, testes controlados)

#### Engenharia
- Desenvolvimento de protótipos
- Implementação dos algoritmos de inteligência artificial
- Integração de componentes de hardware e software
- Testes em ambiente simulado

#### Avaliação
- Testes em ambiente controlado
- Validação com stakeholders
- Coleta de feedback
- Decisão sobre continuidade, ajustes ou encerramento do ciclo

---

## 3. Parte 2 – Diagnóstico de Maturidade (CMMI)

### 3.1 Nível Atual

A Chaos-IT encontra-se no:

**Nível 1 – Inicial**

### 3.2 Justificativa

As características observadas incluem:

- Ausência de processos definidos
- Execução dependente de práticas individuais
- Inexistência de registro histórico de falhas
- Estimativas de prazo imprecisas
- Dependência de esforço individual (não institucionalizado)

Esse cenário caracteriza um ambiente imprevisível, reativo e com alto risco de falhas.

---

### 3.3 Evolução para o Nível 2 – Gerenciado

Para atingir o próximo nível de maturidade, a organização deve implementar:

#### Gerenciamento de Processos
- Definição de fluxos padronizados de desenvolvimento
- Estabelecimento de práticas organizacionais

#### Gerenciamento de Requisitos
- Documentação formal de requisitos
- Controle de mudanças

#### Planejamento de Projetos
- Elaboração de cronogramas baseados em dados
- Estimativas fundamentadas em histórico

#### Garantia da Qualidade
- Registro e análise de defeitos
- Construção de base de conhecimento organizacional

#### Monitoramento e Controle
- Acompanhamento de progresso
- Definição de métricas básicas de desempenho

---

### 3.4 Benefícios Esperados

A evolução para o Nível 2 proporcionará:

- Maior previsibilidade dos projetos
- Redução de falhas críticas
- Melhor controle gerencial
- Menor dependência de esforço individual

---

## 4. Conclusão

A adoção do Modelo Espiral e a evolução no modelo CMMI são medidas essenciais para a melhoria da qualidade dos processos da Chaos-IT.

Sem essas mudanças, a organização continuará sujeita a falhas recorrentes e prejuízos operacionais, especialmente em projetos de alta complexidade, como o de inteligência artificial subaquática.

---

## 5. Referência

SOMMERVILLE, Ian. *Engenharia de Software*. 10ª edição.

```mermaid
flowchart LR
    A[🟦 Planejamento] --> B[🟥 Análise de Riscos]
    B --> C[🟩 Engenharia]
    C --> D[🟨 Avaliação]
    D --> A

